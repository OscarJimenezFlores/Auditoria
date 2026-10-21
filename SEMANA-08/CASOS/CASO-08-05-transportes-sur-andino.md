[Semana 08](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 08·04](CASO-08-04-coopac-frontera-sur.md) · **Caso 08·05** · [Caso 08·06](CASO-08-06-distribuidora-andina-sur.md) · [Encargo 08](../../ENCARGOS-UNIDAD-II/CASO-08-seguridad-de-la-informacion.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>TRANSPORTES SUR ANDINO S.A.</strong><br>
  <em>Solicitud de auditoría · Sistema de gestión de seguridad de la información</em>
</div>

---

# Solicitud de auditoría de nuestro sistema de gestión de seguridad de la información

| | |
|---|---|
| **Documento** | Solicitud de auditoría de nuestro sistema de gestión de seguridad de la información |
| **De** | Gerente General, por encargo del Directorio, TRANSPORTES SUR ANDINO S.A. |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 5 de octubre de 2026 |
| **Clasificación** | CONFIDENCIAL — USO ACADÉMICO |

---

## 1. Quiénes somos

Somos **TRANSPORTES SUR ANDINO S.A.**, transporte terrestre de pasajeros interprovincial, con sede en Tacna, con terminales en Moquegua, Arequipa y Puno. Operamos desde hace 27 años, con 268 trabajadores estables y Conductores en régimen mixto. Nuestros ingresos son de S/ 52.6 millones y atendemos corredor sur. Tacna–Arequipa–Puno–Cusco.

Nos regulan o supervisan **MTC · SUTRAN · SUNAT · ANPD · SUNAFIL**.

Nuestra área de tecnologías de la información tiene **4 personas**. La encabeza nuestro jefe de Sistemas, que reporta a Gerencia de Operaciones, no a Gerencia General. El presupuesto de tecnologías de la información es de **S/ 598 000**, el 1.14 % de nuestros ingresos. El objetivo que le declaramos a esa área es «Recuperar el control del canal en línea e integrar la operación de venta, embarque y flota».

**Lo que más nos cuesta.** El control de horas de conducción y descanso —exigible por SUTRAN— se lleva en Excel y no cruza con el GPS. Una fiscalización de 2025 detectó inconsistencias en 23 manifiestos.

### 1.1. Los sistemas con los que operamos

| Sistema | Qué es | Dónde corre | Desde | ¿Tiene soporte vigente? |
|---|---|---|---|---|
| **Venta de pasajes y manifiesto** | Producto del rubro, terminales en counter | Servidor central en Tacna | 2016 | Sí |
| **Venta en línea y app de pasajeros** | Desarrollo tercerizado en 2021 | Nube pública | 2021 | Contrato vencido |
| **GPS y control de flota** | Servicio del proveedor de rastreo | SaaS | 2019 | Sí |
| **Mantenimiento de unidades** | Hojas de cálculo compartidas | Drive corporativo | 2018 | No |
| **Planillas y control de descanso de conductores** | Sistema local | PC de RR. HH. | 2017 | No |

### 1.2. Nuestros procesos

1. Programación de flota y rutas
2. Venta de pasajes en counter y en línea
3. Embarque y manifiesto de pasajeros
4. Mantenimiento de unidades
5. Control de conductores y descansos
6. Encomiendas y carga

## 2. Por qué pedimos esta auditoría

Nuestra política de seguridad de la información se aprobó en 2024 y declara como implementado el control sobre proveedores. El canal en línea, con datos de pasajeros, opera con un proveedor cuyo contrato venció. La venta duplicada de 78 asientos se produjo en un dominio que la declaración considera cubierto. Queremos saber qué vale nuestra declaración.

## 3. Lo que ya sabemos que no está bien

Estos riesgos los tenemos identificados y no los hemos tratado.

- Sistema en línea sin proveedor ni código fuente en poder de la empresa
- Datos personales de pasajeros en un servicio sin contrato vigente
- Sin control automatizado de jornada de conductores

**Lo que nos pasó en el periodo. Venta duplicada de asientos en feriado largo.** El sistema de venta en línea y el de counter no comparten bloqueo de asiento. En el feriado de julio de 2025 se vendieron 78 asientos duplicados. Se resolvió con reembolsos y una crisis en terminal. El proveedor del sistema en línea no responde desde marzo.

## 4. Lo que ya nos dijeron

- SUTRAN fiscalizó en 2025 el control de horas de conducción y encontró inconsistencias en 23 manifiestos. El procedimiento sancionador está en curso.
- Nunca nos han auditado el área de sistemas. El incidente de los 78 asientos duplicados lo resolvimos con reembolsos y no produjo ninguna revisión.
- La auditoría financiera externa observó en 2025 que la venta en línea no concilia con la contabilidad de forma automática.

## 5. Lo que queremos saber

Son las preguntas que la dirección espera que la auditoría responda. Cómo responderlas, con qué alcance, con qué criterios y con qué procedimientos, es lo que esperamos de su plan.

1. Saber qué podemos probar sobre la seguridad de los datos de pasajeros si el proveedor del canal en línea no tiene contrato vigente.
2. Saber si los usuarios de los counters de nuestras cuatro terminales en tres regiones corresponden a personal activo.
3. Saber si el libro de cálculo con el que controlamos los descansos de conductores debe estar dentro del sistema de gestión.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | El Directorio lo pidió después de la fiscalización de SUTRAN y la Gerencia General contrata el servicio |
| **Contraparte designada** | Nuestro Gerente de Operaciones, de quien depende el Jefe de Sistemas |
| **Canal único** | Toda solicitud entra y sale por el correo de la Gerencia de Operaciones, con copia al Jefe de Sistemas |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 12 de octubre de 2026. Trabajo de campo del 13 de octubre de 2026 al 2 de noviembre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 3 de noviembre de 2026 y el 9 de noviembre de 2026. Informe entre el 10 de noviembre de 2026 y el 16 de noviembre de 2026 |
| **Horas que financiamos** | Hasta 193 horas de la comisión. Unas 39 de planificación, 116 de trabajo de campo, 15 de comunicación de resultados y 23 de informe. Más que eso no lo pagamos |
| **Horas que podemos dedicarles** | Nuestra área de tecnologías de la información dedica unas 96 horas al mes al proceso que van a auditar, entre sus 4 personas. No pueden pedirle más tiempo que ese |
| **Presupuesto que aprobamos** | S/ 13 992, a tarifa de referencia de S/ 110 la hora de supervisión, S/ 85 la de jefe de comisión y S/ 60 la de integrante, sin viáticos. Si necesitan ir a nuestras sedes fuera de Tacna, los pasajes y viáticos se presupuestan aparte |
| **Confidencialidad** | Todo lo que les entregamos es confidencial. Lo guardan en un repositorio privado, cifrado, con la marca CONFIDENCIAL — USO ACADÉMICO, y al cierre conservan solo lo que el informe cite |
| **Lo que no autorizamos** | Ninguna prueba se ejecuta sobre nuestros sistemas en esta etapa. Lo que pedimos es un plan. Si el plan incluye pruebas, dirá cuáles y nos pedirá autorización escrita antes |
| **Las personas** | En su plan y en su informe nos nombran por el cargo, no por el nombre |

## 7. Lo que les entregamos

Lo que sigue lo entregamos **a solicitud escrita**, indicando para qué lo necesitan y qué procedimiento lo va a usar. Los documentos propios de esta materia van ya como anexos de esta solicitud. Los demás se entregan por el canal único, en la carpeta que indica la tabla.

| Documento | Qué contiene | Dónde está |
|---|---|---|
| `sgsi-politica-y-aplicabilidad.md` | Nuestra política vigente, los roles que declaramos y la declaración de aplicabilidad con el estado de cada control | Anexo 1 |
| `politica-de-respaldo.md` | La política de respaldo que citamos como evidencia del control A.8.13 | Anexo 2 |
| `organigrama-y-accesos.md` | Quién tiene qué acceso en nuestro sistema principal | [`documentos/organigrama-y-accesos.md`](../../../CASOS/EMPRESA-05-transportes-sur-andino/documentos/organigrama-y-accesos.md) |
| `incidente-detallado.md` | El incidente del periodo, ocurrido en un dominio que declaramos implementado | [`documentos/incidente-detallado.md`](../../../CASOS/EMPRESA-05-transportes-sur-andino/documentos/incidente-detallado.md) |
| `datos/bia.csv` | El análisis de impacto al negocio que mantenemos, con tiempos de recuperación por proceso | Anexo 3 y [archivo](../../../CASOS/EMPRESA-05-transportes-sur-andino/datos/bia.csv) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/usuarios_erp.csv` | Los usuarios de nuestro sistema principal, con perfil, último acceso y segundo factor | 181 registros · 181 habilitados · 181 sin segundo factor |
| `datos/empleados.csv` | Nuestra planilla del periodo, con ingresos y ceses | 268 registros · 232 activos · 36 cesados en el periodo |
| `datos/bia.csv` | Nuestro análisis de impacto al negocio | 6 registros |
| `datos/pagos.csv` | Nuestros pagos del periodo | 13694 registros · S/ 20 728 005 en total |

Atentamente,

**Gerente General, por encargo del Directorio**
TRANSPORTES SUR ANDINO S.A.

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
| Aprobada el | 1 de marzo de 2023 |
| Aprobada por | Gerencia General |
| Última revisión | Ninguna desde su aprobación |
| Difusión | Correo masivo el día de la aprobación |
| Acuse de recibo | 10 de 232 trabajadores firmaron el cargo |
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
| Responsable de seguridad de la información | Iván Maquera Quispe, Practicante | Memorando interno, sin resolución | Adicional a sus funciones de TI |
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
| Charla de inducción en seguridad | 10 de diciembre de 2023 | 55 | Lista de asistencia en papel |
| Campaña de contraseñas seguras | 25 de mayo de 2025 | No se registró | Afiche en el comedor |
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

**Dato del sistema principal, extraído por TI a solicitud del equipo.** De 181 usuarios habilitados, **181 no tienen segundo factor de autenticación**.

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
| Código | POL-TI-011 |
| Versión | 1.0 |
| Fecha de aprobación | 11 de abril de 2023 |
| Aprobado por | Gerencia de Administración y Finanzas |
| Próxima revisión programada | 5 de agosto de 2024 |
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

Elaborado por un practicante en abril de 2024. No fue revisado ni aprobado. Se entrega tal como está.

| ID | Proceso | Criticidad | RTO (h) | RPO (h) | Sistema de soporte | Responsable | Impacto a 24 h | Última prueba |
|---|---|---|---|---|---|---|---|---|
| BIA01 | Programación de flota y rutas | Baja | 8 | 32 | GPS y control de flota | Nelson Ilaquita Calisaya | Bajo | **Nunca** |
| BIA02 | Venta de pasajes en counter y en línea | Alta | 72 | 24 | Venta de pasajes y manifiesto | Silvia Quispe Ilaquita | Alto | **Nunca** |
| BIA03 | Embarque y manifiesto de pasajeros | Alta | 8 | 48 | Venta de pasajes y manifiesto | Vanessa Calisaya Flores | Medio | 2025-04-21 |
| BIA04 | Mantenimiento de unidades | Baja | 12 | 48 | Mantenimiento de unidades | Julio Nina Flores | Medio | **Nunca** |
| BIA05 | Control de conductores y descansos | Baja | 2 | 48 | Planillas y control de descanso de conductores | Silvia Colque Apaza | Medio | 2025-02-11 |
| BIA06 | Encomiendas y carga | Alta | 8 | 1 | Venta de pasajes y manifiesto | Silvia Flores Copaja | Medio | **Nunca** |

> El archivo original está en [`datos/bia.csv`](../../../CASOS/EMPRESA-05-transportes-sur-andino/datos/bia.csv).

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
| BIA01 · Programación de flota y rutas | Baja | 8 | 32 | GPS y control de flota | Bajo | Nunca |
| BIA02 · Venta de pasajes en counter y en línea | Alta | 72 | 24 | Venta de pasajes y manifiesto | Alto | Nunca |
| BIA03 · Embarque y manifiesto de pasajeros | Alta | 8 | 48 | Venta de pasajes y manifiesto | Medio | 2025-04-21 |
| BIA04 · Mantenimiento de unidades | Baja | 12 | 48 | Mantenimiento de unidades | Medio | Nunca |
| BIA05 · Control de conductores y descansos | Baja | 2 | 48 | Planillas y control de descanso de conductores | Medio | 2025-02-11 |
| BIA06 · Encomiendas y carga | Alta | 8 | 1 | Venta de pasajes y manifiesto | Medio | Nunca |

---

[Semana 08](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 08·04](CASO-08-04-coopac-frontera-sur.md) · **Caso 08·05** · [Caso 08·06](CASO-08-06-distribuidora-andina-sur.md) · [Encargo 08](../../ENCARGOS-UNIDAD-II/CASO-08-seguridad-de-la-informacion.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
