[Semana 13](README.md) · [Teoría](1-TEORIA.md) · [Dinámica de aula](2-DINAMICA.md) · **Taller de laboratorio**

# Semana 13

## Trabajo de campo, papeles de trabajo y redacción de hallazgos

**SI-084 - Auditoría de Sistemas** - Sesión 2 en laboratorio · calificación **procedimental**

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](../GLOSARIO.md).

---

## Qué entregas

| | |
|---|---|
| **Archivo** | `SI084-S13-TALLER-Grupo<N>.pdf` |
| **Plantilla obligatoria** | [SI084-PLANTILLA-TALLER.docx](../PLANTILLAS/SI084-PLANTILLA-TALLER.docx) |
| **Formato** | PDF exportado desde la plantilla en Word, con la carátula de la UPT, el índice actualizado y las capturas numeradas |
| **Qué va dentro** | Las secciones de la plantilla. La **5. Resultados y evidencias** se califica contra la tabla de resultados esperados de esta guía, y **cada resultado necesita la evidencia que lo demuestre**. No se copian de aquí los objetivos, la duración ni los resultados de aprendizaje |
| **Dónde se sube** | Aula virtual, tarea «Taller · Semana 13» |
| **Cuándo vence** | Según lo programado en el aula virtual |

> No se califica un informe entregado en `.docx`, sin carátula, sin los códigos de los integrantes o con resultados declarados sin evidencia.

---

## 1. Información sobre el evento práctico

### 1.1. Título del evento práctico

Ejecución del trabajo de campo sobre la empresa auditada conforme al plan del Encargo 12 aprobado, con producción de papeles de trabajo trazables, redacción de hallazgos en estructura CCCER y preparación del acta de validación con el auditado.

### 1.2. Objetivos

- Ejecutar los procedimientos de **controles generales de TI** del programa consolidado sobre la empresa real.
- Producir **papeles de trabajo completos**, con referencia cruzada al programa y a la evidencia sellada.
- Redactar **al menos cinco hallazgos** en estructura CCCER, con causa raíz derivada de los cinco porqués.
- **Clasificar la severidad** de cada hallazgo con criterio de riesgo documentado.
- Preparar el **acta de validación** para contrastar los hallazgos con el responsable del proceso.
- Verificar la **trazabilidad completa**. Procedimiento → papel de trabajo → evidencia → hallazgo.

### 1.3. Resultados de Aprendizaje (RA)

- **RA1** Diseña y aplica estrategias para los diversos tipos de auditoría de sistemas.
- **RA2** Descubre la importancia y diferencia entre auditor interno y externo.

### 1.4. Recursos

| Recurso | Detalle |
|---|---|
| Plan Integral v2.0 | `10_planificacion/PLAN_INTEGRAL_AUDITORIA.md` |
| Información recibida de la empresa | Según la matriz PBC de la Semana 08 |
| **LibreOffice Calc / Python + pandas** | Análisis de las extracciones recibidas |
| **Markdown + Pandoc** | Papeles de trabajo y hallazgos |
| **Git** | Versionado y sellado |
| `ANEXO-CASO-SIMULADO.md` | Dataset completo para equipos sin acceso a empresa real |

### 1.5. Seguridad

1. Toda la información de la empresa se clasifica **Confidencial**; la que contenga datos personales, **Restringido**.
2. Se trabaja sobre **copias** de la información entregada; nunca se modifica el archivo original recibido.
3. Se calcula el hash de cada archivo **en el momento de recibirlo** y se registra en la cadena de custodia con el nombre de quien lo entregó.
4. **En el informe no se nombran personas naturales**. Se usan cargos. La única excepción son las firmas del propio equipo auditor.
5. Al cierre del encargo, la información se devuelve o se destruye según lo acordado en la carta de encargo, dejando acta.

---

## 2. Procedimiento o Metodología

> **Documento del caso para esta semana.** La organización entrega **Registro de cambios y de respaldos**, en `CASOS/EMPRESA-<NN>-<slug>/documentos/extracciones-y-registros.md`. Es consistente con los datos de `datos/`. Las personas, usuarios y proveedores que menciona existen en los archivos. **No señala sus debilidades**; declara lo que la organización dice hacer.

### Paso A — Recepción y sellado de la evidencia

