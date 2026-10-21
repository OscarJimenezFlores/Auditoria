[Semana 16](README.md) · [Teoría](1-TEORIA.md) · [Dinámica de aula](2-DINAMICA.md) · **Taller de laboratorio**

# Semana 16

## Redacción del informe final y matriz de seguimiento de recomendaciones

**SI-084 - Auditoría de Sistemas** - Sesión 2 en laboratorio · calificación **procedimental**

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](../GLOSARIO.md).

---

## Qué entregas

| | |
|---|---|
| **Archivo** | `SI084-S16-TALLER-Grupo<N>.pdf` |
| **Plantilla obligatoria** | [SI084-PLANTILLA-TALLER.docx](../PLANTILLAS/SI084-PLANTILLA-TALLER.docx) |
| **Formato** | PDF exportado desde la plantilla en Word, con la carátula de la UPT, el índice actualizado y las capturas numeradas |
| **Qué va dentro** | Las secciones de la plantilla. La **5. Resultados y evidencias** se califica contra la tabla de resultados esperados de esta guía, y **cada resultado necesita la evidencia que lo demuestre**. No se copian de aquí los objetivos, la duración ni los resultados de aprendizaje |
| **Dónde se sube** | Aula virtual, tarea «Taller · Semana 16» |
| **Cuándo vence** | Según lo programado en el aula virtual |

> No se califica un informe entregado en `.docx`, sin carátula, sin los códigos de los integrantes o con resultados declarados sin evidencia.

---

## 1. Información sobre el evento práctico

### 1.1. Título del evento práctico

Ensamblaje del informe final de auditoría de sistemas conforme a la ISO 19011:2018 y a ITAF, con validación de hallazgos, incorporación de la respuesta de la administración y construcción de la matriz de seguimiento de recomendaciones.

### 1.2. Objetivos

- **Consolidar y priorizar** todos los hallazgos de las semanas 13 a 15 en un listado único.
- Ejecutar la **validación de hallazgos** con el auditado y documentar los ajustes.
- **Ensamblar el informe final** con las siete secciones y sus anexos.
- Redactar el **resumen ejecutivo** en un máximo de dos páginas, apto para el directorio.
- Construir la **matriz de seguimiento** con criterio de cierre verificable por recomendación.
- Verificar la **trazabilidad completa** del informe. Cada afirmación referenciada a un papel de trabajo.
- Preparar la **carta de distribución controlada**.

### 1.3. Resultados de Aprendizaje (RA)

- **RA1** Diseña y aplica estrategias para los diversos tipos de auditoría de sistemas.
- **RA2** Descubre la importancia y diferencia entre auditor interno y externo.

### 1.4. Recursos

| Recurso | Detalle |
|---|---|
| Todos los papeles de trabajo y hallazgos | Semanas 13 a 15 |
| **ISO 19011:2018**, cláusulas 6.5 y 6.6 | https://www.iso.org/standard/70017.html |
| **ITAF (ISACA)** — lineamientos de reporte | https://www.isaca.org/resources/frameworks-standards-and-models |
| **COSO 2013** | https://www.coso.org/guidance-on-ic |
| **Pandoc** + plantilla LaTeX o Word | Generación del informe: https://pandoc.org/ |
| **Python 3.11+** con `pandas`, `matplotlib` | Consolidación y gráficos |
| **draw.io** | Diagramas del informe |

### 1.5. Seguridad

1. El informe final contiene el mapa completo de las debilidades de la organización. Se clasifica **Confidencial** o **Restringido** y se marca en cada página.
2. La distribución es **nominal y registrada**. Se lleva un control de a quién se entregó, en qué fecha y en qué formato.
3. El informe **no nombra personas naturales**. Usa cargos.
4. El detalle técnico explotable (rutas exactas, versiones vulnerables, credenciales) va en anexos de circulación **más restringida** que el cuerpo del informe.
5. Al cierre del encargo se ejecuta lo acordado en la carta sobre devolución o destrucción de la información, dejando acta.

---

## 2. Procedimiento o Metodología

