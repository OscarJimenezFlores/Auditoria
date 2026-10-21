[Semana 14](README.md) · [Teoría](1-TEORIA.md) · [Dinámica de aula](2-DINAMICA.md) · **Taller de laboratorio**

# Semana 14

## Evaluación del gobierno de TI y construcción del Balanced Scorecard de TI

**SI-084 - Auditoría de Sistemas** - Sesión 2 en laboratorio · calificación **procedimental**

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](../GLOSARIO.md).

---

## Qué entregas

| | |
|---|---|
| **Archivo** | `SI084-S14-TALLER-Grupo<N>.pdf` |
| **Plantilla obligatoria** | [SI084-PLANTILLA-TALLER.docx](../PLANTILLAS/SI084-PLANTILLA-TALLER.docx) |
| **Formato** | PDF exportado desde la plantilla en Word, con la carátula de la UPT, el índice actualizado y las capturas numeradas |
| **Qué va dentro** | Las secciones de la plantilla. La **5. Resultados y evidencias** se califica contra la tabla de resultados esperados de esta guía, y **cada resultado necesita la evidencia que lo demuestre**. No se copian de aquí los objetivos, la duración ni los resultados de aprendizaje |
| **Dónde se sube** | Aula virtual, tarea «Taller · Semana 14» |
| **Cuándo vence** | Según lo programado en el aula virtual |

> No se califica un informe entregado en `.docx`, sin carátula, sin los códigos de los integrantes o con resultados declarados sin evidencia.

---

## 1. Información sobre el evento práctico

### 1.1. Título del evento práctico

Evaluación del gobierno de tecnologías de información de la organización auditada contra los objetivos EDM de COBIT 2019 y los principios de la ISO/IEC 38500:2024, con construcción de un Balanced Scorecard de TI auditable y evaluación de la realización de beneficios de las inversiones.

### 1.2. Objetivos

- Evaluar los **cinco objetivos de gobierno (EDM01–EDM05)** con evidencia documental, no declarativa.
- Evaluar el cumplimiento de los **11 principios de la ISO/IEC 38500:2024** y verificar que el ciclo **Evaluar–Dirigir–Supervisar** esté cerrado.
- Aplicar el modelo **Val IT** a tres inversiones cerradas para verificar la **realización de beneficios**.
- Construir un **Balanced Scorecard de TI** con indicadores auditables en las cuatro perspectivas.
- **Probar** los indicadores existentes de la organización — verificar fórmula, fuente, meta y responsable.
- Producir **tres hallazgos de gobierno** dirigidos al directorio, no al área de TI.

### 1.3. Resultados de Aprendizaje (RA)

- **RA1** Diseña y aplica estrategias para los diversos tipos de auditoría de sistemas.
- **RA2** Descubre la importancia y diferencia entre auditor interno y externo.

### 1.4. Recursos

| Recurso | Detalle |
|---|---|
| **COBIT 2019** — dominio EDM y cascada de metas | https://www.isaca.org/resources/cobit |
| **ISO/IEC 38500:2024** | https://www.iso.org/standard/81684.html · vista previa en https://www.iso.org/obp/ui#iso:std:iso-iec:38500:ed-3:v1:en |
| **ISO 37000:2021** — principios de gobierno de organizaciones | https://www.iso.org/standard/65036.html |
| Documentos de la empresa | Actas de directorio o de comité, plan estratégico, presupuesto de TI, casos de negocio, reportes a la dirección |
| **Python 3.11+** con `pandas`, `matplotlib` | Cálculo de indicadores y tableros |
| **Metabase** (libre, Docker) o **LibreOffice Calc** | Tablero del BSC |
| **draw.io** | Diagrama de la cascada de metas |

### 1.5. Seguridad

