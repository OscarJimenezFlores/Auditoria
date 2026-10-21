[Semana 08](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 08·07](CASO-08-07-instituto-vertiente-sur.md) · **Caso 08·08** · [Caso 08·09](CASO-08-09-servicios-mineros-cordillera.md) · [Encargo 08](../../ENCARGOS-UNIDAD-II/CASO-08-seguridad-de-la-informacion.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>EPS AGUAS DEL SUR S.A.</strong><br>
  <em>Solicitud de auditoría · Sistema de gestión de seguridad de la información</em>
</div>

---

# Solicitud de auditoría de nuestro sistema de gestión de seguridad de la información

| | |
|---|---|
| **Documento** | Solicitud de auditoría de nuestro sistema de gestión de seguridad de la información |
| **De** | Gerente General, EPS AGUAS DEL SUR S.A. |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 5 de octubre de 2026 |
| **Clasificación** | CONFIDENCIAL — USO ACADÉMICO |

---

## 1. Quiénes somos

Somos **EPS AGUAS DEL SUR S.A.**, servicio de agua potable y alcantarillado, con sede en Tacna. Funcionamos desde hace 44 años, con 312 trabajadores estables y 58 por servicios. Nuestro presupuesto institucional es de S/ 74.1 millones y atendemos 86 000 conexiones domiciliarias.

Nos regulan o supervisan **SUNASS · OTASS · ANA · Contraloría General · PCM-SGTD · ANPD**. Somos una entidad pública, sujeta al gobierno digital y al control gubernamental.

Nuestra área de tecnologías de la información tiene **6 personas**. La encabeza nuestro jefe del Departamento de Tecnologías de la Información, que reporta a Gerencia de Administración. El presupuesto de tecnologías de la información es de **S/ 1 080 000**, el 1.46 % de nuestros ingresos. El objetivo que le declaramos a esa área es «Segmentar la red industrial y dar trazabilidad al ciclo comercial ante el regulador».

**Lo que más nos cuesta.** La red del SCADA de plantas comparte switches con la red administrativa desde una ampliación hecha en 2023, pese a que el diseño original las separaba.

### 1.1. Los sistemas con los que operamos

| Sistema | Qué es | Dónde corre | Desde | ¿Tiene soporte vigente? |
|---|---|---|---|---|
| **Sistema comercial** | Producto del sector saneamiento: catastro, facturación y cobranza | Servidor propio | 2014 | Sí |
| **SCADA de plantas y reservorios** | Sistema del proveedor de automatización | Red industrial separada | 2019 | Sí |
| **Micromedición y lectura** | Terminales portátiles del proveedor | Mixto | 2018 | Sí |
| **SIAF y patrimonio** | Sistemas del MEF | Cliente local | 2010 | MEF |
| **Atención de reclamos** | Formulario web y hoja de cálculo | Hosting propio | 2021 | No |

### 1.2. Nuestros procesos

1. Catastro comercial de usuarios
2. Lectura de medidores y facturación
3. Cobranza y corte/reconexión
4. Atención de reclamos comerciales
5. Operación de plantas y redes
6. Contrataciones y presupuesto público

## 2. Por qué pedimos esta auditoría

Aprobamos nuestra política de seguridad de la información y declaramos implementada la gestión de la configuración de redes. La red del SCADA comparte switches con la red administrativa desde 2023. El Órgano de Control Institucional nos recomendó segmentarla y no lo hemos hecho. Queremos auditar nuestra declaración contra la realidad antes de que lo haga el regulador.

## 3. Lo que ya sabemos que no está bien

Estos riesgos los tenemos identificados y no los hemos tratado.

- Red industrial (SCADA) sin segmentación efectiva
- Sin trazabilidad del proceso de carga de lecturas
- **Doble marco.** Gobierno digital y regulación sectorial, ninguno cubierto por completo

**Lo que nos pasó en el periodo. Reclamo masivo por facturación estimada.** Un fallo en la carga de lecturas dejó tres ciclos de facturación estimados para 11 200 conexiones. SUNASS abrió procedimiento. No se pudo determinar qué lote de lecturas falló porque el sistema no conserva el archivo de carga original.

## 4. Lo que ya nos dijeron

- El Órgano de Control Institucional nos emitió en 2025 un informe sobre el proceso de facturación estimada, con dos recomendaciones. Conservar los archivos de carga de lecturas y segmentar la red del SCADA. Ambas abiertas.
- SUNASS tiene abierto un procedimiento por los tres ciclos de facturación estimada a 11 200 conexiones.
- OTASS evaluó nuestra gestión en 2025 y registró la ausencia de un Plan de Gobierno Digital.

## 5. Lo que queremos saber

Son las preguntas que la dirección espera que la auditoría responda. Cómo responderlas, con qué alcance, con qué criterios y con qué procedimientos, es lo que esperamos de su plan.

1. Saber si la red del SCADA debe estar dentro de nuestro sistema de gestión y qué controles le aplican.
2. Saber qué nos exige la Secretaría de Gobierno y Transformación Digital además de la norma, como entidad pública.
3. Saber qué podemos demostrar del incidente de la carga de lecturas, si el archivo que lo originó ya no existe.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | Pedimos este servicio de control al Órgano de Control Institucional, con conocimiento del Directorio y de OTASS |
| **Contraparte designada** | Nuestro Gerente de Administración, de quien depende el Departamento de Tecnologías de la Información |
| **Canal único** | Toda solicitud entra y sale por la mesa de partes institucional y el correo del Órgano de Control Institucional, con número de expediente por cada solicitud |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 12 de octubre de 2026. Trabajo de campo del 13 de octubre de 2026 al 2 de noviembre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 3 de noviembre de 2026 y el 9 de noviembre de 2026. Informe entre el 10 de noviembre de 2026 y el 16 de noviembre de 2026 |
| **Horas que financiamos** | Hasta 222 horas de la comisión. Unas 44 de planificación, 133 de trabajo de campo, 18 de comunicación de resultados y 27 de informe. Más que eso no lo pagamos |
| **Horas que podemos dedicarles** | Nuestra área de tecnologías de la información dedica unas 144 horas al mes al proceso que van a auditar, entre sus 6 personas. No pueden pedirle más tiempo que ese |
| **Presupuesto que aprobamos** | S/ 16 095, a tarifa de referencia de S/ 110 la hora de supervisión, S/ 85 la de jefe de comisión y S/ 60 la de integrante, sin viáticos |
| **Confidencialidad** | Todo lo que les entregamos es confidencial. Lo guardan en un repositorio privado, cifrado, con la marca CONFIDENCIAL — USO ACADÉMICO, y al cierre conservan solo lo que el informe cite |
| **Lo que no autorizamos** | Ninguna prueba se ejecuta sobre nuestros sistemas en esta etapa. Lo que pedimos es un plan. Si el plan incluye pruebas, dirá cuáles y nos pedirá autorización escrita antes |
| **Las personas** | En su plan y en su informe nos nombran por el cargo, no por el nombre |

## 7. Lo que les entregamos

Lo que sigue lo entregamos **a solicitud escrita**, indicando para qué lo necesitan y qué procedimiento lo va a usar. Los documentos propios de esta materia van ya como anexos de esta solicitud. Los demás se entregan por el canal único, en la carpeta que indica la tabla.

| Documento | Qué contiene | Dónde está |
|---|---|---|
| `sgsi-politica-y-aplicabilidad.md` | Nuestra política vigente, los roles que declaramos y la declaración de aplicabilidad con el estado de cada control | Anexo 1 |
| `politica-de-respaldo.md` | La política de respaldo que citamos como evidencia del control A.8.13 | Anexo 2 |
| `organigrama-y-accesos.md` | Quién tiene qué acceso en nuestro sistema principal | [`documentos/organigrama-y-accesos.md`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/documentos/organigrama-y-accesos.md) |
| `incidente-detallado.md` | El incidente del periodo, ocurrido en un dominio que declaramos implementado | [`documentos/incidente-detallado.md`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/documentos/incidente-detallado.md) |
| `datos/bia.csv` | El análisis de impacto al negocio que mantenemos, con tiempos de recuperación por proceso | Anexo 3 y [archivo](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/datos/bia.csv) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/usuarios_erp.csv` | Los usuarios de nuestro sistema principal, con perfil, último acceso y segundo factor | 199 registros · 199 habilitados · 199 sin segundo factor |
| `datos/empleados.csv` | Nuestra planilla del periodo, con ingresos y ceses | 312 registros · 264 activos · 48 cesados en el periodo |
| `datos/bia.csv` | Nuestro análisis de impacto al negocio | 6 registros |
| `datos/pagos.csv` | Nuestros pagos del periodo | 19281 registros · S/ 28 844 992 en total |

Atentamente,

**Gerente General**
EPS AGUAS DEL SUR S.A.

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
| Aprobada el | 11 de agosto de 2024 |
| Aprobada por | Gerencia General |
| Última revisión | Ninguna desde su aprobación |
| Difusión | Correo masivo el día de la aprobación |
| Acuse de recibo | 34 de 264 trabajadores firmaron el cargo |
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
| Responsable de seguridad de la información | Ricardo Nina Mamani, Analista | Resolución de Gerencia General | Parcial, sin horas asignadas |
| Propietarios de los activos de información | «Cada jefe de área» | No hay designación nominal | Sin asignar |
| Comité de seguridad de la información | Constituido en el papel | — | — |

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
| Charla de inducción en seguridad | 27 de mayo de 2024 | 12 | Lista de asistencia en papel |
| Campaña de contraseñas seguras | 3 de abril de 2025 | No se registró | Afiche en el comedor |
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

**Dato del sistema principal, extraído por TI a solicitud del equipo.** De 199 usuarios habilitados, **199 no tienen segundo factor de autenticación**.

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
| **D. Leg. 1412 y D. S. 029-2021-PCM** | Seguridad de la información exigible a la entidad pública |

### Anexo 2 · `politica-de-respaldo.md`

### Ficha del documento

| Campo | Contenido |
|---|---|
| Código | POL-TI-016 |
| Versión | 1.0 |
| Fecha de aprobación | 12 de junio de 2023 |
| Aprobado por | Gerencia de Administración y Finanzas |
| Próxima revisión programada | 7 de junio de 2024 |
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

Elaborado por un practicante en marzo de 2024. No fue revisado ni aprobado. Se entrega tal como está.

| ID | Proceso | Criticidad | RTO (h) | RPO (h) | Sistema de soporte | Responsable | Impacto a 24 h | Última prueba |
|---|---|---|---|---|---|---|---|---|
| BIA01 | Catastro comercial de usuarios | Alta | 12 | 36 | Sistema comercial | Julio Bravo Colque | Alto | 2025-05-17 |
| BIA02 | Lectura de medidores y facturación | Alta | 72 | 8 | Micromedición y lectura | Paola Copaja Ticona | Medio | 2025-07-13 |
| BIA03 | Cobranza y corte/reconexión | Alta | 48 | 1 | Sistema comercial | Nadia Peralta Zapana | Medio | **Nunca** |
| BIA04 | Atención de reclamos comerciales | Alta | 4 | 48 | Atención de reclamos | Julio Calisaya Núñez | Alto | 2025-12-07 |
| BIA05 | Operación de plantas y redes | Alta | 2 | 48 | SCADA de plantas y reservorios | Lucía Zapana Ilaquita | Alto | **Nunca** |
| BIA06 | Contrataciones y presupuesto público | Alta | 2 | 48 | SIAF y patrimonio | Víctor Aguilar Cáceres | Bajo | **Nunca** |

> El archivo original está en [`datos/bia.csv`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/datos/bia.csv).

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
| BIA01 · Catastro comercial de usuarios | Alta | 12 | 36 | Sistema comercial | Alto | 2025-05-17 |
| BIA02 · Lectura de medidores y facturación | Alta | 72 | 8 | Micromedición y lectura | Medio | 2025-07-13 |
| BIA03 · Cobranza y corte/reconexión | Alta | 48 | 1 | Sistema comercial | Medio | Nunca |
| BIA04 · Atención de reclamos comerciales | Alta | 4 | 48 | Atención de reclamos | Alto | 2025-12-07 |
| BIA05 · Operación de plantas y redes | Alta | 2 | 48 | SCADA de plantas y reservorios | Alto | Nunca |
| BIA06 · Contrataciones y presupuesto público | Alta | 2 | 48 | SIAF y patrimonio | Bajo | Nunca |

---

[Semana 08](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 08·07](CASO-08-07-instituto-vertiente-sur.md) · **Caso 08·08** · [Caso 08·09](CASO-08-09-servicios-mineros-cordillera.md) · [Encargo 08](../../ENCARGOS-UNIDAD-II/CASO-08-seguridad-de-la-informacion.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
