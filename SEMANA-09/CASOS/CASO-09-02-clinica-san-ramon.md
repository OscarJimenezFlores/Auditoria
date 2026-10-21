[Semana 09](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 09·01](CASO-09-01-agroexportadora-valle-viejo.md) · **Caso 09·02** · [Caso 09·03](CASO-09-03-municipalidad-alto-selva.md) · [Encargo 09](../../ENCARGOS-UNIDAD-II/CASO-09-ciclo-de-vida-del-software.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>CLÍNICA SAN RAMÓN S.A.C.</strong><br>
  <em>Solicitud de auditoría · Ciclo de vida del software</em>
</div>

---

# Solicitud de auditoría de el ciclo de vida de nuestro software

| | |
|---|---|
| **Documento** | Solicitud de auditoría de el ciclo de vida de nuestro software |
| **De** | Gerente General, por acuerdo del Directorio, CLÍNICA SAN RAMÓN S.A.C. |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 12 de octubre de 2026 |
| **Clasificación** | CONFIDENCIAL — USO ACADÉMICO |

---

## 1. Quiénes somos

Somos **CLÍNICA SAN RAMÓN S.A.C.**, salud privada · clínica de mediana complejidad, con sede en Cercado de Tacna. Operamos desde hace 23 años, con 214 trabajadores estables y 46 médicos por honorarios. Nuestros ingresos son de S/ 38.9 millones y atendemos tacna y pacientes de Arica, Chile.

Nos regulan o supervisan **SUSALUD · DIRESA Tacna · SUNAT · ANPD (datos de salud) · DIGEMID**.

Nuestra área de tecnologías de la información tiene **4 personas**. La encabeza nuestro coordinador de TI, técnico titulado, 3 años en el puesto, que reporta a Gerencia General. El presupuesto de tecnologías de la información es de **S/ 686 000**, el 1.76 % de nuestros ingresos. El objetivo que le declaramos a esa área es «Eliminar la carga manual entre sistemas clínicos y cumplir la protección reforzada de datos de salud».

**Lo que más nos cuesta.** La integración entre laboratorio y HIS es por archivo plano copiado a mano dos veces al día. En 2025 se detectaron 34 resultados adjuntados al paciente equivocado.

### 1.1. Los sistemas con los que operamos

| Sistema | Qué es | Dónde corre | Desde | ¿Tiene soporte vigente? |
|---|---|---|---|---|
| **HIS — historia clínica electrónica** | Producto peruano, módulos de admisión, consulta, hospitalización y farmacia | Servidor propio en sala de máquinas | 2018 | Sí, soporte por horas |
| **Facturación y convenios con aseguradoras** | Módulo del mismo HIS | Mismo servidor | 2018 | Sí |
| **Laboratorio (LIS)** | Software del proveedor de equipos, integrado por archivos planos | PC de laboratorio | 2020 | Parcial |
| **Imágenes (PACS)** | Servidor de imágenes del proveedor de tomógrafo | Servidor dedicado | 2022 | Sí |
| **Planillas y asistencia** | Sistema local con marcador biométrico | PC de RR. HH. | 2017 | No |

### 1.2. Nuestros procesos

1. Admisión y filiación del paciente
2. Atención ambulatoria y hospitalización
3. Laboratorio e imágenes
4. Farmacia y dispensación
5. Facturación a aseguradoras
6. Gestión de historias clínicas

## 2. Por qué pedimos esta auditoría

Los scripts que cargan los resultados del laboratorio a la historia clínica los escribió un técnico que renunció en 2024. Nadie los había abierto hasta que asignaron 34 resultados a pacientes equivocados. No tenemos repositorio con historia, ni prueba, ni forma de saber qué versión corría ese día.

## 3. Lo que ya sabemos que no está bien

Estos riesgos los tenemos identificados y no los hemos tratado.

- Datos sensibles de salud sin cifrado en reposo
- Integración manual entre sistemas clínicos
- Cuentas de médicos compartidas en consultorios

**Lo que nos pasó en el periodo. Resultados de laboratorio asignados a pacientes equivocados.** El proceso manual de carga del LIS al HIS asignó 34 resultados a historias clínicas incorrectas durante seis semanas. Se detectó por reclamo de un paciente. No existe registro de quién ejecutó cada carga.

## 4. Lo que ya nos dijeron

- Nunca nos han auditado un sistema de información.
- SUSALUD supervisó en 2025 la gestión de historias clínicas, a raíz del reclamo, y nos dejó una medida correctiva sobre el registro de quién accede a la historia. Está abierta.
- La auditoría financiera externa no revisa los sistemas clínicos. Se limita a facturación.

## 5. Lo que queremos saber

Son las preguntas que la dirección espera que la auditoría responda. Cómo responderlas, con qué alcance, con qué criterios y con qué procedimientos, es lo que esperamos de su plan.

1. Saber si los scripts de carga producen resultados exactos, y qué debió haber impedido que asignaran 34 resultados a pacientes equivocados.
2. Saber qué nos exige SUSALUD sobre la integridad de la historia clínica cuando la alimenta software nuestro.
3. Saber cómo se aplicó el ajuste que hicimos después del incidente, de principio a fin, y si se puede repetir.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | El Directorio acordó encargar esta auditoría después del reclamo del paciente, y la Gerencia General la contrata |
| **Contraparte designada** | Nuestro Gerente General, con el Coordinador de TI como enlace técnico |
| **Canal único** | Toda solicitud entra y sale por el correo de la Gerencia General, con copia al Coordinador de TI y al responsable de historias clínicas |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 19 de octubre de 2026. Trabajo de campo del 20 de octubre de 2026 al 9 de noviembre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 10 de noviembre de 2026 y el 16 de noviembre de 2026. Informe entre el 17 de noviembre de 2026 y el 23 de noviembre de 2026 |
| **Horas que financiamos** | Hasta 188 horas de la comisión. Unas 38 de planificación, 113 de trabajo de campo, 15 de comunicación de resultados y 22 de informe. Más que eso no lo pagamos |
| **Horas que podemos dedicarles** | Nuestra área de tecnologías de la información dedica unas 160 horas al mes al proceso que van a auditar, entre sus 4 personas. No pueden pedirle más tiempo que ese |
| **Presupuesto que aprobamos** | S/ 13 630, a tarifa de referencia de S/ 110 la hora de supervisión, S/ 85 la de jefe de comisión y S/ 60 la de integrante, sin viáticos |
| **Confidencialidad** | Todo lo que les entregamos es confidencial. Lo guardan en un repositorio privado, cifrado, con la marca CONFIDENCIAL — USO ACADÉMICO, y al cierre conservan solo lo que el informe cite |
| **Lo que no autorizamos** | Ninguna prueba se ejecuta sobre nuestros sistemas en esta etapa. Lo que pedimos es un plan. Si el plan incluye pruebas, dirá cuáles y nos pedirá autorización escrita antes |
| **Las personas** | En su plan y en su informe nos nombran por el cargo, no por el nombre |

## 7. Lo que les entregamos

Lo que sigue lo entregamos **a solicitud escrita**, indicando para qué lo necesitan y qué procedimiento lo va a usar. Los documentos propios de esta materia van ya como anexos de esta solicitud. Los demás se entregan por el canal único, en la carpeta que indica la tabla.

| Documento | Qué contiene | Dónde está |
|---|---|---|
| `ciclo-de-vida-del-software.md` | El expediente de nuestro software propio, con las métricas del repositorio, los despliegues y los pedidos de cambio del periodo | Anexo 1 |
| `contratos-proveedores.md` | Lo que dicen nuestros contratos sobre la propiedad del código y el soporte | [`documentos/contratos-proveedores.md`](../../../CASOS/EMPRESA-02-clinica-san-ramon/documentos/contratos-proveedores.md) |
| `extracciones-y-registros.md` | Las extracciones del sistema principal y la bitácora que conservamos | [`documentos/extracciones-y-registros.md`](../../../CASOS/EMPRESA-02-clinica-san-ramon/documentos/extracciones-y-registros.md) |
| `narrativa-proceso-compras.md` | Cómo opera el proceso que nuestro software soporta o alimenta | [`documentos/narrativa-proceso-compras.md`](../../../CASOS/EMPRESA-02-clinica-san-ramon/documentos/narrativa-proceso-compras.md) |
| `organigrama-y-accesos.md` | Quién desarrolla, quién despliega y quién aprueba, según los accesos | [`documentos/organigrama-y-accesos.md`](../../../CASOS/EMPRESA-02-clinica-san-ramon/documentos/organigrama-y-accesos.md) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/usuarios_erp.csv` | Los usuarios de nuestro sistema principal, con perfil, último acceso y segundo factor | 143 registros · 143 habilitados · 143 sin segundo factor |
| `datos/pagos.csv` | Nuestros pagos del periodo | 10129 registros · S/ 15 599 828 en total |

Atentamente,

**Gerente General, por acuerdo del Directorio**
CLÍNICA SAN RAMÓN S.A.C.

---

## Anexos

### Anexo 1 · `ciclo-de-vida-del-software.md`

### 1. El sistema desarrollado internamente

| Campo | Contenido |
|---|---|
| Sistema | **Carga de resultados del laboratorio a la historia clínica** |
| Descripción | Scripts desarrollados internamente que convierten los archivos planos del LIS y los cargan en el HIS dos veces al día |
| En producción desde | 2020 |
| Lenguaje y plataforma | Visual Basic para Aplicaciones y SQL Server |
| Personas que lo mantienen hoy | 2 |
| ¿Existe documentación técnica? | Parcial, desactualizada |
| ¿Existe control de versiones? | Sí, repositorio interno |
| ¿Existe ambiente de pruebas separado de producción? | Sí, pero con datos de producción copiados |

> **Contexto que da la organización.** «Los escribió un técnico del área de TI que renunció en 2024. Nadie más los había abierto hasta el incidente. Desde entonces se le hacen ajustes cuando algo falla o cuando el área pide un cambio.»

### 2. Métricas del repositorio

Extraídas con `git log` sobre el periodo auditado.

| Métrica | Valor |
|---|---|
| Commits en el periodo | 121 |
| Autores distintos | 2 |
| Commits del autor principal | 68 % del total |
| Ramas activas | 4 |
| Ramas sin fusionar con más de 90 días | 4 |
| Commits directos a la rama principal | **79 %** |
| Pull Requests abiertos en el periodo | 2 |
| Pull Requests con revisión de un segundo | **1** |
| Etiquetas de versión creadas | 3 |
| Commits con mensaje de una sola palabra | 56 |
| Archivos con más de 1 000 líneas | 6 |
| ¿Hay pruebas automatizadas en el repositorio? | No |

### 3. Últimos despliegues a producción

| Fecha | Versión | Qué se desplegó | ¿Hubo etiqueta? | ¿Hubo prueba previa? | ¿Se pudo revertir? |
|---|---|---|---|---|---|
| 2025-12-08 | — | Corrección de error en reportes | No | No | Sí |
| 2025-05-26 | v1.2 | Cambio de formato de comprobante | Sí | Parcial | Sí |
| 2025-11-16 | — | Corrección urgente en producción | Sí | Parcial | Sí |
| 2025-05-16 | v1.3 | Corrección de error en reportes | Sí | Parcial | Sí |
| 2025-04-14 | — | Corrección de error en reportes | Sí | No | No |
| 2025-08-26 | — | Cambio de formato de comprobante | No | Parcial | Sí |

### 4. Trazabilidad de requisitos

La organización entrega los pedidos de cambio del periodo, tal como los registra.

| N.º | Fecha | Solicitado por | Qué se pidió | ¿Especificación escrita? | ¿Aceptación formal? | ¿Se desplegó? |
|---|---|---|---|---|---|---|
| 01 | 2025-03-18 | Legal | Cambiar el cálculo del descuento | No | No | Sí |
| 02 | 2025-03-26 | Legal | Nuevo reporte mensual | Correo | No | Sí |
| 03 | 2025-02-21 | Gerencia | Corregir el redondeo | No | No | No |
| 04 | 2025-08-07 | Tesorería | Nuevo reporte mensual | No | Verbal | No |
| 05 | 2025-11-12 | Logística | Ampliar el campo de observaciones | Correo | No | Sí |
| 06 | 2025-04-25 | Logística | Bloquear la edición tras el cierre | Correo | No | No |
| 07 | 2025-05-05 | Logística | Corregir el redondeo | No | Verbal | Sí |
| 08 | 2025-05-20 | Logística | Exportar a hoja de cálculo | Correo | No | Sí |

### 5. Lo que la organización responde

| Pregunta | Respuesta |
|---|---|
| ¿Hay un procedimiento de desarrollo documentado? | «No. Se hace según la necesidad» |
| ¿Quién aprueba pasar un cambio a producción? | «El jefe de sistemas, o el mismo que lo hizo si es urgente» |
| ¿Se revisan los cambios entre pares? | «Somos pocos. No da el tiempo» |
| ¿Hay ambiente de pruebas? | «Se prueba en producción fuera de horario» |
| ¿Existe un plan de reversión? | «Si algo sale mal, se restaura el respaldo» |
| ¿Hay pruebas automatizadas? | «No» |
| ¿Qué pasa si el sistema deja de funcionar? | «No hay alternativa. Habría que operar en papel» |

### 6. Marco de referencia

| Norma | Procesos aplicables |
|---|---|
| **NTP-ISO/IEC 12207** | Procesos del ciclo de vida del software: adquisición, desarrollo, mantenimiento, gestión de la configuración, verificación y validación |
| **COBIT 2019 · BAI03** | Gestión de la identificación y construcción de soluciones |
| **COBIT 2019 · BAI06** | Gestión de cambios de TI |
| **COBIT 2019 · BAI07** | Gestión de la aceptación y transición del cambio |
| **ISO/IEC 25010** | Características de calidad del producto software |

---

[Semana 09](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 09·01](CASO-09-01-agroexportadora-valle-viejo.md) · **Caso 09·02** · [Caso 09·03](CASO-09-03-municipalidad-alto-selva.md) · [Encargo 09](../../ENCARGOS-UNIDAD-II/CASO-09-ciclo-de-vida-del-software.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