1. Las actas de directorio y los presupuestos son información **Restringida**. Se consultan en las instalaciones de la empresa o mediante copia controlada, y no se replican en el repositorio.
2. En el papel de trabajo se registra la **referencia** al documento (acta N.º, fecha, punto de agenda), no su contenido íntegro.
3. Los datos financieros se agregan o se expresan en porcentajes cuando su publicación no es necesaria para sostener el hallazgo.
4. Si el equipo trabaja con el caso simulado, se declara explícitamente en el papel de trabajo.

---

## 2. Procedimiento o Metodología

> **Documento del caso para esta semana.** La organización entrega **Expedientes de las inversiones cerradas**, en `CASOS/EMPRESA-<NN>-<slug>/documentos/expedientes-de-inversion.md`. Es consistente con los datos de `datos/`. Las personas, usuarios y proveedores que menciona existen en los archivos. **No señala sus debilidades**; declara lo que la organización dice hacer.

### Paso A — Evaluar los objetivos de gobierno EDM

`30_papeles_trabajo/PT14-01_gobierno_edm.md`. Para cada objetivo, la regla es la misma — **la declaración de un directivo no sostiene ninguna calificación; solo la evidencia documental lo hace.**

| Objetivo | Procedimiento de auditoría | Evidencia solicitada | Excepción |
|---|---|---|---|
| **EDM01** Marco de gobierno | Solicitar el documento que establece la estructura de gobierno de TI; verificar composición, periodicidad y quórum del comité; revisar las actas de los últimos 12 meses | Estatuto o política; actas del comité | No existe estructura formal, o el comité no sesionó en el periodo |
| **EDM02** Entrega de beneficios | Seleccionar 3 inversiones de TI cerradas; solicitar su caso de negocio y **la medición del beneficio realizado** | Caso de negocio y medición posterior | Inversión sin caso de negocio, o sin medición del beneficio |
| **EDM03** Optimización del riesgo | Solicitar la declaración de apetito de riesgo aprobada y los informes de riesgo tecnológico presentados al directorio | Declaración de apetito; actas donde se discutió riesgo de TI | Sin apetito declarado, o riesgo de TI nunca tratado en directorio |
| **EDM04** Optimización de recursos | Obtener el presupuesto de TI de dos ejercicios; analizar su distribución entre operar, crecer y transformar; contrastar con las prioridades estratégicas declaradas | Presupuesto aprobado y ejecutado | Presupuesto sin vínculo con las prioridades estratégicas |
| **EDM05** Transparencia | Identificar qué información sobre TI recibe el directorio, con qué frecuencia y en qué formato | Reportes efectivamente entregados | El directorio no recibe información periódica de TI |

**Análisis del presupuesto (EDM04)** — la prueba que revela la estrategia real:

```python
# 30_papeles_trabajo/PT14_presupuesto.py
import pandas as pd, matplotlib.pyplot as plt

p = pd.DataFrame([
 # categoria, ejecutado_periodo_anterior, solicitado_periodo, tipo
 ("Licencias y suscripciones",   180000, 210000, "Operar"),
 ("Infraestructura y nube",      120000, 145000, "Operar"),
 ("Soporte y personal operativo",240000, 250000, "Operar"),
 ("Mantenimiento correctivo",     60000,  72000, "Operar"),
 ("Nuevos módulos del ERP",       90000,  40000, "Crecer"),
 ("Canal digital",                45000,  20000, "Crecer"),
 ("Analítica de datos",           30000,      0, "Transformar"),
 ("Seguridad de la información",  25000,  18000, "Operar"),
], columns=["categoria","anio_ant","anio_act","tipo"])

r = p.groupby("tipo")[["anio_ant","anio_act"]].sum()
r["var_%"] = ((r.anio_act/r.anio_ant - 1)*100).round(1)
r["part_2026_%"] = (r.anio_act/r.anio_act.sum()*100).round(1)
print(r.to_string())
print(f"\nAño anterior: {p.anio_ant.sum():,} | Año en curso: {p.anio_act.sum():,}  "
      f"({(p.anio_act.sum()/p.anio_ant.sum()-1)*100:+.1f} %)")
print(f"Seguridad de la información: {p[p.categoria.str.contains('Seguridad')].anio_act.iloc[0]/p.anio_act.sum()*100:.1f} % del presupuesto")

r[["anio_ant","anio_act"]].plot.bar(figsize=(8,5), title="Presupuesto de TI por tipo de inversión")
plt.ylabel("S/"); plt.tight_layout(); plt.savefig("../20_evidencia/E14_gob/presupuesto.png", dpi=140)
```

