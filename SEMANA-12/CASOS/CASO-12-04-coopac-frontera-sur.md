[Semana 12](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 12·03](CASO-12-03-municipalidad-alto-selva.md) · **Caso 12·04** · [Caso 12·05](CASO-12-05-transportes-sur-andino.md) · [Encargo 12](../../ENCARGOS-UNIDAD-II/CASO-12-seguridad-del-canal-digital.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>COOPAC FRONTERA SUR</strong><br>
  <em>Solicitud de auditoría · Seguridad del canal digital y de las aplicaciones expuestas</em>
</div>

---

# Solicitud de auditoría de la seguridad de nuestro canal digital y de las aplicaciones que exponemos

| | |
|---|---|
| **Documento** | Solicitud de auditoría de la seguridad de nuestro canal digital y de las aplicaciones que exponemos |
| **De** | Gerente General, por acuerdo del Consejo de Vigilancia, COOPAC FRONTERA SUR |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 2 de noviembre de 2026 |
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

Nuestra banca por internet para socios está en la nube del proveedor y nadie en la cooperativa sabe dónde termina la responsabilidad del proveedor. La SBS nos exige seguridad del canal digital con requisitos propios, y el acceso indebido a expedientes mostró que el registro de accesos no existe. El Consejo quiere auditar el canal antes de que lo haga el regulador.

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

1. Saber qué nos exige la SBS sobre el canal digital y cómo se relaciona con los estándares técnicos con los que nos van a revisar.
2. Saber de qué responde el proveedor del core, que opera la banca por internet en su nube, según el contrato que tenemos.
3. Saber qué nivel de exigencia corresponde a un canal con 21 400 socios y datos financieros.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | El Consejo de Vigilancia lo acordó a propuesta de la Unidad de Auditoría Interna, dentro del plan anual que remitimos a la SBS |
| **Contraparte designada** | Nuestro Gerente General, con el Oficial de Seguridad de la Información como enlace |
| **Canal único** | Toda solicitud entra y sale por el correo de la Unidad de Auditoría Interna, que registra cada solicitud en su sistema de seguimiento |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 9 de noviembre de 2026. Trabajo de campo del 11 de noviembre de 2026 al 27 de noviembre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 30 de noviembre de 2026 y el 2 de diciembre de 2026. Informe entre el 3 de diciembre de 2026 y el 4 de diciembre de 2026 |
| **Horas que financiamos** | Hasta 185 horas de la comisión. Unas 37 de planificación, 111 de trabajo de campo, 15 de comunicación de resultados y 22 de informe. Más que eso no lo pagamos |
| **Horas que podemos dedicarles** | Nuestra área de tecnologías de la información dedica unas 80 horas al mes al proceso que van a auditar, entre sus 5 personas. No pueden pedirle más tiempo que ese |
| **Presupuesto que aprobamos** | S/ 13 412, a tarifa de referencia de S/ 110 la hora de supervisión, S/ 85 la de jefe de comisión y S/ 60 la de integrante, sin viáticos. Si necesitan ir a nuestras sedes fuera de Tacna, los pasajes y viáticos se presupuestan aparte |
| **Confidencialidad** | Todo lo que les entregamos es confidencial. Lo guardan en un repositorio privado, cifrado, con la marca CONFIDENCIAL — USO ACADÉMICO, y al cierre conservan solo lo que el informe cite |
| **Lo que no autorizamos** | Ninguna prueba se ejecuta sobre nuestros sistemas en esta etapa. Lo que pedimos es un plan. Si el plan incluye pruebas, dirá cuáles y nos pedirá autorización escrita antes |
| **Las personas** | En su plan y en su informe nos nombran por el cargo, no por el nombre |

## 7. Lo que les entregamos

Lo que sigue lo entregamos **a solicitud escrita**, indicando para qué lo necesitan y qué procedimiento lo va a usar. Los documentos propios de esta materia van ya como anexos de esta solicitud. Los demás se entregan por el canal único, en la carpeta que indica la tabla.

| Documento | Qué contiene | Dónde está |
|---|---|---|
| `canal-digital-y-aplicaciones.md` | El inventario de nuestro canal digital, armado a pedido, con la arquitectura declarada, la autenticación, los certificados, los componentes de terceros y los formularios | Anexo 1 |
| `contratos-proveedores.md` | El contrato con el proveedor del portal, con o sin matriz de responsabilidad compartida | [`documentos/contratos-proveedores.md`](../../../CASOS/EMPRESA-04-coopac-frontera-sur/documentos/contratos-proveedores.md) |
| `sgsi-politica-y-aplicabilidad.md` | Los controles del Anexo A que declaramos sobre el canal | [`documentos/sgsi-politica-y-aplicabilidad.md`](../../../CASOS/EMPRESA-04-coopac-frontera-sur/documentos/sgsi-politica-y-aplicabilidad.md) |
| `registro-datos-y-licencias.md` | Los datos personales que cada formulario recoge, según nuestro registro de tratamiento | [`documentos/registro-datos-y-licencias.md`](../../../CASOS/EMPRESA-04-coopac-frontera-sur/documentos/registro-datos-y-licencias.md) |
| `incidente-detallado.md` | El incidente del periodo | [`documentos/incidente-detallado.md`](../../../CASOS/EMPRESA-04-coopac-frontera-sur/documentos/incidente-detallado.md) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/usuarios_erp.csv` | Los usuarios de nuestro sistema principal, con perfil, último acceso y segundo factor | 75 registros · 75 habilitados · 75 sin segundo factor |
| `datos/pagos.csv` | Nuestros pagos del periodo | 28016 registros · S/ 42 214 064 en total |

Atentamente,

**Gerente General, por acuerdo del Consejo de Vigilancia**
COOPAC FRONTERA SUR

---

## Anexos

### Anexo 1 · `canal-digital-y-aplicaciones.md`

### 1. Qué es este documento

Es el inventario de lo que la organización tiene publicado en internet, con lo que se sabe de cada pieza. Lo armó TI junto con el proveedor del portal a pedido del equipo auditor. **Antes de este pedido no existía.**

> **La organización no autoriza pruebas técnicas sobre estos activos.** Autoriza entregar documentación, planos y configuraciones declaradas, y responder preguntas. Toda prueba activa requeriría una autorización escrita de Gerencia que no se ha solicitado ni otorgado. El producto de esta semana es un **plan**, no una ejecución.

### 2. Inventario del canal digital

| ID | Activo expuesto | Dirección declarada | Qué hace | Quién lo mantiene | Autenticación |
|---|---|---|---|---|---|
| AP-01 | Portal institucional | `https://www.fronterasur.com.pe` | Información pública y formularios de contacto | Proveedor del portal | No |
| AP-02 | Formulario de contacto | `https://www.fronterasur.com.pe/contacto` | Recoge nombre, documento, teléfono y correo | Proveedor del portal | No |
| AP-03 | Banca por internet para socios | Dominio del proveedor, no registrado | Módulo web del mismo proveedor | Proveedor del sistema | Usuario y contraseña |
| AP-04 | Consola de administración del portal | `https://www.fronterasur.com.pe/gestor` | Publicación de contenido | Proveedor del portal | Usuario y contraseña |
| AP-05 | Correo web | `https://correo.fronterasur.com.pe` | Acceso al correo del personal | Proveedor de correo | Usuario y contraseña |
| AP-06 | Servicio de archivos compartidos | `https://archivos.fronterasur.com.pe` | Intercambio de archivos con terceros | TI | Enlace con clave |
| AP-07 | Central de riesgos | Consola del proveedor | Consulta a bureau externo por servicio web | Proveedor | Usuario y contraseña |

> **La organización no sabe cuántos subdominios tiene publicados.** El dominio lo administra Teresa Condori Cutipa, con la cuenta `dominios@fronterasur.com.pe`, cuya contraseña «la tienen dos personas».

### 3. Arquitectura declarada

```
Internet
   │
   ├── Portal institucional (AP-01, AP-02, AP-04)  ── hosting compartido contratado
   │        └── base de datos del portal, en el mismo hosting
   │
   ├── Banca por internet para socios (AP-03)  ── Nube del proveedor
   │        └── base de datos del sistema, en el mismo servidor que la aplicación
   │
   └── Correo y archivos (AP-05, AP-06)  ── servicios de terceros

Red interna ── sin segmentación declarada ── una red plana con red inalámbrica de invitados
```

**Lo que la organización no puede precisar.** Dónde termina el hosting del proveedor y dónde empieza su propia responsabilidad. El contrato no tiene matriz de responsabilidad compartida.

### 4. Autenticación y gestión de sesión, tal como se declara

| Aspecto | Lo que la organización declara |
|---|---|
| Longitud mínima de contraseña | 8 caracteres |
| Complejidad exigida | «Letras y números» |
| Caducidad de la contraseña | Cada 90 días en el sistema principal, no en el portal |
| Bloqueo por intentos fallidos | No |
| Segundo factor de autenticación | No |
| Duración de la sesión | «Hasta que el usuario cierre el navegador» |
| Cierre de sesión por inactividad | «El sistema cierra a las 8 horas» |
| Recuperación de contraseña | «Se pide a TI por teléfono o por el grupo de mensajería» |
| Registro de accesos fallidos | No se revisa |

### 5. Transporte y certificados

| Activo | Certificado | Vence | Redirección de HTTP a HTTPS | Cabeceras de seguridad declaradas |
|---|---|---|---|---|
| AP-01 Portal | Emitido por autoridad gratuita | 25 de noviembre de 2026 | No se verificó | «Las que trae el hosting» |
| AP-03 Banca por internet para socios | Del proveedor | 21 de noviembre de 2026 | No se verificó | No se revisaron nunca |
| AP-05 Correo | Del proveedor | Lo gestiona el proveedor | Sí | Las del proveedor |

### 6. Componentes de terceros en el portal

Lo que el proveedor del portal reporta como instalado.

| Componente | Versión instalada | ¿Se actualiza? | ¿Quién decide actualizar? |
|---|---|---|---|
| Gestor de contenidos | 6.4 | «Cuando el proveedor avisa» | Proveedor |
| Plantilla del sitio | 2.5 | No desde la instalación | Nadie |
| Complemento de formularios | 3.4 | No | Nadie |
| Complemento de estadísticas | 3.0 | No | Nadie |
| Biblioteca de carrusel de imágenes | 2.0.1 | No | Nadie |
| Etiqueta de analítica de terceros | — | Automática | El proveedor de analítica |
| Chat de atención de terceros | — | Automática | El proveedor del chat |

> **Hay 27 componentes instalados en total.** El proveedor entregó la versión de los siete más visibles y declaró que del resto «habría que revisar en el panel».

### 7. Datos personales que recoge cada formulario

| Formulario | Campos | Finalidad declarada | Dónde se almacena | ¿Hay cláusula de consentimiento? |
|---|---|---|---|---|
| Contacto general | Nombre, documento, teléfono, correo, mensaje | «Atender la consulta» | Base del portal y correo de la cuenta de contacto | Casilla sin texto legal |
| Reclamo o queja | Nombre, documento, teléfono, correo, detalle y archivos adjuntos | «Registrar el reclamo» | Base del portal | No |
| Postulación de personal | Nombre, documento, dirección, currículum | «Procesos de selección» | Carpeta compartida en el servicio de archivos | No |
| Suscripción a novedades | Nombre y correo | «Enviar información» | Servicio de correo masivo de un tercero | No |

### 8. Revisiones de seguridad previas

| Revisión | Cuándo | Quién la hizo | Informe |
|---|---|---|---|
| Prueba de penetración | Nunca | — | — |
| Análisis de vulnerabilidades del portal | Nunca | — | — |
| Revisión de código del Banca por internet para socios | Nunca | — | — |
| Revisión del proveedor del portal | 2023 | — | — |

### 9. Lo que la organización responde

| Pregunta del auditor | Respuesta |
|---|---|
| ¿Quién es el responsable del portal dentro de la organización? | «Óscar Ramos Bravo coordina con el proveedor» |
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

---

[Semana 12](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 12·03](CASO-12-03-municipalidad-alto-selva.md) · **Caso 12·04** · [Caso 12·05](CASO-12-05-transportes-sur-andino.md) · [Encargo 12](../../ENCARGOS-UNIDAD-II/CASO-12-seguridad-del-canal-digital.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
