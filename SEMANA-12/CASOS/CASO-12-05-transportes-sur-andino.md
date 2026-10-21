[Semana 12](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 12·04](CASO-12-04-coopac-frontera-sur.md) · **Caso 12·05** · [Caso 12·06](CASO-12-06-distribuidora-andina-sur.md) · [Encargo 12](../../ENCARGOS-UNIDAD-II/CASO-12-seguridad-del-canal-digital.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>TRANSPORTES SUR ANDINO S.A.</strong><br>
  <em>Solicitud de auditoría · Seguridad del canal digital y de las aplicaciones expuestas</em>
</div>

---

# Solicitud de auditoría de la seguridad de nuestro canal digital y de las aplicaciones que exponemos

| | |
|---|---|
| **Documento** | Solicitud de auditoría de la seguridad de nuestro canal digital y de las aplicaciones que exponemos |
| **De** | Gerente General, por encargo del Directorio, TRANSPORTES SUR ANDINO S.A. |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 2 de noviembre de 2026 |
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

La venta en línea y la aplicación de pasajeros las desarrolló un tercero cuyo contrato venció y que ya no responde. Recogen nombre, documento, tarjeta y ruta de cada pasajero. La venta duplicada de 78 asientos demostró que nadie controla el canal. El Directorio quiere saber qué tenemos expuesto y de quién es la responsabilidad.

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

1. Saber qué podemos revisar del canal en línea si no tenemos proveedor con contrato ni código, y qué tenemos que hacer antes.
2. Saber si procesamos datos de tarjeta nosotros o una pasarela, y qué nos exige cada caso.
3. Saber qué falla permitió vender 78 asientos dos veces y cómo se clasifica.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | El Directorio lo pidió después de la fiscalización de SUTRAN y la Gerencia General contrata el servicio |
| **Contraparte designada** | Nuestro Gerente de Operaciones, de quien depende el Jefe de Sistemas |
| **Canal único** | Toda solicitud entra y sale por el correo de la Gerencia de Operaciones, con copia al Jefe de Sistemas |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 9 de noviembre de 2026. Trabajo de campo del 11 de noviembre de 2026 al 27 de noviembre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 30 de noviembre de 2026 y el 2 de diciembre de 2026. Informe entre el 3 de diciembre de 2026 y el 4 de diciembre de 2026 |
| **Horas que financiamos** | Hasta 193 horas de la comisión. Unas 39 de planificación, 116 de trabajo de campo, 15 de comunicación de resultados y 23 de informe. Más que eso no lo pagamos |
| **Horas que podemos dedicarles** | Nuestra área de tecnologías de la información dedica unas 64 horas al mes al proceso que van a auditar, entre sus 4 personas. No pueden pedirle más tiempo que ese |
| **Presupuesto que aprobamos** | S/ 13 992, a tarifa de referencia de S/ 110 la hora de supervisión, S/ 85 la de jefe de comisión y S/ 60 la de integrante, sin viáticos. Si necesitan ir a nuestras sedes fuera de Tacna, los pasajes y viáticos se presupuestan aparte |
| **Confidencialidad** | Todo lo que les entregamos es confidencial. Lo guardan en un repositorio privado, cifrado, con la marca CONFIDENCIAL — USO ACADÉMICO, y al cierre conservan solo lo que el informe cite |
| **Lo que no autorizamos** | Ninguna prueba se ejecuta sobre nuestros sistemas en esta etapa. Lo que pedimos es un plan. Si el plan incluye pruebas, dirá cuáles y nos pedirá autorización escrita antes |
| **Las personas** | En su plan y en su informe nos nombran por el cargo, no por el nombre |

## 7. Lo que les entregamos

Lo que sigue lo entregamos **a solicitud escrita**, indicando para qué lo necesitan y qué procedimiento lo va a usar. Los documentos propios de esta materia van ya como anexos de esta solicitud. Los demás se entregan por el canal único, en la carpeta que indica la tabla.

| Documento | Qué contiene | Dónde está |
|---|---|---|
| `canal-digital-y-aplicaciones.md` | El inventario de nuestro canal digital, armado a pedido, con la arquitectura declarada, la autenticación, los certificados, los componentes de terceros y los formularios | Anexo 1 |
| `contratos-proveedores.md` | El contrato con el proveedor del portal, con o sin matriz de responsabilidad compartida | [`documentos/contratos-proveedores.md`](../../../CASOS/EMPRESA-05-transportes-sur-andino/documentos/contratos-proveedores.md) |
| `sgsi-politica-y-aplicabilidad.md` | Los controles del Anexo A que declaramos sobre el canal | [`documentos/sgsi-politica-y-aplicabilidad.md`](../../../CASOS/EMPRESA-05-transportes-sur-andino/documentos/sgsi-politica-y-aplicabilidad.md) |
| `registro-datos-y-licencias.md` | Los datos personales que cada formulario recoge, según nuestro registro de tratamiento | [`documentos/registro-datos-y-licencias.md`](../../../CASOS/EMPRESA-05-transportes-sur-andino/documentos/registro-datos-y-licencias.md) |
| `incidente-detallado.md` | El incidente del periodo | [`documentos/incidente-detallado.md`](../../../CASOS/EMPRESA-05-transportes-sur-andino/documentos/incidente-detallado.md) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/usuarios_erp.csv` | Los usuarios de nuestro sistema principal, con perfil, último acceso y segundo factor | 181 registros · 181 habilitados · 181 sin segundo factor |
| `datos/pagos.csv` | Nuestros pagos del periodo | 13694 registros · S/ 20 728 005 en total |

Atentamente,

**Gerente General, por encargo del Directorio**
TRANSPORTES SUR ANDINO S.A.

---

## Anexos

### Anexo 1 · `canal-digital-y-aplicaciones.md`

### 1. Qué es este documento

Es el inventario de lo que la organización tiene publicado en internet, con lo que se sabe de cada pieza. Lo armó TI junto con el proveedor del portal a pedido del equipo auditor. **Antes de este pedido no existía.**

> **La organización no autoriza pruebas técnicas sobre estos activos.** Autoriza entregar documentación, planos y configuraciones declaradas, y responder preguntas. Toda prueba activa requeriría una autorización escrita de Gerencia que no se ha solicitado ni otorgado. El producto de esta semana es un **plan**, no una ejecución.

### 2. Inventario del canal digital

| ID | Activo expuesto | Dirección declarada | Qué hace | Quién lo mantiene | Autenticación |
|---|---|---|---|---|---|
| AP-01 | Portal institucional | `https://www.surandino.com.pe` | Información pública y formularios de contacto | Proveedor del portal | No |
| AP-02 | Formulario de contacto | `https://www.surandino.com.pe/contacto` | Recoge nombre, documento, teléfono y correo | Proveedor del portal | No |
| AP-03 | Venta en línea y app de pasajeros | `https://servicios.surandino.com.pe` | Desarrollo tercerizado en 2021 | TI | Usuario y contraseña |
| AP-04 | Consola de administración del portal | `https://www.surandino.com.pe/gestor` | Publicación de contenido | Proveedor del portal | Usuario y contraseña |
| AP-05 | Correo web | `https://correo.surandino.com.pe` | Acceso al correo del personal | Proveedor de correo | Usuario y contraseña |
| AP-06 | Servicio de archivos compartidos | `https://archivos.surandino.com.pe` | Intercambio de archivos con terceros | TI | Enlace con clave |
| AP-07 | GPS y control de flota | Consola del proveedor | Servicio del proveedor de rastreo | Proveedor | Usuario y contraseña |

> **La organización no sabe cuántos subdominios tiene publicados.** El dominio lo administra Gabriela Ramos Quispe, con la cuenta `dominios@surandino.com.pe`, cuya contraseña «la tienen dos personas».

### 3. Arquitectura declarada

```
Internet
   │
   ├── Portal institucional (AP-01, AP-02, AP-04)  ── hosting compartido contratado
   │        └── base de datos del portal, en el mismo hosting
   │
   ├── Venta en línea y app de pasajeros (AP-03)  ── Nube pública
   │        └── base de datos del sistema, en el mismo servidor que la aplicación
   │
   └── Correo y archivos (AP-05, AP-06)  ── servicios de terceros

Red interna ── sin segmentación declarada ── equipos de usuario, servidores y cámaras en la misma red
```

**Lo que la organización no puede precisar.** Dónde termina el hosting del proveedor y dónde empieza su propia responsabilidad. El contrato no tiene matriz de responsabilidad compartida.

### 4. Autenticación y gestión de sesión, tal como se declara

| Aspecto | Lo que la organización declara |
|---|---|
| Longitud mínima de contraseña | 7 caracteres |
| Complejidad exigida | No se exige |
| Caducidad de la contraseña | No |
| Bloqueo por intentos fallidos | No |
| Segundo factor de autenticación | No |
| Duración de la sesión | «Hasta que el usuario cierre el navegador» |
| Cierre de sesión por inactividad | No |
| Recuperación de contraseña | «Se pide a TI por teléfono o por el grupo de mensajería» |
| Registro de accesos fallidos | El proveedor dice que sí los guarda |

### 5. Transporte y certificados

| Activo | Certificado | Vence | Redirección de HTTP a HTTPS | Cabeceras de seguridad declaradas |
|---|---|---|---|---|
| AP-01 Portal | Emitido por autoridad gratuita | 2 de noviembre de 2026 | Sí | «Las que trae el hosting» |
| AP-03 Venta en línea y app de pasajeros | Del proveedor | 11 de mayo de 2026 | No se verificó | No se revisaron nunca |
| AP-05 Correo | Del proveedor | Lo gestiona el proveedor | Sí | Las del proveedor |

### 6. Componentes de terceros en el portal

Lo que el proveedor del portal reporta como instalado.

| Componente | Versión instalada | ¿Se actualiza? | ¿Quién decide actualizar? |
|---|---|---|---|
| Gestor de contenidos | 6.0 | «Cuando el proveedor avisa» | Proveedor |
| Plantilla del sitio | 3.3 | No desde la instalación | Nadie |
| Complemento de formularios | 2.1 | No | Nadie |
| Complemento de estadísticas | 1.2 | No | Nadie |
| Biblioteca de carrusel de imágenes | 1.4.5 | No | Nadie |
| Etiqueta de analítica de terceros | — | Automática | El proveedor de analítica |
| Chat de atención de terceros | — | Automática | El proveedor del chat |

> **Hay 20 componentes instalados en total.** El proveedor entregó la versión de los siete más visibles y declaró que del resto «habría que revisar en el panel».

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
| Revisión de código del Venta en línea y app de pasajeros | Nunca | — | — |
| Revisión del proveedor del portal | Nunca | — | — |

### 9. Lo que la organización responde

| Pregunta del auditor | Respuesta |
|---|---|
| ¿Quién es el responsable del portal dentro de la organización? | «Ana Cáceres Aguilar coordina con el proveedor» |
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

[Semana 12](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 12·04](CASO-12-04-coopac-frontera-sur.md) · **Caso 12·05** · [Caso 12·06](CASO-12-06-distribuidora-andina-sur.md) · [Encargo 12](../../ENCARGOS-UNIDAD-II/CASO-12-seguridad-del-canal-digital.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
