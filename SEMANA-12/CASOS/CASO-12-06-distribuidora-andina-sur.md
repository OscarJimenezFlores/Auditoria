[Semana 12](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 12·05](CASO-12-05-transportes-sur-andino.md) · **Caso 12·06** · [Caso 12·07](CASO-12-07-instituto-vertiente-sur.md) · [Encargo 12](../../ENCARGOS-UNIDAD-II/CASO-12-seguridad-del-canal-digital.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>DISTRIBUIDORA ANDINA DEL SUR S.A.C.</strong><br>
  <em>Solicitud de auditoría · Seguridad del canal digital y de las aplicaciones expuestas</em>
</div>

---

# Solicitud de auditoría de la seguridad de nuestro canal digital y de las aplicaciones que exponemos

| | |
|---|---|
| **Documento** | Solicitud de auditoría de la seguridad de nuestro canal digital y de las aplicaciones que exponemos |
| **De** | Gerente General, por acuerdo de la Junta General de Accionistas, DISTRIBUIDORA ANDINA DEL SUR S.A.C. |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 2 de noviembre de 2026 |
| **Clasificación** | CONFIDENCIAL — USO ACADÉMICO |

---

## 1. Quiénes somos

Somos **DISTRIBUIDORA ANDINA DEL SUR S.A.C.**, distribución mayorista de consumo masivo, con sede en Tacna, con almacenes en Tacna e Ilo. Operamos desde hace 21 años, con 157 trabajadores estables y 34 en temporada alta. Nuestros ingresos son de S/ 68.4 millones y atendemos tacna, Moquegua y frontera.

Nos regulan o supervisan **SUNAT · INDECOPI · SUNAFIL · ANPD**.

Nuestra área de tecnologías de la información tiene **4 personas**. La encabeza nuestro jefe de Sistemas, que reporta a Gerencia de Administración y Finanzas. El presupuesto de tecnologías de la información es de **S/ 742 000**, el 1.08 % de nuestros ingresos. El objetivo que le declaramos a esa área es «Restablecer el control interno sobre el ciclo de compras y pagos y conciliar el inventario».

**Lo que más nos cuesta.** El módulo de almacén del ERP se dejó de usar para la gestión de ubicaciones y se sostiene en hojas de cálculo. El inventario contable y el físico difieren en promedio 4.7 %.

### 1.1. Los sistemas con los que operamos

| Sistema | Qué es | Dónde corre | Desde | ¿Tiene soporte vigente? |
|---|---|---|---|---|
| **ERP comercial** | Producto peruano con módulos de compras, ventas, almacén, tesorería y contabilidad | Servidor propio | 2015 | Sí |
| **Fuerza de ventas móvil** | App del proveedor del ERP | Nube del proveedor | 2020 | Sí |
| **Facturación electrónica** | OSE contratado | SaaS | 2018 | Sí |
| **Gestión de almacén** | Módulo del ERP más hojas de cálculo paralelas | Mixto | 2015 | Parcial |
| **Portal de pedidos para clientes** | Desarrollo propio | Hosting compartido | 2022 | No |

### 1.2. Nuestros procesos

1. Compras a proveedores y reposición
2. Almacenamiento y despacho
3. Venta y distribución en ruta
4. Cobranza y crédito a clientes
5. Tesorería y pagos
6. Contabilidad y cierre

## 2. Por qué pedimos esta auditoría

El portal de pedidos para clientes corre en un hosting compartido, lo desarrolló un practicante y nadie lo actualiza desde 2022. Recoge datos de clientes, RUC y pedidos. Un cliente reportó que vio los pedidos de otro. Queremos una revisión de seguridad antes de que INDECOPI o la Autoridad de datos personales pregunten.

## 3. Lo que ya sabemos que no está bien

Estos riesgos los tenemos identificados y no los hemos tratado.

- Segregación de funciones inexistente en compras y pagos
- Inventario sin conciliación sistemática
- Portal de clientes sin mantenimiento ni pruebas de seguridad

**Lo que nos pasó en el periodo. Fraccionamiento de compras bajo el umbral de aprobación.** Una revisión interna detectó órdenes de compra fraccionadas sistemáticamente bajo el umbral de S/ 5 000 que exige aprobación de gerencia. El mismo usuario registraba y aprobaba. El ERP lo permitía por configuración de perfiles.

## 4. Lo que ya nos dijeron

- Nuestra revisión interna de 2025, hecha por Contabilidad a pedido de la gerencia, detectó el fraccionamiento de compras y la autoaprobación en el ERP. No tuvo forma de informe y no generó un plan de acción.
- La auditoría financiera externa de 2025 nos recomendó segregar el registro y la aprobación de pagos. La recomendación está abierta.
- Nunca nos han auditado el ERP ni el portal de pedidos.

## 5. Lo que queremos saber

Son las preguntas que la dirección espera que la auditoría responda. Cómo responderlas, con qué alcance, con qué criterios y con qué procedimientos, es lo que esperamos de su plan.

1. Saber de qué responde el hosting compartido y de qué respondemos nosotros, según sus condiciones.
2. Saber cómo se verifica que un cliente no pueda ver los pedidos de otro sin hacer una prueba sobre el portal.
3. Saber qué se puede concluir sobre la seguridad del código si quien lo escribió ya no está.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | La Junta General de Accionistas dispuso una auditoría externa del control interno sobre tecnologías de la información, tras la revisión interna que detectó el fraccionamiento |
| **Contraparte designada** | Nuestro Gerente de Administración y Finanzas, de quien depende el Jefe de Sistemas |
| **Canal único** | Toda solicitud entra y sale por el correo de la Gerencia de Administración y Finanzas, con copia a Contabilidad y al Jefe de Sistemas |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 9 de noviembre de 2026. Trabajo de campo del 11 de noviembre de 2026 al 27 de noviembre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 30 de noviembre de 2026 y el 2 de diciembre de 2026. Informe entre el 3 de diciembre de 2026 y el 4 de diciembre de 2026 |
| **Horas que financiamos** | Hasta 183 horas de la comisión. Unas 37 de planificación, 110 de trabajo de campo, 15 de comunicación de resultados y 21 de informe. Más que eso no lo pagamos |
| **Horas que podemos dedicarles** | Nuestra área de tecnologías de la información dedica unas 64 horas al mes al proceso que van a auditar, entre sus 4 personas. No pueden pedirle más tiempo que ese |
| **Presupuesto que aprobamos** | S/ 13 268, a tarifa de referencia de S/ 110 la hora de supervisión, S/ 85 la de jefe de comisión y S/ 60 la de integrante, sin viáticos. Si necesitan ir a nuestras sedes fuera de Tacna, los pasajes y viáticos se presupuestan aparte |
| **Confidencialidad** | Todo lo que les entregamos es confidencial. Lo guardan en un repositorio privado, cifrado, con la marca CONFIDENCIAL — USO ACADÉMICO, y al cierre conservan solo lo que el informe cite |
| **Lo que no autorizamos** | Ninguna prueba se ejecuta sobre nuestros sistemas en esta etapa. Lo que pedimos es un plan. Si el plan incluye pruebas, dirá cuáles y nos pedirá autorización escrita antes |
| **Las personas** | En su plan y en su informe nos nombran por el cargo, no por el nombre |

## 7. Lo que les entregamos

Lo que sigue lo entregamos **a solicitud escrita**, indicando para qué lo necesitan y qué procedimiento lo va a usar. Los documentos propios de esta materia van ya como anexos de esta solicitud. Los demás se entregan por el canal único, en la carpeta que indica la tabla.

| Documento | Qué contiene | Dónde está |
|---|---|---|
| `canal-digital-y-aplicaciones.md` | El inventario de nuestro canal digital, armado a pedido, con la arquitectura declarada, la autenticación, los certificados, los componentes de terceros y los formularios | Anexo 1 |
| `contratos-proveedores.md` | El contrato con el proveedor del portal, con o sin matriz de responsabilidad compartida | [`documentos/contratos-proveedores.md`](../../../CASOS/EMPRESA-06-distribuidora-andina-sur/documentos/contratos-proveedores.md) |
| `sgsi-politica-y-aplicabilidad.md` | Los controles del Anexo A que declaramos sobre el canal | [`documentos/sgsi-politica-y-aplicabilidad.md`](../../../CASOS/EMPRESA-06-distribuidora-andina-sur/documentos/sgsi-politica-y-aplicabilidad.md) |
| `registro-datos-y-licencias.md` | Los datos personales que cada formulario recoge, según nuestro registro de tratamiento | [`documentos/registro-datos-y-licencias.md`](../../../CASOS/EMPRESA-06-distribuidora-andina-sur/documentos/registro-datos-y-licencias.md) |
| `incidente-detallado.md` | El incidente del periodo | [`documentos/incidente-detallado.md`](../../../CASOS/EMPRESA-06-distribuidora-andina-sur/documentos/incidente-detallado.md) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/usuarios_erp.csv` | Los usuarios de nuestro sistema principal, con perfil, último acceso y segundo factor | 119 registros · 119 habilitados · 119 sin segundo factor |
| `datos/pagos.csv` | Nuestros pagos del periodo | 17798 registros · S/ 26 668 856 en total |

Atentamente,

**Gerente General, por acuerdo de la Junta General de Accionistas**
DISTRIBUIDORA ANDINA DEL SUR S.A.C.

---

## Anexos

### Anexo 1 · `canal-digital-y-aplicaciones.md`

### 1. Qué es este documento

Es el inventario de lo que la organización tiene publicado en internet, con lo que se sabe de cada pieza. Lo armó TI junto con el proveedor del portal a pedido del equipo auditor. **Antes de este pedido no existía.**

> **La organización no autoriza pruebas técnicas sobre estos activos.** Autoriza entregar documentación, planos y configuraciones declaradas, y responder preguntas. Toda prueba activa requeriría una autorización escrita de Gerencia que no se ha solicitado ni otorgado. El producto de esta semana es un **plan**, no una ejecución.

### 2. Inventario del canal digital

| ID | Activo expuesto | Dirección declarada | Qué hace | Quién lo mantiene | Autenticación |
|---|---|---|---|---|---|
| AP-01 | Portal institucional | `https://www.andinasur.com.pe` | Información pública y formularios de contacto | Proveedor del portal | No |
| AP-02 | Formulario de contacto | `https://www.andinasur.com.pe/contacto` | Recoge nombre, documento, teléfono y correo | Proveedor del portal | No |
| AP-03 | Fuerza de ventas móvil | Dominio del proveedor, no registrado | App del proveedor del ERP | Proveedor del sistema | Usuario y contraseña |
| AP-04 | Consola de administración del portal | `https://www.andinasur.com.pe/gestor` | Publicación de contenido | Proveedor del portal | Usuario y contraseña |
| AP-05 | Correo web | `https://correo.andinasur.com.pe` | Acceso al correo del personal | Proveedor de correo | Usuario y contraseña |
| AP-06 | Servicio de archivos compartidos | `https://archivos.andinasur.com.pe` | Intercambio de archivos con terceros | TI | Enlace con clave |
| AP-07 | Facturación electrónica | Consola del proveedor | OSE contratado | Proveedor | Usuario y contraseña |

> **La organización no sabe cuántos subdominios tiene publicados.** El dominio lo administra Marta Ilaquita Choque, con la cuenta `dominios@andinasur.com.pe`, cuya contraseña «la tienen dos personas».

### 3. Arquitectura declarada

```
Internet
   │
   ├── Portal institucional (AP-01, AP-02, AP-04)  ── hosting compartido contratado
   │        └── base de datos del portal, en el mismo hosting
   │
   ├── Fuerza de ventas móvil (AP-03)  ── Nube del proveedor
   │        └── base de datos del sistema, en el mismo servidor que la aplicación
   │
   └── Correo y archivos (AP-05, AP-06)  ── servicios de terceros

Red interna ── sin segmentación declarada ── un único segmento para oficinas y servidores
```

**Lo que la organización no puede precisar.** Dónde termina el hosting del proveedor y dónde empieza su propia responsabilidad. El contrato no tiene matriz de responsabilidad compartida.

### 4. Autenticación y gestión de sesión, tal como se declara

| Aspecto | Lo que la organización declara |
|---|---|
| Longitud mínima de contraseña | 7 caracteres |
| Complejidad exigida | «Una mayúscula y un número» |
| Caducidad de la contraseña | No |
| Bloqueo por intentos fallidos | «Creo que el portal lo trae» |
| Segundo factor de autenticación | No |
| Duración de la sesión | «Hasta que el usuario cierre el navegador» |
| Cierre de sesión por inactividad | No |
| Recuperación de contraseña | «Se pide a TI por teléfono o por el grupo de mensajería» |
| Registro de accesos fallidos | No existe |

### 5. Transporte y certificados

| Activo | Certificado | Vence | Redirección de HTTP a HTTPS | Cabeceras de seguridad declaradas |
|---|---|---|---|---|
| AP-01 Portal | Emitido por autoridad gratuita | 24 de febrero de 2026 | Sí | «Las que trae el hosting» |
| AP-03 Fuerza de ventas móvil | Del proveedor | 5 de mayo de 2026 | No | No se revisaron nunca |
| AP-05 Correo | Del proveedor | Lo gestiona el proveedor | Sí | Las del proveedor |

### 6. Componentes de terceros en el portal

Lo que el proveedor del portal reporta como instalado.

| Componente | Versión instalada | ¿Se actualiza? | ¿Quién decide actualizar? |
|---|---|---|---|
| Gestor de contenidos | 6.4 | «Cuando el proveedor avisa» | Proveedor |
| Plantilla del sitio | 3.8 | No desde la instalación | Nadie |
| Complemento de formularios | 4.1 | No | Nadie |
| Complemento de estadísticas | 1.5 | No | Nadie |
| Biblioteca de carrusel de imágenes | 2.4.0 | No | Nadie |
| Etiqueta de analítica de terceros | — | Automática | El proveedor de analítica |
| Chat de atención de terceros | — | Automática | El proveedor del chat |

> **Hay 24 componentes instalados en total.** El proveedor entregó la versión de los siete más visibles y declaró que del resto «habría que revisar en el panel».

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
| Revisión de código del Fuerza de ventas móvil | Nunca | — | — |
| Revisión del proveedor del portal | Nunca | El propio proveedor | Correo con el resumen |

### 9. Lo que la organización responde

| Pregunta del auditor | Respuesta |
|---|---|
| ¿Quién es el responsable del portal dentro de la organización? | «Silvia Choque Chura coordina con el proveedor» |
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

[Semana 12](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 12·05](CASO-12-05-transportes-sur-andino.md) · **Caso 12·06** · [Caso 12·07](CASO-12-07-instituto-vertiente-sur.md) · [Encargo 12](../../ENCARGOS-UNIDAD-II/CASO-12-seguridad-del-canal-digital.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
