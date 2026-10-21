[Semana 10](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 10·03](CASO-10-03-municipalidad-alto-selva.md) · **Caso 10·04** · [Caso 10·05](CASO-10-05-transportes-sur-andino.md) · [Encargo 10](../../ENCARGOS-UNIDAD-II/CASO-10-gestion-de-servicios-de-ti.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>COOPAC FRONTERA SUR</strong><br>
  <em>Solicitud de auditoría · Gestión de servicios de tecnologías de la información</em>
</div>

---

# Solicitud de auditoría de nuestra gestión de servicios de tecnologías de la información

| | |
|---|---|
| **Documento** | Solicitud de auditoría de nuestra gestión de servicios de tecnologías de la información |
| **De** | Gerente General, por acuerdo del Consejo de Vigilancia, COOPAC FRONTERA SUR |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 19 de octubre de 2026 |
| **Clasificación** | CONFIDENCIAL — USO ACADÉMICO |

---

## 1. Quiénes somos

Somos **COOPAC FRONTERA SUR**, cooperativa de ahorro y crédito, con sede en Tacna, con agencias en Tarata y Locumba. Operamos desde hace 34 años, con 96 trabajadores estables y 12 promotores de campo. Manejamos S/ 189 millones en activos · 21 400 socios y atendemos socios de Tacna y valles del interior.

Nos regulan o supervisan **SBS (Resolución 504-2021 de gestión de seguridad de la información) · UIF-Perú · ANPD · SUNAT**.

Nuestra área de tecnologías de la información tiene **5 personas**. La encabeza nuestro jefe de TI, que reporta a Gerencia General. Existe un Oficial de Seguridad de la Información con dedicación parcial. El presupuesto de tecnologías de la información es de **S/ 1 240 000**, el 2.9 % de gastos operativos. El objetivo que le declaramos a esa área es «Implementar de verdad el sistema de gestión de seguridad exigido por el regulador y hacerlo auditable».

**Lo que más nos cuesta.** La Resolución SBS 504-2021 exige un sistema de gestión de seguridad de la información con roles, riesgos y continuidad. Existe un documento redactado en 2022 que nunca se implementó ni se auditó.

### 1.1. Los sistemas con los que operamos

| Sistema | Qué es | Dónde corre | Desde | ¿Tiene soporte vigente? |
|---|---|---|---|---|
| **Core financiero** | Producto especializado en cooperativas, licenciado | Servidor propio con réplica | 2017 | Sí, contrato con SLA |
| **Banca por internet para socios** | Módulo web del mismo proveedor | Nube del proveedor | 2021 | Sí |
| **Prevención de lavado de activos** | Sistema de alertas del proveedor | Servidor propio | 2019 | Sí |
| **Central de riesgos** | Consulta a bureau externo por servicio web | SaaS | 2018 | Sí |
| **Gestión documental de expedientes de crédito** | Carpetas compartidas en red | Servidor de archivos | 2015 | No |

### 1.2. Nuestros procesos

1. Captación de ahorros
2. Evaluación y otorgamiento de créditos
3. Recuperaciones y cobranza
4. Prevención de lavado de activos
5. Atención al socio en agencias
6. Cierre contable y reportes a la SBS

## 2. Por qué pedimos esta auditoría

Nuestras agencias de Tarata y Locumba reclaman que las caídas del core se atienden más tarde que en la sede. El contrato del core tiene un acuerdo de nivel de servicio con penalidad que nunca hemos calculado. La SBS nos exige gestión de incidentes y la llevamos por teléfono. La Unidad de Auditoría Interna quiere saber qué nivel de servicio reciben los socios.

## 3. Lo que ya sabemos que no está bien

Estos riesgos los tenemos identificados y no los hemos tratado.

- Incumplimiento verificable de la Resolución SBS 504-2021
- Sin registro de accesos de lectura a información de socios
- Plan de continuidad sin pruebas documentadas

**Lo que nos pasó en el periodo. Acceso indebido a expedientes de crédito.** Un analista consultó y descargó 1 900 expedientes de crédito de socios que no le correspondían durante cuatro meses. Se detectó por denuncia interna, no por control. El servidor de archivos no registraba accesos de lectura.

## 4. Lo que ya nos dijeron

- La SBS nos visitó en 2024 y dejó cuatro observaciones sobre el sistema de gestión de seguridad de la información que exige la Resolución SBS N.º 504-2021. Roles sin designar por resolución, apreciación del riesgo sin metodología, plan de continuidad sin pruebas y registro de accesos a información de socios inexistente. Las cuatro siguen abiertas.
- Nuestra Unidad de Auditoría Interna audita cada año el proceso de créditos y el de prevención de lavado de activos. Nunca ha auditado tecnologías de la información.
- La auditoría externa financiera de 2025 nos emitió una carta de control interno con una recomendación sobre la segregación de funciones en el core financiero.

## 5. Lo que queremos saber

Son las preguntas que la dirección espera que la auditoría responda. Cómo responderlas, con qué alcance, con qué criterios y con qué procedimientos, es lo que esperamos de su plan.

1. Saber qué nos exige la SBS sobre gestión de incidentes y en qué se diferencia de un incidente de servicio.
2. Saber si nuestras tres agencias reciben el mismo nivel de servicio que la sede.
3. Saber si el proveedor del core y de la banca por internet cumplió el acuerdo de nivel de servicio con penalidad que nunca calculamos.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | El Consejo de Vigilancia lo acordó a propuesta de la Unidad de Auditoría Interna, dentro del plan anual que remitimos a la SBS |
| **Contraparte designada** | Nuestro Gerente General, con el Oficial de Seguridad de la Información como enlace |
| **Canal único** | Toda solicitud entra y sale por el correo de la Unidad de Auditoría Interna, que registra cada solicitud en su sistema de seguimiento |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 26 de octubre de 2026. Trabajo de campo del 27 de octubre de 2026 al 16 de noviembre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 17 de noviembre de 2026 y el 23 de noviembre de 2026. Informe entre el 24 de noviembre de 2026 y el 30 de noviembre de 2026 |
| **Horas que financiamos** | Hasta 185 horas de la comisión. Unas 37 de planificación, 111 de trabajo de campo, 15 de comunicación de resultados y 22 de informe. Más que eso no lo pagamos |
| **Horas que podemos dedicarles** | Nuestra área de tecnologías de la información dedica unas 320 horas al mes al proceso que van a auditar, entre sus 5 personas. No pueden pedirle más tiempo que ese |
| **Presupuesto que aprobamos** | S/ 13 412, a tarifa de referencia de S/ 110 la hora de supervisión, S/ 85 la de jefe de comisión y S/ 60 la de integrante, sin viáticos. Si necesitan ir a nuestras sedes fuera de Tacna, los pasajes y viáticos se presupuestan aparte |
| **Confidencialidad** | Todo lo que les entregamos es confidencial. Lo guardan en un repositorio privado, cifrado, con la marca CONFIDENCIAL — USO ACADÉMICO, y al cierre conservan solo lo que el informe cite |
| **Lo que no autorizamos** | Ninguna prueba se ejecuta sobre nuestros sistemas en esta etapa. Lo que pedimos es un plan. Si el plan incluye pruebas, dirá cuáles y nos pedirá autorización escrita antes |
| **Las personas** | En su plan y en su informe nos nombran por el cargo, no por el nombre |

## 7. Lo que les entregamos

Lo que sigue lo entregamos **a solicitud escrita**, indicando para qué lo necesitan y qué procedimiento lo va a usar. Los documentos propios de esta materia van ya como anexos de esta solicitud. Los demás se entregan por el canal único, en la carpeta que indica la tabla.

| Documento | Qué contiene | Dónde está |
|---|---|---|
| `mesa-de-servicio-y-sla.md` | Nuestros canales, el catálogo que TI reconoce, las metas que declaramos, el extracto del registro de atenciones y los problemas recurrentes | Anexo 1 |
| `cuestionario-diagnostico.md` | El cuestionario con el que nos autoevaluamos, tal como lo respondimos | Anexo 2 |
| `contratos-proveedores.md` | Las cláusulas de nivel de servicio con penalidad que nunca hemos calculado | [`documentos/contratos-proveedores.md`](../../../CASOS/EMPRESA-04-coopac-frontera-sur/documentos/contratos-proveedores.md) |
| `extracciones-y-registros.md` | Los registros del sistema principal con los que se puede contrastar lo que afirmamos | [`documentos/extracciones-y-registros.md`](../../../CASOS/EMPRESA-04-coopac-frontera-sur/documentos/extracciones-y-registros.md) |
| `incidente-detallado.md` | El incidente del periodo, como atención con consecuencia | [`documentos/incidente-detallado.md`](../../../CASOS/EMPRESA-04-coopac-frontera-sur/documentos/incidente-detallado.md) |
| `datos/bia.csv` | Nuestro análisis de impacto al negocio, con el tiempo de recuperación que cada proceso declara tolerar | Anexo 3 y [archivo](../../../CASOS/EMPRESA-04-coopac-frontera-sur/datos/bia.csv) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/bia.csv` | Nuestro análisis de impacto al negocio | 6 registros |
| `datos/proveedores.csv` | Nuestro maestro de proveedores | 60 registros · 60 activos |
| `datos/pagos.csv` | Nuestros pagos del periodo | 28016 registros · S/ 42 214 064 en total |

Atentamente,

**Gerente General, por acuerdo del Consejo de Vigilancia**
COOPAC FRONTERA SUR

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

> **Hay 1529 registros en la hoja del periodo.** El propio jefe de TI estima que «se atiende el doble o el triple de lo que se anota».

### 3. Catálogo de servicios

No existe un catálogo aprobado. Lo que sigue es la lista que TI reconoce como sus servicios, redactada a pedido del equipo auditor.

| Servicio | Usuarios | Horario declarado | Dueño del servicio | Acuerdo escrito |
|---|---|---|---|---|
| Core financiero | Toda la organización | Lunes a sábado, 7 a 19 h | No designado | No |
| Correo electrónico | Personal administrativo | Permanente | No designado | No |
| Red y conexión a internet | Toda la organización | Permanente | No designado | No |
| Equipos de cómputo y periféricos | Toda la organización | Horario de oficina | No designado | No |
| Impresión y digitalización | Toda la organización | Horario de oficina | No designado | No |
| Respaldo y recuperación de archivos | Jefaturas | No definido | No designado | No |
| Accesos y cuentas de usuario | Toda la organización | Horario de oficina | No designado | No |

### 4. Niveles de servicio

| Servicio | Meta declarada | ¿Está firmada? | ¿Se mide? | ¿Se reporta? |
|---|---|---|---|---|
| Core financiero | «Atención el mismo día» | No | No | No |
| Correo electrónico | «Disponible siempre» | No | No | No |
| Red e internet | «99 %» | No | Solo cuando el proveedor envía su reporte | No |
| Equipos de cómputo | «48 horas» | No | No | No |
| Accesos y cuentas | «24 horas» | No | No | No |

**Contrato con el proveedor de Core financiero.** Tiene cláusula de nivel de servicio con penalidad. Nadie en la organización ha calculado nunca si el proveedor la cumplió.

### 5. Registro de atenciones del periodo · extracto

Las primeras filas de la hoja de cálculo, tal como están.

| N.º | Fecha | Quién reportó | Qué pasó | Tipo anotado | Prioridad | Estado | Fecha de cierre | Quién atendió |
|---|---|---|---|---|---|---|---|---|
| 001 | 2025-03-23 | Iván Rivera Torres | No entra al sistema | Incidente |  | Cerrado | 2025-04-12 | Ricardo Nina Ticona |
| 002 | 2025-07-22 | Alberto Zapana Huanca | No ve el reporte de su área | Incidente | Urgente | Cerrado | 2025-07-23 | Diana Peralta Cáceres |
| 003 | 2025-07-29 | Óscar Torres Flores | El sistema quedó colgado en el cierre | Incidente | Media | Cerrado | 2025-08-04 | Rosa Ancco Peralta |
| 004 | 2025-10-05 | Hugo Ramos Colque | Pide crear un usuario nuevo | Requerimiento |  | Cerrado | 2025-10-16 | Marco Copaja Yufra |
| 005 | 2025-08-10 | Gabriela Nina Vargas | Pide permiso para ver otro módulo | Consulta | Media | Cerrado | 2025-08-13 | Teresa Aguilar Peralta |
| 006 | 2025-11-18 | Diana Núñez Calisaya | Pide crear un usuario nuevo | Incidente |  | Cerrado | 2025-12-08 | Álvaro Rivera Vargas |
| 007 | 2025-04-08 | Hugo Cutipa Peralta | Pide permiso para ver otro módulo |  |  | Cerrado | 2025-04-24 | Pedro Ilaquita Aguilar |
| 008 | 2025-11-15 | Ricardo Paredes Calisaya | Internet lento |  | Media | Cerrado | 2025-12-09 | Teresa Condori Cutipa |
| 009 | 2025-10-12 | Ricardo Nina Ticona | El sistema se cerró solo | Incidente | Alta | Cerrado | 2025-10-22 | Diana Peralta Cáceres |
| 010 | 2025-11-11 | Álvaro Laura Cutipa | No ve el reporte de su área | Incidente |  | En proceso |  | Teresa Condori Cutipa |
| 011 | 2025-01-15 | Diana Chura Condori | El sistema quedó colgado en el cierre | Incidente |  | Cerrado | 2025-01-31 | Marco Copaja Yufra |
| 012 | 2025-08-15 | Marco Rivera Colque | No ve el reporte de su área | Incidente |  | Abierto |  | Álvaro Rivera Vargas |
| 013 | 2025-11-14 | Alberto Zapana Huanca | Internet lento | Incidente |  | Cerrado | 2025-12-01 | Julio Ticona Yufra |
| 014 | 2025-11-20 | Carlos Copaja Medina | La impresora no responde | Consulta | Media | Cerrado | 2025-12-11 | Pedro Ilaquita Aguilar |

> **Del total de 1529 registros, 163 siguen abiertos**, el más antiguo desde hace 307 días. La columna «Tipo anotado» está vacía en 126 filas y la de prioridad en 379.

### 6. Problemas recurrentes que TI reconoce

| Situación | Veces en el periodo | ¿Se buscó la causa? | ¿Se cerró de forma definitiva? |
|---|---|---|---|
| Acceso indebido a expedientes de crédito | 13 | No | No |
| Lentitud del sistema en el cierre de mes | 13 | «Se reinicia el servidor» | No |
| Caída del enlace de internet | 8 | «Es del proveedor» | No |
| Usuario bloqueado por contraseña | 55 | No | No |
| El reporte sale con cifras distintas al sistema | 9 | No | No |

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

### Anexo 2 · `cuestionario-diagnostico.md`

### 1. Ficha del instrumento

| Campo | Contenido |
|---|---|
| Propósito declarado | «Conocer la percepción de los usuarios sobre los servicios de TI» |
| Población | Todo el personal con acceso al sistema |
| Aplicación | Correo electrónico, respuesta voluntaria |
| Respuestas obtenidas | 53 de 96 |
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
| BIA01 · Captación de ahorros | Media | 2 | 26 | Core financiero | Bajo | Nunca |
| BIA02 · Evaluación y otorgamiento de créditos | Alta | 72 | 48 | Central de riesgos | Bajo | 2025-06-11 |
| BIA03 · Recuperaciones y cobranza | Media | 8 | 4 | Core financiero | Medio | Nunca |
| BIA04 · Prevención de lavado de activos | Media | 12 | 24 | Prevención de lavado de activos | Medio | 2025-05-25 |
| BIA05 · Atención al socio en agencias | Baja | 8 | 4 | Banca por internet para socios | Bajo | 2025-02-24 |
| BIA06 · Cierre contable y reportes a la SBS | Media | 24 | 1 | Core financiero | Alto | Nunca |

---

[Semana 10](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 10·03](CASO-10-03-municipalidad-alto-selva.md) · **Caso 10·04** · [Caso 10·05](CASO-10-05-transportes-sur-andino.md) · [Encargo 10](../../ENCARGOS-UNIDAD-II/CASO-10-gestion-de-servicios-de-ti.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
