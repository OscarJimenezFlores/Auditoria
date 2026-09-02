<div align="center">
  <img src="../Logos/logo_universidad.png" alt="Universidad Privada de Tacna" height="62">
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="../Logos/logo_escuela_sistemas.jpeg" alt="Escuela Profesional de Ingeniería de Sistemas" height="62">
</div>

<p align="center">
  <strong>Universidad Privada de Tacna</strong><br>
  Facultad de Ingeniería · Escuela Profesional de Ingeniería de Sistemas
</p>

<h1 align="center">Semana 02 · Principios de Seguridad de la Información · Roles y Responsabilidades</h1>

<p align="center">
  <strong>SI-084 · Auditoría de Sistemas</strong><br>
  4 horas académicas de 50 min · aula: teoría 60 + dinámica 35 + cierre 5 · laboratorio: taller 60 + avance asistido 40
</p>

---

## Datos de la asignatura

| | |
|---|---|
| **Asignatura** | SI-084 · Auditoría de Sistemas |
| **Escuela** | Escuela Profesional de Ingeniería de Sistemas |
| **Ciclo** | X · 04 horas semanales · 03 créditos · Obligatorio |
| **Prerrequisito** | SI-985 Gestión de la Configuración de Software |
| **Unidad** | I — Seguridad de la Información en Auditoría de Sistemas |
| **Semana** | 02 de 17 |
| **Duración** | 4 horas académicas de 50 min · aula: teoría 60 + dinámica 35 + cierre 5 · laboratorio: taller 60 + avance asistido 40 |
| **Resultados de aprendizaje** | **RA1** Analiza e interpreta los conceptos y terminología de Auditoría de Sistemas · **RA2** Evalúa la seguridad de la información en Auditoría de Sistemas |
| **Atributos del graduado** | AG-I02 Ética (CD2, nivel 4) · AG-I08 Análisis de Problemas (CD2, nivel 4) |

### Lo que indica el sílabo

**Contenido conceptual.** Principios de seguridad de la Información, información vs. seguridad. Seguridad de la Información, roles y responsabilidades.

**Contenido procedimental.** Comprensión sobre los principios y la relevancia de la seguridad informática y la evaluación de los riesgos.

## Materiales de esta semana

| | Documento | Qué encontrarás | Dónde y cuánto dura |
|---|---|---|---|
| 1 | **[Teoría](1-TEORIA.md)** | Información y seguridad de la información · Los principios que sostienen el diseño de controles · Roles y responsabilidades en seguridad de la información | Aula · 100 min |
| 2 | **[Dinámica de aula](2-DINAMICA.md)** | El organigrama tóxico, con su material, su ejemplo resuelto y su rúbrica | Aula · dentro de los 100 min de la sesión de teoría |
| 3 | **[Taller de laboratorio](3-TALLER.md)** | Auditoría de identidades, accesos y segregación de funciones con Keycloak | Laboratorio · 100 min |

## Ruta de la semana

```mermaid
flowchart LR
    A["<b>Sesión 1 · Aula</b><br/>Teoría · 100 min"]
    B["<b>Dinámica de aula</b><br/>El organigrama tóxico<br/><i>nota cognitiva</i>"]
    C["<b>Sesión 2 · Laboratorio</b><br/>Auditoría de identidades,<br/>accesos y segregación de<br/>funciones con Keycloak<br/><i>nota procedimental</i>"]
    D["<b>Entregables</b><br/>de la semana 02"]
    A --> B --> C --> D
    classDef aula fill:#E8F1FB,stroke:#16285C,stroke-width:1px,color:#16285C;
    classDef lab fill:#E9F6F2,stroke:#0F766E,stroke-width:1px,color:#0F4C46;
    classDef ent fill:#FDF2E2,stroke:#B45309,stroke-width:1px,color:#7C3E00;
    class A,B aula;
    class C lab;
    class D ent;
```

## Entregables

| Entregable | Formato y nombre del archivo | Vence |
|---|---|---|
| **Dinámica de aula** · El organigrama tóxico | PDF desde la [plantilla de dinámica](../PLANTILLAS/SI084-PLANTILLA-DINAMICA.docx) · `SI084-S02-DINAMICA-Grupo<N>.pdf` | Antes de cerrar la sesión de teoría |
| **Informe del taller de laboratorio N.º 02** | PDF en formato EPIS desde la [plantilla de taller](../PLANTILLAS/SI084-PLANTILLA-TALLER.docx) · `SI084-S02-TALLER-Grupo<N>.pdf` | 48 h después del taller |
| Hallazgos H-002 y H-003 en el repositorio | Commit firmado en Git | 48 h después del laboratorio |

> Ambos se entregan en **PDF**, con la carátula de la UPT y los códigos de todos los integrantes. Las plantillas obligatorias están en [`PLANTILLAS/`](../PLANTILLAS/).

## Cómo se evalúa

| Criterio | Instrumento | Peso |
|---|---|---|
| Cognitivo | Rúbrica del organigrama tóxico + exposición de 10 min en la Semana 03 | 25 % |
| Procedimental | Lista de cotejo de los 7 resultados del laboratorio | 35 % |
| Actitudinal | Participación y cumplimiento de las reglas de seguridad del laboratorio | 15 % |

## Preparación para la Semana 03

- **Leer.** ISO/IEC 27001:2022, cláusulas 6.1.2 y 6.1.3 (apreciación y tratamiento del riesgo).
- **Leer.** ISO/IEC 27005:2022, capítulos sobre identificación y análisis del riesgo.
- Revisar la documentación de **MONARC**. https://www.monarc.lu/
- **Dejar el entorno operativo.** La Semana 03 agrega MONARC y OpenVAS/GVM sobre `audit_net`.

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
