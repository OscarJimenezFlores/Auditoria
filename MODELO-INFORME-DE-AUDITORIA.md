[Auditoría de Sistemas](README.md) · [Modelo del Plan de Auditoría](MODELO-PLAN-DE-AUDITORIA.md) · **Modelo del Informe de Auditoría**

# Modelo del Informe Final de Auditoría de Sistemas

**SI-084 · Auditoría de Sistemas** · Entregable de la **Unidad III**, semanas 13 a 17 · Es el producto acreditable del curso

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](GLOSARIO.md).

---

## Para qué sirve este documento

Es el índice del informe que su equipo sustenta en la Semana 17. **No se escribe desde cero.** Cada sección se alimenta de una pieza del [Plan Integral de Auditoría](MODELO-PLAN-DE-AUDITORIA.md) aprobado en la Unidad II, ejecutada durante las semanas 13 a 16.

La regla que ordena todo el documento es una sola. **No se concluye sobre lo que el plan excluyó**, y no se afirma nada que no pueda señalarse en un papel de trabajo.

**Los archivos viven en** `50_informe/` del repositorio del equipo, una sección por archivo, y se etiquetan `cierre-encargo` al entregarse.

## Las normas que lo sostienen

| Norma | Qué aporta al informe |
|---|---|
| **ISO 19011:2018** | El contenido del informe de auditoría, la comunicación de hallazgos y el cierre del encargo |
| **ITAF de ISACA** | La suficiencia de la evidencia y la forma de la opinión del auditor |
| **COSO 2013** | El marco de control interno sobre el que se concluye en la sección 5.1 |
| **ISO/IEC 38500:2024** | Los principios de gobierno de TI que se evalúan en la sección 3.3 |
| **ISO 22301:2019** | El criterio de continuidad de la sección 5.3 |
| **Ley 29733 y D. S. 016-2024-JUS** | El criterio de cumplimiento legal de la sección 5.2 |

## La estructura, sección por sección

| # | Sección | Qué debe contener | De dónde sale |
|---|---|---|---|
| **0** | Portada | Organización, tipo de encargo, periodo auditado, fecha, clasificación y **lista nominal de distribución** | Semana 16 |
| **1** | Resumen ejecutivo | Máximo dos páginas. Es lo único que la gerencia lee con seguridad | Semana 16 |
| 1.1 | · Objetivo y alcance | En tres líneas, con las exclusiones nombradas | Sección 6 del plan |
| 1.2 | · Conclusión general | **La opinión del auditor, con veredicto explícito**. Va aquí, no al final | Semana 16 |
| 1.3 | · Hallazgos por severidad | Tabla con el número de hallazgos crítico, alto, medio y bajo | Semana 16 |
| 1.4 | · Los tres asuntos que requieren decisión del directorio | Tres, no diez. Si son diez, no se priorizó | Semana 16 |
| 1.5 | · Comparación con el ciclo anterior | Solo si existe un encargo previo | Semana 16 |
| **2** | Introducción | El encuadre formal del encargo | Unidad II |
| 2.1 | · Antecedentes y origen del encargo | Por qué este encargo y no otro | Sección 3 del plan |
| 2.2 | · Objetivos de la auditoría | La pregunta que el informe responde | Sección 6 del plan |
| 2.3 | · Alcance | Sistemas, procesos y periodo · **exclusiones explícitas** | Sección 6 del plan |
| 2.4 | · Criterios aplicados | Cada norma con **su edición vigente** | Sección 6 del plan |
| 2.5 | · Metodología y normas profesionales | ISO 19011 e ITAF, y cómo se aplicaron | Sección 7 del plan |
| 2.6 | · Limitaciones al alcance | Qué no se pudo verificar y **su efecto sobre la conclusión** | Semanas 13 a 16 |
| 2.7 | · Equipo auditor y declaración de independencia | Con las salvaguardas, si las hubo | Anexo B del plan |
| **3** | Diagnóstico de la situación | El estado en el que se encontró la organización | Unidad II |
| 3.1 | · Descripción del ambiente de TI auditado | Sistemas, personal, infraestructura | Semana 07 |
| 3.2 | · Nivel de madurez por dominio | La matriz y el radar | Semana 10 |
| 3.3 | · Evaluación del gobierno de TI | Contra la ISO/IEC 38500:2024 | Semana 14 |
| 3.4 | · Estado del cumplimiento legal | Contra la Ley 29733 y el D. Leg. 822 | Semana 11 |
| **4** | Hallazgos | Ordenados por severidad, cada uno en estructura **CCCER** | Semanas 13 a 16 |
| **5** | Conclusiones | Una por cada objetivo declarado en 2.2, y ninguna fuera del alcance | Semana 16 |
| 5.1 | · Sobre la efectividad del control interno de TI | Contra el marco COSO | Semana 16 |
| 5.2 | · Sobre el cumplimiento normativo | Contra el criterio de 3.4 | Semana 16 |
| 5.3 | · Sobre la capacidad de continuidad | Contra la ISO 22301 | Semana 15 |
| 5.4 | · Riesgos residuales que la organización asume | Lo que queda vivo aunque se atiendan todas las recomendaciones | Semana 16 |
| **6** | Recomendaciones consolidadas | Matriz priorizada con responsable, plazo y verificación de cierre | Semana 16 |
| **7** | Plan de seguimiento | Fechas de verificación y criterio de cierre de cada recomendación | Semana 17 |