> **Documento del caso para esta semana.** La organización entrega **Guion del auditado · material del docente**, en `CASOS/EMPRESA-<NN>-<slug>/documentos/guion-del-auditado.md`. Es consistente con los datos de `datos/`. Las personas, usuarios y proveedores que menciona existen en los archivos. **No señala sus debilidades**; declara lo que la organización dice hacer.

### Paso A — Consolidar y priorizar los hallazgos

```python
# 30_papeles_trabajo/PT16_consolidacion.py
import glob, re, pathlib, pandas as pd

filas = []
for f in sorted(glob.glob("../40_hallazgos/H-*.md")):
    t = open(f).read()
    def campo(s, sig="##"):
        try: return t.split(s)[1].split(sig)[0].strip()
        except IndexError: return ""
    sev = re.search(r"\*\*Severidad\*\*\s*\|\s*\*?\*?(\w+)", t)
    dom = re.search(r"\*\*Dominio\*\*\s*\|\s*(.+)", t)
    filas.append({
        "id": pathlib.Path(f).stem,
        "titulo": t.split("\n")[0].replace("#","").strip(),
        "severidad": sev.group(1) if sev else "Sin clasificar",
        "dominio": dom.group(1).strip() if dom else "Sin dominio",
        "tiene_criterio_con_codigo": bool(re.search(r"A\.\d+\.\d+|[A-Z]{3}\d{2}|art\.\s*\d+", t)),
        "efecto_cuantificado": bool(re.search(r"\d", campo("## Efecto"))),
        "recomendacion_con_plazo": bool(re.search(r"\b(\d+)\s*(días|d[ií]as|meses)", t)),
        "tiene_respuesta_admin": "*(A completar" not in t and "Respuesta de la administración" in t,
    })

h = pd.DataFrame(filas)
ORD = {"Crítico":0, "Alto":1, "Medio":2, "Bajo":3, "Sin clasificar":9}
h = h.sort_values(["severidad","id"], key=lambda c: c.map(ORD) if c.name=="severidad" else c)
h.to_csv("../50_informe/INF_hallazgos_consolidados.csv", index=False)

print("=== RESUMEN DEL INFORME ===")
print(h.severidad.value_counts().reindex(["Crítico","Alto","Medio","Bajo"]).fillna(0).astype(int).to_string())
print("\nPor dominio:\n", h.dominio.value_counts().to_string())
print("\n=== CONTROL DE CALIDAD ===")
for col, msg in [("tiene_criterio_con_codigo","sin criterio citado con código"),
                 ("efecto_cuantificado","con efecto no cuantificado"),
                 ("recomendacion_con_plazo","sin plazo en la recomendación"),
                 ("tiene_respuesta_admin","sin respuesta de la administración")]:
    faltan = h[~h[col]]
    print(f"{len(faltan):2d} hallazgos {msg}: {list(faltan.id)}")
```

**Regla de corte.** Ningún hallazgo llega al informe sin criterio citado con código, efecto cuantificado y recomendación con plazo. Los que no cumplen se corrigen o se retiran.

### Paso B — Validación con el auditado

Se ejecuta la reunión de validación (o se simula con el docente en el rol de responsable del proceso) y se completa `40_hallazgos/ACTA_VALIDACION.md`:

| Hallazgo | Condición presentada | ¿Confirma? | Evidencia adicional aportada | Ajuste realizado | Posición final |
|---|---|---|---|---|---|
| H-101 | 23 usuarios activos sin vínculo | Parcial | Actas de baja de 6 usuarios, posteriores a la extracción | Condición ajustada a 17 usuarios | Acepta |
| H-102 | | | | | |

**Reglas de la validación.**

- El auditado **puede** modificar la condición aportando evidencia nueva.
- El auditado **no puede** modificar el criterio ni suprimir el hallazgo.
- Todo ajuste queda registrado con la evidencia que lo motiva y su hash.
- Si persiste el desacuerdo, el informe recoge **ambas posiciones**.

### Paso C — Ensamblar el informe

Qué va en cada sección lo dice el **[Modelo del Informe de Auditoría](../MODELO-INFORME-DE-AUDITORIA.md)**. Aquí se ensambla.

Estructura de archivos en `50_informe/`:

