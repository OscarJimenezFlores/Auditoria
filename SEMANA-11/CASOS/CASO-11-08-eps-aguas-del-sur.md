[Semana 11](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 11·07](CASO-11-07-instituto-vertiente-sur.md) · **Caso 11·08** · [Caso 11·09](CASO-11-09-servicios-mineros-cordillera.md) · [Encargo 11](../../ENCARGOS-UNIDAD-II/CASO-11-cumplimiento-legal.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>EPS AGUAS DEL SUR S.A.</strong><br>
  <em>Solicitud de auditoría · Cumplimiento legal del entorno informático</em>
</div>

---

# Solicitud de auditoría de el cumplimiento legal de nuestro entorno informático

| | |
|---|---|
| **Documento** | Solicitud de auditoría de el cumplimiento legal de nuestro entorno informático |
| **De** | Gerente General, EPS AGUAS DEL SUR S.A. |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 26 de octubre de 2026 |
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

Un usuario del servicio nos pidió saber qué datos suyos tratamos y por qué su deuda apareció en un tercero. Somos empresa pública, estamos sujetos al gobierno digital, tratamos datos de 86 000 conexiones y no tenemos registro de actividades de tratamiento. El sistema comercial es un producto con licencia que nadie ha conciliado con las instalaciones.

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

1. Saber qué normas nos alcanzan como entidad pública y regulada, además de la ley de datos personales.
2. Saber qué significa tratar el banco de datos de 86 000 conexiones en términos de obligaciones y de riesgo.
3. Saber qué sistemas nuestros tratan datos personales y cuáles no, porque el SCADA y el control de acceso a la planta no son lo mismo.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | Pedimos este servicio de control al Órgano de Control Institucional, con conocimiento del Directorio y de OTASS |
| **Contraparte designada** | Nuestro Gerente de Administración, de quien depende el Departamento de Tecnologías de la Información |
| **Canal único** | Toda solicitud entra y sale por la mesa de partes institucional y el correo del Órgano de Control Institucional, con número de expediente por cada solicitud |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 2 de noviembre de 2026. Trabajo de campo del 3 de noviembre de 2026 al 23 de noviembre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 24 de noviembre de 2026 y el 30 de noviembre de 2026. Informe entre el 1 de diciembre de 2026 y el 7 de diciembre de 2026 |
| **Horas que financiamos** | Hasta 222 horas de la comisión. Unas 44 de planificación, 133 de trabajo de campo, 18 de comunicación de resultados y 27 de informe. Más que eso no lo pagamos |
| **Horas que podemos dedicarles** | Nuestra área de tecnologías de la información dedica unas 48 horas al mes al proceso que van a auditar, entre sus 6 personas. No pueden pedirle más tiempo que ese |
| **Presupuesto que aprobamos** | S/ 16 095, a tarifa de referencia de S/ 110 la hora de supervisión, S/ 85 la de jefe de comisión y S/ 60 la de integrante, sin viáticos |
| **Confidencialidad** | Todo lo que les entregamos es confidencial. Lo guardan en un repositorio privado, cifrado, con la marca CONFIDENCIAL — USO ACADÉMICO, y al cierre conservan solo lo que el informe cite |
| **Lo que no autorizamos** | Ninguna prueba se ejecuta sobre nuestros sistemas en esta etapa. Lo que pedimos es un plan. Si el plan incluye pruebas, dirá cuáles y nos pedirá autorización escrita antes |
| **Las personas** | En su plan y en su informe nos nombran por el cargo, no por el nombre |

## 7. Lo que les entregamos

Lo que sigue lo entregamos **a solicitud escrita**, indicando para qué lo necesitan y qué procedimiento lo va a usar. Los documentos propios de esta materia van ya como anexos de esta solicitud. Los demás se entregan por el canal único, en la carpeta que indica la tabla.

| Documento | Qué contiene | Dónde está |
|---|---|---|
| `registro-datos-y-licencias.md` | El registro de actividades de tratamiento que armamos a pedido, y el inventario de software instalado contra las licencias | Anexo 1 |
| `contratos-proveedores.md` | Nuestros contratos con terceros que tratan información nuestra, con o sin cláusula de encargo | Anexo 2 |
| `plan-institucional-extracto.md` | Lo que declaramos sobre nuestras obligaciones | [`documentos/plan-institucional-extracto.md`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/documentos/plan-institucional-extracto.md) |
| `organigrama-y-accesos.md` | Qué área responde por cada obligación, si alguna lo hace | [`documentos/organigrama-y-accesos.md`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/documentos/organigrama-y-accesos.md) |
| `incidente-detallado.md` | El incidente del periodo, para evaluar si activó un deber de notificación | [`documentos/incidente-detallado.md`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/documentos/incidente-detallado.md) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/empleados.csv` | Nuestra planilla del periodo, con ingresos y ceses | 312 registros · 264 activos · 48 cesados en el periodo |
| `datos/proveedores.csv` | Nuestro maestro de proveedores | 156 registros · 156 activos |
| `datos/usuarios_erp.csv` | Los usuarios de nuestro sistema principal, con perfil, último acceso y segundo factor | 199 registros · 199 habilitados · 199 sin segundo factor |
| `datos/pagos.csv` | Nuestros pagos del periodo | 19281 registros · S/ 28 844 992 en total |

Atentamente,

**Gerente General**
EPS AGUAS DEL SUR S.A.

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
| 6 | Padrón de contribuyentes o usuarios | Nombre, documento, domicilio, deuda | Recaudación y prestación del servicio | Obligación legal | No requerido | Indefinido | No |

#### Lo que la organización responde

| Pregunta | Respuesta |
|---|---|
| ¿Está inscrito el banco de datos ante la autoridad? | «No consta la inscripción» |
| ¿Existe un responsable de protección de datos designado? | «No» |
| ¿Se informa a los titulares sobre el tratamiento? | «En el contrato hay una cláusula» |
| ¿Cómo se atiende un pedido de acceso o supresión? | «Nunca nos han pedido» |
| ¿Se autorizó el flujo transfronterizo? | «No sabíamos que había que hacerlo» |
| ¿Hay medidas de seguridad documentadas para estos datos? | «Las del sistema» |
| ¿Se evaluó el impacto del tratamiento de datos sensibles? | «No» |

### Parte 2 · Inventario de software instalado

Extraído de 31 estaciones de trabajo con la herramienta de inventario. Se entrega el consolidado.

| Software | Versión | Instalaciones | Licencias adquiridas | Diferencia | Tipo de licencia | ¿Soporte vigente? |
|---|---|---|---|---|---|---|
| Suite ofimática | 2021 | 120 | 120 | **+0** | Perpetua | No |
| Sistema operativo de escritorio | 11 | 72 | 35 | **-37** | Suscripción anual | No |
| Antivirus corporativo | — | 57 | 48 | **-9** | Perpetua | Vencido |
| Compresor de archivos | — | 102 | 18 | **-84** | Perpetua | No |
| Lector de PDF | — | 151 | 151 | **+0** | Libre / GPL | No |
| Editor de imágenes | — | 7 | 2 | **-5** | Libre / MIT | No |
| Herramienta de diseño | — | 7 | 0 | **-7** | Perpetua | No |
| Cliente de base de datos | — | 7 | 7 | **+0** | Suscripción anual | No |
| Software de contabilidad | — | 11 | 9 | **-2** | Perpetua | No |

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
| **D. Leg. 1412 y D. S. 029-2021-PCM** | Obligaciones de gobierno digital y seguridad de la información |

### Anexo 2 · `contratos-proveedores.md`

### Contrato 1 · Servicio de planilla y gestión de personal

| Campo | Contenido |
|---|---|
| Proveedor | **Servicios Pacífico S.A.C.** · RUC 20354002494 |
| Objeto | Procesamiento de planilla, boletas electrónicas y declaraciones a la autoridad tributaria |
| Vigencia | Del 1 de julio de 2023 al 28 de julio de 2025, con **renovación automática** salvo aviso con 30 días de anticipación |
| Contraprestación | S/ 3 396.00 mensuales |
| Datos que trata | Nombres, documento de identidad, domicilio, cuenta bancaria, remuneraciones, descuentos judiciales y **datos de salud del personal en descanso médico** |
| Dónde se alojan | «Servidores del proveedor» |
| Contacto | Elena Condori Maquera |

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
| Proveedor | **Grupo Continental E.I.R.L.** · RUC 20492212991 |
| Objeto | Alojamiento de SCADA de plantas y reservorios y respaldo externo |
| Vigencia | Del 1 de enero de 2024 al 31 de diciembre de 2026 |
| Contraprestación | S/ 13 014.00 mensuales, más consumo variable |
| Ubicación de los servidores | «Centros de datos del proveedor» — no se especifica el país |
| Nivel de servicio comprometido | «Alta disponibilidad» |
| Contacto | Iván Zapana Condori |

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

---

[Semana 11](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 11·07](CASO-11-07-instituto-vertiente-sur.md) · **Caso 11·08** · [Caso 11·09](CASO-11-09-servicios-mineros-cordillera.md) · [Encargo 11](../../ENCARGOS-UNIDAD-II/CASO-11-cumplimiento-legal.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
