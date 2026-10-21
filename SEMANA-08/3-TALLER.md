[Semana 08](README.md) · [Teoría](1-TEORIA.md) · [Dinámica de aula](2-DINAMICA.md) · **Taller de laboratorio**

# Semana 08

## Plan de auditoría interna del sistema de gestión de seguridad de la información

**SI-084 - Auditoría de Sistemas** - Sesión 2 en laboratorio · calificación **procedimental**

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](../GLOSARIO.md).

---

## Qué entregas

| | |
|---|---|
| **Archivo** | `SI084-S08-TALLER-Grupo<N>.pdf` |
| **Plantilla obligatoria** | [SI084-PLANTILLA-TALLER.docx](../PLANTILLAS/SI084-PLANTILLA-TALLER.docx) |
| **Formato** | PDF exportado desde la plantilla en Word, con la carátula de la UPT, el índice actualizado y las capturas numeradas |
| **Qué va dentro** | Las secciones de la plantilla. La **5. Resultados y evidencias** se califica contra la tabla de resultados esperados de esta guía, y **cada resultado necesita la evidencia que lo demuestre**. No se copian de aquí los objetivos, la duración ni los resultados de aprendizaje |
| **El plan de auditoría** | Va completo como anexo del informe, con las doce secciones y los seis anexos del [modelo](../MODELO-PLAN-DE-AUDITORIA.md) |
| **Dónde se sube** | Aula virtual, tarea «Taller · Semana 08» |
| **Cuándo vence** | Según lo programado en el aula virtual |

> No se califica un informe entregado en `.docx`, sin carátula, sin los códigos de los integrantes o con resultados declarados sin evidencia.

---

## 1. Información sobre el evento práctico

### 1.1. Título del evento práctico

Elaboración del plan de auditoría interna del sistema de gestión de seguridad de la información de la organización asignada, conforme a la cláusula 9.2 de la NTP-ISO/IEC 27001:2022 y a la cláusula 6 de la ISO 19011:2018, con la regla de clasificación de no conformidades fijada antes de recolectar.

### 1.2. Objetivos

- Elaborar el **plan de auditoría completo** del sistema de gestión de seguridad de la información para la organización que el docente le asigne, con la estructura del [modelo del plan](../MODELO-PLAN-DE-AUDITORIA.md).
- Convertir **las preguntas de la organización** en objetivos de auditoría y **lo que entrega** en procedimientos.
- Revisar el plan con la lista de comprobación antes de entregarlo.

### 1.3. Resultados de Aprendizaje (RA)

- **RA1** Analiza e identifica las responsabilidades que asume un auditor de sistemas.
- **RA2** Valora la importancia de los roles del auditor de sistemas.

### 1.4. Recursos

| Recurso | Detalle |
|---|---|
| **NTP-ISO/IEC 27001:2022** y **NTP-ISO/IEC 27002:2022** | Disponibles en la biblioteca de la UPT |
| **ISO 19011:2018**, cláusula 6 | Disponible en la biblioteca de la UPT |
| **LibreOffice Calc** o Google Sheets | El programa de procedimientos y la matriz de controles |

### 1.5. Seguridad

1. La información de la organización es **Confidencial**. El repositorio del equipo es privado y todo documento lleva la marca **CONFIDENCIAL — USO ACADÉMICO**.
2. Las personas se nombran por su cargo, nunca por su nombre.
3. **Ninguna prueba se ejecuta sobre ningún sistema.** Esta semana se produce un plan.

---

## 2. Procedimiento o Metodología

**Su equipo auditor ha sido convocado para elaborar un plan de auditoría del sistema de gestión de seguridad de la información.** El docente le designa el caso, una de las diez solicitudes de [CASOS/](CASOS/README.md), en la que la organización expone sus problemas y lo que espera de la auditoría. El plan sigue la estructura del [modelo del plan](../MODELO-PLAN-DE-AUDITORIA.md) y los criterios del [Encargo 08](../ENCARGOS-UNIDAD-II/CASO-08-seguridad-de-la-informacion.md).

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
2. La **materialidad** se fija con esta base. La población de usuarios habilitados del sistema principal, de `datos/usuarios_erp.csv`, y el número de controles del Anexo A que la declaración incluye.
3. El **riesgo de auditoría** se declara en sus tres componentes, con el nivel y una línea de sustento cada uno.
4. Los **criterios** son los del encargo, citados con su código. Obligatorios. las cláusulas 4.3, 5.1, 5.3, 6.1.2, 6.1.3, 7.2, 7.3, 9.1, 9.2 y 9.3, y los controles A.5.15 a A.5.18, A.5.19, A.5.23, A.5.24, A.5.30, A.6.3, A.8.2, A.8.5, A.8.13, A.8.15 y A.8.16. Se añaden los que el régimen de la organización haga exigibles, como dice su solicitud.

