[Semana 06](README.md) · [Teoría](1-TEORIA.md) · [Dinámica de aula](2-DINAMICA.md) · **Taller de laboratorio**

# Semana 06

## CAATs con Python y DuckDB, Ley de Benford y triaje de hallazgos con un LLM local

**SI-084 - Auditoría de Sistemas** - Sesión 2 en laboratorio · calificación **procedimental**

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](../GLOSARIO.md).

---

## Qué entregas

| | |
|---|---|
| **Archivo** | `SI084-S06-TALLER-Grupo<N>.pdf` |
| **Plantilla obligatoria** | [SI084-PLANTILLA-TALLER.docx](../PLANTILLAS/SI084-PLANTILLA-TALLER.docx) |
| **Formato** | PDF exportado desde la plantilla en Word, con la carátula de la UPT, el índice actualizado y las capturas numeradas |
| **Qué va dentro** | Las secciones de la plantilla. La **5. Resultados y evidencias** se califica contra la tabla de resultados esperados de esta guía, y **cada resultado necesita la evidencia que lo demuestre**. No se copian de aquí los objetivos, la duración ni los resultados de aprendizaje |
| **Dónde se sube** | Aula virtual, tarea «Taller · Semana 06» |
| **Cuándo vence** | Según lo programado en el aula virtual. El plazo se cuenta desde la sesión de laboratorio de la semana, se desarrolle el taller dentro de ella o fuera de ella |

> No se califica un informe entregado en `.docx`, sin carátula, sin los códigos de los integrantes o con resultados declarados sin evidencia.

---

## 1. Información sobre el evento práctico

### 1.1. Título del evento práctico

Técnicas de auditoría asistidas por computador aplicadas al 100 % de una población transaccional, con detección de excepciones, análisis de Ley de Benford y uso de un modelo de lenguaje ejecutado localmente para el triaje y la consolidación de los hallazgos de toda la Unidad I.

### 1.2. Objetivos

- Cargar y **verificar la integridad** de una población transaccional completa en **DuckDB**.
- Ejecutar **pruebas de excepción sobre el 100 % de la población**, sin muestreo.
- Aplicar la **Ley de Benford** verificando primero sus condiciones de aplicabilidad y midiendo la desviación con un contraste chi-cuadrado.
- Ejecutar un **cruce entre archivos** para detectar empleados y proveedores con la misma cuenta bancaria.
- Usar **Ollama en local** para agrupar y priorizar los hallazgos acumulados de las semanas 01–05, **verificando manualmente** cada afirmación del modelo.
- Producir el **expediente consolidado de la Unidad I**.

### 1.3. Resultados de Aprendizaje (RA)

- **RA1** Analiza e interpreta los conceptos y terminología de Auditoría de Sistemas.
- **RA2** Evalúa la seguridad de la información en Auditoría de Sistemas.

### 1.4. Recursos

| Recurso | Detalle |
|---|---|
| Entorno `si084-lab` | Base de datos `si084_db` operativa |
| **DuckDB** | `pip install duckdb` — https://duckdb.org/ |
| **Python 3.11+** | `pandas`, `scipy`, `matplotlib` |
| **Jupyter Lab** | `pip install jupyterlab` |
| **Ollama** | https://ollama.com/ — modelo abierto pequeño (p. ej. `llama3.2:3b` o `qwen2.5:7b`) |
| Dataset | `poblacion_pagos.csv` (180 000 pagos sintéticos), `empleados.csv`, `proveedores.csv` — provistos por el docente |
| LibreOffice Calc | Presentación de resultados |

### 1.5. Seguridad

1. El dataset es **sintético**. Nunca se carga en este laboratorio información transaccional real de la empresa auditada.
2. **Ollama se ejecuta exclusivamente en local.** Está prohibido enviar evidencia de auditoría a servicios de IA en la nube sin autorización escrita del titular de la información y acuerdo de tratamiento de datos.
3. La salida del modelo **no es evidencia**. Toda afirmación se verifica contra el papel de trabajo original antes de incorporarla al informe.
4. Se documenta en el papel de trabajo — modelo, versión, entrada, salida y verificación realizada.

---

## 2. Procedimiento o Metodología

### Paso A — Cargar la población y verificar su integridad

**La primera prueba de un CAAT no es analítica. Es de integridad de la extracción.** Si el dato extraído no es el dato del sistema, todo lo posterior es inválido.

