[Semana 08](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 08·01](CASO-08-01-agroexportadora-valle-viejo.md) · **Caso 08·02** · [Caso 08·03](CASO-08-03-municipalidad-alto-selva.md) · [Encargo 08](../../ENCARGOS-UNIDAD-II/CASO-08-seguridad-de-la-informacion.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>CLÍNICA SAN RAMÓN S.A.C.</strong><br>
  <em>Solicitud de auditoría · Sistema de gestión de seguridad de la información</em>
</div>

---

# Solicitud de auditoría de nuestro sistema de gestión de seguridad de la información

| | |
|---|---|
| **Documento** | Solicitud de auditoría de nuestro sistema de gestión de seguridad de la información |
| **De** | Gerente General, por acuerdo del Directorio, CLÍNICA SAN RAMÓN S.A.C. |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 5 de octubre de 2026 |
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

Aprobamos nuestra política de seguridad de la información y una declaración de aplicabilidad en la que la gestión de incidentes figura como implementada. El incidente de los 34 resultados mal asignados lo detectamos por el reclamo de un paciente, no por el control que declaramos. SUSALUD nos dejó una medida correctiva sobre el registro de accesos a la historia clínica.

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

1. Saber qué controles declaramos como implementados sin tener más evidencia que una frase, y cuáles son los que protegen datos de salud.
2. Saber cómo tratar en el sistema de gestión a los 46 médicos por honorarios, que usan el sistema clínico y no están en la planilla.
3. Saber bajo qué control de los que declaramos cae la integración manual entre laboratorio e historia clínica, donde ocurrió el incidente.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | El Directorio acordó encargar esta auditoría después del reclamo del paciente, y la Gerencia General la contrata |
| **Contraparte designada** | Nuestro Gerente General, con el Coordinador de TI como enlace técnico |
| **Canal único** | Toda solicitud entra y sale por el correo de la Gerencia General, con copia al Coordinador de TI y al responsable de historias clínicas |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 12 de octubre de 2026. Trabajo de campo del 13 de octubre de 2026 al 2 de noviembre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 3 de noviembre de 2026 y el 9 de noviembre de 2026. Informe entre el 10 de noviembre de 2026 y el 16 de noviembre de 2026 |
| **Horas que financiamos** | Hasta 188 horas de la comisión. Unas 38 de planificación, 113 de trabajo de campo, 15 de comunicación de resultados y 22 de informe. Más que eso no lo pagamos |
| **Horas que podemos dedicarles** | Nuestra área de tecnologías de la información dedica unas 96 horas al mes al proceso que van a auditar, entre sus 4 personas. No pueden pedirle más tiempo que ese |
| **Presupuesto que aprobamos** | S/ 13 630, a tarifa de referencia de S/ 110 la hora de supervisión, S/ 85 la de jefe de comisión y S/ 60 la de integrante, sin viáticos |
| **Confidencialidad** | Todo lo que les entregamos es confidencial. Lo guardan en un repositorio privado, cifrado, con la marca CONFIDENCIAL — USO ACADÉMICO, y al cierre conservan solo lo que el informe cite |
| **Lo que no autorizamos** | Ninguna prueba se ejecuta sobre nuestros sistemas en esta etapa. Lo que pedimos es un plan. Si el plan incluye pruebas, dirá cuáles y nos pedirá autorización escrita antes |
| **Las personas** | En su plan y en su informe nos nombran por el cargo, no por el nombre |

## 7. Lo que les entregamos

Lo que sigue lo entregamos **a solicitud escrita**, indicando para qué lo necesitan y qué procedimiento lo va a usar. Los documentos propios de esta materia van ya como anexos de esta solicitud. Los demás se entregan por el canal único, en la carpeta que indica la tabla.

| Documento | Qué contiene | Dónde está |
|---|---|---|
| `sgsi-politica-y-aplicabilidad.md` | Nuestra política vigente, los roles que declaramos y la declaración de aplicabilidad con el estado de cada control | Anexo 1 |
| `politica-de-respaldo.md` | La política de respaldo que citamos como evidencia del control A.8.13 | Anexo 2 |
| `organigrama-y-accesos.md` | Quién tiene qué acceso en nuestro sistema principal | [`documentos/organigrama-y-accesos.md`](../../../CASOS/EMPRESA-02-clinica-san-ramon/documentos/organigrama-y-accesos.md) |
| `incidente-detallado.md` | El incidente del periodo, ocurrido en un dominio que declaramos implementado | [`documentos/incidente-detallado.md`](../../../CASOS/EMPRESA-02-clinica-san-ramon/documentos/incidente-detallado.md) |
| `datos/bia.csv` | El análisis de impacto al negocio que mantenemos, con tiempos de recuperación por proceso | Anexo 3 y [archivo](../../../CASOS/EMPRESA-02-clinica-san-ramon/datos/bia.csv) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/usuarios_erp.csv` | Los usuarios de nuestro sistema principal, con perfil, último acceso y segundo factor | 143 registros · 143 habilitados · 143 sin segundo factor |
| `datos/empleados.csv` | Nuestra planilla del periodo, con ingresos y ceses | 214 registros · 178 activos · 36 cesados en el periodo |
| `datos/bia.csv` | Nuestro análisis de impacto al negocio | 6 registros |
| `datos/pagos.csv` | Nuestros pagos del periodo | 10129 registros · S/ 15 599 828 en total |

Atentamente,

**Gerente General, por acuerdo del Directorio**
CLÍNICA SAN RAMÓN S.A.C.

---

## Anexos

### Anexo 1 · `sgsi-politica-y-aplicabilidad.md`

### 1. Qué es este documento

La organización aprobó una **política de seguridad de la información** y una primera **declaración de aplicabilidad** de los controles del Anexo A de la NTP-ISO/IEC 27001:2022. Se entregan tal como están, sin actualizar.

No existe certificación ni auditoría externa previa del sistema de gestión de seguridad de la información.

### 2. La política vigente

| Campo | Contenido |
|---|---|
| Documento | «Política de Seguridad de la Información» |
| Versión | 1.0 |
| Aprobada el | 19 de mayo de 2024 |
| Aprobada por | Gerencia General |
| Última revisión | Ninguna desde su aprobación |
| Difusión | Correo masivo el día de la aprobación |
| Acuse de recibo | 9 de 178 trabajadores firmaron el cargo |
| Alcance declarado | «Todos los sistemas de información de la organización» |

**Texto del alcance, transcrito.** *«La presente política aplica a todos los procesos, sistemas, personas y terceros que traten información de la organización, en cualquier soporte y en cualquier ubicación.»*

**Objetivos declarados en la política.**

1. Proteger la confidencialidad, la integridad y la disponibilidad de la información.
2. Cumplir la normativa aplicable a la organización.
3. Asegurar la continuidad de los procesos críticos.
4. Crear conciencia de seguridad en el personal.

### 3. Roles declarados

| Rol de la norma | Designado | Acto que lo designa | Dedicación |
|---|---|---|---|
| Alta dirección | Gerencia General | Acta de aprobación de la política | Propia del cargo |
| Responsable de seguridad de la información | Gabriela Vargas Rivera, Operario | Memorando interno, sin resolución | Parcial, sin horas asignadas |
| Propietarios de los activos de información | «Cada jefe de área» | No hay designación nominal | Sin asignar |
| Comité de seguridad de la información | No constituido | Acta única de instalación | — |

### 4. Declaración de aplicabilidad · extracto

Hoja de cálculo que mantiene TI. Se entrega el extracto de los 27 controles que la organización marcó como aplicables.

| Control del Anexo A 2022 | Aplicable | Estado declarado | Evidencia que la organización dice tener |
|---|---|---|---|
| A.5.1 Políticas de seguridad de la información | Sí | Implementado | La política v1.0 |
| A.5.9 Inventario de información y otros activos asociados | Sí | Parcial | Hoja de cálculo de equipos de TI |
| A.5.10 Uso aceptable de la información y otros activos asociados | Sí | No implementado | — |
| A.5.15 Control de acceso | Sí | Implementado | Matriz de accesos del sistema principal |
| A.5.16 Gestión de la identidad | Sí | Parcial | Altas y bajas por correo |
| A.5.17 Información de autenticación | Sí | Implementado | Política de contraseñas del sistema |
| A.5.18 Derechos de acceso | Sí | Parcial | Revisión «cuando se solicita» |
| A.5.19 Seguridad de la información en las relaciones con los proveedores | Sí | No implementado | — |
| A.5.23 Seguridad de la información para el uso de servicios en la nube | Sí | No implementado | — |
| A.5.24 Planificación y preparación de la gestión de incidentes | Sí | Parcial | Correo del incidente del periodo |
| A.5.30 Preparación de las TIC para la continuidad del negocio | Sí | No implementado | — |
| A.5.31 Requisitos legales, estatutarios, reglamentarios y contractuales | Sí | Parcial | Lista de normas del área legal |
| A.5.34 Privacidad y protección de la información de identificación personal | Sí | No implementado | — |
| A.5.37 Procedimientos operativos documentados | Sí | Parcial | Manual del sistema principal |
| A.6.3 Concienciación, educación y formación en seguridad de la información | Sí | No implementado | — |
| A.8.2 Derechos de acceso privilegiado | Sí | Parcial | «Solo TI tiene administrador» |
| A.8.5 Autenticación segura | Sí | Parcial | Usuario y contraseña |
| A.8.7 Protección contra el malware | Sí | Implementado | Consola del antivirus corporativo |
| A.8.9 Gestión de la configuración | Sí | No implementado | — |
| A.8.12 Prevención de fuga de datos | No | Excluido | «No aplica a nuestro tamaño» |
| A.8.13 Respaldo de la información | Sí | Implementado | La política de respaldo |
| A.8.15 Registro de actividad | Sí | Parcial | Bitácora del sistema principal |
| A.8.16 Actividades de seguimiento | Sí | No implementado | — |
| A.8.24 Uso de criptografía | Sí | Parcial | Certificado del portal |
| A.8.28 Codificación segura | No | Excluido | «No desarrollamos software» |
| A.8.31 Separación de los entornos de desarrollo, prueba y producción | No | Excluido | «Un solo entorno» |
| A.8.32 Gestión de cambios | Sí | Parcial | Correo de autorización del jefe de TI |

> **Las tres exclusiones están escritas tal como las redactó la organización.** La norma exige justificar cada exclusión del Anexo A, y la justificación tiene que sostenerse en el contexto real de la organización.

### 5. Gestión del riesgo de seguridad de la información

| Pregunta | Respuesta de la organización |
|---|---|
| ¿Existe metodología de apreciación del riesgo? | «Se usa la matriz de probabilidad por impacto de Administración» |
| ¿Hay criterios de aceptación del riesgo aprobados? | «No» |
| ¿Hay plan de tratamiento del riesgo? | «Está en el registro de riesgos» |
| ¿Quién aprueba el riesgo residual? | «Gerencia, cuando se le presenta» |
| ¿Se ha hecho auditoría interna del sistema de gestión? | «No» |
| ¿Se ha hecho revisión por la dirección? | «No formalmente» |

### 6. Formación y concienciación

| Actividad | Fecha | Asistentes | Evidencia |
|---|---|---|---|
| Charla de inducción en seguridad | 9 de setiembre de 2024 | 17 | Lista de asistencia en papel |
| Campaña de contraseñas seguras | 9 de junio de 2025 | No se registró | Afiche en el comedor |
| Simulacro de phishing | Nunca | — | — |
| Capacitación del responsable de seguridad | Nunca | — | — |

### 7. Lo que la organización responde

| Pregunta del auditor | Respuesta |
|---|---|
| ¿La política se revisó desde su aprobación? | «No, no ha habido cambios que lo ameriten» |
| ¿Cómo se verifica que el personal la conoce? | «Se envió por correo a todos» |
| ¿Quién mantiene la declaración de aplicabilidad? | «TI, cuando hay tiempo» |
| ¿Cuántos usuarios tienen segundo factor de autenticación? | «Los del sistema principal, creo» |
| ¿Hay indicadores del sistema de gestión? | «No» |

**Dato del sistema principal, extraído por TI a solicitud del equipo.** De 143 usuarios habilitados, **143 no tienen segundo factor de autenticación**.

### 8. Marco aplicable

| Norma | Qué exige |
|---|---|
| **NTP-ISO/IEC 27001:2022**, cláusula 4 | Determinar el contexto, las partes interesadas y el alcance del sistema de gestión |
| **NTP-ISO/IEC 27001:2022**, cláusula 5 | Liderazgo, política y asignación de roles con responsabilidad y autoridad |
| **NTP-ISO/IEC 27001:2022**, cláusula 6.1.3 | Declaración de aplicabilidad con la justificación de inclusiones y exclusiones |
| **NTP-ISO/IEC 27001:2022**, cláusula 9.2 | Auditoría interna del sistema de gestión, con programa y criterios |
| **NTP-ISO/IEC 27001:2022**, cláusula 9.3 | Revisión por la dirección, con sus entradas y salidas |
| **NTP-ISO/IEC 27002:2022** | Guía de implementación de cada control del Anexo A |
| **ISO 19011:2018**, cláusula 6 | Cómo se planifica y se ejecuta la auditoría de un sistema de gestión |

### Anexo 2 · `politica-de-respaldo.md`

### Ficha del documento

| Campo | Contenido |
|---|---|
| Código | POL-TI-016 |
| Versión | 1.0 |
| Fecha de aprobación | 3 de noviembre de 2023 |
| Aprobado por | Gerencia de Administración y Finanzas |
| Próxima revisión programada | 21 de enero de 2024 |
| ¿Se ha revisado? | **No** |
| ¿Se difundió al personal? | «Se envió por correo» |

### 1. Objetivo

Establecer los lineamientos para la generación, custodia y recuperación de las copias de seguridad de la información de la organización.

### 2. Alcance

Aplica a todos los sistemas de información de la organización.

### 3. Lineamientos

**3.1.** Se realizará una copia de seguridad **completa semanal** y copias **incrementales diarias** de todos los sistemas críticos.

**3.2.** Las copias se conservarán por un periodo mínimo de **doce meses**.

**3.3.** Se mantendrá **una copia fuera de las instalaciones** de la organización.

**3.4.** Se realizará una **prueba de restauración trimestral**, dejando constancia de su resultado.

**3.5.** El responsable de Tecnologías de la Información verificará **diariamente** la ejecución correcta de las copias.

**3.6.** Los medios de respaldo se **cifrarán** y su acceso se restringirá al personal autorizado.

**3.7.** Se mantendrá un **registro de las restauraciones** solicitadas y ejecutadas.

**3.8.** Los tiempos objetivo de recuperación se definirán en el **análisis de impacto al negocio**, que se actualizará anualmente.

### 4. Responsables

| Rol | Responsabilidad |
|---|---|
| Jefe de Tecnologías de la Información | Ejecución, verificación y custodia |
| Gerencia de Administración y Finanzas | Aprobación y provisión de recursos |
| Usuarios | Guardar la información en las unidades de red establecidas |

---

### 5. Análisis de impacto al negocio vigente

Elaborado por un practicante en diciembre de 2024. No fue revisado ni aprobado. Se entrega tal como está.

| ID | Proceso | Criticidad | RTO (h) | RPO (h) | Sistema de soporte | Responsable | Impacto a 24 h | Última prueba |
|---|---|---|---|---|---|---|---|---|
| BIA01 | Admisión y filiación del paciente | Media | 4 | 28 | HIS — historia clínica electrónica | Ana Apaza Cáceres | Medio | **Nunca** |
| BIA02 | Atención ambulatoria y hospitalización | Alta | 72 | 8 | HIS — historia clínica electrónica | Ricardo Rivera Rivera | Alto | 2025-10-22 |
| BIA03 | Laboratorio e imágenes | Alta | 24 | 1 | Laboratorio (LIS) | Álvaro Maquera Ancco | Medio | **Nunca** |
| BIA04 | Farmacia y dispensación | Media | 8 | 24 | HIS — historia clínica electrónica | Raúl Rivera Calisaya | Medio | **Nunca** |
| BIA05 | Facturación a aseguradoras | Media | 8 | 8 | Facturación y convenios con aseguradoras | Teresa Ramos Aguilar | Bajo | 2025-11-10 |
| BIA06 | Gestión de historias clínicas | Alta | 4 | 24 | HIS — historia clínica electrónica | Gabriela Maquera Yufra | Alto | **Nunca** |

> El archivo original está en [`datos/bia.csv`](../../../CASOS/EMPRESA-02-clinica-san-ramon/datos/bia.csv).

### 6. Lo que la organización responde

| Pregunta | Respuesta |
|---|---|
| ¿Se cumple la prueba de restauración trimestral del punto 3.4? | «No se ha hecho. Se asume que el respaldo funciona porque termina sin error» |
| ¿Dónde está la copia fuera de las instalaciones del punto 3.3? | «El jefe de sistemas se lleva un disco los viernes» |
| ¿Los medios están cifrados, como pide el 3.6? | «El disco no. El respaldo en nube sí, según el proveedor» |
| ¿Existe el registro de restauraciones del punto 3.7? | «No se lleva» |
| ¿El BIA se actualiza anualmente, como pide el 3.8? | «Es el único que tenemos» |
| ¿Quién definió los RTO y RPO de la tabla? | «El practicante los propuso. Nadie los validó con las áreas» |
| ¿Existe un plan de continuidad del negocio? | «No» |

### Anexo 3 · `datos/bia.csv`

El análisis de impacto al negocio que mantenemos, con tiempos de recuperación por proceso.

| Proceso | Criticidad | RTO (h) | RPO (h) | Sistema de soporte | Impacto a 24 h | Última prueba |
|---|---|---|---|---|---|---|
| BIA01 · Admisión y filiación del paciente | Media | 4 | 28 | HIS — historia clínica electrónica | Medio | Nunca |
| BIA02 · Atención ambulatoria y hospitalización | Alta | 72 | 8 | HIS — historia clínica electrónica | Alto | 2025-10-22 |
| BIA03 · Laboratorio e imágenes | Alta | 24 | 1 | Laboratorio (LIS) | Medio | Nunca |
| BIA04 · Farmacia y dispensación | Media | 8 | 24 | HIS — historia clínica electrónica | Medio | Nunca |
| BIA05 · Facturación a aseguradoras | Media | 8 | 8 | Facturación y convenios con aseguradoras | Bajo | 2025-11-10 |
| BIA06 · Gestión de historias clínicas | Alta | 4 | 24 | HIS — historia clínica electrónica | Alto | Nunca |

---

[Semana 08](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 08·01](CASO-08-01-agroexportadora-valle-viejo.md) · **Caso 08·02** · [Caso 08·03](CASO-08-03-municipalidad-alto-selva.md) · [Encargo 08](../../ENCARGOS-UNIDAD-II/CASO-08-seguridad-de-la-informacion.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