```
50_informe/
├── 00_portada.md
├── 01_resumen_ejecutivo.md      ← máximo 2 páginas
├── 02_introduccion.md
├── 03_diagnostico.md
├── 04_hallazgos.md              ← generado desde 40_hallazgos/
├── 05_conclusiones.md
├── 06_recomendaciones.md
├── 07_seguimiento.md
├── anexos/
└── INFORME_FINAL.pdf
```

**Generación del gráfico del resumen ejecutivo.**

```python
# 50_informe/graficos.py
import pandas as pd, matplotlib.pyplot as plt
h = pd.read_csv("INF_hallazgos_consolidados.csv")

fig, (a1, a2) = plt.subplots(1, 2, figsize=(13,5))
ORD = ["Crítico","Alto","Medio","Bajo"]
COL = ["#8B0000","#D2691E","#DAA520","#4682B4"]
s = h.severidad.value_counts().reindex(ORD).fillna(0)
a1.bar(ORD, s.values, color=COL)
a1.set_title("Hallazgos por severidad"); a1.set_ylabel("Cantidad")
for i, v in enumerate(s.values): a1.text(i, v+.1, int(v), ha="center", fontweight="bold")

d = h.dominio.value_counts()
a2.barh(d.index[::-1], d.values[::-1], color="#16285C")
a2.set_title("Hallazgos por dominio de control")
plt.tight_layout(); plt.savefig("resumen_hallazgos.png", dpi=140)
```

**Resumen ejecutivo — plantilla de dos páginas.**

```markdown
# Resumen Ejecutivo
**CONFIDENCIAL** · Auditoría de Sistemas · <organización> · Periodo <___ a ___>

## Qué se auditó
Se evaluaron los controles generales de tecnología de información —gestión de accesos,
gestión de cambios, operaciones y continuidad—, el gobierno de TI y el cumplimiento
del marco legal aplicable, sobre <sistemas>, durante el periodo <___>.
**No formaron parte del alcance:** <exclusiones>.

## Conclusión
<Un párrafo con veredicto explícito, base y alcance referenciados.>

## Situación en cifras
| Severidad | Cantidad | Plazo recomendado |
|---|---|---|
| Crítico | | Inmediato / 30 días |
| Alto | | 90 días |
| Medio | | 180 días |
| Bajo | | Siguiente ciclo |

![Resumen](resumen_hallazgos.png)

## Los tres asuntos que requieren decisión del directorio
1. **<Título>** — <consecuencia de negocio cuantificada> · <decisión que se solicita>
2. **<Título>** — …
3. **<Título>** — …

## Riesgos que la organización asume si no actúa
<Tres líneas, en lenguaje de negocio, sin términos técnicos.>
```

**Generación del PDF.**

```bash
cd 50_informe
cat 00_portada.md 01_resumen_ejecutivo.md 02_introduccion.md 03_diagnostico.md \
    04_hallazgos.md 05_conclusiones.md 06_recomendaciones.md 07_seguimiento.md \
    > INFORME_COMPLETO.md

pandoc INFORME_COMPLETO.md -o INFORME_FINAL.pdf \
  --toc --toc-depth=2 --number-sections \
  -V geometry:margin=2.5cm -V fontsize=11pt -V documentclass=report \
  -V colorlinks=true -V linkcolor=NavyBlue \
  --metadata title="Informe de Auditoría de Sistemas" \
  --metadata author="Equipo auditor — SI-084 · UPT" \
```

### Paso D — Matriz de seguimiento y distribución

**D.1 — Matriz de seguimiento** (`50_informe/07_seguimiento.md`):

| ID | Recomendación | Severidad | Responsable (cargo) | Plazo | **Criterio de cierre verificable** | Fecha de verificación | Estado |
|---|---|---|---|---|---|---|---|
| R-01 | Implementar el proceso de gestión del ciclo de vida de identidades con revocación automática al cese | Crítico | Jefatura de RR. HH. y Jefatura de TI | 30 días | Conciliación usuarios activos vs. personal vigente con **cero excepciones**, y evidencia del proceso automatizado | | Abierto |
| R-02 | Ejecutar una prueba de restauración completa y ajustar el RTO declarado al tiempo real medido | Crítico | Jefatura de TI | 60 días | **Acta de prueba** con tiempo medido < MTPD de la actividad, firmada por el dueño del proceso | | Abierto |
| R-03 | Establecer al menos una copia de respaldo inmutable o fuera de línea | Alto | Jefatura de TI | 90 días | Evidencia de configuración de retención y **prueba fallida de eliminación** anticipada | | Abierto |

