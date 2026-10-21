[Semana 14](README.md) · [Teoría](1-TEORIA.md) · **Dinámica de aula** · [Taller de laboratorio](3-TALLER.md)

# Semana 14

## La cascada rota

**SI-084 - Auditoría de Sistemas** - Actividad en aula, **dentro de la sesión de teoría** · calificación **cognitiva**

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](../GLOSARIO.md).

---

## Qué entregas

| | |
|---|---|
| **Archivo** | `SI084-S14-DINAMICA-Grupo<N>.pdf` |
| **Plantilla obligatoria** | [SI084-PLANTILLA-DINAMICA.docx](../PLANTILLAS/SI084-PLANTILLA-DINAMICA.docx) |
| **Formato** | PDF exportado desde la plantilla en Word, con la carátula de la UPT y los apellidos, nombres y códigos de todos los integrantes |
| **Qué va dentro** | Lo que el grupo resolvió en aula. Las tablas de la sección **Producto** van completas, con los textos redactados, y cada decisión va justificada |
| **Dónde se sube** | Aula virtual, tarea «Dinámica · Semana 14» |
| **Cuándo vence** | Según lo programado en el aula virtual. La tabla se resuelve en aula; el PDF se formatea y se sube después |
| **Exposición** | En la ronda de cierre de **esta misma sesión**. El grupo **lee y explica su resultado** ante el aula, con el documento a la vista. No se usan diapositivas |

> No se califica un trabajo entregado en `.docx`, sin carátula, sin los códigos de los integrantes o con las tablas del producto vacías.

---

## Consigna

> **«La cascada rota»**
> Cada equipo toma **un objetivo estratégico real de su empresa auditada** (del plan estratégico institucional, del plan operativo o declarado en la entrevista con gerencia) y **rastrea la cascada completa** hasta los componentes de TI que deberían soportarlo, **identificando dónde se rompe la cadena**.

| | |
|---|---|
| **Su papel** | **Auditor de gobierno** que expone ante el directorio, no ante el área de TI |
| **Misión** | Rastrear la cascada del objetivo estratégico hasta TI y localizar el eslabón donde se rompe |
| **Restricción** | **La primera respuesta «no» cierra la cascada.** No se sigue bajando a buscar un nivel donde la respuesta sea mejor |

## Producto

**Producto 1 — La cascada.** Diagrama con los cinco niveles, completando cada uno con contenido real de la empresa y marcando en rojo el eslabón roto:

```
Objetivo estratégico del negocio: «..............................»
        ▼
Meta empresarial (COBIT): «..............................»
        ▼
Meta de alineamiento: «..............................»
        ▼
Objetivos COBIT que la soportan: ......, ......, ......
        ▼
¿Están en el plan de TI?  ¿Tienen presupuesto?  ¿Tienen responsable?
```

**Producto 2 — El hallazgo de desalineamiento y su indicador.** El hallazgo redactado en CCCER más **un indicador del BSC de TI** que, de haber existido, habría hecho visible la desconexión — nombre, fórmula, fuente, frecuencia, meta y responsable.

> **Dónde va.** Este producto se presenta en la **sección 2 de la [plantilla de dinámica](../PLANTILLAS/SI084-PLANTILLA-DINAMICA.docx)**, «El producto». No se copia la consigna ni la teoría. Solo el resultado y lo que lo sostiene.

## Ejemplo resuelto

*El caso de este ejemplo es distinto del que le toca a tu grupo. Sirve para que veas el nivel de detalle que se espera, no para copiarlo.*

**Una cascada bien resuelta.** El objetivo del ejemplo es de una empresa agroexportadora.

```
Objetivo estratégico del negocio
«Reducir el tiempo de certificación de lotes de exportación de 9 a 4 días»
        ▼
Meta empresarial (COBIT 2019)
EG08 «Optimización de la funcionalidad interna de los procesos de negocio»
        ▼
Meta de alineamiento
AG06 «Agilidad para convertir los requerimientos de negocio en soluciones operativas»
        ▼
Objetivos COBIT que la soportan
APO11 Gestión de la calidad · BAI03 Gestión de la identificación y construcción de soluciones · DSS01 Gestión de operaciones
        ▼
¿Están en el plan de TI?   BAI03 sí · APO11 no · DSS01 no
¿Tienen presupuesto?       BAI03 parcial, sin partida propia
¿Tienen responsable?       NINGUNO   ← aquí se rompe la cadena
```

