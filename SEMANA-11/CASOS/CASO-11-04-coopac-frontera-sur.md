[Semana 11](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 11·03](CASO-11-03-municipalidad-alto-selva.md) · **Caso 11·04** · [Caso 11·05](CASO-11-05-transportes-sur-andino.md) · [Encargo 11](../../ENCARGOS-UNIDAD-II/CASO-11-cumplimiento-legal.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>COOPAC FRONTERA SUR</strong><br>
  <em>Solicitud de auditoría · Cumplimiento legal del entorno informático</em>
</div>

---

# Solicitud de auditoría de el cumplimiento legal de nuestro entorno informático

| | |
|---|---|
| **Documento** | Solicitud de auditoría de el cumplimiento legal de nuestro entorno informático |
| **De** | Gerente General, por acuerdo del Consejo de Vigilancia, COOPAC FRONTERA SUR |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 26 de octubre de 2026 |
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

Un socio nos pidió por escrito el detalle de cómo tratamos sus datos y a quién los transferimos. Consultamos una central de riesgos externa, compartimos información con la UIF-Perú y con la SBS, y el proveedor de planilla procesa datos de nuestro personal. El acceso indebido a 1 900 expedientes puede haber activado un deber de notificación que nadie evaluó.

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

1. Saber qué transferencias hacemos por obligación legal, como las de la UIF-Perú y la SBS, y cuáles requieren consentimiento del socio.
2. Saber si la central de riesgos y el proveedor de planilla tienen el contrato que la ley exige.
3. Saber si el acceso indebido a 1 900 expedientes debió notificarse, a quién, y qué evidencia debimos preservar.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | El Consejo de Vigilancia lo acordó a propuesta de la Unidad de Auditoría Interna, dentro del plan anual que remitimos a la SBS |
| **Contraparte designada** | Nuestro Gerente General, con el Oficial de Seguridad de la Información como enlace |
| **Canal único** | Toda solicitud entra y sale por el correo de la Unidad de Auditoría Interna, que registra cada solicitud en su sistema de seguimiento |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 2 de noviembre de 2026. Trabajo de campo del 3 de noviembre de 2026 al 23 de noviembre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 24 de noviembre de 2026 y el 30 de noviembre de 2026. Informe entre el 1 de diciembre de 2026 y el 7 de diciembre de 2026 |
| **Horas que financiamos** | Hasta 185 horas de la comisión. Unas 37 de planificación, 111 de trabajo de campo, 15 de comunicación de resultados y 22 de informe. Más que eso no lo pagamos |
| **Horas que podemos dedicarles** | Nuestra área de tecnologías de la información dedica unas 40 horas al mes al proceso que van a auditar, entre sus 5 personas. No pueden pedirle más tiempo que ese |
| **Presupuesto que aprobamos** | S/ 13 412, a tarifa de referencia de S/ 110 la hora de supervisión, S/ 85 la de jefe de comisión y S/ 60 la de integrante, sin viáticos. Si necesitan ir a nuestras sedes fuera de Tacna, los pasajes y viáticos se presupuestan aparte |
| **Confidencialidad** | Todo lo que les entregamos es confidencial. Lo guardan en un repositorio privado, cifrado, con la marca CONFIDENCIAL — USO ACADÉMICO, y al cierre conservan solo lo que el informe cite |
| **Lo que no autorizamos** | Ninguna prueba se ejecuta sobre nuestros sistemas en esta etapa. Lo que pedimos es un plan. Si el plan incluye pruebas, dirá cuáles y nos pedirá autorización escrita antes |
| **Las personas** | En su plan y en su informe nos nombran por el cargo, no por el nombre |

## 7. Lo que les entregamos

Lo que sigue lo entregamos **a solicitud escrita**, indicando para qué lo necesitan y qué procedimiento lo va a usar. Los documentos propios de esta materia van ya como anexos de esta solicitud. Los demás se entregan por el canal único, en la carpeta que indica la tabla.

| Documento | Qué contiene | Dónde está |
|---|---|---|
| `registro-datos-y-licencias.md` | El registro de actividades de tratamiento que armamos a pedido, y el inventario de software instalado contra las licencias | Anexo 1 |
| `contratos-proveedores.md` | Nuestros contratos con terceros que tratan información nuestra, con o sin cláusula de encargo | Anexo 2 |
| `plan-institucional-extracto.md` | Lo que declaramos sobre nuestras obligaciones | [`documentos/plan-institucional-extracto.md`](../../../CASOS/EMPRESA-04-coopac-frontera-sur/documentos/plan-institucional-extracto.md) |
| `organigrama-y-accesos.md` | Qué área responde por cada obligación, si alguna lo hace | [`documentos/organigrama-y-accesos.md`](../../../CASOS/EMPRESA-04-coopac-frontera-sur/documentos/organigrama-y-accesos.md) |
| `incidente-detallado.md` | El incidente del periodo, para evaluar si activó un deber de notificación | [`documentos/incidente-detallado.md`](../../../CASOS/EMPRESA-04-coopac-frontera-sur/documentos/incidente-detallado.md) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/empleados.csv` | Nuestra planilla del periodo, con ingresos y ceses | 96 registros · 84 activos · 12 cesados en el periodo |
| `datos/proveedores.csv` | Nuestro maestro de proveedores | 60 registros · 60 activos |
| `datos/usuarios_erp.csv` | Los usuarios de nuestro sistema principal, con perfil, último acceso y segundo factor | 75 registros · 75 habilitados · 75 sin segundo factor |
| `datos/pagos.csv` | Nuestros pagos del periodo | 28016 registros · S/ 42 214 064 en total |

Atentamente,

**Gerente General, por acuerdo del Consejo de Vigilancia**
COOPAC FRONTERA SUR

---

## Anexos

### Anexo 1 · `registro-datos-y-licencias.md`

### Parte 1 · Registro de actividades de tratamiento de datos personales

> **Nota de la organización.** «No teníamos este registro. Lo armamos ahora, a pedido del equipo auditor, con lo que sabemos. Puede faltar algo.»

El artículo correspondiente de la **Ley 29733** y su reglamento, el **D. S. 016-2024-JUS**, exigen mantener este registro de forma permanente y actualizada, no elaborarlo cuando alguien lo pide.

| N.º | Actividad de tratamiento | Datos que trata | Finalidad declarada | Base legal | ¿Consentimiento? | Plazo de conservación | ¿Se transfiere a terceros? |
|---|---|---|---|---|---|---|---|
| 1 | Gestión de planilla | Nombre, documento, domicilio, cuenta bancaria, remuneración, descuentos judiciales | Pago de remuneraciones y cumplimiento laboral | Obligación legal | No requerido | Indefinido | Sí — proveedor de planilla |
| 2 | Datos de salud del personal | Descansos médicos, diagnósticos, exámenes ocupacionales | Gestión de ausencias y seguridad ocupacional | **Sin declarar** | **No consta** | Indefinido | Sí — proveedor de planilla |
| 3 | Proceso de selección | Currículos, antecedentes, referencias | Contratación de personal | **Sin declarar** | **No consta** | «Se guardan por si acaso» | No |
| 4 | Videovigilancia | Imagen de personas en instalaciones | Seguridad de las instalaciones | Interés legítimo | **No hay aviso visible** | «Lo que dure el disco» | No |
| 5 | Control de asistencia biométrico | **Huella dactilar** | Control de jornada | **Sin declarar** | **No consta** | Indefinido | No |
| 6 | Expedientes de crédito de socios | Ingresos, patrimonio, referencias, situación crediticia | Evaluación crediticia | Ejecución de contrato | En la solicitud | Según norma SBS | Sí — central de riesgos |

#### Lo que la organización responde

| Pregunta | Respuesta |
|---|---|
| ¿Está inscrito el banco de datos ante la autoridad? | «Se hizo hace años, no sabemos si sigue vigente» |
| ¿Existe un responsable de protección de datos designado? | «No» |
| ¿Se informa a los titulares sobre el tratamiento? | «En el contrato hay una cláusula» |
| ¿Cómo se atiende un pedido de acceso o supresión? | «Nunca nos han pedido» |
| ¿Se autorizó el flujo transfronterizo? | «No sabíamos que había que hacerlo» |
| ¿Hay medidas de seguridad documentadas para estos datos? | «Las del sistema» |
| ¿Se evaluó el impacto del tratamiento de datos sensibles? | «No» |

### Parte 2 · Inventario de software instalado

Extraído de 62 estaciones de trabajo con la herramienta de inventario. Se entrega el consolidado.

| Software | Versión | Instalaciones | Licencias adquiridas | Diferencia | Tipo de licencia | ¿Soporte vigente? |
|---|---|---|---|---|---|---|
| Suite ofimática | 2020 | 167 | 3 | **-164** | Libre / GPL | Vencido |
| Sistema operativo de escritorio | 10 | 48 | 48 | **+0** | Libre / MIT | Vencido |
| Antivirus corporativo | — | 146 | 93 | **-53** | Libre / MIT | No |
| Compresor de archivos | — | 44 | 44 | **+0** | Perpetua | Vencido |
| Lector de PDF | — | 49 | 49 | **+0** | Suscripción anual | Sí |
| Editor de imágenes | — | 4 | 1 | **-3** | Libre / MIT | Sí |
| Herramienta de diseño | — | 7 | 7 | **+0** | Perpetua | No |
| Cliente de base de datos | — | 7 | 4 | **-3** | Libre / GPL | Vencido |
| Software de contabilidad | — | 8 | 4 | **-4** | Suscripción anual | Vencido |

#### Lo que la organización responde

| Pregunta | Respuesta |
|---|---|
| ¿Quién controla las licencias? | «Sistemas lleva las facturas» |
| ¿Se verifica antes de instalar? | «El usuario pide y se instala si está» |
| ¿Se ha hecho una revisión de cumplimiento de licencias? | «No» |
| ¿Hay software instalado por los propios usuarios? | «No deberían tener permisos, pero algunos sí» |

### Marco aplicable

| Norma | Qué exige |
|---|---|
| **Ley 29733**, arts. 13 a 15 | Consentimiento, finalidad determinada y flujo transfronterizo |
| **D. S. 016-2024-JUS** | Registro de actividades de tratamiento, medidas de seguridad y encargo |
| **Datos sensibles** | Salud, biometría y datos de menores tienen protección reforzada |
| **D. Leg. 822** | Derecho de autor sobre programas de ordenador. Cada instalación requiere licencia |

### Anexo 2 · `contratos-proveedores.md`

### Contrato 1 · Servicio de planilla y gestión de personal

| Campo | Contenido |
|---|---|
| Proveedor | **Servicios Pacífico S.A.** · RUC 20601957820 |
| Objeto | Procesamiento de planilla, boletas electrónicas y declaraciones a la autoridad tributaria |
| Vigencia | Del 1 de marzo de 2023 al 28 de marzo de 2025, con **renovación automática** salvo aviso con 30 días de anticipación |
| Contraprestación | S/ 3 808.00 mensuales |
| Datos que trata | Nombres, documento de identidad, domicilio, cuenta bancaria, remuneraciones, descuentos judiciales y **datos de salud del personal en descanso médico** |
| Dónde se alojan | «Servidores del proveedor» |
| Contacto | Silvia Medina Copaja |

#### Cláusulas relevantes, transcritas

> **Cláusula quinta — Confidencialidad.** «EL PROVEEDOR se obliga a mantener reserva sobre la información que reciba de EL CLIENTE, no pudiendo divulgarla a terceros sin autorización escrita.»

> **Cláusula octava — Responsabilidad.** «EL PROVEEDOR responderá por los daños directos que ocasione por dolo o culpa inexcusable, hasta por el monto equivalente a tres mensualidades del servicio.»

> **Cláusula décima — Terminación.** «Cualquiera de las partes podrá resolver el contrato con aviso de 30 días. EL PROVEEDOR entregará la información procesada a la fecha de terminación.»

#### Lo que el contrato **no** dice

Se transcribe el índice completo del contrato para que el equipo verifique qué cláusulas existen y cuáles no:

`Primera` Partes · `Segunda` Objeto · `Tercera` Plazo · `Cuarta` Contraprestación · `Quinta` Confidencialidad · `Sexta` Obligaciones del cliente · `Séptima` Obligaciones del proveedor · `Octava` Responsabilidad · `Novena` Solución de controversias · `Décima` Terminación · `Undécima` Domicilios.

### Contrato 2 · Servicio de infraestructura en nube

| Campo | Contenido |
|---|---|
| Proveedor | **Inversiones Pacífico E.I.R.L.** · RUC 20102320512 |
| Objeto | Alojamiento de Core financiero y respaldo externo |
| Vigencia | Del 1 de octubre de 2024 al 31 de diciembre de 2026 |
| Contraprestación | S/ 5 010.00 mensuales, más consumo variable |
| Ubicación de los servidores | «Centros de datos del proveedor» — no se especifica el país |
| Nivel de servicio comprometido | «Alta disponibilidad» |
| Contacto | Elena Medina Laura |

#### Cláusulas relevantes, transcritas

> **Cláusula sexta — Disponibilidad.** «EL PROVEEDOR realizará sus mejores esfuerzos para mantener el servicio disponible de manera continua.»

> **Cláusula séptima — Respaldos.** «EL PROVEEDOR realizará copias de seguridad conforme a sus políticas internas.»

> **Cláusula novena — Subcontratación.** «EL PROVEEDOR podrá subcontratar total o parcialmente la prestación, informando a EL CLIENTE.»

### Lo que la organización responde

| Pregunta del auditor | Respuesta |
|---|---|
| ¿Existe un acuerdo de nivel de servicio con métricas? | «Está en el contrato: alta disponibilidad» |
| ¿Se mide el cumplimiento del proveedor? | «No formalmente. Si algo falla, se le llama» |
| ¿Se sabe en qué país están los datos? | «Se asume que en la región» |
| ¿Hay contrato de encargo de tratamiento de datos personales? | «El contrato tiene cláusula de confidencialidad» |
| ¿Se autorizó el flujo transfronterizo de datos? | «No se ha tramitado nada» |
| ¿Se revisó la seguridad del proveedor? | «Es un proveedor conocido» |
| ¿Quién controla los vencimientos? | «Administración lleva las fechas» |

### Marco aplicable

| Norma | Qué exige |
|---|---|
| **Ley 29733**, art. 15 | Autorización previa para el flujo transfronterizo de datos personales |
| **D. S. 016-2024-JUS** | Contenido mínimo del encargo de tratamiento y obligaciones del encargado |
| **Ley 29733**, art. 14 | Consentimiento previo, informado, expreso e inequívoco |
| **NTP-ISO/IEC 27001:2022**, A.5.19 a A.5.23 | Seguridad en las relaciones con proveedores y en servicios en nube |
| **Resolución SBS 504-2021** | Gestión de la seguridad de la información en entidades supervisadas |

---

[Semana 11](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 11·03](CASO-11-03-municipalidad-alto-selva.md) · **Caso 11·04** · [Caso 11·05](CASO-11-05-transportes-sur-andino.md) · [Encargo 11](../../ENCARGOS-UNIDAD-II/CASO-11-cumplimiento-legal.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