> **Lectura de auditor.** Una distribución en la que «Operar» crece y «Transformar» desaparece revela que la organización **declara** una estrategia de transformación digital y **financia** el mantenimiento del statu quo. Ese contraste entre lo declarado y lo presupuestado es un hallazgo de gobierno de primer orden, y su criterio es EDM04 más el principio de **Estrategia** de la ISO/IEC 38500:2024.

### Paso B — Evaluar los 11 principios de la ISO/IEC 38500:2024

`30_papeles_trabajo/PT14-02_principios_38500.csv`:

| # | Principio (edición 2024) | Pregunta de auditoría | Evidencia | ¿Cumple? | Observación |
|---|---|---|---|---|---|
| 1 | **Propósito** | ¿El uso de TI está explícitamente vinculado al propósito declarado de la organización? | Plan estratégico, acta de directorio | | |
| 2 | **Generación de valor** | ¿Se define y se mide el valor que TI debe generar? | Casos de negocio con medición posterior | | |
| 3 | **Estrategia** | ¿Existe una estrategia de TI derivada de la del negocio y con presupuesto asignado? | Plan de TI, presupuesto | | |
| 4 | **Supervisión** | ¿El órgano de gobierno supervisa el desempeño y la conformidad de TI? | Reportes recibidos, actas | | |
| 5 | **Rendición de cuentas** | ¿Están definidas las responsabilidades por las decisiones de TI? | Matriz RACI, estatuto de gobierno | | |
| 6 | **Compromiso con las partes interesadas** | ¿Se identifican y consideran las necesidades de usuarios, clientes y reguladores? | Encuestas, actas de comité, requisitos regulatorios | | |
| 7 | **Liderazgo** | ¿La dirección modela la conducta esperada respecto del uso de TI y de la información? | Política de uso aceptable firmada por la dirección; conducta observada | | |
| 8 | **Datos y decisiones** | ¿Las decisiones sobre TI se toman con datos y evidencia? | Actas con datos citados; existencia de indicadores usados en decisiones | | |
| 9 | **Gobierno del riesgo** | ¿El riesgo tecnológico llega al directorio con un apetito declarado? | Declaración de apetito; informes de riesgo | | |
| 10 | **Responsabilidad social** | ¿Se consideran los efectos del uso de TI sobre las personas, la privacidad y el ambiente? | Cumplimiento de la Ley 29733; política de residuos electrónicos | | |
| 11 | **Viabilidad y desempeño en el tiempo** | ¿La arquitectura y las capacidades actuales son sostenibles a mediano plazo? | Análisis de obsolescencia, plan de renovación, gestión de deuda técnica | | |

**Verificación del ciclo cerrado.** Se completa la tabla que determina si hay gobierno o solo intención:

| Objetivo estratégico de TI | ¿Se **evaluó** antes de decidir? | ¿Se **dirigió** con una instrucción formal? | ¿Se **supervisó** el resultado? | Ciclo cerrado |
|---|---|---|---|---|

### Paso C — Val IT · la prueba de realización de beneficios

Para tres inversiones de TI cerradas en los últimos 24 meses:

| Campo | Inversión 1 | Inversión 2 | Inversión 3 |
|---|---|---|---|
| Descripción y año | | | |
| Monto aprobado / ejecutado | | | |
| ¿Existe caso de negocio? | | | |
| Beneficio **proyectado** (cifra y unidad) | | | |
| ¿Se definió cómo se mediría? | | | |
| Beneficio **realizado** (cifra medida) | | | |
| ¿Quién midió y cuándo? | | | |
| Desviación | | | |
| **Veredicto** | | | |