## La estructura de cada hallazgo

Todo hallazgo de la sección 4 se redacta con los cinco elementos, en este orden, y ninguno es opcional.

| Elemento | Pregunta que responde | Si falta |
|---|---|---|
| **C**ondición | ¿Qué se observó? | No hay hecho, hay opinión |
| **C**riterio | ¿Qué debería ser, y según qué norma con su código? | El hallazgo no es exigible |
| **C**ausa | ¿Por qué ocurre? | La recomendación ataca el síntoma |
| **E**fecto | ¿Qué consecuencia tiene, en cifra o en riesgo? | La gerencia no lo prioriza |
| **R**ecomendación | ¿Qué debe hacerse? | El informe no es accionable |

A los cinco se añaden **responsable propuesto**, **plazo** y **respuesta de la administración**, que se recoge en la reunión de validación de la Semana 16 y se transcribe aunque discrepe.

## Los anexos obligatorios

| Anexo | Contenido |
|---|---|
| **A** | Programa de trabajo ejecutado, con lo que se hizo y lo que no |
| **B** | Índice de papeles de trabajo con su referencia cruzada a cada hallazgo |
| **C** | Detalle técnico de los hallazgos |
| **D** | Cadena de custodia de la evidencia, con hash y fecha |
| **E** | Actas de apertura, validación y cierre, firmadas |
| **F** | Glosario de términos técnicos, que es lo que hace legible el informe |

## Las cuatro comprobaciones que decide la nota

| Comprobación | Qué debe ser consistente |
|---|---|
| **Alcance → conclusión** | Ninguna conclusión de la sección 5 cae fuera de lo declarado en 2.3 |
| **Hallazgo → evidencia** | Todo hallazgo de la sección 4 tiene su papel de trabajo referenciado en el anexo B |
| **Criterio → edición** | Toda norma citada lleva su edición vigente, y es exigible al régimen de la organización |
| **Objetivo → conclusión** | Cada objetivo de 2.2 tiene su conclusión en la sección 5, y ninguna sobra |

> **La prueba del resumen ejecutivo.** Si alguien lee solo las dos primeras páginas y no sabe a qué se concluyó, cuántos hallazgos hay y qué debe decidir el directorio, el informe está mal ordenado por muy correcto que sea el resto.

---

---

[Auditoría de Sistemas](README.md) · [Modelo del Plan de Auditoría](MODELO-PLAN-DE-AUDITORIA.md) · **Modelo del Informe de Auditoría**

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
