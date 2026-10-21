[Semana 10](README.md) · [Teoría](1-TEORIA.md) · **Dinámica de aula** · [Taller de laboratorio](3-TALLER.md)

# Semana 10

## Reformular el cuestionario

**SI-084 - Auditoría de Sistemas** - Actividad en aula, **dentro de la sesión de teoría** · calificación **cognitiva**

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](../GLOSARIO.md).

---

## Qué entregas

| | |
|---|---|
| **Archivo** | `SI084-S10-DINAMICA-Grupo<N>.pdf` |
| **Plantilla obligatoria** | [SI084-PLANTILLA-DINAMICA.docx](../PLANTILLAS/SI084-PLANTILLA-DINAMICA.docx) |
| **Formato** | PDF exportado desde la plantilla en Word, con la carátula de la UPT y los apellidos, nombres y códigos de todos los integrantes |
| **Qué va dentro** | Lo que el grupo resolvió en aula. Las tablas de la sección **Producto** van completas, con los textos redactados, y cada decisión va justificada |
| **Dónde se sube** | Aula virtual, tarea «Dinámica · Semana 10» |
| **Cuándo vence** | Según lo programado en el aula virtual. La tabla se resuelve en aula; el PDF se formatea y se sube después |
| **Exposición** | En la ronda de cierre de **esta misma sesión**. El grupo **lee y explica su resultado** ante el aula, con el documento a la vista. No se usan diapositivas |

> No se califica un trabajo entregado en `.docx`, sin carátula, sin los códigos de los integrantes o con las tablas del producto vacías.

---

## Consigna

> **«Reformular el cuestionario»**
> Cada equipo recibe un **cuestionario de diagnóstico de TI defectuoso de 12 preguntas**, con los errores típicos de la sección 1.4. Debe **reformular las 12 preguntas** para que cada una obtenga un hecho verificable con su evidencia, y **definir la regla de decisión** que convierte la respuesta en un nivel de capacidad.

| | |
|---|---|
| **Su papel** | **Auditor que hereda un instrumento** aplicado por el propio auditado |
| **Misión** | Reformular las doce preguntas y fijar la regla que convierte la respuesta en un nivel |
| **Restricción** | **Si el auditado puede contestar «sí» sin mostrar nada, la pregunta sigue mal.** Y alguna pregunta no se corrige: se reasigna |

Que el equipo convierta un cuestionario que recoge opiniones en un instrumento que recoge **hechos con evidencia**. Es la diferencia entre un diagnóstico que el auditado firma sin leer y uno que le obliga a mostrar documentos.

## Lo que la teoría de hoy te da

Esta dinámica aplica piezas concretas de la sesión de teoría de hoy. Se usan tal cual, sin buscar nada más.

| De la teoría | Para qué se usa aquí |
|---|---|
| [Diseño de los instrumentos de diagnóstico](1-TEORIA.md) | Enumera los defectos típicos. Pregunta cerrada que admite «sí» sin prueba, pregunta doble, pregunta que sugiere la respuesta y pregunta sin evidencia asociada |
| [El diagnóstico de la situación actual](1-TEORIA.md) | Fija que el diagnóstico se cierra con un nivel de capacidad, y que ese nivel debe derivarse de una regla escrita antes de preguntar |
| [Metodologías de evaluación de sistemas informáticos](1-TEORIA.md) | Da la escala de niveles con la que se construye la regla de decisión del segundo producto |

## Producto

**Producto 1 — Reformulación.** Tabla con las 12 preguntas:

| # | Pregunta original | Defecto que tiene | Pregunta reformulada | Evidencia que se solicita |
|---|---|---|---|---|

**Producto 2 — Regla de decisión.** Para **tres** de las preguntas reformuladas, la escala completa:

| Pregunta | Nivel 0 | Nivel 1 | Nivel 2 | Nivel 3 | Nivel 4 |
|---|---|---|---|---|---|

Cada celda dice **qué respuesta corresponde a ese nivel y qué evidencia la sostiene**.

> **Dónde va.** Este producto se presenta en la **sección 2 de la [plantilla de dinámica](../PLANTILLAS/SI084-PLANTILLA-DINAMICA.docx)**, «El producto». No se copia la consigna ni la teoría. Solo el resultado y lo que lo sostiene.

## Ejemplo resuelto

*El caso de este ejemplo es distinto del que le toca a tu grupo. Sirve para que veas el nivel de detalle que se espera, no para copiarlo.*

**Tres preguntas bien reformuladas.** Son preguntas distintas de las doce que te tocan.

*Reformulación*