```bash
mkdir -p 20_evidencia/E13_campo && cd 20_evidencia/E13_campo
# Los archivos recibidos se sellan ANTES de abrirlos
sha256sum * | tee ../SHA256SUMS_E13.txt
```

Se registra en `20_evidencia/CADENA_DE_CUSTODIA.md`:

| ID | Archivo | SHA-256 | Fecha y hora (UTC) | Entregado por (cargo) | Medio de entrega | Sistema origen | Recibido por |
|----|---------|---------|--------------------|----------------------|------------------|----------------|--------------|
| E13-01 | usuarios_erp.csv | … | aaaa-mm-ddThh:mm:ssZ | Jefe de TI | Correo institucional | ERP módulo Seguridad | … |

> **Control de integridad de la extracción.** Antes de analizar se verifica el total de control — conteo de registros y, cuando aplica, suma de un campo numérico, contrastados con la cifra que reporta el sistema. Si no coinciden, el análisis se detiene y se documenta la limitación.

### Paso B — Ejecutar los procedimientos y producir papeles de trabajo

Se ejecutan al menos **seis procedimientos** del programa. Plantilla de papel de trabajo (`30_papeles_trabajo/PT13-01.md`):

```markdown
# PT13-01 — Revisión del ciclo de vida de los usuarios del ERP
| Campo | Contenido |
|---|---|
| **Referencia del programa** | P-03 |
| **Objetivo del procedimiento** | Verificar que los accesos se revocan oportunamente al cese del vínculo laboral |
| **Criterio** | ISO/IEC 27001:2022 A.5.18 *Access rights*; COBIT 2019 DSS05.04; Política de Seguridad de la Información vigente, numeral 6.3 |
| **Población** | 87 usuarios activos del ERP al dd/mm/aaaa (E13-01, SHA-256: …) |
| **Muestra** | 100 % — CAAT, sin muestreo |
| **Método** | Cruce del listado de usuarios activos contra la relación de personal vigente (E13-02) |
| **Definición de excepción** | (fijada en el programa) Cualquier usuario activo sin vínculo laboral vigente |
| **Fuente** | E13-01 entregado por el Jefe de TI el dd/mm/aaaa; E13-02 por el Jefe de RR. HH. el dd/mm/aaaa |

## Trabajo realizado
1. Se verificó la integridad de ambas extracciones: 87 y 64 registros, coincidentes con los
   totales reportados por los sistemas de origen.
2. Se normalizaron los campos de identificación (DNI) en ambos archivos.
3. Se ejecutó el cruce mediante el script `PT13-01_cruce.py` (adjunto).
4. Se solicitó al Jefe de TI la fecha del último acceso de cada usuario excepcionado.

## Resultado
| Métrica | Valor |
|---|---|
| Usuarios activos en el ERP | 87 |
| Personal con vínculo vigente | 64 |
| Usuarios activos sin vínculo vigente | **23** |
| De ellos, con acceso registrado tras la fecha de cese | **4** |
| Antigüedad máxima del cese sin revocación | 14 meses |
| Usuarios con rol de administrador entre los excepcionados | 2 |

## Excepciones
23 usuarios cumplen la definición de excepción. Detalle en `PT13-01_excepciones.csv`
(identificados por código de usuario, no por nombre).

## Conclusión
El control de revocación de accesos al cese **no es efectivo** en su eficacia operativa
durante el periodo auditado. El 26,4 % de las cuentas activas corresponden a personas sin
vínculo laboral vigente, y cuatro de ellas registran actividad posterior al cese.

## Referencia cruzada
Origina el hallazgo **H-101**.

| Ejecutado por | Fecha | Revisado por | Fecha |
|---|---|---|---|
| | | | |
```

**Los seis procedimientos mínimos del laboratorio.**

| PT | Objetivo | Tipo | Criterio |
|---|---|---|---|
| PT13-01 | Revocación de accesos al cese | CAAT 100 % | A.5.18 · DSS05.04 |
| PT13-02 | Cuentas privilegiadas y su justificación | Inspección del sistema | A.8.2 · DSS05.04 |
| PT13-03 | Autorización de cambios a producción | Inspección documental, muestra de 25 | A.8.32 · BAI06.01 |
| PT13-04 | Segregación desarrollo-producción | Inspección del sistema | A.8.31 · BAI07 |
| PT13-05 | Existencia y prueba de respaldos | Inspección + reejecución | A.8.13 · DSS04.07 |
| PT13-06 | Registro de eventos y su protección | Inspección del sistema | A.8.15 · DSS01.03 |

