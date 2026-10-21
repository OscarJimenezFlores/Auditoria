[Semana 12](README.md) · [Teoría](1-TEORIA.md) · [Dinámica de aula](2-DINAMICA.md) · **Taller de laboratorio**

# Semana 12

## Plan de auditoría de seguridad del canal digital y de las aplicaciones expuestas

**SI-084 - Auditoría de Sistemas** - Sesión 2 en laboratorio · calificación **procedimental**

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](../GLOSARIO.md).

---

## Qué entregas

| | |
|---|---|
| **Archivo** | `SI084-S12-TALLER-Grupo<N>.pdf` |
| **Plantilla obligatoria** | [SI084-PLANTILLA-TALLER.docx](../PLANTILLAS/SI084-PLANTILLA-TALLER.docx) |
| **Formato** | PDF exportado desde la plantilla en Word, con la carátula de la UPT, el índice actualizado y las capturas numeradas |
| **Qué va dentro** | Las secciones de la plantilla. La **5. Resultados y evidencias** se califica contra la tabla de resultados esperados de esta guía, y **cada resultado necesita la evidencia que lo demuestre**. No se copian de aquí los objetivos, la duración ni los resultados de aprendizaje |
| **El plan de auditoría** | Va completo como anexo del informe, con las doce secciones y los seis anexos del [modelo](../MODELO-PLAN-DE-AUDITORIA.md) |
| **Dónde se sube** | Aula virtual, tarea «Taller · Semana 12» |
| **Cuándo vence** | Según lo programado en el aula virtual. El plazo se cuenta desde la sesión de laboratorio de la semana, **se desarrolle el taller dentro de ella o fuera de ella** |

> No se califica un informe entregado en `.docx`, sin carátula, sin los códigos de los integrantes o con resultados declarados sin evidencia.

---

## 1. Información sobre el evento práctico

### 1.1. Título del evento práctico

Elaboración del plan de auditoría de seguridad del canal digital de la organización asignada, con el nivel de verificación del OWASP ASVS 4.0.3 declarado y justificado, la responsabilidad compartida con el proveedor resuelta antes del alcance, y el texto de la autorización escrita que cualquier prueba activa requeriría. **Es el plan que se ejecuta en la Unidad III.**

### 1.2. Objetivos

- Elaborar el **plan de auditoría completo** de la seguridad del canal digital y de las aplicaciones expuestas para la organización que el docente le asigne, con la estructura del [modelo del plan](../MODELO-PLAN-DE-AUDITORIA.md).
- Convertir **las preguntas de la organización** en objetivos de auditoría y **lo que entrega** en procedimientos.
- Revisar el plan con la lista de comprobación antes de entregarlo.

### 1.3. Resultados de Aprendizaje (RA)

- **RA1** Analiza e identifica las responsabilidades que asume un auditor de sistemas.
- **RA2** Valora la importancia de los roles del auditor de sistemas.

### 1.4. Recursos

| Recurso | Detalle |
|---|---|
| **OWASP Application Security Verification Standard 4.0.3** | https://owasp.org/www-project-application-security-verification-standard/ |
| **OWASP Top 10:2021** | https://owasp.org/Top10/ |
| **OWASP Web Security Testing Guide 4.2** | https://owasp.org/www-project-web-security-testing-guide/ |
| **LibreOffice Calc** o Google Sheets | La matriz de requisitos del ASVS y el programa |

### 1.5. Seguridad

1. La información de la organización es **Confidencial**. El repositorio del equipo es privado y todo documento lleva la marca **CONFIDENCIAL — USO ACADÉMICO**.
2. Las personas se nombran por su cargo, nunca por su nombre.
3. **Ninguna prueba se ejecuta sobre ningún sistema.** Esta semana se produce un plan.

---

## 2. Procedimiento o Metodología

**Su equipo auditor ha sido convocado para elaborar un plan de auditoría de la seguridad del canal digital y de las aplicaciones expuestas.** El docente le designa el caso, una de las diez solicitudes de [CASOS/](CASOS/README.md), en la que la organización expone sus problemas y lo que espera de la auditoría. El plan sigue la estructura del [modelo del plan](../MODELO-PLAN-DE-AUDITORIA.md) y los criterios del [Encargo 12](../ENCARGOS-UNIDAD-II/CASO-12-seguridad-del-canal-digital.md).

### Paso A — Comprender la organización (secciones I a III)

1. De la sección «Quiénes somos» de la solicitud y de la ficha del banco, se completa la **sección II** del plan. Razón social, sector, regulador, procesos, sistemas, área de TI y presupuesto.
2. De «Por qué pedimos esta auditoría» y «Cómo se dispuso», se redacta la **sección I**, el origen. En tres párrafos, con el hecho que motiva la auditoría y el acto que la dispone.
3. La **sección III** es una frase. La materia de control, la organización y el periodo auditado. La misma frase va en la carátula.