> **El criterio de cierre es lo que hace útil la matriz.** «Se implementó el control» no es verificable. «Conciliación con cero excepciones y evidencia del proceso automatizado» sí lo es, y evita la discusión sobre si la recomendación se cumplió.

**D.2 — Verificación de trazabilidad del informe.**

```python
# 30_papeles_trabajo/PT16_trazabilidad_informe.py
import re, glob
inf = open("../50_informe/INFORME_COMPLETO.md").read()
pts = {p.split("/")[-1].replace(".md","") for p in glob.glob("PT1*.md")}
ev  = {l.split("|")[1].strip() for l in open("../20_evidencia/CADENA_DE_CUSTODIA.md") if l.startswith("| E")}

refs_pt = set(re.findall(r"PT1\d-\d+", inf))
refs_ev = set(re.findall(r"E\d+-\d+", inf))

print(f"Papeles de trabajo referenciados en el informe : {len(refs_pt)} de {len(pts)}")
print(f"  NO referenciados (¿trabajo no reportado?)    : {sorted(pts - refs_pt)}")
print(f"  Referenciados pero inexistentes              : {sorted(refs_pt - pts)}")
print(f"\nEvidencia referenciada                        : {len(refs_ev)}")
print(f"  Referenciada pero no en la cadena de custodia : {sorted(refs_ev - ev)}")

# Control de lenguaje del resumen ejecutivo
res = inf.split("# Resumen Ejecutivo")[1].split("# ")[0]
TEC = r"\b(CVE|CVSS|socket|daemon|hash|SHA-256|endpoint|payload|SQL injection|XSS|contenedor)\b"
jerga = set(re.findall(TEC, res, re.I))
print(f"\nJerga técnica en el resumen ejecutivo: {jerga if jerga else 'ninguna ✔'}")
print(f"Palabras del resumen ejecutivo: {len(res.split())}  (objetivo: ≤ 900 ≈ 2 páginas)")

# Verificación de que no se nombran personas
print("\nRevisar manualmente que no figuren nombres de personas naturales.")
```

**D.3 — Carta de distribución controlada** (`50_informe/CARTA_DISTRIBUCION.md`):

| Destinatario (cargo) | Versión entregada | Anexos incluidos | Fecha | Formato | Acuse |
|---|---|---|---|---|---|
| Presidente del Directorio | Completa | A–F | | PDF cifrado | |
| Gerente General | Completa | A–F | | PDF cifrado | |
| Jefe de TI | Completa | A–F | | PDF cifrado | |
| Jefe de RR. HH. | Cuerpo del informe | Solo los hallazgos de su ámbito | | PDF | |

```bash
cd ../.. && sha256sum 50_informe/INFORME_FINAL.pdf >> 20_evidencia/SHA256SUMS_INFORME.txt
git add . && git commit -m "INF: informe final de auditoria, matriz de seguimiento y distribucion"
git tag -a informe-final -m "Informe final de auditoria de sistemas — version entregable"
```

---

### Paso E — Validar y corregir

El resultado no vale por estar hecho, sino por resistir una comprobación. Se ejecutan estas tres y **se corrige lo que falle antes de cerrar la sesión**.

1. Ejecutar el verificador y comprobar cero hallazgos sin criterio con código, sin efecto cuantificado o sin plazo.
2. Dar a leer el resumen ejecutivo a alguien ajeno al equipo y comprobar que entiende el veredicto sin preguntar nada.
3. Verificar que **ninguna persona natural** aparece nombrada en el informe.

> Lo que no se pueda corregir hoy se anota en la sección **Problemas y mejoras** de la evidencia, con lo que faltó y por qué. Un resultado parcial documentado con honestidad vale más que uno declarado sin prueba.

### Paso F — Registrar la evidencia y cerrar

Se versiona lo producido, se anota la URL de cada resultado y se responde en dos frases la pregunta de transferencia — **qué riesgo correría una organización real si esto se hiciera mal**.

---

## 3. Resultados

