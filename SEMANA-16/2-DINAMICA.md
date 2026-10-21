[Semana 16](README.md) · [Teoría](1-TEORIA.md) · **Dinámica de aula** · [Taller de laboratorio](3-TALLER.md)

# Semana 16

## La conclusión general

**SI-084 - Auditoría de Sistemas** - Actividad en aula, **dentro de la sesión de teoría** · calificación **cognitiva**

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](../GLOSARIO.md).

---

## Qué entregas

| | |
|---|---|
| **Archivo** | `SI084-S16-DINAMICA-Grupo<N>.pdf` |
| **Plantilla obligatoria** | [SI084-PLANTILLA-DINAMICA.docx](../PLANTILLAS/SI084-PLANTILLA-DINAMICA.docx) |
| **Formato** | PDF exportado desde la plantilla en Word, con la carátula de la UPT y los apellidos, nombres y códigos de todos los integrantes |
| **Qué va dentro** | Lo que el grupo resolvió en aula. Las tablas de la sección **Producto** van completas, con los textos redactados, y cada decisión va justificada |
| **Dónde se sube** | Aula virtual, tarea «Dinámica · Semana 16» |
| **Cuándo vence** | Según lo programado en el aula virtual. La tabla se resuelve en aula; el PDF se formatea y se sube después |
| **Exposición** | En la ronda de cierre de **esta misma sesión**. El grupo **lee y explica su resultado** ante el aula, con el documento a la vista. No se usan diapositivas |

> No se califica un trabajo entregado en `.docx`, sin carátula, sin los códigos de los integrantes o con las tablas del producto vacías.

---

## Consigna

> **«La conclusión general»**
> Cada equipo debe redactar la **conclusión general de su informe** (sección 1.2) y las **tres conclusiones específicas** (sección 5), sobre la base de todos los hallazgos acumulados en las semanas 13 a 15, y **clasificar cada deficiencia** como deficiencia de control, deficiencia significativa o debilidad material, con su justificación.

| | |
|---|---|
| **Su papel** | **Socio a cargo** que firma el informe y responde por él |
| **Misión** | Redactar la conclusión general y las tres específicas, clasificando cada deficiencia por su gravedad |
| **Restricción** | **La conclusión lleva veredicto explícito.** «Se observaron oportunidades de mejora» no es una conclusión de auditoría |

## Producto

**Producto 1 — La conclusión.** El texto completo de la conclusión general, en un solo párrafo, que debe contener — la base (procedimientos ejecutados), la referencia al alcance, el veredicto explícito y la calificación de las deficiencias.

**Producto 2 — Clasificación de deficiencias.**

| Hallazgo | Severidad asignada | Clasificación COSO (*Committee of Sponsoring Organizations of the Treadway Commission*) | Justificación de la clasificación | Destinatario |
|---|---|---|---|---|

> **Dónde va.** Este producto se presenta en la **sección 2 de la [plantilla de dinámica](../PLANTILLAS/SI084-PLANTILLA-DINAMICA.docx)**, «El producto». No se copia la consigna ni la teoría. Solo el resultado y lo que lo sostiene.

## Ejemplo resuelto

*El caso de este ejemplo es distinto del que le toca a tu grupo. Sirve para que veas el nivel de detalle que se espera, no para copiarlo.*

**Una conclusión general bien resuelta.** Corresponde a otra empresa auditada.

> Sobre la base de los procedimientos ejecutados entre el inicio y el cierre del trabajo de campo, que comprendieron la revisión de los controles generales de tecnología de los procesos de gestión de accesos, gestión de cambios y respaldo, sobre los sistemas de facturación y de planillas, y con las limitaciones de alcance declaradas en la sección 3 —no se evaluaron los sistemas de la sede de Arequipa ni los controles del proveedor de nube—, concluimos que **los controles generales de tecnología de la información de la Compañía no operaron de manera efectiva durante el período examinado**. Se identificaron seis deficiencias, de las cuales una constituye una **debilidad material**, referida a la ausencia de segregación entre el desarrollo y el despliegue a producción del sistema de facturación, y dos constituyen **deficiencias significativas**, referidas al control de accesos privilegiados y a la ausencia de pruebas de restauración. Las tres restantes son deficiencias de control que, individualmente y en conjunto, no alcanzan a ser significativas.

*Clasificación de deficiencias*

| Hallazgo | Severidad | Clasificación COSO | Justificación | Destinatario |
|---|---|---|---|---|
| Un mismo desarrollador escribe el código y lo despliega a producción en el sistema de facturación, sin aprobación de un tercero | Crítica | **Debilidad material** | Existe posibilidad razonable de que un error o una alteración en la facturación no se prevenga ni se detecte oportunamente. La facturación representa el 100 % de los ingresos y no hay control compensatorio de detección. | Directorio y comité de auditoría |
| Tres cuentas con privilegios administrativos compartidas por seis personas | Alta | **Deficiencia significativa** | Merece la atención de los responsables del gobierno, pero existe un control compensatorio parcial. La revisión trimestral de bitácoras por el jefe de TI, aunque sin evidencia formal en dos de los cuatro trimestres. | Comité de auditoría |
| No hay prueba de restauración documentada en los últimos once meses | Alta | **Deficiencia significativa** | La efectividad del respaldo no está demostrada, y de ella depende la recuperación de los dos sistemas críticos. | Comité de auditoría |
| El inventario de activos de información está desactualizado en 14 equipos | Media | Deficiencia de control | No afecta directamente la confiabilidad de la información financiera y existe registro alterno en el área de logística. | Gerencia de TI |

**La diferencia entre aprobar y no aprobar.**

| Así no | Así sí |
|---|---|
| «Se concluye que existen debilidades en los controles.» | «Los controles generales de tecnología no operaron de manera efectiva durante el período examinado.» |
| *(No se menciona el alcance.)* | «Con las limitaciones declaradas en la sección 3: no se evaluaron los sistemas de Arequipa ni los controles del proveedor de nube.» |
| «Hallazgo crítico: falta segregación de funciones.» | «Debilidad material: existe posibilidad razonable de que un error en la facturación no se prevenga ni se detecte. La facturación es el 100 % de los ingresos y no hay control compensatorio.» |

## Reglas

- La conclusión debe caber en **un párrafo** y contener un veredicto explícito — los controles operaron con efectividad, con efectividad parcial, o no operaron con efectividad.
- **Prohibido** concluir sobre lo que la carta de encargo excluyó.
- La clasificación de deficiencias debe justificarse por el **efecto potencial**, no por el esfuerzo de corrección.
- La exposición es la ronda de cierre de esta misma sesión. El grupo **lee y explica su resultado**. No se usan diapositivas.

## Rúbrica cognitiva (20 puntos)

| Criterio | 5 | 3 | 1 |
|---|---|---|---|
| **Veredicto explícito** | Conclusión inequívoca, con base y alcance referenciados | Conclusión clara sin referenciar el alcance | Conclusión ambigua o ausente |
| **Coherencia con los hallazgos** | La conclusión se deriva demostrablemente de los hallazgos acumulados | Coherente en general | Contradice la severidad de los hallazgos |
| **Respeto del alcance** | No concluye sobre nada excluido; menciona las limitaciones | Respeta el alcance sin mencionar limitaciones | Concluye sobre lo excluido |
| **Clasificación COSO** | Correcta y justificada por efecto potencial en todos los hallazgos | Correcta en la mayoría | Clasifica por esfuerzo de corrección |

---

---

[Semana 16](README.md) · [Teoría](1-TEORIA.md) · **Dinámica de aula** · [Taller de laboratorio](3-TALLER.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
