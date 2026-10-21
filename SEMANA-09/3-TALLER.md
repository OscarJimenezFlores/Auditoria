[Semana 09](README.md) · [Teoría](1-TEORIA.md) · [Dinámica de aula](2-DINAMICA.md) · **Taller de laboratorio**

# Semana 09

## Plan de auditoría del ciclo de vida del software

**SI-084 - Auditoría de Sistemas** - Sesión 2 en laboratorio · calificación **procedimental**

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](../GLOSARIO.md).

---

## Qué entregas

| | |
|---|---|
| **Archivo** | `SI084-S09-TALLER-Grupo<N>.pdf` |
| **Plantilla obligatoria** | [SI084-PLANTILLA-TALLER.docx](../PLANTILLAS/SI084-PLANTILLA-TALLER.docx) |
| **Formato** | PDF exportado desde la plantilla en Word, con la carátula de la UPT, el índice actualizado y las capturas numeradas |
| **Qué va dentro** | Las secciones de la plantilla. La **5. Resultados y evidencias** se califica contra la tabla de resultados esperados de esta guía, y **cada resultado necesita la evidencia que lo demuestre**. No se copian de aquí los objetivos, la duración ni los resultados de aprendizaje |
| **El plan de auditoría** | Va completo como anexo del informe, con las doce secciones y los seis anexos del [modelo](../MODELO-PLAN-DE-AUDITORIA.md) |
| **Dónde se sube** | Aula virtual, tarea «Taller · Semana 09» |
| **Cuándo vence** | Según lo programado en el aula virtual |

> No se califica un informe entregado en `.docx`, sin carátula, sin los códigos de los integrantes o con resultados declarados sin evidencia.

---

## 1. Información sobre el evento práctico

### 1.1. Título del evento práctico

Elaboración del plan de auditoría del ciclo de vida del software de la organización asignada, con los procesos de la NTP-ISO/IEC 12207 seleccionados y justificados, la medición de la cobertura de trazabilidad definida sobre una población declarada, y verificación y validación como objetivos separados.

### 1.2. Objetivos

- Elaborar el **plan de auditoría completo** del ciclo de vida del software para la organización que el docente le asigne, con la estructura del [modelo del plan](../MODELO-PLAN-DE-AUDITORIA.md).
- Convertir **las preguntas de la organización** en objetivos de auditoría y **lo que entrega** en procedimientos.
- Revisar el plan con la lista de comprobación antes de entregarlo.

### 1.3. Resultados de Aprendizaje (RA)

- **RA1** Analiza e identifica las responsabilidades que asume un auditor de sistemas.
- **RA2** Valora la importancia de los roles del auditor de sistemas.

### 1.4. Recursos

| Recurso | Detalle |
|---|---|
| **NTP-ISO/IEC 12207** y **NTP-ISO/IEC 25010** | Disponibles en la biblioteca de la UPT |
| **Git** | El historial como fuente de evidencia objetiva del proceso |
| **LibreOffice Calc** o Google Sheets | La matriz de trazabilidad y el programa |

### 1.5. Seguridad

1. La información de la organización es **Confidencial**. El repositorio del equipo es privado y todo documento lleva la marca **CONFIDENCIAL — USO ACADÉMICO**.
2. Las personas se nombran por su cargo, nunca por su nombre.
3. **Ninguna prueba se ejecuta sobre ningún sistema.** Esta semana se produce un plan.

---

## 2. Procedimiento o Metodología

**Su equipo auditor ha sido convocado para elaborar un plan de auditoría del ciclo de vida del software.** El docente le designa el caso, una de las diez solicitudes de [CASOS/](CASOS/README.md), en la que la organización expone sus problemas y lo que espera de la auditoría. El plan sigue la estructura del [modelo del plan](../MODELO-PLAN-DE-AUDITORIA.md) y los criterios del [Encargo 09](../ENCARGOS-UNIDAD-II/CASO-09-ciclo-de-vida-del-software.md).

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
2. La **materialidad** se fija con esta base. La población de cambios del periodo y la de pedidos de cambio registrados, del expediente del ciclo de vida.
3. El **riesgo de auditoría** se declara en sus tres componentes, con el nivel y una línea de sustento cada uno.
4. Los **criterios** son los del encargo, citados con su código. Obligatorios. los procesos de gestión de la configuración, gestión de requisitos, verificación, validación, integración, mantenimiento y aseguramiento de la calidad de la NTP-ISO/IEC 12207, y los controles A.8.25, A.8.28, A.8.31, A.8.32 y A.8.33. Se añaden los que el régimen de la organización haga exigibles, como dice su solicitud.

### Paso D — El programa de procedimientos (sección VII y anexos)

