[Semana 12](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 12·07](CASO-12-07-instituto-vertiente-sur.md) · **Caso 12·08** · [Caso 12·09](CASO-12-09-servicios-mineros-cordillera.md) · [Encargo 12](../../ENCARGOS-UNIDAD-II/CASO-12-seguridad-del-canal-digital.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>EPS AGUAS DEL SUR S.A.</strong><br>
  <em>Solicitud de auditoría · Seguridad del canal digital y de las aplicaciones expuestas</em>
</div>

---

# Solicitud de auditoría de la seguridad de nuestro canal digital y de las aplicaciones que exponemos

| | |
|---|---|
| **Documento** | Solicitud de auditoría de la seguridad de nuestro canal digital y de las aplicaciones que exponemos |
| **De** | Gerente General, EPS AGUAS DEL SUR S.A. |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 2 de noviembre de 2026 |
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

Publicamos el portal con consulta de recibos, el formulario de reclamos propio y el pago en línea por una pasarela de terceros. Nunca hemos tenido revisión de seguridad. Un usuario reportó que pudo ver el recibo de otra conexión cambiando el número en la dirección web. SUNASS y la Autoridad de datos personales pueden sancionarnos.

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

1. Saber qué nos exigen los lineamientos de seguridad digital y SUNASS sobre nuestros servicios en internet.
2. Saber de qué responde la pasarela de pagos y de qué respondemos nosotros.
3. Saber qué hacer con el reporte del usuario que vio el recibo de otra conexión, sobre 86 000 conexiones, sin exponer más recibos.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | Pedimos este servicio de control al Órgano de Control Institucional, con conocimiento del Directorio y de OTASS |
| **Contraparte designada** | Nuestro Gerente de Administración, de quien depende el Departamento de Tecnologías de la Información |
| **Canal único** | Toda solicitud entra y sale por la mesa de partes institucional y el correo del Órgano de Control Institucional, con número de expediente por cada solicitud |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 9 de noviembre de 2026. Trabajo de campo del 11 de noviembre de 2026 al 27 de noviembre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 30 de noviembre de 2026 y el 2 de diciembre de 2026. Informe entre el 3 de diciembre de 2026 y el 4 de diciembre de 2026 |
| **Horas que financiamos** | Hasta 222 horas de la comisión. Unas 44 de planificación, 133 de trabajo de campo, 18 de comunicación de resultados y 27 de informe. Más que eso no lo pagamos |
| **Horas que podemos dedicarles** | Nuestra área de tecnologías de la información dedica unas 96 horas al mes al proceso que van a auditar, entre sus 6 personas. No pueden pedirle más tiempo que ese |
| **Presupuesto que aprobamos** | S/ 16 095, a tarifa de referencia de S/ 110 la hora de supervisión, S/ 85 la de jefe de comisión y S/ 60 la de integrante, sin viáticos |
| **Confidencialidad** | Todo lo que les entregamos es confidencial. Lo guardan en un repositorio privado, cifrado, con la marca CONFIDENCIAL — USO ACADÉMICO, y al cierre conservan solo lo que el informe cite |
| **Lo que no autorizamos** | Ninguna prueba se ejecuta sobre nuestros sistemas en esta etapa. Lo que pedimos es un plan. Si el plan incluye pruebas, dirá cuáles y nos pedirá autorización escrita antes |
| **Las personas** | En su plan y en su informe nos nombran por el cargo, no por el nombre |

## 7. Lo que les entregamos

Lo que sigue lo entregamos **a solicitud escrita**, indicando para qué lo necesitan y qué procedimiento lo va a usar. Los documentos propios de esta materia van ya como anexos de esta solicitud. Los demás se entregan por el canal único, en la carpeta que indica la tabla.

| Documento | Qué contiene | Dónde está |
|---|---|---|
| `canal-digital-y-aplicaciones.md` | El inventario de nuestro canal digital, armado a pedido, con la arquitectura declarada, la autenticación, los certificados, los componentes de terceros y los formularios | Anexo 1 |
| `contratos-proveedores.md` | El contrato con el proveedor del portal, con o sin matriz de responsabilidad compartida | [`documentos/contratos-proveedores.md`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/documentos/contratos-proveedores.md) |
| `sgsi-politica-y-aplicabilidad.md` | Los controles del Anexo A que declaramos sobre el canal | [`documentos/sgsi-politica-y-aplicabilidad.md`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/documentos/sgsi-politica-y-aplicabilidad.md) |
| `registro-datos-y-licencias.md` | Los datos personales que cada formulario recoge, según nuestro registro de tratamiento | [`documentos/registro-datos-y-licencias.md`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/documentos/registro-datos-y-licencias.md) |
| `incidente-detallado.md` | El incidente del periodo | [`documentos/incidente-detallado.md`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/documentos/incidente-detallado.md) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/usuarios_erp.csv` | Los usuarios de nuestro sistema principal, con perfil, último acceso y segundo factor | 199 registros · 199 habilitados · 199 sin segundo factor |
| `datos/pagos.csv` | Nuestros pagos del periodo | 19281 registros · S/ 28 844 992 en total |

Atentamente,

**Gerente General**
EPS AGUAS DEL SUR S.A.

---

## Anexos

### Anexo 1 · `canal-digital-y-aplicaciones.md`

### 1. Qué es este documento

Es el inventario de lo que la organización tiene publicado en internet, con lo que se sabe de cada pieza. Lo armó TI junto con el proveedor del portal a pedido del equipo auditor. **Antes de este pedido no existía.**

> **La organización no autoriza pruebas técnicas sobre estos activos.** Autoriza entregar documentación, planos y configuraciones declaradas, y responder preguntas. Toda prueba activa requeriría una autorización escrita de Gerencia que no se ha solicitado ni otorgado. El producto de esta semana es un **plan**, no una ejecución.

### 2. Inventario del canal digital

| ID | Activo expuesto | Dirección declarada | Qué hace | Quién lo mantiene | Autenticación |
|---|---|---|---|---|---|
| AP-01 | Portal institucional | `https://www.aguassur.gob.pe` | Información pública y formularios de contacto | Proveedor del portal | No |
| AP-02 | Formulario de contacto | `https://www.aguassur.gob.pe/contacto` | Recoge nombre, documento, teléfono y correo | Proveedor del portal | No |
| AP-03 | Atención de reclamos | `https://servicios.aguassur.gob.pe` | Formulario web y hoja de cálculo | TI | Usuario y contraseña |
| AP-04 | Consola de administración del portal | `https://www.aguassur.gob.pe/gestor` | Publicación de contenido | Proveedor del portal | Usuario y contraseña |
| AP-05 | Correo web | `https://correo.aguassur.gob.pe` | Acceso al correo del personal | Proveedor de correo | Usuario y contraseña |
| AP-06 | Servicio de archivos compartidos | `https://archivos.aguassur.gob.pe` | Intercambio de archivos con terceros | TI | Enlace con clave |
| AP-07 | Tablero de indicadores de gerencia | Consola del proveedor | Hoja de cálculo publicada por un enlace de solo lectura | Proveedor | Usuario y contraseña |

> **La organización no sabe cuántos subdominios tiene publicados.** El dominio lo administra Rocío Medina Vargas, con la cuenta `dominios@aguassur.gob.pe`, cuya contraseña «la tienen dos personas».

### 3. Arquitectura declarada

```
Internet
   │
   ├── Portal institucional (AP-01, AP-02, AP-04)  ── hosting compartido contratado
   │        └── base de datos del portal, en el mismo hosting
   │
   ├── Atención de reclamos (AP-03)  ── Hosting propio
   │        └── base de datos del sistema, en el mismo servidor que la aplicación
   │
   └── Correo y archivos (AP-05, AP-06)  ── servicios de terceros

Red interna ── sin segmentación declarada ── un único segmento para oficinas y servidores
```

**Lo que la organización no puede precisar.** Dónde termina el hosting del proveedor y dónde empieza su propia responsabilidad. El contrato no tiene matriz de responsabilidad compartida.

### 4. Autenticación y gestión de sesión, tal como se declara

| Aspecto | Lo que la organización declara |
|---|---|
| Longitud mínima de contraseña | 4 caracteres |
| Complejidad exigida | «Letras y números» |
| Caducidad de la contraseña | Cada 90 días en el sistema principal, no en el portal |
| Bloqueo por intentos fallidos | No |
| Segundo factor de autenticación | Solo en el correo, es opcional |
| Duración de la sesión | «Hasta que el usuario cierre el navegador» |
| Cierre de sesión por inactividad | «El sistema cierra a las 8 horas» |
| Recuperación de contraseña | «Se pide a TI por teléfono o por el grupo de mensajería» |
| Registro de accesos fallidos | No se revisa |

### 5. Transporte y certificados

| Activo | Certificado | Vence | Redirección de HTTP a HTTPS | Cabeceras de seguridad declaradas |
|---|---|---|---|---|
| AP-01 Portal | Emitido por autoridad gratuita | 3 de diciembre de 2026 | No se verificó | «Las que trae el hosting» |
| AP-03 Atención de reclamos | Autofirmado | 24 de octubre de 2026 | Sí | No se revisaron nunca |
| AP-05 Correo | Del proveedor | Lo gestiona el proveedor | Sí | Las del proveedor |

### 6. Componentes de terceros en el portal

Lo que el proveedor del portal reporta como instalado.

| Componente | Versión instalada | ¿Se actualiza? | ¿Quién decide actualizar? |
|---|---|---|---|
| Gestor de contenidos | 6.7 | «Cuando el proveedor avisa» | Proveedor |
| Plantilla del sitio | 1.5 | No desde la instalación | Nadie |
| Complemento de formularios | 3.8 | No | Nadie |
| Complemento de estadísticas | 3.2 | No | Nadie |
| Biblioteca de carrusel de imágenes | 1.1.8 | No | Nadie |
| Etiqueta de analítica de terceros | — | Automática | El proveedor de analítica |
| Chat de atención de terceros | — | Automática | El proveedor del chat |

> **Hay 24 componentes instalados en total.** El proveedor entregó la versión de los siete más visibles y declaró que del resto «habría que revisar en el panel».

### 7. Datos personales que recoge cada formulario

| Formulario | Campos | Finalidad declarada | Dónde se almacena | ¿Hay cláusula de consentimiento? |
|---|---|---|---|---|
| Contacto general | Nombre, documento, teléfono, correo, mensaje | «Atender la consulta» | Base del portal y correo de la cuenta de contacto | Casilla sin texto legal |
| Mesa de partes virtual | Nombre, documento, teléfono, correo, detalle y archivos adjuntos | «Recibir documentos del ciudadano» | Correo de mesa de partes y carpeta compartida | No |
| Postulación de personal | Nombre, documento, dirección, currículum | «Procesos de selección» | Carpeta compartida en el servicio de archivos | No |
| Suscripción a novedades | Nombre y correo | «Enviar información» | Servicio de correo masivo de un tercero | No |

### 8. Revisiones de seguridad previas

| Revisión | Cuándo | Quién la hizo | Informe |
|---|---|---|---|
| Prueba de penetración | Nunca | — | — |
| Análisis de vulnerabilidades del portal | Nunca | — | — |
| Revisión de código del Atención de reclamos | Nunca | — | — |
| Revisión del proveedor del portal | 2023 | — | — |

### 9. Lo que la organización responde

| Pregunta del auditor | Respuesta |
|---|---|
| ¿Quién es el responsable del portal dentro de la organización? | «Carmen Calisaya Bravo coordina con el proveedor» |
| ¿Existe un ambiente de pruebas del portal? | «El proveedor dice que tiene uno» |
| ¿Se revisa el registro de accesos del portal? | «No» |
| ¿Qué pasa si el portal queda fuera de servicio? | «Se llama al proveedor» |
| ¿Hay inventario de los datos que viajan a terceros? | «No» |
| ¿La organización autoriza pruebas sobre el portal? | «Habría que verlo con Gerencia y con el proveedor» |
| ¿Dónde está alojado físicamente el hosting? | «No lo sabemos» |

### 10. Marco aplicable

| Marco | Qué aporta como criterio |
|---|---|
| **OWASP ASVS 4.0.3** · V1 Arquitectura, diseño y modelado de amenazas | Exige arquitectura documentada y responsabilidades delimitadas con el proveedor |
| **OWASP ASVS 4.0.3** · V2 Autenticación | Requisitos verificables de contraseña, bloqueo y segundo factor |
| **OWASP ASVS 4.0.3** · V3 Gestión de sesión | Caducidad, invalidación y atributos de la cookie de sesión |
| **OWASP ASVS 4.0.3** · V7 Manejo de errores y registro | Qué se registra, qué no se registra y por cuánto tiempo |
| **OWASP ASVS 4.0.3** · V8 Protección de datos | Tratamiento, retención y minimización del dato recogido |
| **OWASP ASVS 4.0.3** · V9 Comunicaciones | Cifrado en tránsito y configuración del transporte |
| **OWASP ASVS 4.0.3** · V14 Configuración | Inventario de componentes, dependencias y endurecimiento |
| **OWASP Top 10:2021** · A01, A02, A05, A06 y A07 | Las categorías de riesgo con las que se ordena el hallazgo |
| **OWASP Web Security Testing Guide** 4.2 | El procedimiento de prueba que el plan referencia, sin ejecutarlo |
| **NTP-ISO/IEC 27001:2022** · A.5.23, A.8.9, A.8.24 y A.8.32 | El control organizativo que respalda cada requisito técnico |
| **Ley 29733** y **D. S. 016-2024-JUS** | Consentimiento, finalidad y flujo transfronterizo de lo que recogen los formularios |
| **D. Leg. 1412**, **D. S. 029-2021-PCM** y las normas de la Secretaría de Gobierno y Transformación Digital | Seguridad digital y servicios digitales exigibles a la entidad |

---

[Semana 12](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 12·07](CASO-12-07-instituto-vertiente-sur.md) · **Caso 12·08** · [Caso 12·09](CASO-12-09-servicios-mineros-cordillera.md) · [Encargo 12](../../ENCARGOS-UNIDAD-II/CASO-12-seguridad-del-canal-digital.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