```python
# 30_papeles_trabajo/PT06_caat.ipynb  — celda 1
import duckdb, pandas as pd, hashlib

con = duckdb.connect("../20_evidencia/E06_caat/auditoria.duckdb")
con.execute("""
    CREATE OR REPLACE TABLE pagos AS
    SELECT * FROM read_csv_auto('../20_evidencia/E06_caat/poblacion_pagos.csv',
                                header=true, sample_size=-1)
""")

# --- CONTROLES DE INTEGRIDAD DE LA EXTRACCIÓN ---
print("Registros extraídos :", con.sql("SELECT COUNT(*) FROM pagos").fetchone()[0])
print("Total de control    :", con.sql("SELECT ROUND(SUM(monto),2) FROM pagos").fetchone()[0])
print("Rango de fechas     :", con.sql("SELECT MIN(fecha), MAX(fecha) FROM pagos").fetchone())
print("Hash del archivo    :",
      hashlib.sha256(open('../20_evidencia/E06_caat/poblacion_pagos.csv','rb').read()).hexdigest())
print("\nNulos por columna:")
print(con.sql("""SELECT column_name, null_percentage
                 FROM (SUMMARIZE pagos)""").df().to_string(index=False))
```

**Papel de trabajo PT06-A.** El total de control y el conteo de registros se **contrastan con el total reportado por el sistema origen**. Si no coinciden, la extracción está incompleta y se detiene el análisis. Este es un procedimiento de auditoría en sí mismo.

### Paso B — Pruebas de excepción sobre el 100 % de la población

```python
# celda 2 — cada consulta es un procedimiento del programa de trabajo
PRUEBAS = {

"X-01 Pagos fuera del horario laboral": """
    SELECT id_pago, fecha, proveedor, monto, usuario_aprobador, EXTRACT(hour FROM fecha) AS h
    FROM pagos
    WHERE EXTRACT(dow FROM fecha) IN (0,6)
       OR EXTRACT(hour FROM fecha) < 7 OR EXTRACT(hour FROM fecha) > 20
    ORDER BY monto DESC""",

"X-02 Montos justo por debajo del umbral de aprobación (S/ 5000)": """
    SELECT id_pago, fecha, proveedor, monto, usuario_aprobador
    FROM pagos WHERE monto BETWEEN 4750 AND 4999.99
    ORDER BY fecha""",

"X-03 Fraccionamiento: mismo proveedor, mismo día, varios pagos bajo el umbral": """
    SELECT proveedor, CAST(fecha AS DATE) AS dia, COUNT(*) AS n,
           ROUND(SUM(monto),2) AS total
    FROM pagos WHERE monto < 5000
    GROUP BY 1,2 HAVING COUNT(*) >= 3 AND SUM(monto) > 5000
    ORDER BY total DESC""",

"X-04 Pagos duplicados exactos": """
    SELECT proveedor, monto, CAST(fecha AS DATE) AS dia, COUNT(*) AS n,
           STRING_AGG(id_pago, ', ') AS ids
    FROM pagos GROUP BY 1,2,3 HAVING COUNT(*) > 1
    ORDER BY monto DESC""",

"X-05 Autoaprobación: solicitante = aprobador": """
    SELECT id_pago, fecha, proveedor, monto, usuario_solicitante
    FROM pagos WHERE usuario_solicitante = usuario_aprobador
    ORDER BY monto DESC""",

"X-06 Proveedores activos sin movimiento en 18 meses que reaparecen": """
    WITH ult AS (SELECT proveedor, MAX(fecha) f, COUNT(*) n FROM pagos GROUP BY 1)
    SELECT p.proveedor, p.fecha, p.monto, u.n AS pagos_historicos
    FROM pagos p JOIN ult u USING (proveedor)
    WHERE u.n <= 2 AND p.monto > 20000
    ORDER BY p.monto DESC""",

"X-07 Montos redondos elevados (indicio de importe fabricado)": """
    SELECT id_pago, fecha, proveedor, monto, usuario_aprobador
    FROM pagos WHERE monto >= 10000 AND monto % 1000 = 0
    ORDER BY monto DESC""",

"X-08 Secuencia de comprobantes con saltos": """
    WITH s AS (SELECT nro_comprobante,
                      LAG(nro_comprobante) OVER (ORDER BY nro_comprobante) AS prev
               FROM pagos WHERE nro_comprobante IS NOT NULL)
    SELECT prev AS desde, nro_comprobante AS hasta,
           nro_comprobante - prev - 1 AS faltantes
    FROM s WHERE nro_comprobante - prev > 1 ORDER BY faltantes DESC""",
}

total = con.sql("SELECT COUNT(*) FROM pagos").fetchone()[0]
resumen = []
for nombre, sql in PRUEBAS.items():
    df = con.sql(sql).df()
    df.to_csv(f"../40_hallazgos/CAAT_{nombre.split()[0]}.csv", index=False)
    resumen.append({"prueba": nombre, "excepciones": len(df),
                    "pct_poblacion": round(100*len(df)/total, 4)})
    print(f"\n{'='*80}\n{nombre}  →  {len(df)} excepciones de {total:,} registros")
    print(df.head(6).to_string(index=False))

pd.DataFrame(resumen).to_csv("../30_papeles_trabajo/PT06_resumen_excepciones.csv", index=False)
```

