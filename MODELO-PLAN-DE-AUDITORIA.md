[Auditoría de Sistemas](README.md) · **Modelo del Plan de Auditoría** · [Los seis encargos de la Unidad II](ENCARGOS-UNIDAD-II/README.md) · [Modelo del Informe de Auditoría](MODELO-INFORME-DE-AUDITORIA.md)

# Modelo del Plan de Auditoría de Tecnologías de la Información

**SI-084 · Auditoría de Sistemas** · Estructura única de la **Unidad II** · Se completa entera en cada una de las semanas 07 a 12

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](GLOSARIO.md).

---

## Para qué sirve este documento

Es la estructura del plan de auditoría que su equipo entrega **seis veces**, una por semana, sobre **seis materias de control distintas** de su propia organización asignada. No es un índice que se llena por partes a lo largo de la unidad. **Cada semana sale del laboratorio un plan completo, firmado y aprobable.**

La estructura no cambia. Lo que cambia cada semana es la **materia de control**, el **marco que aporta los criterios** y la **evidencia que la organización entrega**. Eso está definido en [los seis encargos de la Unidad II](ENCARGOS-UNIDAD-II/README.md).

| Semana | Materia de control | Marco que aporta los criterios |
|---|---|---|
| **07** | Gobierno y gestión de las tecnologías de la información | COBIT 2019 |
| **08** | Sistema de gestión de seguridad de la información | NTP-ISO/IEC 27001:2022 e ISO 19011:2018 |
| **09** | Ciclo de vida del software | NTP-ISO/IEC 12207 y NTP-ISO/IEC 25010 |
| **10** | Gestión de servicios de tecnologías de la información | ITIL 4 e ISO/IEC 20000-1:2018 |
| **11** | Cumplimiento legal del entorno informático | Ley 29733, D. S. 016-2024-JUS, D. Leg. 822 y D. Leg. 1412 |
| **12** | Seguridad del canal digital y de las aplicaciones expuestas | OWASP ASVS 4.0.3, OWASP Top 10:2021 y NTP-ISO/IEC 27001:2022 |

**El plan de la Semana 12 es el que se ejecuta.** Los seis se califican con la misma rúbrica, pero el trabajo de campo de la Unidad III, las semanas 13 a 16, se hace sobre el plan de la Semana 12. Los otros cinco quedan en el expediente de planificación como el programa de auditoría del periodo.

**Cada plan vive en** `10_planificacion/PLAN-S<NN>-<materia>.md` del repositorio del equipo, y se etiqueta `taller-NN` al cerrar su semana.

## De dónde viene esta estructura

La numeración romana y las secciones administrativas provienen del **formato de plan de auditoría de tecnologías de la información** que se usa en el sector público peruano, con el que el egresado se va a encontrar en un órgano de control interno. Sobre ese esqueleto se insertan las secciones que el marco profesional exige y que el formato administrativo no trae.

| Norma | Qué aporta a la estructura |
|---|---|
| **ISO 19011:2018**, cláusula 5 | La distinción entre el programa de auditoría del periodo y la auditoría individual |
| **ISO 19011:2018**, cláusula 6.2 y 6.3 | El contenido del plan del encargo, los objetivos, el alcance y los criterios |
| **ISO 19011:2018**, cláusula 4 | Los siete principios, de los que salen la independencia y el enfoque basado en evidencia |
| **ITAF de ISACA**, norma 1201 y 1202 | La planificación basada en riesgo y el riesgo de auditoría |
| **ITAF de ISACA**, norma 1204 | La materialidad, en su dimensión cuantitativa y cualitativa |
| **ITAF de ISACA**, norma 1002 y 1003 | La independencia organizacional y profesional del auditor |
| **ITAF de ISACA**, norma 1207 | La irregularidad y la acción ilegal, y qué hace el plan si aparece |
| **COBIT 2019** | Los objetivos de gobierno y gestión que delimitan el universo auditable |

> **Las secciones VI y XI no están en el formato administrativo.** Son las que distinguen un plan de auditoría de un cronograma de visitas. Sin materialidad declarada no hay forma de saber qué desviación importa, y sin control de calidad del encargo nadie revisa al que revisa.

