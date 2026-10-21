[Semana 07](README.md) · [Teoría](1-TEORIA.md) · **Dinámica de aula** · [Taller de laboratorio](3-TALLER.md)

# Semana 07

## Las cinco decisiones

**SI-084 - Auditoría de Sistemas** - Actividad en aula, **dentro de la sesión de teoría** · calificación **cognitiva**

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](../GLOSARIO.md).

---

## Qué entregas

| | |
|---|---|
| **Archivo** | `SI084-S07-DINAMICA-Grupo<N>.pdf` |
| **Plantilla obligatoria** | [SI084-PLANTILLA-DINAMICA.docx](../PLANTILLAS/SI084-PLANTILLA-DINAMICA.docx) |
| **Formato** | PDF exportado desde la plantilla en Word, con la carátula de la UPT y los apellidos, nombres y códigos de todos los integrantes |
| **Qué va dentro** | Lo que el grupo resolvió en aula. Las tablas de la sección **Producto** van completas, con los textos redactados, y cada decisión va justificada |
| **Dónde se sube** | Aula virtual, tarea «Dinámica · Semana 07» |
| **Cuándo vence** | Según lo programado en el aula virtual. La tabla se resuelve en aula; el PDF se formatea y se sube después |
| **Exposición** | En la ronda de cierre de **esta misma sesión**. El grupo **lee y explica su resultado** ante el aula, con el documento a la vista. No se usan diapositivas |

> No se califica un trabajo entregado en `.docx`, sin carátula, sin los códigos de los integrantes o con las tablas del producto vacías.

---

## Consigna

> **«Las cinco decisiones»**
> Cada equipo, sobre **su empresa real** (o el caso simulado), debe identificar **las cinco decisiones gerenciales más importantes** que la organización toma, rastrear con qué información se toma cada una y **evaluar la confiabilidad de esa cadena de información**.

| | |
|---|---|
| **Su papel** | **Auditor en la fase de planificación**, decidiendo qué entra al encargo |
| **Misión** | Rastrear con qué información se toman las cinco decisiones y evaluar si esa cadena es confiable |
| **Restricción** | **El dueño del dato se nombra por cargo.** Una decisión sin dueño se declara como hallazgo, no se le inventa uno |

Que el equipo deje de mirar los sistemas y mire las **decisiones** que esos sistemas alimentan. Una organización no se audita por su tecnología, sino por la confiabilidad de la información con la que decide.

## Lo que la teoría de hoy te da

Esta dinámica aplica piezas concretas de la sesión de teoría de hoy. Se usan tal cual, sin buscar nada más.

| De la teoría | Para qué se usa aquí |
|---|---|
| [Los componentes de TI como soporte a la decisión](1-TEORIA.md) | Da la cadena hecho, dato, información y decisión, que es exactamente el recorrido que el producto pide dibujar |
| [El universo auditable y el plan anual basado en riesgo](1-TEORIA.md) | Explica por qué se prioriza por criticidad de la decisión y no por tamaño del sistema |
| [Los pasos de la auditoría de sistemas](1-TEORIA.md) | Sitúa esta actividad en la fase de planificación del encargo, que es donde se decide qué se audita |

## Producto

**Producto 1 — Las cinco decisiones.**

| Decisión gerencial | Quién la toma | Frecuencia | Información que la sustenta | Sistema o fuente | Dueño del dato |
|---|---|---|---|---|---|

**Producto 2 — El eslabón más débil.** Para **una** de las cinco decisiones, la cadena completa hecho → decisión, señalando el eslabón más frágil, el riesgo concreto y el control que debería existir. Se exige indicar **si la información pasa por una hoja de cálculo** en algún punto y qué implica.

> **Dónde va.** Este producto se presenta en la **sección 2 de la [plantilla de dinámica](../PLANTILLAS/SI084-PLANTILLA-DINAMICA.docx)**, «El producto». No se copia la consigna ni la teoría. Solo el resultado y lo que lo sostiene.

## Ejemplo resuelto

*El caso de este ejemplo es distinto del que le toca a tu grupo. Sirve para que veas el nivel de detalle que se espera, no para copiarlo.*

**Una fila bien resuelta y una cadena completa.** El ejemplo es de una distribuidora de productos de consumo.

*Las cinco decisiones — una fila*

| Decisión gerencial | Quién la toma | Frecuencia | Información que la sustenta | Sistema o fuente | Dueño del dato |
|---|---|---|---|---|---|
| Cuánto comprar de cada producto para el mes siguiente | Jefe de Compras | Mensual, primera semana | Rotación de los últimos 90 días, stock actual y quiebres registrados | Reporte del ERP exportado a una hoja de cálculo que el analista ajusta a mano | **No hay dueño designado.** El ERP lo administra TI; el ajuste lo hace Compras |