| # | Pregunta original | Defecto que tiene | Pregunta reformulada | Evidencia que se solicita |
|---|---|---|---|---|
| A | ¿La documentación de los sistemas está actualizada? | Binaria y sesgada al sí, con un adjetivo sin definición. «Actualizada» no dice respecto de qué. | ¿Qué sistemas cuentan con manual técnico y con manual de usuario, cuál es la fecha de la última versión de cada uno y cuál fue el último cambio funcional que se documentó en ellos? | Relación de manuales con su fecha de versión, contrastada con el registro de cambios del período |
| B | ¿Se monitorea el desempeño de los servidores? | No pide evidencia. Aunque la respuesta sea cierta, no queda nada verificable. | ¿Qué herramienta registra el uso de procesador, memoria y disco de cada servidor, con qué retención, qué umbral de alerta está configurado y a quién notifica? | Captura de la configuración de umbrales, relación de destinatarios y muestra del historial del último mes |
| C | ¿Los proveedores cumplen con los tiempos acordados? | Pregunta compuesta y sin dato. Mezcla si existe acuerdo con si se cumple, y la respuesta no distingue cuál. | ¿Qué contratos de servicio de TI fijan un tiempo de respuesta comprometido, cuál es ese tiempo en cada uno y cuántos incidentes del último semestre lo excedieron? | Contratos con la cláusula de nivel de servicio y registro de incidentes con sus marcas de tiempo |

*Regla de decisión de la pregunta B, sobre el monitoreo*

| Nivel | Respuesta y evidencia que corresponden |
|---|---|
| 0 · Incompleto | No se monitorea, o se mira la consola solo cuando algo falla |
| 1 · Ejecutado | Hay una herramienta que registra métricas y se puede mostrar el historial, pero sin umbrales ni destinatarios definidos |
| 2 · Gestionado | Umbrales configurados, destinatario asignado y evidencia de que las alertas llegan, con retención definida del historial |
| 3 · Establecido | Lo anterior aplicado a todos los servidores críticos bajo un estándar único, con procedimiento escrito de atención de la alerta |
| 4 · Predecible | Lo anterior más un indicador de disponibilidad medido contra una meta, con revisión periódica por la dirección |

**La regla que decide la nota.** Ante duda entre dos niveles se asigna el **menor** y se documenta la razón. La declaración del auditado, sin evidencia que la respalde, sostiene como máximo el nivel 1.

**La diferencia entre aprobar y no aprobar.**

| Así no | Así sí |
|---|---|
| «¿Monitorean adecuadamente sus servidores?» | «¿Qué umbral de alerta está configurado y a quién notifica?» |
| «Defecto: es una pregunta cerrada.» | «Defecto: no pide evidencia. Aunque la respuesta sea cierta, no queda nada verificable.» |
| «Evidencia: la herramienta de monitoreo.» | «Captura de la configuración de umbrales, relación de destinatarios y muestra del historial del último mes.» |

## Reglas

- Ninguna pregunta reformulada puede responderse con «sí» o «no».
- Cada pregunta debe pedir **evidencia adjunta**.
- La regla de decisión debe escribirse **antes** de aplicar el cuestionario, y así debe declararse.
- La exposición es la ronda de cierre de esta misma sesión. El grupo **lee y explica su resultado**. No se usan diapositivas.

## Rúbrica cognitiva (20 puntos)

| Criterio | 5 | 3 | 1 |
|---|---|---|---|
| **Diagnóstico del defecto** | Identifica correctamente el defecto en las 12 | En 8 o más | Confunde el defecto |
| **Calidad de la reformulación** | Todas piden hechos verificables con evidencia adjunta | La mayoría | Siguen siendo binarias o de opinión |
| **Regla de decisión** | Escalas completas, con criterios objetivos y no solapados | Escalas completas con alguna ambigüedad | Escalas descriptivas sin criterio |
| **Coherencia con COBIT PAM** | La progresión de niveles respeta la lógica de capacidad acumulativa | Progresión razonable | Niveles asignados arbitrariamente |

## Anexo · Material de trabajo

**No se busca información fuera del aula.** Cada equipo trabaja con la organización que se le asignó del banco de casos, en `CASOS/EMPRESA-<NN>-<slug>/`. Las diez organizaciones tienen cifras, personas y documentos distintos, de modo que ningún equipo puede reutilizar el resultado de otro.

**El cuestionario defectuoso es el que la propia organización aplicó**, con sus doce preguntas y las respuestas que obtuvo.

| Para qué | Archivo del caso | Qué contiene |
|---|---|---|
| El instrumento a reformular | `documentos/cuestionario-diagnostico.md` | Ficha del instrumento, las doce preguntas tal como se aplicaron y las respuestas que la organización dio |
| Contra qué se contrasta la respuesta | `FICHA.md` · `documentos/organigrama-y-accesos.md` | Lo que la organización declara sobre su comité, su política y su personal de TI, para detectar qué respuesta no se sostiene |
| Evidencia disponible para exigir | `datos/usuarios_erp.csv` · `datos/presupuesto_ti.csv` | Sirve para saber qué evidencia es realmente solicitable y cuál no existe en esta organización |

---

---

[Semana 10](README.md) · [Teoría](1-TEORIA.md) · **Dinámica de aula** · [Taller de laboratorio](3-TALLER.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