### Paso C — Redactar los hallazgos con causa raíz

Plantilla (`40_hallazgos/H-101.md`):

```markdown
# H-101 · Accesos no revocados al cese del vínculo laboral

| | |
|---|---|
| **Severidad** | **Crítico** |
| **Dominio** | Controles generales de TI — Gestión de accesos |
| **Papel de trabajo** | PT13-01 |
| **Evidencia** | E13-01 (SHA-256: …), E13-02 (SHA-256: …) |

## Condición
Al cierre del período auditado, 23 de los 87 usuarios activos del ERP (26,4 %) corresponden a
personas cuyo vínculo laboral con la organización concluyó. Cuatro de estas cuentas
registran actividad posterior a la fecha de cese; la más antigua corresponde a un cese
ocurrido 14 meses antes de la fecha de corte. Dos de las cuentas excepcionadas tienen
asignado el rol de administrador del módulo de Compras.

## Criterio
- ISO/IEC 27001:2022, Anexo A, control **A.5.18 Access rights**: los derechos de acceso
  deben ser retirados al término del empleo.
- COBIT 2019, práctica **DSS05.04 Manage user identity and logical access**.
- Política de Seguridad de la Información de la organización, v1.2, numeral 6.3, que
  establece la revocación dentro de las 24 horas del cese.

## Causa
No existe un proceso formal de gestión del ciclo de vida de las identidades que integre a
Recursos Humanos y a Tecnologías de la Información. El procedimiento vigente contempla el
alta —solicitada por el área usuaria— pero no la baja, que depende de que alguien la
recuerde. No hay notificación automática de ceses desde el sistema de planilla ni revisión
periódica de accesos que detecte la desviación.

## Efecto
Veintitrés personas ajenas a la organización conservan la capacidad de acceder a la
información del ERP, que incluye datos de 8 400 clientes y el maestro de proveedores. Dos
de ellas pueden crear proveedores y modificar órdenes de compra. Cuatro accedieron
efectivamente tras su cese, lo que constituye un acceso no autorizado. Además del riesgo de
fraude —acotado por el monto máximo de aprobación del rol— la situación expone a la
organización a una infracción del artículo 9 de la Ley 29733, sancionable por la ANPD.

## Recomendación
Implementar un proceso de gestión del ciclo de vida de identidades en el que el registro
del cese en el sistema de planilla genere automáticamente la solicitud de revocación de
todos los accesos del trabajador, con verificación de cierre en un plazo máximo de 24 horas
y revisión trimestral de conciliación entre usuarios activos y personal vigente.

| Responsable propuesto | Plazo | Verificación de cierre |
|---|---|---|
| Jefatura de Recursos Humanos y Jefatura de TI | 30 días | Conciliación con cero excepciones y evidencia del proceso automatizado |

## Respuesta de la administración
*(A completar tras la reunión de cierre — Semana 16)*
```

**Se producen al menos cinco hallazgos**, cada uno con causa raíz obtenida por los cinco porqués. El análisis de causa se documenta en `30_papeles_trabajo/PT13_causa_raiz.md`.

### Paso D — Verificar la trazabilidad y preparar la validación

```python
# 30_papeles_trabajo/PT13_trazabilidad.py
import re, glob, pathlib, pandas as pd

prog = pd.read_csv("../10_planificacion/E1_programa_trabajo.csv")
pts  = {pathlib.Path(f).stem: open(f).read() for f in glob.glob("PT13-*.md")}
hall = {pathlib.Path(f).stem: open(f).read() for f in glob.glob("../40_hallazgos/H-*.md")}

print("=== TRAZABILIDAD PROGRAMA → PAPEL DE TRABAJO ===")
for _, p in prog.iterrows():
    ejec = [k for k, v in pts.items() if p.id in v]
    print(f"{p.id}: {'✔ ' + ', '.join(ejec) if ejec else '✗ SIN EJECUTAR'}")

print("\n=== TRAZABILIDAD PAPEL DE TRABAJO → HALLAZGO ===")
for k, v in pts.items():
    hs = re.findall(r"H-\d+", v)
    print(f"{k}: {'origina ' + ', '.join(set(hs)) if hs else 'sin hallazgo (control efectivo)'}")

print("\n=== CONTROL DE CALIDAD DE LOS HALLAZGOS ===")
ADJ = r"\b(deficiente|inadecuad|malo|pobre|débil|insuficiente|preocupante|grave|pésim)\w*"
for k, v in hall.items():
    cond = v.split("## Condición")[1].split("##")[0] if "## Condición" in v else ""
    problemas = []
    for s in ["## Condición","## Criterio","## Causa","## Efecto","## Recomendación"]:
        if s not in v: problemas.append(f"falta {s.replace('## ','')}")
    if re.search(ADJ, cond, re.I): problemas.append("adjetivo valorativo en la condición")
    if not re.search(r"A\.\d+\.\d+|[A-Z]{3}\d{2}|art\.\s*\d+", v): problemas.append("criterio sin código")
    if not re.search(r"\d", v.split("## Efecto")[1][:600] if "## Efecto" in v else ""):
        problemas.append("efecto sin cuantificar")
    print(f"{k}: {'OK' if not problemas else ' | '.join(problemas)}")
```