> Si las tres columnas quedan vacías en «beneficio realizado», ese es el hallazgo. La organización aprueba inversiones con promesa de valor y **nunca verifica si el valor llegó**. **Criterio.** COBIT 2019 **EDM02**; ISO/IEC 38500:2024, principio de **Generación de valor**.

### Paso D — Construir y probar el Balanced Scorecard de TI

**D.1 — Probar los indicadores existentes.** Antes de proponer, se auditan los que ya hay:

| Indicador declarado por TI | ¿Tiene fórmula explícita? | ¿Fuente del dato identificada? | ¿Tiene meta? | ¿Tiene responsable? | ¿Se usó en alguna decisión? | Veredicto |
|---|---|---|---|---|---|---|

**D.2 — Construir el BSC de TI.**

```python
# 30_papeles_trabajo/PT14_bsc.py
import pandas as pd

BSC = pd.DataFrame([
 # perspectiva, indicador, formula, fuente, frecuencia, meta, actual, responsable
 ("Contribución al negocio","Gasto de TI sobre ingresos",
  "Gasto total de TI / Ingresos netos × 100","Estados financieros + presupuesto TI",
  "Trimestral","≤ 3,5 %", "4,2 %","Gerencia de Administración"),
 ("Contribución al negocio","Beneficio realizado de inversiones cerradas",
  "Σ beneficio medido / Σ beneficio proyectado × 100","Casos de negocio + medición posterior",
  "Semestral","≥ 80 %","No se mide","Comité de TI"),
 ("Contribución al negocio","Costo por transacción procesada",
  "Gasto de TI del proceso / N.º de transacciones","ERP + contabilidad analítica",
  "Mensual","≤ S/ 0,85","S/ 1,12","Gerencia de Operaciones"),

 ("Orientación al usuario","Satisfacción del usuario interno",
  "Promedio de la encuesta trimestral (escala 1–5)","Encuesta a usuarios",
  "Trimestral","≥ 4,0","3,1","Jefatura de TI"),
 ("Orientación al usuario","Cumplimiento del nivel de servicio",
  "Solicitudes atendidas dentro del SLA / Total × 100","Mesa de ayuda",
  "Mensual","≥ 90 %","76 %","Jefatura de TI"),

 ("Excelencia operativa","Disponibilidad de servicios críticos",
  "(Tiempo total − tiempo de indisponibilidad) / Tiempo total × 100","Monitoreo",
  "Mensual","≥ 99,5 %","98,7 %","Jefatura de TI"),
 ("Excelencia operativa","Tasa de cambios fallidos",
  "Cambios revertidos o con incidente / Total de cambios × 100","Registro de cambios",
  "Mensual","≤ 5 %","14 %","Jefatura de Desarrollo"),
 ("Excelencia operativa","Tiempo medio de recuperación (MTTR)",
  "Σ tiempo de resolución de incidentes S1 / N.º de incidentes S1","Mesa de ayuda",
  "Mensual","≤ 4 h","7,5 h","Jefatura de TI"),

 ("Orientación al futuro","Obsolescencia tecnológica",
  "Activos fuera de soporte del fabricante / Total de activos × 100","Inventario de activos",
  "Semestral","≤ 10 %","34 %","Jefatura de TI"),
 ("Orientación al futuro","Participación de la inversión en transformación",
  "Presupuesto 'Transformar' / Presupuesto total de TI × 100","Presupuesto",
  "Anual","≥ 15 %","0 %","Comité de TI"),
 ("Orientación al futuro","Cobertura de competencias críticas",
  "Competencias críticas con ≥ 2 personas capacitadas / Total × 100","Matriz de competencias",
  "Semestral","100 %","55 %","RR. HH. + TI"),
], columns=["perspectiva","indicador","formula","fuente","frecuencia","meta","actual","responsable"])

BSC.to_csv("../40_hallazgos/PT14_bsc_ti.csv", index=False)
for persp, g in BSC.groupby("perspectiva", sort=False):
    print(f"\n{'='*90}\n{persp.upper()}")
    print(g[["indicador","meta","actual","responsable"]].to_string(index=False))
```