### Paso B — Alcance y objetivos (secciones IV y V)

1. Cada pregunta de «Lo que queremos saber» se convierte en **un objetivo específico**. Entre tres y cinco. El objetivo general los resume.
2. El **alcance** dice qué procesos, sistemas y periodo entran, con el tamaño de cada población que la solicitud declara, y qué queda fuera y por qué.
3. Lo que la organización no entrega o no autoriza se escribe como **limitación**, no se calla.

### Paso C — Enfoque, materialidad, riesgo y criterios (secciones VI y VIII)

1. Para cada objetivo se elige **enfoque sustantivo o de confianza en controles**, y se justifica en una línea con lo que la solicitud cuenta.
2. La **materialidad** se fija con esta base. El número de titulares cuyos datos recogen los formularios del canal y el número de activos expuestos inventariados.
3. El **riesgo de auditoría** se declara en sus tres componentes, con el nivel y una línea de sustento cada uno.
4. Los **criterios** son los del encargo, citados con su código. Obligatorios. los capítulos V1, V2, V3, V4, V7, V8, V9 y V14 del OWASP ASVS 4.0.3, las categorías A01 a A10 del OWASP Top 10:2021, y los controles A.5.19, A.5.23, A.8.9, A.8.15, A.8.16, A.8.24 y A.8.32. Se añaden los que el régimen de la organización haga exigibles, como dice su solicitud.

### Paso D — El programa de procedimientos (sección VII y anexos)

1. El programa tiene **doce procedimientos**, uno por fila, con las trece columnas del modelo. Cada procedimiento prueba un objetivo, cita un criterio con código y usa un documento o un archivo que la organización entrega.
2. Esta semana no pueden faltar estos procedimientos.

- Un procedimiento de **inspección documental sobre el propio inventario** de activos expuestos, que determine su completitud.
- Un procedimiento **asistido por computador sobre la lista completa de componentes** del portal, que compare la versión instalada con la vigente del proveedor.
- Un segundo procedimiento **asistido por computador** sobre los formularios, que inventaríe campo por campo el dato personal recogido y su destino.

3. Los **seis anexos** del modelo se completan a partir del programa. La matriz del Anexo A se organiza por requisito del ASVS, con la categoría del OWASP Top 10:2021 que le corresponde y el control del Anexo A de la NTP-ISO/IEC 27001:2022 que lo respalda. El Anexo D incluye el **texto de la autorización** y la delimitación de lo verificable sin ella.

### Paso E — Lo administrativo (secciones IX a XII)

1. Las **fechas, las horas, la contraparte, el canal y el presupuesto** son los que la organización ofrece en «Cómo trabajaremos con ustedes». No se inventan.
2. La suma de horas del programa, más supervisión e informe, **cabe en las horas que la organización financia**. Si no cabe, se recorta el programa, no la organización.
3. La **sección XII** nombra el documento que se emitirá al final. Un informe de auditoría con la estructura del modelo de la Unidad III.

---

### Paso F — Validar y corregir

1. Revisar el plan contra la rúbrica de la sección 3 y corregir lo que falte.
2. Comprobar que **ningún procedimiento exige un requisito de un nivel superior** al que el plan declaró.
3. Verificar que la sección IV distingue **lo verificable sin autorización** de lo que la requiere, y que ningún procedimiento cruza esa frontera.

**Control de calidad del encargo.** Antes de entregar, el equipo revisa su propio plan con la rúbrica de la sección 3, como lo haría un supervisor, y anota por escrito lo que corrige. En la sesión el docente hace la revisión de calidad de cada plan y devuelve sus observaciones. **Ningún equipo accede al repositorio de otro.** Las observaciones recibidas se atienden o se rebaten, y ambas cosas quedan en el informe.

> **Esta semana la sesión de laboratorio se comparte con el examen de la Unidad II.** El plazo de entrega se cuenta desde la sesión de la semana, se desarrolle el taller dentro de ella o fuera de ella.

### Paso G — Registrar la evidencia y cerrar

1. Se exporta el plan a PDF desde la plantilla, con el programa de procedimientos como anexo.
2. Se entrega como dice la sección 3.

---

## 3. Resultados

### 3.1. El producto del taller

El **plan de auditoría de la seguridad del canal digital y de las aplicaciones expuestas** de la organización asignada, completo. Las doce secciones y los seis anexos del [modelo](../MODELO-PLAN-DE-AUDITORIA.md), con el programa de doce procedimientos como anexo. Es lo que la rúbrica califica.