---

## La estructura, sección por sección

### Carátula y preliminares

| Elemento | Qué debe decir |
|---|---|
| Carátula institucional | La de la plantilla de la UPT, con los apellidos, nombres y códigos de todos los integrantes |
| Tipo de auditoría y entidad | «Auditoría de \<materia de control\> a \<razón social\>» |
| Ubicación geográfica | Distrito, provincia y departamento de la entidad auditada |
| Materia de control, en una línea | Concordante con el objetivo general, breve y específica |
| Lugar y fecha de aprobación | |
| Clasificación | **CONFIDENCIAL — USO ACADÉMICO**, en todas las páginas |
| Índice | Con número de página y actualizado, no escrito a mano |

### I. ORIGEN

Qué lo origina y con qué autoridad se ejecuta. **Tres párrafos como máximo.**

| Debe contener | Error frecuente |
|---|---|
| El acto que dispone la auditoría — acuerdo del comité, requerimiento de la gerencia o programa de auditoría del periodo | Empezar con una definición de libro de qué es la auditoría de tecnologías de la información |
| La naturaleza del servicio, con su alcance temporal | Dejar sin decir si es auditoría interna o externa |
| El marco profesional bajo el que se ejecuta, con su edición | Nombrar «las mejores prácticas» sin citar ninguna |
| El hecho concreto que la motiva, trazado al documento o al dato que lo evidencia | Afirmar que existe una «necesidad de asegurar» sin decir qué pasó |

### II. INFORMACIÓN DE LA ENTIDAD AUDITADA

Lo que el auditor tiene que saber de la organización **antes** de fijar el alcance.

| Campo | Fuente en el caso |
|---|---|
| Razón social, registro único de contribuyentes, sector y naturaleza jurídica | `FICHA.md` de la organización asignada |
| Tamaño — facturación o presupuesto institucional, personal estable y eventual | `FICHA.md` |
| **Régimen regulatorio**, con la entidad que supervisa y la norma que la faculta | `FICHA.md` y el documento del encargo |
| Procesos de negocio críticos | `FICHA.md` |
| Sistemas de información en producción, con función, proveedor y criticidad | `FICHA.md` |
| Estructura del área de tecnologías de la información, con dependencia jerárquica | `organigrama-y-accesos.md` |
| Presupuesto de tecnologías de la información, planificado y ejecutado | `datos/presupuesto_ti.csv` |
| Incidentes del periodo | `incidente-detallado.md` |
| Auditorías previas y hallazgos abiertos | El documento del encargo de la semana |
| **Las decisiones de negocio que dependen del proceso auditado** | Trabajo del equipo |

> **El régimen regulatorio decide la mitad del plan.** La misma materia de control auditada en una cooperativa supervisada por la Superintendencia de Banca, Seguros y Administradoras Privadas de Fondos de Pensiones y en una distribuidora privada produce criterios distintos, plazos distintos y un documento a emitir distinto.

### III. DENOMINACIÓN DE LA MATERIA DE CONTROL

Qué se audita, en una frase, y **por qué esta y no otra**.

| Debe contener |
|---|
| La denominación exacta de la materia de control, idéntica en la carátula, en el índice y aquí |
| El proceso, sistema o actividad que la compone, delimitado |
| El riesgo que justifica auditarla, con el dato o documento que lo evidencia |
| Su lugar en el programa de auditoría del periodo, con el puntaje de riesgo que la priorizó |

**Ejemplo aceptable.** *«Gestión de los derechos de acceso al sistema principal de la organización, en el periodo comprendido entre el 1 de enero y el 31 de diciembre. Se prioriza porque el incidente del periodo se produjo por una cuenta de personal cesado que permaneció habilitada, y porque la matriz de accesos declara nueve perfiles mientras el sistema registra catorce.»*

**Ejemplo inaceptable.** *«Gestión de seguridad de la información.»* No es una materia de control, es un título de curso.

### IV. ALCANCE

La sección que determina sobre qué se puede concluir. Tiene **cuatro bloques obligatorios**.