**D.3 — Los tres hallazgos de gobierno.** Se redactan en `40_hallazgos/`, dirigidos **al directorio**, no a TI. La diferencia está en la recomendación. Un hallazgo de gobierno no se corrige comprando tecnología, se corrige creando un mecanismo de decisión.

```bash
sha256sum 20_evidencia/E14_gob/* 40_hallazgos/PT14_*.csv >> 20_evidencia/SHA256SUMS_E14.txt
git add . && git commit -m "E14: evaluacion de gobierno de TI, principios ISO 38500:2024 y BSC de TI"
```

---

### Paso E — Validar y corregir

El resultado no vale por estar hecho, sino por resistir una comprobación. Se ejecutan estas tres y **se corrige lo que falle antes de cerrar la sesión**.

1. Comprobar que los cinco objetivos EDM se evaluaron con **evidencia documental**, no con la declaración del entrevistado.
2. Verificar que el contraste entre estrategia declarada y financiada está escrito como tal, con las cifras de los dos ejercicios.
3. Revisar que ninguna de las tres recomendaciones al directorio consiste en adquirir una herramienta.

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
> | Capturas y videos que el taller exija | `docs/evidencias/S14/` | URL del archivo |
> | Salida de comandos | `docs/evidencias/S14/salidas/*.txt` | URL del archivo |
>
> **Etiqueta del taller.** Al cerrar el taller se crea la etiqueta `taller-14` sobre el commit entregado:
>
> ```bash
> git tag -a taller-14 -m "Taller 14 · SI084"
> git push origin taller-14
> ```
>
> La URL que se consigna en el informe apunta a esa etiqueta:
> `https://github.com/<organizacion>/<repositorio>/tree/taller-14`
>
> **El informe es lo que se califica; el repositorio es lo que lo prueba.** Cada resultado de la sección 3 del informe lleva la URL con la que se verifica, y **un resultado sin su URL se califica como no logrado**, por bien redactado que esté. Lo que no se puede abrir no se puede dar por hecho.

### 3.1. Los tres resultados que se califican

Son los que la rúbrica evalúa. El resto de la lista tiene que existir, pero no se califica fila por fila.

| Resultado | Qué demuestra | Dónde está |
|---|---|---|
| **El contraste estrategia declarada frente a financiada** | Las cifras de dos ejercicios por tipo de gasto, con la conclusión escrita | Papel de trabajo y `presupuesto.png` |
| **El cuadro de mando de TI** | Tres indicadores por perspectiva y tres de contribución al negocio, con fórmula y meta | `PT14_bsc_ti.csv` |
| **Los tres hallazgos de gobierno** | Dirigidos al directorio, citando la edición 2024 de la ISO/IEC 38500 | `40_hallazgos/` |

### 3.2. Lista de comprobación del taller

Todo esto debe existir al cerrar la sesión.

| # | Resultado esperado | Verificación |
|---|---|---|
| 1 | Los cinco objetivos EDM evaluados **con evidencia documental**, no declarativa | `PT14-01_gobierno_edm.md` |
| 2 | Análisis del presupuesto de TI por tipo (operar/crecer/transformar) de dos ejercicios | `presupuesto.png` y salida del script |
| 3 | Contraste explícito entre **la estrategia declarada y la estrategia financiada** | Papel de trabajo |
| 4 | Los **11 principios** de la ISO/IEC 38500:**2024** evaluados con evidencia | `PT14-02_principios_38500.csv` |
| 5 | Verificación de **ciclo cerrado** Evaluar–Dirigir–Supervisar para al menos 3 decisiones | Tabla del Paso B |
| 6 | Val IT aplicado a **tres inversiones cerradas** con veredicto de realización de beneficios | Tabla del Paso C |
| 7 | Auditoría de los indicadores existentes — fórmula, fuente, meta, responsable y uso en decisiones | Tabla D.1 |
| 8 | BSC de TI con **al menos 3 indicadores por perspectiva**, todos con fórmula y meta | `PT14_bsc_ti.csv` |
| 9 | **Al menos 3 indicadores de contribución al negocio**, no solo operativos | Revisión del BSC |
| 10 | Tres hallazgos de gobierno dirigidos al directorio, cuya recomendación **no sea comprar tecnología** | `40_hallazgos/` |
| 11 | Criterio citado con la edición **2024** de la ISO/IEC 38500 | Revisión de los hallazgos |
| 12 | Hashes y *commit* en Git | `SHA256SUMS_E14.txt` |