> **Punto de método.** Cada excepción **no es un hallazgo**. Es un caso que requiere investigación. El auditor documenta cuántas investigó, cuántas tuvieron explicación satisfactoria y cuántas quedaron sin sustento. Reportar «se encontraron 340 excepciones» sin haber investigado ninguna es un informe que la gerencia descartará con razón.

### Paso C — Ley de Benford

```python
# celda 3
import numpy as np
from scipy import stats
import matplotlib.pyplot as plt

# --- CONDICIONES DE APLICABILIDAD · se verifican ANTES de aplicar la prueba ---
m = con.sql("SELECT monto FROM pagos WHERE monto > 0").df()["monto"]
ordenes = np.log10(m.max()) - np.log10(m.min())
print(f"Órdenes de magnitud cubiertos : {ordenes:.2f}  (se requiere > 2)")
print(f"Tamaño de la población        : {len(m):,}    (se requiere > 1000)")
print(f"¿Hay mínimo o máximo impuesto?: revisar la política de pagos")
assert ordenes > 2 and len(m) > 1000, "No se cumplen las condiciones: la prueba no aplica"

# --- CONTRASTE ---
primer = m.astype(str).str.replace(r"[^1-9]", "", regex=True).str[0].astype(int)
obs = primer.value_counts().sort_index().reindex(range(1,10), fill_value=0)
esp = pd.Series([np.log10(1+1/d) for d in range(1,10)], index=range(1,10)) * len(primer)

chi2, p = stats.chisquare(obs.values, esp.values)
mad = np.abs(obs/len(primer) - esp/len(primer)).mean()   # Mean Absolute Deviation

print(f"\nChi-cuadrado = {chi2:.2f}   p-valor = {p:.6f}")
print(f"MAD = {mad:.5f}  →  ", 
      "conformidad estrecha" if mad < .006 else
      "conformidad aceptable" if mad < .012 else
      "conformidad marginal" if mad < .015 else "NO CONFORMIDAD")

comp = pd.DataFrame({"observado_%": 100*obs/len(primer),
                     "esperado_%": 100*esp/len(primer)})
comp["desviacion_pp"] = comp["observado_%"] - comp["esperado_%"]
print("\n", comp.round(2).to_string())

comp[["observado_%","esperado_%"]].plot.bar(figsize=(9,4),
     title="Ley de Benford — primer dígito significativo de los pagos")
plt.ylabel("% de la población"); plt.xlabel("Primer dígito")
plt.tight_layout(); plt.savefig("../20_evidencia/E06_caat/benford.png", dpi=140)
```

**Interpretación obligatoria en el papel de trabajo.** Se redacta explícitamente:

> «La desviación observada en el dígito *d* **no constituye evidencia de fraude**. Constituye un criterio de priorización que justifica examinar en detalle los N registros que inician con ese dígito. El resultado de ese examen —y no la prueba estadística— sustenta o descarta el hallazgo.»

### Paso D — Cruce entre archivos independientes