**Acta de validación** (`40_hallazgos/ACTA_VALIDACION.md`), a usar en la reunión con el auditado:

| Hallazgo | Condición presentada | ¿El auditado la confirma? | Evidencia adicional aportada | Ajuste realizado | Posición final del auditado |
|---|---|---|---|---|---|
| H-101 | | Sí / No / Parcial | | | Acepta / Acepta con observación / Discrepa |

```bash
cd ../.. && sha256sum 30_papeles_trabajo/PT13-* 40_hallazgos/H-1*.md >> 20_evidencia/SHA256SUMS_E13.txt
git add . && git commit -m "E13: trabajo de campo, papeles de trabajo y hallazgos CCCER"
```

---

### Paso E — Validar y corregir

El resultado no vale por estar hecho, sino por resistir una comprobación. Se ejecutan estas tres y **se corrige lo que falle antes de cerrar la sesión**.

1. Ejecutar el verificador de trazabilidad y corregir hasta que devuelva cero en ambos conteos.
2. Comprobar que cada papel de trabajo tiene **conclusión explícita** sobre la efectividad del control, no solo el resultado de la prueba.
3. Revisar que **ninguna persona natural** aparece nombrada en los hallazgos.

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
> | Capturas y videos que el taller exija | `docs/evidencias/S13/` | URL del archivo |
> | Salida de comandos | `docs/evidencias/S13/salidas/*.txt` | URL del archivo |
>
> **Etiqueta del taller.** Al cerrar el taller se crea la etiqueta `taller-13` sobre el commit entregado:
>
> ```bash
> git tag -a taller-13 -m "Taller 13 · SI084"
> git push origin taller-13
> ```
>
> La URL que se consigna en el informe apunta a esa etiqueta:
> `https://github.com/<organizacion>/<repositorio>/tree/taller-13`
>
> **El informe es lo que se califica; el repositorio es lo que lo prueba.** Cada resultado de la sección 3 del informe lleva la URL con la que se verifica, y **un resultado sin su URL se califica como no logrado**, por bien redactado que esté. Lo que no se puede abrir no se puede dar por hecho.

### 3.1. Los tres resultados que se califican

Son los que la rúbrica evalúa. El resto de la lista tiene que existir, pero no se califica fila por fila.

| Resultado | Qué demuestra | Dónde está |
|---|---|---|
| **Los seis papeles de trabajo** | Los doce campos completos y conclusión explícita en cada uno | `PT13-01` a `PT13-06` |
| **Los cinco hallazgos con causa raíz** | Estructura CCCER y cinco porqués documentados | `40_hallazgos/H-1xx.md` y `PT13_causa_raiz.md` |
| **La trazabilidad verificada** | Cero procedimientos sin ejecutar y cero hallazgos con problemas | Salida del verificador |

### 3.2. Lista de comprobación del taller

Todo esto debe existir al cerrar la sesión.