> **Evidencia obligatoria en GitHub.** Todo resultado de este taller se versiona en el repositorio del equipo. El informe **no consigna capturas sueltas**. Consigna la **URL** del artefacto en GitHub. Una captura no permite verificar autoría, fecha ni contenido; un enlace sí.
>
> | Qué se entrega | Dónde vive | Qué se escribe en el informe |
> |---|---|---|
> | Código y archivos de configuración | Rama del taller, fusionada a `develop` vía Pull Request | URL del Pull Request |
> | Documentos y matrices | `docs/`, en formato de texto versionable | URL del archivo en la rama |
> | Capturas y videos que el taller exija | `docs/evidencias/S16/` | URL del archivo |
> | Salida de comandos | `docs/evidencias/S16/salidas/*.txt` | URL del archivo |
>
> **Etiqueta del taller.** Al cerrar el taller se crea la etiqueta `taller-16` sobre el commit entregado:
>
> ```bash
> git tag -a taller-16 -m "Taller 16 · SI084"
> git push origin taller-16
> ```
>
> La URL que se consigna en el informe apunta a esa etiqueta:
> `https://github.com/<organizacion>/<repositorio>/tree/taller-16`
>
> **El informe es lo que se califica; el repositorio es lo que lo prueba.** Cada resultado de la sección 3 del informe lleva la URL con la que se verifica, y **un resultado sin su URL se califica como no logrado**, por bien redactado que esté. Lo que no se puede abrir no se puede dar por hecho.

### 3.1. Los tres resultados que se califican

Son los que la rúbrica evalúa. El resto de la lista tiene que existir, pero no se califica fila por fila.

| Resultado | Qué demuestra | Dónde está |
|---|---|---|
| **El informe final** | Las siete secciones y sus anexos, con índice, en PDF | `INFORME_FINAL.pdf` |
| **El resumen ejecutivo** | Novecientas palabras o menos, sin jerga, con veredicto explícito | Sección 1 y salida del verificador |
| **La matriz de seguimiento** | Criterio de cierre verificable en cada recomendación | Sección 7 del informe |

### 3.2. Lista de comprobación del taller

Todo esto debe existir al cerrar la sesión.

| # | Resultado esperado | Verificación |
|---|---|---|
| 1 | Hallazgos consolidados y priorizados por severidad y dominio | `INF_hallazgos_consolidados.csv` |
| 2 | **Cero hallazgos** sin criterio con código, sin efecto cuantificado o sin plazo | Salida del control de calidad |
| 3 | Acta de validación completa, con los ajustes derivados de la evidencia aportada | `ACTA_VALIDACION.md` |
| 4 | **Respuesta de la administración incorporada** en cada hallazgo | Sección 4 del informe |
| 5 | Informe final con las siete secciones y sus anexos, en PDF con índice | `INFORME_FINAL.pdf` |
| 6 | Resumen ejecutivo de **≤ 900 palabras** y **sin jerga técnica** | Salida del verificador |
| 7 | Conclusión general con veredicto explícito, base y alcance referenciados | Sección 1.2 |
| 8 | Gráfico del resumen ejecutivo generado | `resumen_hallazgos.png` |
| 9 | Matriz de seguimiento con **criterio de cierre verificable** en cada recomendación | Sección 7 |
| 10 | Verificador de trazabilidad. **Cero papeles de trabajo no referenciados** y cero referencias inexistentes | Salida de `PT16_trazabilidad_informe.py` |
| 11 | Ninguna persona natural nombrada en el informe | Revisión manual |
| 12 | Carta de distribución controlada con versiones diferenciadas por destinatario | `CARTA_DISTRIBUCION.md` |
| 13 | Etiqueta `informe-final` en Git y hash del PDF registrado | `git tag`, `SHA256SUMS_INFORME.txt` |

## Rúbrica procedimental (20 puntos)

Se aplica sobre el informe entregado y la evidencia enlazada en el repositorio. **Cada criterio se califica de forma independiente.**