```python
# celda 4 — empleados que comparten cuenta bancaria con proveedores
con.execute("""
  CREATE OR REPLACE TABLE empleados   AS SELECT * FROM read_csv_auto('../20_evidencia/E06_caat/empleados.csv');
  CREATE OR REPLACE TABLE proveedores AS SELECT * FROM read_csv_auto('../20_evidencia/E06_caat/proveedores.csv');
""")

cruce = con.sql("""
  SELECT e.nombre AS empleado, e.area, e.cuenta_bancaria,
         p.razon_social AS proveedor, p.ruc,
         (SELECT ROUND(SUM(monto),2) FROM pagos WHERE proveedor = p.razon_social) AS total_pagado
  FROM empleados e
  JOIN proveedores p ON e.cuenta_bancaria = p.cuenta_bancaria
  ORDER BY total_pagado DESC NULLS LAST
""").df()

cruce.to_csv("../40_hallazgos/CAAT_X09_empleado_proveedor.csv", index=False)
print(cruce.to_string(index=False))

# Coincidencias adicionales de alto valor probatorio
for campo in ["direccion", "telefono", "correo"]:
    r = con.sql(f"""SELECT e.nombre, p.razon_social, e.{campo}
                    FROM empleados e JOIN proveedores p ON e.{campo} = p.{campo}""").df()
    print(f"\nCoincidencias en '{campo}': {len(r)}")
    if len(r): print(r.to_string(index=False))
```

> Este cruce es imposible de detectar por muestreo y es una de las pruebas de mayor rendimiento en auditoría de compras. **Criterio.** Control interno sobre el maestro de proveedores; COBIT 2019 **DSS06.03 Manage roles, responsibilities, access privileges and levels of authority**.

### Paso E — Triaje de hallazgos con un LLM local

```bash
ollama serve &                     # si no está corriendo
ollama pull llama3.2:3b
```

```python
# celda 5
import json, subprocess, glob, pathlib

# 1. Consolidar TODOS los hallazgos de las semanas 01-05
corpus = []
for f in sorted(glob.glob("../40_hallazgos/*.md")):
    corpus.append(f"### {pathlib.Path(f).name}\n{open(f).read()[:1500]}")
texto = "\n\n".join(corpus)

PROMPT = f"""Eres asistente de un auditor de sistemas. A partir de los siguientes hallazgos,
produce EXCLUSIVAMENTE un JSON con este esquema:
{{"temas":[{{"tema":"...","hallazgos":["H-001",...],"riesgo_agregado":"Critico|Alto|Medio|Bajo",
"control_iso_sugerido":"A.x.y","justificacion":"..."}}],
"tres_prioridades":["...","...","..."]}}

Reglas: no inventes hallazgos que no estén en el texto; si no estás seguro de un control ISO,
escribe "verificar". No agregues texto fuera del JSON.

HALLAZGOS:
{texto}
"""

r = subprocess.run(["ollama","run","llama3.2:3b"], input=PROMPT,
                   capture_output=True, text=True, timeout=300)
salida = r.stdout
open("../30_papeles_trabajo/PT06_ia_salida_cruda.txt","w").write(salida)
print(salida[:2500])
```

**Verificación obligatoria — el paso que convierte la salida en trabajo de auditoría.** Se completa la tabla `PT06_verificacion_ia.md`:

| # | Afirmación del modelo | ¿Se sostiene en la evidencia? | Control ISO propuesto | ¿El código existe en el Anexo A 2022? | Acción del auditor |
|---|---|---|---|---|---|
| 1 | | Sí / No / Parcial | A.x.y | **Sí / No** | Acepta / Corrige / Descarta |

> **Se espera que el modelo cometa al menos un error verificable.** Encontrarlo y documentarlo es parte del resultado del laboratorio. Demuestra que el estudiante ejerció debida diligencia profesional en lugar de delegar el juicio.

**Registro del uso de IA** en `30_papeles_trabajo/PT06_registro_ia.md`:

| Campo | Valor |
|---|---|
| Herramienta y versión | Ollama x.y.z, modelo `llama3.2:3b` |
| Ejecución | Local, sin salida de datos del equipo |
| Entrada proporcionada | Hallazgos H-001 a H-00N, sin datos personales |
| Salida obtenida | `PT06_ia_salida_cruda.txt` (SHA-256: ...) |
| Afirmaciones verificadas / total | N de M |
| Errores detectados en la salida | |
| Uso final | Solo priorización; ninguna conclusión del informe se sostiene únicamente en la salida del modelo |

### Paso F — Cierre del expediente de la Unidad I

```bash
sha256sum 20_evidencia/E06_caat/* 40_hallazgos/CAAT_*.csv >> 20_evidencia/SHA256SUMS_E06.txt
git add . && git commit -m "E06: CAATs, Ley de Benford, cruce de archivos y triaje asistido"
git tag -a unidad-1 -m "Cierre del expediente de pruebas tecnicas — Unidad I"
git log --oneline --decorate | head -12
```