| Bloque | Qué va |
|---|---|
| **Incluye** | Sistemas, procesos, ubicaciones y población, cada uno con su tamaño declarado |
| **Periodo auditado** | Fecha de inicio y de fin, con la justificación de por qué ese periodo |
| **Excluye expresamente** | Lo que **no** se audita y la razón de cada exclusión |
| **Limitaciones inherentes** | La auditoría da seguridad razonable, no absoluta. El riesgo de muestreo. Lo que no se pudo verificar y por qué |

> **Lo que no se excluye por escrito se da por incluido.** Si el alcance no dice que la continuidad operativa queda fuera, el lector del informe esperará una conclusión sobre continuidad operativa. Las exclusiones protegen al auditor y al auditado por igual.

### V. OBJETIVOS

Un objetivo general y entre tres y cinco específicos. **Cada objetivo específico se redacta como una pregunta de auditoría que admite respuesta, y lleva su propia conclusión en el informe.**

| Elemento | Regla |
|---|---|
| Objetivo general | Empieza con un verbo de determinación — determinar, evaluar, verificar. No con «analizar» ni «conocer» |
| Objetivo específico | Uno por cada dominio del marco que entra en el alcance |
| Pregunta de auditoría | La pregunta exacta que el objetivo responde, escrita en interrogativo |
| Trazabilidad | Cada específico tiene al menos dos procedimientos de la sección VII asociados |

**Ejemplo.** *«Objetivo específico 2. Determinar si los derechos de acceso al sistema principal se otorgan, modifican y revocan conforme al control A.5.18 de la NTP-ISO/IEC 27001:2022. Pregunta de auditoría — ¿existe para cada cuenta habilitada una autorización vigente, y se revocó el acceso de todo el personal cesado en el plazo que la política establece?»*

### VI. ENFOQUE, MATERIALIDAD Y RIESGO DE AUDITORÍA

Esta sección no está en el formato administrativo y es la que hace auditable el plan.

**VI.1 Enfoque.** Se elige uno de los dos y se justifica.

| Enfoque | Cuándo se elige | Qué implica |
|---|---|---|
| Confianza en controles | El control existe, está documentado y opera | Se prueba el diseño y la eficacia operativa, y se reduce la prueba sustantiva |
| Sustantivo | El control no existe, o existe y no es confiable | Se prueba directamente el dato o la condición, sin apoyarse en el control |

> **Un proceso sin control no admite prueba de eficacia operativa.** No hay nada que opere. Programar una prueba de eficacia sobre un control inexistente es el error de planificación más común, y se detecta solo.

**VI.2 Materialidad.** En sus dos dimensiones, ambas justificadas.

| Dimensión | Cómo se fija |
|---|---|
| Cuantitativa | Un monto o un porcentaje, derivado de una base declarada — facturación, presupuesto de tecnologías de la información, población de transacciones |
| Cualitativa | Las condiciones que son materiales con independencia del monto. Pérdida de trazabilidad, incumplimiento legal, exposición de datos personales, fraude |

**VI.3 Riesgo de auditoría.** Los tres componentes, con el nivel asignado y su sustento.

| Componente | Qué es | De dónde sale el nivel |
|---|---|---|
| Riesgo inherente | La exposición propia del proceso, antes de considerar el control | Naturaleza del proceso, volumen, regulación y antecedentes |
| Riesgo de control | Que el control no prevenga ni detecte a tiempo | Diagnóstico de la madurez del proceso |
| Riesgo de detección | Que el procedimiento del auditor no encuentre lo que existe | Se gestiona con el tamaño y el método de la muestra |

### VII. PROCEDIMIENTOS DE AUDITORÍA

El programa de trabajo. **Mínimo doce procedimientos**, cada uno con las trece columnas completas.

