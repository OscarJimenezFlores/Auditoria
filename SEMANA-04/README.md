<div align="center">
  <img src="../Logos/logo_universidad.png" alt="Universidad Privada de Tacna" height="62">
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="../Logos/logo_escuela_sistemas.jpeg" alt="Escuela Profesional de Ingeniería de Sistemas" height="62">
</div>

<p align="center">
  <strong>Universidad Privada de Tacna</strong><br>
  Facultad de Ingeniería · Escuela Profesional de Ingeniería de Sistemas
</p>

<h1 align="center">Semana 04 · Controles de Auditoría de Aplicación, Físicos, Lógicos y de Calidad · La Ley SOX en el Perú</h1>

<p align="center">
  <strong>SI-084 · Auditoría de Sistemas</strong><br>
  4 horas académicas de 50 min · 100 min de teoría con la dinámica incluida en aula · 100 min de taller en laboratorio
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
| **Semana** | 04 de 17 |
| **Duración** | 4 horas académicas de 50 min · 100 min de teoría con la dinámica incluida en aula · 100 min de taller en laboratorio |
| **Resultados de aprendizaje** | **RA1** Analiza e interpreta los conceptos y terminología de Auditoría de Sistemas · **RA2** Evalúa la seguridad de la información en Auditoría de Sistemas |
| **Atributos del graduado** | AG-I02 Ética (CD3, nivel 4) · AG-I11 Uso de Herramientas (CD1 y CD2, nivel 4) |

## Materiales de esta semana

| | Documento | Qué encontrarás | Dónde y cuánto dura |
|---|---|---|---|
| 1 | **[Teoría](1-TEORIA.md)** | Taxonomía de los controles de auditoría · Controles generales de TI · Controles de aplicación sobre el ciclo del dato | Aula · 100 min |
| 2 | **[Dinámica de aula](2-DINAMICA.md)** | El control que no se puede creer, con su material, su ejemplo resuelto y su rúbrica | Aula · dentro de los 100 min de la sesión de teoría |
| 3 | **[Taller de laboratorio](3-TALLER.md)** | Auditoría de configuración segura con Lynis, OpenSCAP, Docker Bench y Trivy | Laboratorio · 100 min |

## Ruta de la semana

```mermaid
flowchart LR
    A["<b>Sesión 1 · Aula</b><br/>Teoría · 100 min"]
    B["<b>Dinámica de aula</b><br/>El control que no se puede<br/>creer<br/><i>nota cognitiva</i>"]
    C["<b>Sesión 2 · Laboratorio</b><br/>Auditoría de configuración<br/>segura con Lynis, OpenSCAP,<br/>Docker Bench y Trivy<br/><i>nota procedimental</i>"]
    D["<b>Entregables</b><br/>de la semana 04"]
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
| **Dinámica de aula** · El control que no se puede creer | PDF desde la [plantilla de dinámica](../PLANTILLAS/SI084-PLANTILLA-DINAMICA.docx) · `SI084-S04-DINAMICA-Grupo<N>.pdf` | Hasta 24 h después de la sesión de teoría |
| **Informe del taller de laboratorio N.º 04** | PDF en formato EPIS desde la [plantilla de taller](../PLANTILLAS/SI084-PLANTILLA-TALLER.docx) · `SI084-S04-TALLER-Grupo<N>.pdf` | 48 h después del taller |
| Matriz de control consolidada en el repositorio | Commit en Git | 48 h después del laboratorio |

> Ambos se entregan en **PDF**, con la carátula de la UPT y los códigos de todos los integrantes. Las plantillas obligatorias están en [`PLANTILLAS/`](../PLANTILLAS/).

## Cómo se evalúa

| Criterio | Instrumento | Peso |
|---|---|---|
| Cognitivo | Rúbrica de la matriz riesgo-control + exposición de 10 min en la Semana 05 | 25 % |
| Procedimental | Lista de cotejo de los 8 resultados del laboratorio | 35 % |
| Actitudinal | Manejo responsable de los reportes clasificados como Confidencial | 15 % |

## Preparación para la Semana 05

- **Leer.** Piattini y Del Peso, capítulos de auditoría de la explotación, del desarrollo y de las redes.
- **Revisar.** OWASP (*Open Worldwide Application Security Project*) Web Security Testing Guide (https://owasp.org/www-project-web-security-testing-guide/) y la documentación de Wazuh (https://documentation.wazuh.com/).
- **Mantener el entorno operativo.** La Semana 05 audita las aplicaciones y la infraestructura del laboratorio.

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