## Rúbrica procedimental (20 puntos)

Se aplica sobre el informe entregado y la evidencia enlazada en el repositorio. **Cada criterio se califica de forma independiente.**

| Criterio | 4 — Logrado | 2 — En proceso | 0 — Insuficiente |
|---|---|---|---|
| **Evaluar los objetivos de gobierno EDM** | Completo y correcto, con la evidencia que lo respalda | Completo con errores menores, o correcto pero sin toda la evidencia | Incompleto, o entregado sin ejecutar |
| **Evaluar los 11 principios de la ISO/IEC 38500:2024** | Completo y correcto, con la evidencia que lo respalda | Completo con errores menores, o correcto pero sin toda la evidencia | Incompleto, o entregado sin ejecutar |
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

1. El gobierno de TI se audita en las actas del directorio y en el presupuesto, no en el área de sistemas; una gestión impecable sobre un gobierno inexistente produce eficiencia sin dirección.
2. El presupuesto revela la estrategia real de la organización con más fidelidad que el plan estratégico. Donde no hay dinero asignado no hay prioridad, cualquiera sea el documento que la declare.
3. La ausencia de medición del beneficio realizado convierte el caso de negocio en un trámite de aprobación; sin verificación posterior, la organización no puede aprender de sus decisiones de inversión.

## 5. Referencias Bibliográficas

- ISO/IEC 38500:2024. *Information technology — Governance of IT for the organization* (3.ª edición; cancela y reemplaza la ISO/IEC 38500:2015). https://www.iso.org/standard/81684.html
- ISO 37000:2021. *Governance of organizations — Guidance*. https://www.iso.org/standard/65036.html
- ISACA. (2018). *COBIT 2019 Framework: Governance and Management Objectives*, dominio EDM y cascada de metas. https://www.isaca.org/resources/cobit
- ISACA. (2018). *COBIT 2019 Framework: Introduction and Methodology*. https://www.isaca.org/resources/cobit
- ISACA. *Val IT Framework — Enterprise Value: Governance of IT Investments*. https://www.isaca.org/resources/frameworks-standards-and-models
- Kaplan, R. S. y Norton, D. P. (1996). *The Balanced Scorecard: Translating Strategy into Action*. Harvard Business School Press.
- Kaplan, R. S. y Norton, D. P. (2004). *Strategy Maps: Converting Intangible Assets into Tangible Outcomes*. Harvard Business School Press.
- Van Grembergen, W. y De Haes, S. (2009). *Enterprise Governance of Information Technology*. Springer.
- Piattini Velthuis, M., Del Peso Navarro, E. y Del Peso Ruiz, M. (2009). *Auditoría de tecnologías y sistemas de información* (6.ª ed.). Alfaomega / Ra-Ma.

## 6. Anexos

- `anexo_A_evaluacion_edm.pdf`
- `anexo_B_principios_38500.xlsx`
- `anexo_C_presupuesto_ti.png`
- `anexo_D_valit_inversiones.xlsx`
- `anexo_E_bsc_ti.xlsx` — tablero completo con las cuatro perspectivas
- `anexo_F_cascada_metas.png`

---

---

[Semana 14](README.md) · [Teoría](1-TEORIA.md) · [Dinámica de aula](2-DINAMICA.md) · **Taller de laboratorio**

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