| Columna | Regla de calidad |
|---|---|
| `id` | P-01, P-02, … |
| `objetivo_especifico` | A qué objetivo de la sección V responde |
| `riesgo` | Qué ocurre si el control falla |
| `criterio` | La norma **con su código** — `NTP-ISO/IEC 27001:2022 A.5.18`, `COBIT 2019 DSS05.04`, `Ley 29733 art. 9` |
| `tipo_prueba` | Indagación · Observación · Inspección documental · Inspección del sistema · Reejecución · Técnica de auditoría asistida por computador |
| `poblacion` | El universo, con su tamaño numérico |
| `muestra` | El tamaño **y el método** de selección |
| `justificacion_muestra` | Derivada de la frecuencia del control y del riesgo asignado |
| `procedimiento` | Los pasos en imperativo, ejecutables por un tercero que no participó en la planificación |
| `evidencia_a_obtener` | El artefacto concreto que queda en el papel de trabajo |
| `definicion_excepcion` | Qué cuenta como desviación, fijado **antes** de ver los datos |
| `horas_estimadas` | |
| `ejecutado_por` · `revisado_por` · `fecha` | Vacías al planificar. Se llenan en la Unidad III |

**Distribución mínima de tipos de prueba.**

| Tipo de prueba | Mínimo | Por qué |
|---|---|---|
| Reejecución | 2 | Es la evidencia más fuerte. El auditor reproduce el control |
| Técnica asistida por computador sobre el 100 % | 2 | Elimina el riesgo de muestreo en la población completa |
| Inspección del sistema | 3 | La configuración vigente, no lo que la política dice |
| Inspección documental | 3 | La autorización, el contrato, el acta |
| Observación | 1 | Lo que ocurre, no lo que se declara |
| Indagación | Máximo 2 | **Nunca como sustento único de una conclusión** |

### VIII. CRITERIOS DE AUDITORÍA

La norma contra la que se compara lo observado. **Un criterio sin código no es un criterio.**

| Debe contener | Error frecuente |
|---|---|
| La norma, con edición vigente y el código del control o el artículo | «Las mejores prácticas de la industria» |
| La política o el procedimiento interno, con nombre, versión y fecha de aprobación | Citar una política interna que la organización no ha aprobado |
| La norma legal exigible **a esta** organización, con su artículo | Citar como obligatoria una norma del sector público en una sociedad anónima |
| La cláusula contractual, cuando el criterio nace de un contrato | Olvidar que el acuerdo de nivel de servicio firmado es criterio exigible |

> **La prueba de exigibilidad.** Antes de citar un criterio, responda quién puede sancionar su incumplimiento. Si la respuesta es «nadie», es una buena práctica recomendable, no un criterio de auditoría, y así debe declararse.

### IX. PLAZO DE LA AUDITORÍA Y CRONOGRAMA

| Etapa | Qué incluye | Entregable que la cierra |
|---|---|---|
| Planificación | Comprensión, alcance, programa y apertura | Este plan, aprobado |
| Ejecución | Trabajo de campo y papeles de trabajo | Papeles de trabajo referenciados y revisados |
| Comunicación de resultados | Hallazgos preliminares y reunión de cierre | Acta con la respuesta de la administración |
| Elaboración del informe | Redacción, revisión de calidad y emisión | Informe de auditoría |

Cada etapa lleva fecha de inicio, fecha de fin y las horas que consume. **La suma de horas de esta sección tiene que coincidir con la suma de la columna `horas_estimadas` de la sección VII**, más las horas de supervisión y de informe.

### X. INFORMACIÓN ADMINISTRATIVA

**X.1 Comisión auditora.**

| Cargo | Nombres y apellidos | Profesión o especialidad | Planificación | Ejecución | Informe | Total |
|---|---|---|---|---|---|---|
| Supervisor | | | | | | |
| Jefe de comisión | | | | | | |
| Integrante | | | | | | |
| Experto, cuando corresponda | | | | | | |

**X.2 Independencia y objetividad.** Una declaración por integrante, con las cinco preguntas y la salvaguarda aplicada cuando alguna se responde afirmativamente. El formato está en el **Anexo F**.

**X.3 Costos directos estimados.** Horas-hombre por nivel, asignaciones, pasajes y viáticos, con el total. **Si el plan exige más horas de auditoría que las que la organización dedica a operar el proceso auditado, el plan está mal dimensionado y no se ejecutará.**

### XI. COMUNICACIÓN Y CONTROL DE CALIDAD DEL ENCARGO

**XI.1 Comunicación.**