---

### Paso G — Validar y corregir

El resultado no vale por estar hecho, sino por resistir una comprobación. Se ejecutan estas tres y **se corrige lo que falle antes de cerrar la sesión**.

1. Comprobar que el control de integridad de la extracción cuadra. Conteo, total de control y hash coinciden con el origen.
2. Verificar que la interpretación de Benford dice explícitamente que **prioriza, no prueba**, y que las condiciones de aplicabilidad se comprobaron.
3. Revisar que `PT06_verificacion_ia.md` documenta **al menos un error del modelo** detectado por el equipo.

> Lo que no se pueda corregir hoy se anota en la sección **Problemas y mejoras** de la evidencia, con lo que faltó y por qué. Un resultado parcial documentado con honestidad vale más que uno declarado sin prueba.

### Paso H — Registrar la evidencia y cerrar

Se versiona lo producido, se anota la URL de cada resultado y se responde en dos frases la pregunta de transferencia — **qué riesgo correría una organización real si esto se hiciera mal**.

---

## 3. Resultados

> **Evidencia obligatoria en GitHub.** Todo resultado de este taller se versiona en el repositorio del equipo. El informe **no consigna capturas sueltas**. Consigna la **URL** del artefacto en GitHub. Una captura no permite verificar autoría, fecha ni contenido; un enlace sí.
>
> | Qué se entrega | Dónde vive | Qué se escribe en el informe |
> |---|---|---|
> | Código y archivos de configuración | Rama del taller, fusionada a `develop` vía Pull Request | URL del Pull Request |
> | Documentos y matrices | `docs/`, en formato de texto versionable | URL del archivo en la rama |
> | Capturas y videos que el taller exija | `docs/evidencias/S06/` | URL del archivo |
> | Salida de comandos | `docs/evidencias/S06/salidas/*.txt` | URL del archivo |
>
> **Etiqueta del taller.** Al cerrar el taller se crea la etiqueta `taller-06` sobre el commit entregado:
>
> ```bash
> git tag -a taller-06 -m "Taller 06 · SI084"
> git push origin taller-06
> ```
>
> La URL que se consigna en el informe apunta a esa etiqueta:
> `https://github.com/<organizacion>/<repositorio>/tree/taller-06`
>
> **El informe es lo que se califica; el repositorio es lo que lo prueba.** Cada resultado de la sección 3 del informe lleva la URL con la que se verifica, y **un resultado sin su URL se califica como no logrado**, por bien redactado que esté. Lo que no se puede abrir no se puede dar por hecho.

### 3.1. El producto del taller

El informe del taller, con estos resultados y la evidencia de cada uno.

| # | Resultado esperado | Verificación |
|---|---|---|
| 1 | Población cargada con **controles de integridad de la extracción** documentados (conteo, total de control, hash) | `PT06-A` |
| 2 | Las 8 pruebas de excepción ejecutadas sobre el 100 %, con su CSV y el porcentaje de la población | `PT06_resumen_excepciones.csv` |
| 3 | **Al menos 3 excepciones investigadas individualmente**, con su explicación o su elevación a hallazgo | Papel de trabajo |
| 4 | Ley de Benford con **condiciones de aplicabilidad verificadas**, chi-cuadrado, MAD y gráfico | `benford.png` y celda 3 |
| 5 | Interpretación escrita que aclara que Benford **prioriza, no prueba** | Papel de trabajo |
| 6 | Cruce empleado-proveedor con al menos una coincidencia y su hallazgo redactado | `CAAT_X09_*.csv` y `H-00x.md` |
| 7 | `PT06_verificacion_ia.md` completo, con **al menos un error del modelo detectado y documentado** | Contenido del archivo |
| 8 | `PT06_registro_ia.md` con los siete campos completos | Contenido del archivo |
| 9 | Etiqueta `unidad-1` en Git y expediente completo con la cadena de custodia al día | `git tag`, `CADENA_DE_CUSTODIA.md` |

### 3.2. Cómo y dónde se entrega

1. En PDF exportado desde la [plantilla de taller](../PLANTILLAS/SI084-PLANTILLA-TALLER.docx), con la carátula de la UPT, el índice actualizado y los códigos de los integrantes.
2. Con el nombre `SI084-S06-TALLER-Grupo<N>.pdf`.
3. En el aula virtual, tarea «Taller · Semana 06», en el plazo programado.

