[Semana 10](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 10·07](CASO-10-07-instituto-vertiente-sur.md) · **Caso 10·08** · [Caso 10·09](CASO-10-09-servicios-mineros-cordillera.md) · [Encargo 10](../../ENCARGOS-UNIDAD-II/CASO-10-gestion-de-servicios-de-ti.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>EPS AGUAS DEL SUR S.A.</strong><br>
  <em>Solicitud de auditoría · Gestión de servicios de tecnologías de la información</em>
</div>

---

# Solicitud de auditoría de nuestra gestión de servicios de tecnologías de la información

| | |
|---|---|
| **Documento** | Solicitud de auditoría de nuestra gestión de servicios de tecnologías de la información |
| **De** | Gerente General, EPS AGUAS DEL SUR S.A. |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 19 de octubre de 2026 |
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

Las lecturas de 11 200 conexiones se facturaron estimadas por un fallo que nadie registró como incidente, y SUNASS abrió procedimiento. Nuestro Departamento de Tecnologías de la Información atiende por teléfono a 312 trabajadores y a la planta, sin catálogo ni registro consistente. El contrato del sistema comercial tiene nivel de servicio con penalidad y nunca lo hemos calculado.

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

1. Saber qué le debemos al usuario según SUNASS y qué le debemos al trabajador, porque son dos cosas distintas.
2. Saber si los incidentes de la planta y del SCADA deben entrar en nuestra gestión de servicios de TI.
3. Saber si el proveedor del sistema comercial cumplió el nivel de servicio en el incidente de la carga de lecturas, que nos costó un procedimiento.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | Pedimos este servicio de control al Órgano de Control Institucional, con conocimiento del Directorio y de OTASS |
| **Contraparte designada** | Nuestro Gerente de Administración, de quien depende el Departamento de Tecnologías de la Información |
| **Canal único** | Toda solicitud entra y sale por la mesa de partes institucional y el correo del Órgano de Control Institucional, con número de expediente por cada solicitud |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 26 de octubre de 2026. Trabajo de campo del 27 de octubre de 2026 al 16 de noviembre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 17 de noviembre de 2026 y el 23 de noviembre de 2026. Informe entre el 24 de noviembre de 2026 y el 30 de noviembre de 2026 |
| **Horas que financiamos** | Hasta 222 horas de la comisión. Unas 44 de planificación, 133 de trabajo de campo, 18 de comunicación de resultados y 27 de informe. Más que eso no lo pagamos |
| **Horas que podemos dedicarles** | Nuestra área de tecnologías de la información dedica unas 384 horas al mes al proceso que van a auditar, entre sus 6 personas. No pueden pedirle más tiempo que ese |
| **Presupuesto que aprobamos** | S/ 16 095, a tarifa de referencia de S/ 110 la hora de supervisión, S/ 85 la de jefe de comisión y S/ 60 la de integrante, sin viáticos |
| **Confidencialidad** | Todo lo que les entregamos es confidencial. Lo guardan en un repositorio privado, cifrado, con la marca CONFIDENCIAL — USO ACADÉMICO, y al cierre conservan solo lo que el informe cite |
| **Lo que no autorizamos** | Ninguna prueba se ejecuta sobre nuestros sistemas en esta etapa. Lo que pedimos es un plan. Si el plan incluye pruebas, dirá cuáles y nos pedirá autorización escrita antes |
| **Las personas** | En su plan y en su informe nos nombran por el cargo, no por el nombre |

## 7. Lo que les entregamos

Lo que sigue lo entregamos **a solicitud escrita**, indicando para qué lo necesitan y qué procedimiento lo va a usar. Los documentos propios de esta materia van ya como anexos de esta solicitud. Los demás se entregan por el canal único, en la carpeta que indica la tabla.

| Documento | Qué contiene | Dónde está |
|---|---|---|
| `mesa-de-servicio-y-sla.md` | Nuestros canales, el catálogo que TI reconoce, las metas que declaramos, el extracto del registro de atenciones y los problemas recurrentes | Anexo 1 |
| `cuestionario-diagnostico.md` | El cuestionario con el que nos autoevaluamos, tal como lo respondimos | Anexo 2 |
| `contratos-proveedores.md` | Las cláusulas de nivel de servicio con penalidad que nunca hemos calculado | [`documentos/contratos-proveedores.md`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/documentos/contratos-proveedores.md) |
| `extracciones-y-registros.md` | Los registros del sistema principal con los que se puede contrastar lo que afirmamos | [`documentos/extracciones-y-registros.md`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/documentos/extracciones-y-registros.md) |
| `incidente-detallado.md` | El incidente del periodo, como atención con consecuencia | [`documentos/incidente-detallado.md`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/documentos/incidente-detallado.md) |
| `datos/bia.csv` | Nuestro análisis de impacto al negocio, con el tiempo de recuperación que cada proceso declara tolerar | Anexo 3 y [archivo](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/datos/bia.csv) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/bia.csv` | Nuestro análisis de impacto al negocio | 6 registros |
| `datos/proveedores.csv` | Nuestro maestro de proveedores | 156 registros · 156 activos |
| `datos/pagos.csv` | Nuestros pagos del periodo | 19281 registros · S/ 28 844 992 en total |

Atentamente,

**Gerente General**
EPS AGUAS DEL SUR S.A.

---

## Anexos

### Anexo 1 · `mesa-de-servicio-y-sla.md`

### 1. Qué es este documento

Es lo que el área de TI entrega cuando se le pide cómo atiende a los usuarios. No hay herramienta de gestión de servicios. El registro se lleva en una hoja de cálculo que un practicante llena al final del día.

Con esto el equipo diagnostica la capacidad de las prácticas de gestión de servicios y construye el plan de auditoría de la Semana 10.

### 2. Cómo se recibe un pedido

| Canal | Uso declarado | ¿Queda registrado? |
|---|---|---|
| Teléfono interno de TI | El más usado | Solo si el técnico lo anota |
| Grupo de mensajería del personal | Segundo más usado | No |
| Correo a la cuenta de soporte | Formal, poco usado | Sí |
| El usuario baja al área de TI | Frecuente | No |
| Pedido verbal de una gerencia | Prioridad de hecho | No |

> **Hay 2047 registros en la hoja del periodo.** El propio jefe de TI estima que «se atiende el doble o el triple de lo que se anota».

### 3. Catálogo de servicios

No existe un catálogo aprobado. Lo que sigue es la lista que TI reconoce como sus servicios, redactada a pedido del equipo auditor.

| Servicio | Usuarios | Horario declarado | Dueño del servicio | Acuerdo escrito |
|---|---|---|---|---|
| Sistema comercial | Toda la organización | Lunes a sábado, 7 a 19 h | No designado | No |
| Correo electrónico | Personal administrativo | Permanente | No designado | No |
| Red y conexión a internet | Toda la organización | Permanente | No designado | No |
| Equipos de cómputo y periféricos | Toda la organización | Horario de oficina | No designado | No |
| Impresión y digitalización | Toda la organización | Horario de oficina | No designado | No |
| Respaldo y recuperación de archivos | Jefaturas | No definido | No designado | No |
| Accesos y cuentas de usuario | Toda la organización | Horario de oficina | No designado | No |

### 4. Niveles de servicio

| Servicio | Meta declarada | ¿Está firmada? | ¿Se mide? | ¿Se reporta? |
|---|---|---|---|---|
| Sistema comercial | «Atención el mismo día» | No | No | No |
| Correo electrónico | «Disponible siempre» | No | No | No |
| Red e internet | «99 %» | No | Solo cuando el proveedor envía su reporte | No |
| Equipos de cómputo | «48 horas» | No | No | No |
| Accesos y cuentas | «24 horas» | No | No | No |

**Contrato con el proveedor de Sistema comercial.** Tiene cláusula de nivel de servicio con penalidad. Nadie en la organización ha calculado nunca si el proveedor la cumplió.

### 5. Registro de atenciones del periodo · extracto

Las primeras filas de la hoja de cálculo, tal como están.

| N.º | Fecha | Quién reportó | Qué pasó | Tipo anotado | Prioridad | Estado | Fecha de cierre | Quién atendió |
|---|---|---|---|---|---|---|---|---|
| 001 | 2025-08-27 | Vanessa Flores Paredes | El sistema se cerró solo | Incidente |  | Cerrado | 2025-09-06 | Ricardo Nina Huanca |
| 002 | 2025-07-03 | Alberto Yufra Flores | La pantalla no enciende | Incidente | Alta | Cerrado | 2025-07-12 | Karla Flores Zapana |
| 003 | 2025-11-12 | Karla Apaza Vargas | El sistema quedó colgado en el cierre |  | Alta | Cerrado | 2025-11-14 | Lucía Peralta Peralta |
| 004 | 2025-10-06 | Karla Ticona Paredes | Olvidó la contraseña | Incidente |  | Cerrado | 2025-10-24 | Marco Yufra Peralta |
| 005 | 2025-01-20 | Carlos Peralta Colque | Olvidó la contraseña | Incidente | Urgente | Cerrado | 2025-02-03 | Óscar Chura Colque |
| 006 | 2025-07-17 | Silvia Laura Nina | No puede guardar el documento | Requerimiento | Urgente | Abierto |  | Carmen Calisaya Bravo |
| 007 | 2025-08-31 | Nelson Peralta Salazar | Pide permiso para ver otro módulo |  | Alta | Cerrado | 2025-09-11 | Nelson Peralta Salazar |
| 008 | 2025-05-29 | Paola Vargas Bravo | Pide permiso para ver otro módulo |  | Media | Abierto |  | Marco Copaja Maquera |
| 009 | 2025-08-06 | Iván Salazar Núñez | No entra al sistema | Incidente | Alta | Cerrado | 2025-08-06 | Marco Salazar Ilaquita |
| 010 | 2025-07-13 | Julia Ancco Ilaquita | No puede guardar el documento | Consulta |  | Cerrado | 2025-07-26 | Karla Flores Zapana |
| 011 | 2025-02-20 | Julio Apaza Nina | No entra al sistema | Incidente |  | Abierto |  | Marco Copaja Maquera |
| 012 | 2025-12-01 | Pedro Vargas Ilaquita | Pide crear un usuario nuevo |  | Alta | Cerrado | 2025-12-24 | Karla Ticona Paredes |
| 013 | 2025-06-10 | Sofía Ilaquita Ticona | Internet lento | Requerimiento |  | Cerrado | 2025-06-28 | Rocío Medina Vargas |
| 014 | 2025-07-05 | Paola Calisaya Calisaya | No entra al sistema | Incidente | Alta | Cerrado | 2025-07-28 | Marco Copaja Maquera |

> **Del total de 2047 registros, 102 siguen abiertos**, el más antiguo desde hace 385 días. La columna «Tipo anotado» está vacía en 123 filas y la de prioridad en 363.

### 6. Problemas recurrentes que TI reconoce

| Situación | Veces en el periodo | ¿Se buscó la causa? | ¿Se cerró de forma definitiva? |
|---|---|---|---|
| Reclamo masivo por facturación estimada | 7 | No | No |
| Lentitud del sistema en el cierre de mes | 23 | «Se reinicia el servidor» | No |
| Caída del enlace de internet | 12 | «Es del proveedor» | No |
| Usuario bloqueado por contraseña | 170 | No | No |
| El reporte sale con cifras distintas al sistema | 4 | No | No |

### 7. Gestión de cambios en los servicios

| Pregunta | Respuesta de TI |
|---|---|
| ¿Quién autoriza un cambio en producción? | «El jefe de TI, por correo o de palabra» |
| ¿Existe comité de cambios? | «No» |
| ¿Hay ventana de cambio acordada con los usuarios? | «Se avisa cuando se puede» |
| ¿Se prueba antes de pasar a producción? | «Depende del cambio» |
| ¿Existe plan de retorno si el cambio falla? | «Se restaura el respaldo» |
| ¿Cuántos cambios hubo en el periodo? | «No se cuentan» |

### 8. Lo que la organización responde

| Pregunta del auditor | Respuesta |
|---|---|
| ¿Existe un dueño por cada servicio? | «TI responde por todo» |
| ¿Se mide la satisfacción del usuario? | «No» |
| ¿Hay indicadores de la mesa de servicio? | «El practicante arma un cuadro cuando se le pide» |
| ¿Se clasifican los pedidos en incidente, requerimiento y consulta? | «En la hoja hay una columna, no siempre se llena» |
| ¿Existe base de conocimiento? | «Cada técnico sabe lo suyo» |
| ¿Qué pasa cuando el técnico de turno está de vacaciones? | «Se acumula» |

### 9. Marco aplicable

| Marco | Qué aporta como criterio |
|---|---|
| **ITIL 4** · práctica de mesa de servicio | Punto único de contacto, registro de toda interacción y clasificación del pedido |
| **ITIL 4** · práctica de gestión de incidentes | Registro, categorización, priorización y restauración del servicio acordado |
| **ITIL 4** · práctica de gestión de problemas | Identificación de la causa, error conocido y eliminación de la recurrencia |
| **ITIL 4** · práctica de gestión de niveles de servicio | Metas acordadas con el negocio, medidas y reportadas |
| **ITIL 4** · práctica de habilitación del cambio | Autorización, evaluación del riesgo y plan de retorno de cada cambio |
| **ISO/IEC 20000-1:2018**, apartado 8.2.4 | Catálogo de servicios con su contenido mínimo |
| **ISO/IEC 20000-1:2018**, apartado 8.3.3 | Gestión del nivel de servicio, con metas medidas y revisadas |
| **ISO/IEC 20000-1:2018**, apartado 8.6.1 | Gestión de incidentes, con clasificación, registro y escalamiento |
| **ISO/IEC 20000-1:2018**, apartado 8.6.3 | Gestión de problemas, con análisis de causa y acciones |
| **ISO/IEC 20000-1:2018**, apartado 8.5.1 | Gestión del cambio, con autorización y evaluación del riesgo |
| **ISO/IEC 20000-1:2018**, apartado 9.1 | Seguimiento, medición, análisis y evaluación del sistema de gestión del servicio |
| **COBIT 2019** · DSS02 y DSS03 | Gestión de solicitudes e incidentes y gestión de problemas |
| **D. S. 029-2021-PCM** | Gestión de servicios digitales en la entidad pública |

### Anexo 2 · `cuestionario-diagnostico.md`

### 1. Ficha del instrumento

| Campo | Contenido |
|---|---|
| Propósito declarado | «Conocer la percepción de los usuarios sobre los servicios de TI» |
| Población | Todo el personal con acceso al sistema |
| Aplicación | Correo electrónico, respuesta voluntaria |
| Respuestas obtenidas | 22 de 312 |
| Fecha de aplicación | 9 de abril de 2026 |
| Quién lo elaboró | El área de Tecnologías de la Información |
| ¿Se validó antes de aplicarlo? | No |

### 2. Las doce preguntas, tal como se aplicaron

| N.º | Pregunta | Escala |
|---|---|---|
| 1 | ¿Considera usted que los sistemas de la empresa son seguros y funcionan correctamente? | Sí / No |
| 2 | ¿Está de acuerdo con que el área de TI responde rápido, aunque a veces se demore? | Sí / No |
| 3 | ¿Cuántas veces al mes aproximadamente tiene problemas con el sistema? | Número |
| 4 | ¿No cree que sería mejor cambiar de proveedor? | Sí / No |
| 5 | Evalúe la calidad del servicio de TI. | Bueno / Regular / Malo |
| 6 | ¿Usted recibió capacitación en seguridad de la información en el último año? | Sí / No |
| 7 | ¿Comparte su contraseña con algún compañero cuando es necesario para no detener el trabajo? | Sí / No |
| 8 | ¿Qué tan satisfecho está con la disponibilidad y el rendimiento del sistema? | 1 a 5 |
| 9 | Los respaldos se realizan correctamente. ¿Está de acuerdo? | Sí / No |
| 10 | ¿Sabe a quién reportar un incidente de seguridad? | Sí / No |
| 11 | ¿Cree que la empresa invierte lo suficiente en tecnología? | Sí / No |
| 12 | Indique todos los problemas que ha tenido con el sistema en los últimos dos años. | Texto libre |

### Anexo 3 · `datos/bia.csv`

Nuestro análisis de impacto al negocio, con el tiempo de recuperación que cada proceso declara tolerar.

| Proceso | Criticidad | RTO (h) | RPO (h) | Sistema de soporte | Impacto a 24 h | Última prueba |
|---|---|---|---|---|---|---|
| BIA01 · Catastro comercial de usuarios | Alta | 12 | 36 | Sistema comercial | Alto | 2025-05-17 |
| BIA02 · Lectura de medidores y facturación | Alta | 72 | 8 | Micromedición y lectura | Medio | 2025-07-13 |
| BIA03 · Cobranza y corte/reconexión | Alta | 48 | 1 | Sistema comercial | Medio | Nunca |
| BIA04 · Atención de reclamos comerciales | Alta | 4 | 48 | Atención de reclamos | Alto | 2025-12-07 |
| BIA05 · Operación de plantas y redes | Alta | 2 | 48 | SCADA de plantas y reservorios | Alto | Nunca |
| BIA06 · Contrataciones y presupuesto público | Alta | 2 | 48 | SIAF y patrimonio | Bajo | Nunca |

---

[Semana 10](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 10·07](CASO-10-07-instituto-vertiente-sur.md) · **Caso 10·08** · [Caso 10·09](CASO-10-09-servicios-mineros-cordillera.md) · [Encargo 10](../../ENCARGOS-UNIDAD-II/CASO-10-gestion-de-servicios-de-ti.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