| Elemento | Qué se define |
|---|---|
| Contraparte designada | Nombre, cargo y acto que la designa |
| Canal único | Por dónde entra y sale toda la información del encargo |
| Plazo de respuesta a la solicitud de información | En días hábiles, con el mecanismo de escalamiento si se incumple |
| Regla de comunicación de hallazgos preliminares | Cuándo se comunican y cuánto tiempo tiene la administración para responder |
| Confidencialidad y custodia | Dónde se guarda la evidencia, cifrada, y qué se hace con ella al cierre |

**XI.2 Control de calidad.**

| Elemento | Qué se define |
|---|---|
| Supervisión | Quién revisa cada papel de trabajo y con qué criterio lo acepta |
| Revisión independiente | Quién, dentro del equipo, revisa el trabajo que no hizo |
| Criterios de aceptación del papel de trabajo | Identificación, fuente, procedimiento aplicado, resultado y conclusión |
| Tratamiento de la irregularidad | Qué se hace si durante el trabajo aparece un indicio de acto ilegal |

### XII. DOCUMENTO A EMITIR

Qué se emite al terminar, con qué estructura y a quién se dirige. El contenido está en el [modelo del informe de auditoría](MODELO-INFORME-DE-AUDITORIA.md), que es el entregable de la Unidad III.

### Suscripción

Lugar, fecha, y la firma de quien elabora, quien revisa y quien aprueba. **Las tres son personas distintas.**

---

## Los anexos obligatorios

| Anexo | Contenido | Qué demuestra |
|---|---|---|
| **A** | Matriz de riesgos de la materia de control, con riesgo, causa, impacto, nivel, control existente y control esperado | Que el programa de la sección VII nace de un riesgo y no de una lista de deseos |
| **B** | Matriz de trazabilidad — objetivo específico, procedimiento, criterio, evidencia requerida, fuente y responsable | Que ningún objetivo quedó sin procedimiento y ningún procedimiento sin objetivo |
| **C** | Matriz de solicitud de información, con responsable, fecha solicitada, fecha comprometida y estado | Que el retraso en la entrega de información queda documentado, no comentado |
| **D** | Instrumentos de recolección — lista de verificación, guion de entrevista y plantilla del papel de trabajo | Que el procedimiento se puede ejecutar tal como está escrito |
| **E** | Cronograma detallado por actividad, con responsable y producto intermedio | Que las horas de la sección IX están repartidas entre personas y fechas |
| **F** | Declaración de independencia de cada integrante, con sus salvaguardas | Que la objetividad se declaró antes de empezar, no después |

---

## Las cinco comprobaciones que deciden la nota

Un plan cuyas secciones son correctas por separado puede ser un plan defectuoso. Estas cinco se verifican **entre** secciones, y son las que la rúbrica procedimental mira primero.

| Comprobación | Qué debe ser consistente | Inconsistencia típica |
|---|---|---|
| **Objetivo → procedimiento** | Todo objetivo específico de la sección V tiene procedimientos en la VII, y todo procedimiento responde a un objetivo | Un objetivo sobre continuidad operativa sin un solo procedimiento que la pruebe |
| **Criterio → régimen** | Todo criterio de la sección VIII es exigible a **esta** organización | Citar la Resolución SBS N.º 504-2021 en una agroexportadora |
| **Enfoque → madurez** | No se prueba eficacia operativa de un control que el diagnóstico calificó inexistente | Programar reejecución sobre un control que nadie opera |
| **Alcance → conclusión** | No se concluye sobre lo que la sección IV excluyó | Prometer opinión sobre el canal digital cuando el alcance lo dejó fuera |
| **Horas → riesgo** | Las horas de la sección IX se concentran donde la sección VI asignó mayor riesgo | Dedicar el 70 % de las horas al dominio de menor riesgo inherente |

> **La comprobación que más planes reprueba es la primera.** Un plan con doce procedimientos impecables y un objetivo huérfano es un plan que va a emitir una conclusión sin sustento, y eso en un informe real es una afirmación sin evidencia.

---

---

[Auditoría de Sistemas](README.md) · **Modelo del Plan de Auditoría** · [Los seis encargos de la Unidad II](ENCARGOS-UNIDAD-II/README.md) · [Modelo del Informe de Auditoría](MODELO-INFORME-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