## Rúbrica procedimental (20 puntos)

Se aplica sobre el informe entregado y la evidencia enlazada en el repositorio. **Cada criterio se califica de forma independiente.**

| Criterio | 4 — Logrado | 2 — En proceso | 0 — Insuficiente |
|---|---|---|---|
| **Cargar la población y verificar su integridad** | Completo y correcto, con la evidencia que lo respalda | Completo con errores menores, o correcto pero sin toda la evidencia | Incompleto, o entregado sin ejecutar |
| **Pruebas de excepción sobre el 100 % de la población** | Completo y correcto, con la evidencia que lo respalda | Completo con errores menores, o correcto pero sin toda la evidencia | Incompleto, o entregado sin ejecutar |
| **Evidencia verificable en el repositorio** | Cada resultado tiene su URL sobre la etiqueta `taller-NN`, y el enlace abre lo que dice | La mayoría tiene URL; alguna evidencia es una captura suelta | Se declaran resultados sin enlace, o el enlace no corresponde |
| **Trazabilidad de la evidencia** | Todo hallazgo o dato se rastrea hasta el archivo, registro y fecha que lo sustenta | Rastreable en su mayoría; algún dato sin origen | Se afirman hechos sin poder ubicarlos en la evidencia |
| **La evidencia entregada** | Las secciones de la plantilla completas; los papeles de trabajo quedan archivados y referenciados | Secciones completas con papeles de trabajo incompletos | Faltan secciones o no hay papeles de trabajo |

## 4. Conclusiones

1. Cuando el dato es accesible por consulta, el muestreo deja de ser una necesidad metodológica — analizar el 100 % de la población elimina el riesgo de muestreo y detecta patrones —fraccionamiento, duplicados, cruces— que ninguna muestra aleatoria encontraría.
2. La Ley de Benford y la detección de anomalías priorizan el esfuerzo del auditor; no sustituyen la investigación individual de cada excepción, que es donde se decide si hay hallazgo.
3. Un modelo de lenguaje acelera la consolidación y la redacción, pero produce afirmaciones plausibles y falsas con la misma fluidez que las verdaderas; sin verificación documentada, incorporar su salida al informe traslada al auditor una responsabilidad que la herramienta no puede asumir.

## 5. Referencias Bibliográficas

- ISACA. *ITAF: A Professional Practices Framework for IS Audit/Assurance* (5.ª ed.), lineamientos sobre uso de CAAT y evidencia. https://www.isaca.org/resources/frameworks-standards-and-models
- ISACA. *Code of Professional Ethics*. https://www.isaca.org/credentialing/code-of-professional-ethics
- ISACA. (2018). *COBIT 2019 Framework: Governance and Management Objectives*, DSS06. https://www.isaca.org/resources/cobit
- Benford, F. (1938). The law of anomalous numbers. *Proceedings of the American Philosophical Society*, 78(4), 551–572.
- Nigrini, M. J. (2012). *Benford's Law: Applications for Forensic Accounting, Auditing, and Fraud Detection*. Wiley.
- ACFE. *Report to the Nations — Occupational Fraud and Abuse*. https://www.acfe.com/fraud-resources/report-to-the-nations
- ISO 19011:2018. *Guidelines for auditing management systems*. https://www.iso.org/standard/70017.html
- Ley 29733, Ley de Protección de Datos Personales (Perú). https://www.gob.pe/institucion/minjus/
- DuckDB Foundation. *DuckDB Documentation*. https://duckdb.org/docs/
- Ollama. *Ollama Documentation*. https://github.com/ollama/ollama/tree/main/docs
- Piattini Velthuis, M., Del Peso Navarro, E. y Del Peso Ruiz, M. (2009). *Auditoría de tecnologías y sistemas de información* (6.ª ed.). Alfaomega / Ra-Ma.

## 6. Anexos

- `anexo_A_notebook_caat.ipynb` — cuaderno completo ejecutado con sus salidas.
- `anexo_B_benford.png` — gráfico comparativo.
- `anexo_C_verificacion_ia.pdf` — tabla de verificación de la salida del modelo.
- `anexo_D_expediente_unidad1.pdf` — índice del expediente completo con la cadena de custodia.

---

---

[Semana 06](README.md) · [Teoría](1-TEORIA.md) · [Dinámica de aula](2-DINAMICA.md) · **Taller de laboratorio**

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