### 3.2. Cómo y dónde se entrega

1. En PDF exportado desde la [plantilla de taller](../PLANTILLAS/SI084-PLANTILLA-TALLER.docx), con la carátula de la UPT, el índice actualizado y los códigos de los integrantes.
2. Con el nombre `SI084-S12-TALLER-Grupo<N>.pdf`.
3. En el aula virtual, tarea «Taller · Semana 12», en el plazo programado.

## Rúbrica procedimental (20 puntos)

Se aplica sobre el plan de auditoría entregado. **Cada criterio se califica de forma independiente.**

| Criterio | 4 — Logrado | 2 — En proceso | 0 — Insuficiente |
|---|---|---|---|
| **El plan está completo y es de esta organización** | Las doce secciones y los seis anexos, en la plantilla, con contenido propio de la solicitud asignada | Falta una sección o un anexo, o parte del contenido es genérico | Faltan varias secciones, o es el plan de otra semana con el título cambiado |
| **Origen, entidad y materia salen de la solicitud (secciones I a III)** | El hecho que motiva la auditoría, los datos de la organización y la materia de control están tomados de la solicitud y se citan | Parciales, o con datos que la solicitud no dice | Inventados o ausentes |
| **Alcance y objetivos responden a lo que la organización quiere saber (secciones IV y V)** | Cada pregunta de la solicitud tiene su objetivo específico, con alcance, exclusiones y limitaciones escritas | Alguna pregunta sin objetivo, o alcance sin exclusiones ni limitaciones | Objetivos genéricos del marco, sin relación con la solicitud |
| **Enfoque, materialidad, riesgo y criterios sustentados (secciones VI y VIII)** | Enfoque justificado por objetivo, materialidad con su base declarada, riesgo en sus tres componentes y criterios citados con código | Alguno sin sustento, o criterios sin código | Ausentes, o copiados sin relación con el caso |
| **El programa prueba los objetivos con lo que la organización entrega (secciones VII y IX a XII)** | Doce procedimientos, cada uno con objetivo, criterio y documento o archivo de la solicitud; horas que caben en las financiadas y datos administrativos tomados de la solicitud | Procedimientos incompletos, o horas y fechas que no cuadran con la solicitud | Procedimientos sin objetivo o sin evidencia posible, o secciones administrativas inventadas |

## 4. Conclusiones

1. Un plan de seguridad de aplicaciones que no declara su nivel de verificación no tiene alcance. El nivel es lo que convierte un estándar de cientos de requisitos en un encargo ejecutable y proporcionado al riesgo.
2. Una versión antigua de un componente es una condición observada, no un hallazgo. Que sea explotable en este despliegue es desconocido hasta que un procedimiento lo determine, y el plan dice cuál sería ese procedimiento.
3. La autorización escrita no es un trámite, es lo que separa una auditoría de un acceso no autorizado. Las Leyes 30096 y 30171 tipifican la diferencia, y redactar la autorización es tan parte del oficio como redactar el hallazgo.

## 5. Referencias Bibliográficas

- OWASP. *Application Security Verification Standard 4.0.3*. https://owasp.org/www-project-application-security-verification-standard/
- OWASP. *Top 10:2021*. https://owasp.org/Top10/
- OWASP. *Web Security Testing Guide 4.2*. https://owasp.org/www-project-web-security-testing-guide/
- OWASP. *Proactive Controls*. https://owasp.org/www-project-proactive-controls/
- NTP-ISO/IEC 27001:2022, Anexo A, controles A.5.19, A.5.23, A.8.9, A.8.15, A.8.16, A.8.24 y A.8.32. https://www.inacal.gob.pe/
- ISACA. (2018). *COBIT 2019 Framework: Governance and Management Objectives*, objetivo DSS05. https://www.isaca.org/resources/cobit
- ISACA. *ITAF: A Professional Practices Framework for IS Audit/Assurance* (5.ª ed.), norma 1204. https://www.isaca.org/resources/frameworks-standards-and-models
- Ley 29733, Ley de Protección de Datos Personales, y su Reglamento D. S. 016-2024-JUS. https://www.gob.pe/institucion/anpd
- Ley 30096, Ley de Delitos Informáticos, y Ley 30171 que la modifica.
- Decreto Legislativo 1412, Ley de Gobierno Digital, y D. S. 029-2021-PCM. https://www.gob.pe/13326-reglamento-de-la-ley-de-gobierno-digital

## 6. Anexos

- El plan completo, exportado a PDF y firmado por el equipo.
- El programa de procedimientos, en hoja de cálculo.

---

---

[Semana 12](README.md) · [Teoría](1-TEORIA.md) · [Dinámica de aula](2-DINAMICA.md) · **Taller de laboratorio**

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