| Criterio | 4 — Logrado | 2 — En proceso | 0 — Insuficiente |
|---|---|---|---|
| **Validación con el auditado** | Completo y correcto, con la evidencia que lo respalda | Completo con errores menores, o correcto pero sin toda la evidencia | Incompleto, o entregado sin ejecutar |
| **Ensamblar el informe** | Completo y correcto, con la evidencia que lo respalda | Completo con errores menores, o correcto pero sin toda la evidencia | Incompleto, o entregado sin ejecutar |
| **Evidencia verificable en el repositorio** | Cada resultado tiene su URL sobre la etiqueta `taller-NN`, y el enlace abre lo que dice | La mayoría tiene URL; alguna evidencia es una captura suelta | Se declaran resultados sin enlace, o el enlace no corresponde |
| **Trazabilidad de la evidencia** | Todo hallazgo o dato se rastrea hasta el archivo, registro y fecha que lo sustenta | Rastreable en su mayoría; algún dato sin origen | Se afirman hechos sin poder ubicarlos en la evidencia |
| **La evidencia entregada** | Las secciones de la plantilla completas; los papeles de trabajo quedan archivados y referenciados | Secciones completas con papeles de trabajo incompletos | Faltan secciones o no hay papeles de trabajo |

| Puntaje | Equivalencia |
|---|---|
| 18 – 20 | Destacado |
| 14 – 17 | Logrado |
| 6 – 13 | En proceso |
| 0 – 5 | Insuficiente |

> **Un resultado declarado sin evidencia enlazada no se califica**, aunque el trabajo se haya hecho. La tabla de la sección 3.1 es la lista de cotejo; esta rúbrica es lo que determina la nota.

## 4. Conclusiones

Mínimo tres. Líneas argumentales esperadas:

1. La validación previa con el auditado no debilita el informe. Lo blinda, porque los hallazgos que llegan al directorio ya resistieron el contraste con la evidencia de la parte interesada en refutarlos.
2. Un criterio de cierre verificable convierte la recomendación en un compromiso auditable; sin él, el seguimiento se reduce a preguntar si ya lo hicieron y a creer la respuesta.
3. El resumen ejecutivo es el único componente del informe que el directorio leerá completo. Su longitud y su lenguaje determinan si la auditoría produce decisiones o queda archivada.

## 5. Referencias Bibliográficas

- ISO 19011:2018, cláusulas 6.5 «Preparación y distribución del informe» y 6.6 «Finalización» y 6.7 «Seguimiento». https://www.iso.org/standard/70017.html
- ISACA. *ITAF: A Professional Practices Framework for IS Audit/Assurance* (5.ª ed.). https://www.isaca.org/resources/frameworks-standards-and-models
- The Institute of Internal Auditors. *Global Internal Audit Standards*. https://www.theiia.org/en/standards/
- COSO (*Committee of Sponsoring Organizations of the Treadway Commission*). (2013). *Internal Control — Integrated Framework*. https://www.coso.org/guidance-on-ic
- Contraloría General de la República del Perú. *Normas Generales de Control Gubernamental* y Ley 28716. https://www.gob.pe/contraloria
- Superintendencia de Banca, Seguros y AFP. *Reglamento de Auditoría Interna* y *Reglamento de Auditoría Externa*, modificados por la Res. SBS 504-2021. https://www.sbs.gob.pe/
- IFAC. *Normas Internacionales de Auditoría (NIA)* — NIA 265 sobre comunicación de deficiencias de control interno. https://www.iaasb.org/
- ISACA. (2018). *COBIT 2019*, dominio MEA. https://www.isaca.org/resources/cobit
- Piattini Velthuis, M., Del Peso Navarro, E. y Del Peso Ruiz, M. (2009). *Auditoría de tecnologías y sistemas de información* (6.ª ed.). Alfaomega / Ra-Ma.
- Franklin F., E. B. (2007). *Auditoría administrativa: gestión estratégica del cambio*. Pearson.

## 6. Anexos

- `anexo_A_informe_final.pdf` — informe completo.
- `anexo_B_acta_validacion.pdf`
- `anexo_C_matriz_seguimiento.xlsx`
- `anexo_D_carta_distribucion.pdf`
- `anexo_E_trazabilidad.pdf` — salida del verificador.

---

---

[Semana 16](README.md) · [Teoría](1-TEORIA.md) · [Dinámica de aula](2-DINAMICA.md) · **Taller de laboratorio**

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