| # | Resultado esperado | Verificación |
|---|---|---|
| 1 | Toda la evidencia recibida sellada **en el momento de recepción** y registrada en la cadena de custodia | `CADENA_DE_CUSTODIA.md` |
| 2 | Control de integridad de la extracción documentado para cada archivo analizado | Papeles de trabajo |
| 3 | **Seis papeles de trabajo** completos con los 12 campos de la plantilla | `PT13-01` a `PT13-06` |
| 4 | Cada papel de trabajo con **conclusión explícita** sobre la efectividad del control | Sección Conclusión |
| 5 | **Cinco hallazgos** en estructura CCCER completa | `40_hallazgos/H-1xx.md` |
| 6 | Análisis de causa raíz por cinco porqués documentado para cada hallazgo | `PT13_causa_raiz.md` |
| 7 | Verificador de trazabilidad ejecutado. **Cero procedimientos sin ejecutar** y **cero hallazgos con problemas** | Salida de `PT13_trazabilidad.py` |
| 8 | Severidad asignada a cada hallazgo con su criterio de asignación | Encabezado de cada hallazgo |
| 9 | Acta de validación preparada, con una fila por hallazgo | `ACTA_VALIDACION.md` |
| 10 | Ninguna persona natural nombrada en los hallazgos | Revisión del texto |
| 11 | Hashes y *commit* en Git | `SHA256SUMS_E13.txt` |

## Rúbrica procedimental (20 puntos)

Se aplica sobre el informe entregado y la evidencia enlazada en el repositorio. **Cada criterio se califica de forma independiente.**

| Criterio | 4 — Logrado | 2 — En proceso | 0 — Insuficiente |
|---|---|---|---|
| **Ejecutar los procedimientos y producir papeles de trabajo** | Completo y correcto, con la evidencia que lo respalda | Completo con errores menores, o correcto pero sin toda la evidencia | Incompleto, o entregado sin ejecutar |
| **Redactar los hallazgos con causa raíz** | Completo y correcto, con la evidencia que lo respalda | Completo con errores menores, o correcto pero sin toda la evidencia | Incompleto, o entregado sin ejecutar |
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

1. El papel de trabajo es el puente entre la evidencia y la conclusión. Si un tercero no puede rehacer el procedimiento con él en la mano, la conclusión no está sostenida aunque sea correcta.
2. La causa raíz determina la utilidad de la recomendación; una recomendación derivada del síntoma corrige el caso observado y garantiza que el hallazgo reaparezca en la siguiente auditoría.
3. Cuantificar el efecto en términos de negocio es lo que convierte un hallazgo técnico en una decisión de gerencia; sin esa traducción, el informe compite en desventaja con todas las demás prioridades de la organización.

## 5. Referencias Bibliográficas

- ISO 19011:2018, cláusula 6.5 «Preparación y distribución del informe de auditoría» y 6.4.8 «Generación de hallazgos». https://www.iso.org/standard/70017.html
- ISACA. *ITAF: A Professional Practices Framework for IS Audit/Assurance* (5.ª ed.), lineamientos de reporte y documentación. https://www.isaca.org/resources/frameworks-standards-and-models
- ISACA. (2018). *COBIT 2019*, DSS05.04, BAI06.01, BAI07, DSS04.07, DSS01.03. https://www.isaca.org/resources/cobit
- ISO/IEC 27001:2022, Anexo A, controles A.5.18, A.8.2, A.8.13, A.8.15, A.8.31, A.8.32. https://www.iso.org/standard/27001
- Ley 29733 y D. S. 016-2024-JUS. https://www.gob.pe/institucion/anpd
- The Institute of Internal Auditors. *Global Internal Audit Standards* — comunicación de resultados. https://www.theiia.org/en/standards/
- Contraloría General de la República del Perú. *Normas Generales de Control Gubernamental*. https://www.gob.pe/contraloria
- Piattini Velthuis, M., Del Peso Navarro, E. y Del Peso Ruiz, M. (2009). *Auditoría de tecnologías y sistemas de información* (6.ª ed.). Alfaomega / Ra-Ma. Capítulo del informe de auditoría.

## 6. Anexos

- `anexo_A_papeles_trabajo.pdf` — los seis papeles de trabajo completos.
- `anexo_B_hallazgos.pdf` — los cinco hallazgos.
- `anexo_C_causa_raiz.pdf` — análisis de cinco porqués.
- `anexo_D_cadena_custodia.pdf` — extracto del periodo del trabajo de campo.
- `anexo_E_acta_validacion.pdf` — acta preparada para la reunión con el auditado.

---

---

[Semana 13](README.md) · [Teoría](1-TEORIA.md) · [Dinámica de aula](2-DINAMICA.md) · **Taller de laboratorio**

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