1. El programa tiene **doce procedimientos**, uno por fila, con las trece columnas del modelo. Cada procedimiento prueba un objetivo, cita un criterio con código y usa un documento o un archivo que la organización entrega.
2. Esta semana no pueden faltar estos procedimientos.

- Un procedimiento **asistido por computador sobre la población completa de cambios**, que mida la cobertura de trazabilidad del pedido al cambio.
- Un segundo procedimiento **asistido por computador** que mida la trazabilidad en sentido inverso, del cambio al pedido.
- Un procedimiento de **reejecución del paso de un cambio concreto**, del pedido al despliegue.

3. Los **seis anexos** del modelo se completan a partir del programa. La matriz del Anexo A se organiza por proceso de la NTP-ISO/IEC 12207, con el riesgo propio de cada uno. El Anexo B, el de trazabilidad, duplica su utilidad en este encargo porque la trazabilidad es a la vez el método del anexo y el objeto de la auditoría.

### Paso E — Lo administrativo (secciones IX a XII)

1. Las **fechas, las horas, la contraparte, el canal y el presupuesto** son los que la organización ofrece en «Cómo trabajaremos con ustedes». No se inventan.
2. La suma de horas del programa, más supervisión e informe, **cabe en las horas que la organización financia**. Si no cabe, se recorta el programa, no la organización.
3. La **sección XII** nombra el documento que se emitirá al final. Un informe de auditoría con la estructura del modelo de la Unidad III.

---

### Paso F — Validar y corregir

1. Revisar el plan contra la rúbrica de la sección 3 y corregir lo que falte.
2. Comprobar que la medición de la cobertura **declara su población** y que esa población está en el plan, no solo en el script.
3. Verificar que hay un objetivo específico para **verificación** y otro distinto para **validación**, y que ninguno de los dos usa la palabra del otro.

### Paso G — Registrar la evidencia y cerrar

1. Se exporta el plan a PDF desde la plantilla, con el programa de procedimientos como anexo.
2. Se entrega como dice la sección 3.

---

## 3. Resultados

### 3.1. El producto del taller

El **plan de auditoría del ciclo de vida del software** de la organización asignada, completo. Las doce secciones y los seis anexos del [modelo](../MODELO-PLAN-DE-AUDITORIA.md), con el programa de doce procedimientos como anexo. Es lo que la rúbrica califica.

### 3.2. Cómo y dónde se entrega

1. En PDF exportado desde la [plantilla de taller](../PLANTILLAS/SI084-PLANTILLA-TALLER.docx), con la carátula de la UPT, el índice actualizado y los códigos de los integrantes.
2. Con el nombre `SI084-S09-TALLER-Grupo<N>.pdf`.
3. En el aula virtual, tarea «Taller · Semana 09», en el plazo programado.

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

1. Verificar es comprobar el producto contra su especificación. Validar es comprobarlo contra el uso previsto. Un plan que las confunde deja sin auditar una de las dos, y la que suele quedar fuera es la validación, que es la que el usuario reclama.
2. Un porcentaje de cobertura de trazabilidad sin población declarada es una cifra sin significado. El denominador es lo que hace auditable al numerador.
3. El ciclo de vida existe aunque la organización no se considere una empresa de software. Excluirlo del alcance porque «aquí no desarrollamos» deja sin auditar las hojas de cálculo y los reportes a medida sobre los que se decide.

## 5. Referencias Bibliográficas

- NTP-ISO/IEC 12207, *Procesos del ciclo de vida del software*. https://www.inacal.gob.pe/
- NTP-ISO/IEC 25010, *Modelo de calidad del producto de software*. https://www.inacal.gob.pe/
- ISO/IEC/IEEE 12207:2017, *Systems and software engineering. Software life cycle processes*. https://www.iso.org/standard/63712.html
- NTP-ISO/IEC 27001:2022, Anexo A, controles A.8.25 a A.8.33. https://www.inacal.gob.pe/
- ISACA. (2018). *COBIT 2019 Framework: Governance and Management Objectives*, objetivos BAI03, BAI06 y BAI07. https://www.isaca.org/resources/cobit
- ISACA. *ITAF: A Professional Practices Framework for IS Audit/Assurance* (5.ª ed.). https://www.isaca.org/resources/frameworks-standards-and-models
- Decreto Legislativo 822, Ley sobre el Derecho de Autor. https://www.gob.pe/institucion/indecopi/
- Piattini Velthuis, M., Del Peso Navarro, E. y Del Peso Ruiz, M. (2009). *Auditoría de tecnologías y sistemas de información* (6.ª ed.). Alfaomega / Ra-Ma.

## 6. Anexos

- El plan completo, exportado a PDF y firmado por el equipo.
- El programa de procedimientos, en hoja de cálculo.

---

---

[Semana 09](README.md) · [Teoría](1-TEORIA.md) · [Dinámica de aula](2-DINAMICA.md) · **Taller de laboratorio**

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