*El hallazgo de desalineamiento*

| Elemento | Contenido |
|---|---|
| **Condición** | El objetivo de reducir el tiempo de certificación de 9 a 4 días figura en el plan estratégico institucional aprobado. Ninguno de los tres objetivos COBIT que lo soportan tiene responsable designado ni partida presupuestal propia en el plan de TI del período. El único proyecto relacionado, la digitalización del registro de lotes, está sin fecha de inicio desde hace once meses. |
| **Criterio** | COBIT 2019, **EDM01 Ensured governance framework setting and maintenance** y **APO02 Managed strategy**, que exigen que los objetivos de TI deriven de las metas empresariales y tengan responsable y recursos asignados. |
| **Causa** | El plan de TI se elabora en el área de sistemas a partir de los requerimientos que llegan por tickets, no a partir del plan estratégico institucional. No existe una instancia donde ambos planes se contrasten. |
| **Efecto** | La organización comprometió ante el directorio una reducción del 55 % en el tiempo de certificación sin haber asignado a TI ningún recurso para lograrla. El objetivo no se alcanzará y la desviación se detectará al cierre del período, cuando ya no haya margen de corrección. |
| **Recomendación** | Incorporar al comité de TI la revisión anual de la trazabilidad entre los objetivos del plan estratégico institucional y los objetivos de TI, con acta. Asignar responsable y partida a los tres objetivos COBIT identificados. **Responsable:** Gerente General, como presidente del comité. **Plazo:** próxima sesión del comité. **Criterio de cierre:** acta con la matriz de trazabilidad aprobada. |

*El indicador del cuadro de mando de TI que lo habría hecho visible*

| Campo | Contenido |
|---|---|
| Nombre | Cobertura de objetivos estratégicos con soporte de TI asignado |
| Perspectiva | Contribución al negocio |
| Fórmula | (Objetivos del plan estratégico con al menos un objetivo de TI que tenga responsable y presupuesto ÷ Total de objetivos del plan estratégico) × 100 |
| Fuente | Matriz de trazabilidad del comité de TI |
| Frecuencia | Trimestral |
| Meta | 100 % de los objetivos que dependen de tecnología |
| Responsable | Gerente de Tecnologías de Información |

**La diferencia entre aprobar y no aprobar.**

| Así no | Así sí |
|---|---|
| «El objetivo estratégico es mejorar la eficiencia.» | «Reducir el tiempo de certificación de lotes de 9 a 4 días», citado del plan estratégico institucional con su página. |
| «No hay alineamiento entre TI y el negocio.» | «Ninguno de los tres objetivos COBIT que lo soportan tiene responsable ni partida. El proyecto relacionado lleva once meses sin fecha de inicio.» |
| «Indicador: nivel de alineamiento.» | «(Objetivos con soporte de TI asignado ÷ total) × 100, trimestral, meta 100 %, fuente: matriz de trazabilidad del comité.» |

## Reglas

- El objetivo estratégico debe ser **real y citable** (documento y página, o entrevista con fecha y cargo).
- El indicador propuesto debe pertenecer a la perspectiva de **contribución al negocio**, no a excelencia operativa.
- El criterio del hallazgo debe citar **COBIT 2019 e ISO/IEC 38500:2024** por su edición vigente.
- La exposición es la ronda de cierre de esta misma sesión. El grupo **lee y explica su resultado**. No se usan diapositivas.

## Rúbrica cognitiva (20 puntos)

| Criterio | 5 | 3 | 1 |
|---|---|---|---|
| **Cascada completa** | Los cinco niveles con contenido real y trazable | Tres o cuatro niveles | Salta del objetivo al sistema |
| **Identificación de la ruptura** | Localiza el eslabón exacto y explica su consecuencia | Identifica que hay desalineamiento sin precisar dónde | No detecta la ruptura |
| **Calidad del indicador** | Fórmula, fuente, frecuencia, meta y responsable; mide contribución al negocio | Indicador completo pero de excelencia operativa | Indicador sin fórmula o sin meta |
| **Criterio normativo** | Cita COBIT 2019 y la edición **2024** de la ISO/IEC 38500 | Cita una fuente correcta | Cita la edición 2015 o no cita |

---

---

[Semana 14](README.md) · [Teoría](1-TEORIA.md) · **Dinámica de aula** · [Taller de laboratorio](3-TALLER.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