*El eslabón más débil*

| Campo | Contenido |
|---|---|
| Cadena completa | Venta registrada en el punto de venta → consolidación nocturna en el ERP → exportación manual a hoja de cálculo → **ajuste manual del analista** → propuesta de compra → aprobación del Jefe de Compras → orden de compra |
| Eslabón más frágil | El ajuste manual en la hoja de cálculo. El analista corrige a mano las cantidades de los productos que «sabe» que el ERP calcula mal, sin dejar registro de qué cambió ni por qué. |
| ¿Pasa por una hoja de cálculo? | **Sí.** El archivo vive en el equipo del analista, sin control de versiones, sin respaldo y sin protección de fórmulas. Es la única copia. |
| Riesgo concreto | Una compra mensual de S/ 380 000 se decide sobre un archivo que una sola persona puede modificar sin dejar rastro y que se perdería si falla su equipo. Un error de fórmula en una celda, o su ausencia por vacaciones, altera la compra del mes sin que nadie lo detecte. |
| Control que debería existir | La lógica del ajuste se incorpora al ERP como parámetro auditable, o la hoja se traslada a un repositorio con control de versiones y revisión de un segundo par antes de la aprobación. En ambos casos, el reporte de compra debe dejar constancia de qué cantidades se ajustaron y con qué fundamento. |

**La diferencia entre aprobar y no aprobar.**

| Así no | Así sí |
|---|---|
| «Decisión: gestionar el inventario.» | «Cuánto comprar de cada producto para el mes siguiente. La toma el Jefe de Compras, la primera semana de cada mes.» |
| «El riesgo es que la información no sea confiable.» | «Una compra de S/ 380 000 se decide sobre un archivo que una persona modifica sin dejar rastro y que se perdería si falla su equipo.» |
| «Se usa Excel.» | «Hoja de cálculo en el equipo del analista, sin control de versiones, sin respaldo y sin protección de fórmulas. Es la única copia.» |

## Reglas

- Al menos una decisión debe ser **operativa** (no solo financiera).
- **Prohibido listar sistemas.** Se listan **decisiones**, y los sistemas aparecen solo como soporte.
- La exposición es la ronda de cierre de esta misma sesión. El grupo **lee y explica su resultado**. No se usan diapositivas.

## Rúbrica cognitiva (20 puntos)

| Criterio | 5 | 3 | 1 |
|---|---|---|---|
| **Decisiones identificadas** | Decisiones reales de gerencia, específicas y con frecuencia declarada | Decisiones pertinentes pero genéricas | Lista de sistemas disfrazada de decisiones |
| **Trazado de la cadena** | Recorre los seis eslabones e identifica dueños del dato | Recorre la cadena parcialmente | Salta del sistema a la decisión |
| **Eslabón débil** | Riesgo específico con efecto sobre la calidad de la decisión | Riesgo pertinente sin efecto claro | Riesgo genérico de TI |
| **Hoja de cálculo** | Detecta el EUC y explica sus controles faltantes | Lo menciona sin analizar | Ausente |

## Anexo · Material de trabajo

**No se busca información fuera del aula.** Cada equipo trabaja con la organización que se le asignó del banco de casos, en `CASOS/EMPRESA-<NN>-<slug>/`. Las diez organizaciones tienen cifras, personas y documentos distintos, de modo que ningún equipo puede reutilizar el resultado de otro.

| Para qué | Archivo del caso | Qué contiene |
|---|---|---|
| Lo que la organización dice decidir | `documentos/plan-institucional-extracto.md` | Objetivos estratégicos, indicadores declarados y actas del órgano de gobierno, secciones 4 y 5 |
| Lo que la organización considera riesgo | `documentos/universo-auditable-y-riesgos.md` | Universo auditable y el registro de riesgos que la propia organización mantiene |
| Los procesos y sus responsables | `FICHA.md` | Procesos de negocio y sistemas que los soportan, secciones C y D |
| La confiabilidad de la fuente | `datos/presupuesto_ti.csv` · `datos/inversiones_cerradas.csv` | Para comprobar si las decisiones de inversión se sustentaron en datos medidos o en declaraciones |

---

---

[Semana 07](README.md) · [Teoría](1-TEORIA.md) · **Dinámica de aula** · [Taller de laboratorio](3-TALLER.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