### Paso D — El programa de procedimientos (sección VII y anexos)

1. El programa tiene **doce procedimientos**, uno por fila, con las trece columnas del modelo. Cada procedimiento prueba un objetivo, cita un criterio con código y usa un documento o un archivo que la organización entrega.
2. Esta semana no pueden faltar estos procedimientos.

- Un procedimiento **asistido por computador sobre el 100 % de los usuarios**, que cruce `usuarios_erp.csv` contra `empleados.csv` por fecha de cese.
- Un segundo procedimiento **asistido por computador** que cuente los usuarios habilitados sin segundo factor de autenticación.
- Un procedimiento de **reejecución de la restauración** declarada en la política de respaldo.

3. Los **seis anexos** del modelo se completan a partir del programa. La matriz del Anexo A se organiza por control del Anexo A de la norma, con el estado que la declaración de aplicabilidad afirma, la evidencia que la organización ofrece y el riesgo que queda si esa evidencia no se sostiene.

### Paso E — Lo administrativo (secciones IX a XII)

1. Las **fechas, las horas, la contraparte, el canal y el presupuesto** son los que la organización ofrece en «Cómo trabajaremos con ustedes». No se inventan.
2. La suma de horas del programa, más supervisión e informe, **cabe en las horas que la organización financia**. Si no cabe, se recorta el programa, no la organización.
3. La **sección XII** nombra el documento que se emitirá al final. Un informe de auditoría con la estructura del modelo de la Unidad III.

---

### Paso F — Validar y corregir

1. Revisar el plan contra la rúbrica de la sección 3 y corregir lo que falte.
2. Comprobar que **no hay ninguna prueba de eficacia operativa** programada sobre un control que la declaración marca como no implementado.

### Paso G — Registrar la evidencia y cerrar

1. Se exporta el plan a PDF desde la plantilla, con el programa de procedimientos como anexo.
2. Se entrega como dice la sección 3.

---

## 3. Resultados

### 3.1. El producto del taller

El **plan de auditoría del sistema de gestión de seguridad de la información** de la organización asignada, completo. Las doce secciones y los seis anexos del [modelo](../MODELO-PLAN-DE-AUDITORIA.md), con el programa de doce procedimientos como anexo. Es lo que la rúbrica califica.

### 3.2. Cómo y dónde se entrega

1. En PDF exportado desde la [plantilla de taller](../PLANTILLAS/SI084-PLANTILLA-TALLER.docx), con la carátula de la UPT, el índice actualizado y los códigos de los integrantes.
2. Con el nombre `SI084-S08-TALLER-Grupo<N>.pdf`.
3. En el aula virtual, tarea «Taller · Semana 08», en el plazo programado.

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

1. Un sistema de gestión cuyo alcance es «todo» no tiene alcance. La primera tarea del auditor interno no es comprobar los controles, es comprobar que existe un perímetro sobre el que comprobarlos.
2. La declaración de aplicabilidad convierte una norma voluntaria en criterio exigible, porque la organización se lo fijó a sí misma. Un control declarado implementado cuya única evidencia es una frase entre comillas no está implementado, está afirmado.
3. La regla de clasificación de la no conformidad decide la severidad del informe. Escrita después de ver los resultados, se acomoda a ellos; escrita antes, es un criterio.

## 5. Referencias Bibliográficas

- NTP-ISO/IEC 27001:2022, *Sistemas de gestión de seguridad de la información. Requisitos*. https://www.inacal.gob.pe/
- NTP-ISO/IEC 27002:2022, *Controles de seguridad de la información*. https://www.inacal.gob.pe/
- ISO/IEC 27001:2022. https://www.iso.org/standard/27001
- ISO 19011:2018, cláusula 6 «Realización de una auditoría». https://www.iso.org/standard/70017.html
- ISACA. *ITAF: A Professional Practices Framework for IS Audit/Assurance* (5.ª ed.). https://www.isaca.org/resources/frameworks-standards-and-models
- Resolución SBS N.º 504-2021 y sus modificatorias. https://www.sbs.gob.pe/
- Ley 29733, Ley de Protección de Datos Personales, y su Reglamento D. S. 016-2024-JUS. https://www.gob.pe/institucion/anpd
- Decreto Legislativo 1412, Ley de Gobierno Digital, y D. S. 029-2021-PCM. https://www.gob.pe/13326-reglamento-de-la-ley-de-gobierno-digital

## 6. Anexos

- El plan completo, exportado a PDF y firmado por el equipo.
- El programa de procedimientos, en hoja de cálculo.

---

---

[Semana 08](README.md) · [Teoría](1-TEORIA.md) · [Dinámica de aula](2-DINAMICA.md) · **Taller de laboratorio**

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
