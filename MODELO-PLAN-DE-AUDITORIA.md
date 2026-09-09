[Auditoría de Sistemas](README.md) · **Modelo del Plan de Auditoría** · [Modelo del Informe de Auditoría](MODELO-INFORME-DE-AUDITORIA.md)

# Modelo del Plan Integral de Auditoría de Sistemas

**SI-084 · Auditoría de Sistemas** · Entregable de la **Unidad II**, semanas 07 a 12 · Versión que se aprueba en la Semana 12

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](GLOSARIO.md).

---

## Para qué sirve este documento

Es el índice de lo que su equipo entrega al cerrar la Unidad II. **Cada sección se construye en una semana concreta y no se escribe de golpe al final.** La columna «De dónde sale» dice en qué taller se produjo el contenido, de modo que llegar a la Semana 12 sin una sección significa que falta el trabajo de esa semana, no que falte redactarla.

El plan es el insumo del [Informe de Auditoría](MODELO-INFORME-DE-AUDITORIA.md) de la Unidad III. Lo que aquí se declara como alcance es exactamente sobre lo que allí se puede concluir, y lo que aquí se excluye no admite conclusión después.

**El archivo vive en** `10_planificacion/PLAN_INTEGRAL_AUDITORIA.md` del repositorio del equipo, y se etiqueta `unidad-2` al aprobarse.

## Las normas que lo sostienen

| Norma | Qué aporta al plan |
|---|---|
| **ISO 19011:2018** | La distinción entre programa de auditoría (cláusula 5) y auditoría individual (cláusula 6), los siete principios y la estructura del plan del encargo |
| **ITAF de ISACA** | El marco profesional del auditor de SI, la independencia y los requisitos de la evidencia |
| **COBIT 2019 · PAM** | Los niveles de capacidad con los que se califica cada proceso en el diagnóstico |
| **ISO/IEC 27001:2022 · Anexo A** | El catálogo de controles que se cita como criterio, con su código |
| **NTP-ISO/IEC 12207** | Los procesos del ciclo de vida del software, criterio de la sección 7.2 |
| **Ley 29733 y D. S. 016-2024-JUS · D. Leg. 822** | Las obligaciones cuyo cumplimiento se evalúa en la sección 5 |

## La estructura, sección por sección

| # | Sección | Qué debe contener | De dónde sale |
|---|---|---|---|
| **1** | Resumen ejecutivo | Qué se auditará, por qué, con qué recursos y qué se solicita aprobar. Máximo una página | Se escribe al final, en la S12 |
| **2** | La organización y su contexto | Modelo de negocio, régimen regulatorio, sistemas críticos y las cinco decisiones del negocio que dependen de TI | Semana 07 |
| **3** | Universo auditable y priorización | El universo, el modelo de factores de riesgo, los puntajes, el mapa de calor y **la cobertura que no se alcanza** | Semana 07 |
| **4** | Diagnóstico de la situación actual | Matriz de madurez por dominio, radar de niveles y brechas priorizadas por impacto y esfuerzo | Semana 10 |
| **5** | Marco legal aplicable y exposición | Régimen de la organización, matriz de cumplimiento, registro de tratamiento de datos y exposiciones principales | Semana 11 |
| **6** | Alcance del encargo | Objetivos, alcance incluido, **exclusiones explícitas**, criterios con su edición vigente y materialidad | Semana 08 |
| **7** | Programa de trabajo consolidado | Todos los procedimientos agrupados por dominio, cada uno trazable al riesgo que lo origina | Semanas 08 a 11 |
| 7.1 | · Controles generales de TI | Accesos, cambios, operaciones y continuidad | Semana 08 |
| 7.2 | · Ciclo de vida del software | Procesos de la NTP-ISO/IEC 12207 | Semana 09 |
| 7.3 | · Cumplimiento legal | Datos personales, licenciamiento y evidencia digital | Semana 11 |
| 7.4 | · Continuidad operativa | Preparatorio, se ejecuta en la Semana 15 | Semana 11 |
| **8** | Recursos, cronograma y responsabilidades | Horas por dominio, cronograma de la Unidad III y asignación por integrante | Semana 12 |
| **9** | Gestión de la calidad del encargo | Control de calidad, supervisión del jefe de equipo y criterios de aceptación de los papeles de trabajo | Semana 12 |
| **10** | Comunicación | Contraparte, canal único, frecuencia y protocolo de comunicación de hallazgos preliminares | Semana 08 |
| **11** | Supuestos, restricciones y riesgos del encargo | Qué podría impedir concluir y cómo se mitiga | Semana 12 |
| **12** | Aprobación | Elaborado · Revisado, por control de calidad del propio equipo · Aprobado, por el comité de la asignatura | Semana 12 |

## Los anexos obligatorios

| Anexo | Contenido | De dónde sale |
|---|---|---|
| **A** | Carta de encargo firmada, con sus doce cláusulas | Semana 08 |
| **B** | Declaración de independencia de cada integrante, con sus salvaguardas si las hay | Semana 08 |
| **C** | Matriz PBC con fecha comprometida, fecha real y días de retraso | Semana 08 |
| **D** | Acta de la reunión de apertura, firmada | Semana 08 |
| **E** | Papeles de trabajo del diagnóstico, con su índice | Semana 10 |

## Las cuatro comprobaciones que decide la nota

Un plan cuyas secciones son correctas por separado puede ser un plan defectuoso. Estas cuatro se verifican **entre** secciones.

| Comprobación | Qué debe ser consistente | Inconsistencia típica |
|---|---|---|
| **Riesgo → esfuerzo** | Las horas se concentran donde la sección 3 identificó mayor riesgo | El universo prioriza continuidad y el programa dedica el 80 % de las horas a accesos |
| **Madurez → procedimiento** | Un proceso en nivel 0 no admite prueba de eficacia operativa, porque no hay control que operar | Programar pruebas de eficacia sobre controles que la sección 4 calificó inexistentes |
| **Criterio → régimen** | Todo criterio citado es exigible a **esta** organización | Citar como obligatoria una norma del sector público en una sociedad anónima |
| **Alcance → conclusión** | No se concluye sobre lo que la sección 6 excluyó | Prometer opinión sobre continuidad cuando la carta la dejó fuera |

> **La regla de proporcionalidad.** Si el plan exige más horas de auditoría que las que la organización dedica a operar el proceso auditado, el plan está mal dimensionado y no se ejecutará.

---

---

[Auditoría de Sistemas](README.md) · **Modelo del Plan de Auditoría** · [Modelo del Informe de Auditoría](MODELO-INFORME-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
