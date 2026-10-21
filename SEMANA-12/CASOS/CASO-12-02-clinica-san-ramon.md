[Semana 12](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 12·01](CASO-12-01-agroexportadora-valle-viejo.md) · **Caso 12·02** · [Caso 12·03](CASO-12-03-municipalidad-alto-selva.md) · [Encargo 12](../../ENCARGOS-UNIDAD-II/CASO-12-seguridad-del-canal-digital.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>CLÍNICA SAN RAMÓN S.A.C.</strong><br>
  <em>Solicitud de auditoría · Seguridad del canal digital y de las aplicaciones expuestas</em>
</div>

---

# Solicitud de auditoría de la seguridad de nuestro canal digital y de las aplicaciones que exponemos

| | |
|---|---|
| **Documento** | Solicitud de auditoría de la seguridad de nuestro canal digital y de las aplicaciones que exponemos |
| **De** | Gerente General, por acuerdo del Directorio, CLÍNICA SAN RAMÓN S.A.C. |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 2 de noviembre de 2026 |
| **Clasificación** | CONFIDENCIAL — USO ACADÉMICO |

---

## 1. Quiénes somos

Somos **CLÍNICA SAN RAMÓN S.A.C.**, salud privada · clínica de mediana complejidad, con sede en Cercado de Tacna. Operamos desde hace 23 años, con 214 trabajadores estables y 46 médicos por honorarios. Nuestros ingresos son de S/ 38.9 millones y atendemos tacna y pacientes de Arica, Chile.

Nos regulan o supervisan **SUSALUD · DIRESA Tacna · SUNAT · ANPD (datos de salud) · DIGEMID**.

Nuestra área de tecnologías de la información tiene **4 personas**. La encabeza nuestro coordinador de TI, técnico titulado, 3 años en el puesto, que reporta a Gerencia General. El presupuesto de tecnologías de la información es de **S/ 686 000**, el 1.76 % de nuestros ingresos. El objetivo que le declaramos a esa área es «Eliminar la carga manual entre sistemas clínicos y cumplir la protección reforzada de datos de salud».

**Lo que más nos cuesta.** La integración entre laboratorio y HIS es por archivo plano copiado a mano dos veces al día. En 2025 se detectaron 34 resultados adjuntados al paciente equivocado.

### 1.1. Los sistemas con los que operamos

| Sistema | Qué es | Dónde corre | Desde | ¿Tiene soporte vigente? |
|---|---|---|---|---|
| **HIS — historia clínica electrónica** | Producto peruano, módulos de admisión, consulta, hospitalización y farmacia | Servidor propio en sala de máquinas | 2018 | Sí, soporte por horas |
| **Facturación y convenios con aseguradoras** | Módulo del mismo HIS | Mismo servidor | 2018 | Sí |
| **Laboratorio (LIS)** | Software del proveedor de equipos, integrado por archivos planos | PC de laboratorio | 2020 | Parcial |
| **Imágenes (PACS)** | Servidor de imágenes del proveedor de tomógrafo | Servidor dedicado | 2022 | Sí |
| **Planillas y asistencia** | Sistema local con marcador biométrico | PC de RR. HH. | 2017 | No |

### 1.2. Nuestros procesos

1. Admisión y filiación del paciente
2. Atención ambulatoria y hospitalización
3. Laboratorio e imágenes
4. Farmacia y dispensación
5. Facturación a aseguradoras
6. Gestión de historias clínicas

## 2. Por qué pedimos esta auditoría

Publicamos el portal con citas en línea, un formulario que recoge datos de salud y el acceso a resultados de laboratorio para pacientes. Nunca hemos tenido una revisión de seguridad. Tras el incidente de los resultados mal asignados, el Directorio quiere saber si un paciente puede ver los resultados de otro desde internet.

## 3. Lo que ya sabemos que no está bien

Estos riesgos los tenemos identificados y no los hemos tratado.

- Datos sensibles de salud sin cifrado en reposo
- Integración manual entre sistemas clínicos
- Cuentas de médicos compartidas en consultorios

**Lo que nos pasó en el periodo. Resultados de laboratorio asignados a pacientes equivocados.** El proceso manual de carga del LIS al HIS asignó 34 resultados a historias clínicas incorrectas durante seis semanas. Se detectó por reclamo de un paciente. No existe registro de quién ejecutó cada carga.

## 4. Lo que ya nos dijeron

- Nunca nos han auditado un sistema de información.
- SUSALUD supervisó en 2025 la gestión de historias clínicas, a raíz del reclamo, y nos dejó una medida correctiva sobre el registro de quién accede a la historia. Está abierta.
- La auditoría financiera externa no revisa los sistemas clínicos. Se limita a facturación.

## 5. Lo que queremos saber

Son las preguntas que la dirección espera que la auditoría responda. Cómo responderlas, con qué alcance, con qué criterios y con qué procedimientos, es lo que esperamos de su plan.

1. Saber si un paciente puede ver los resultados de otro desde internet, y qué debe cumplir el acceso a resultados para que no pueda.
2. Saber qué nos exigen SUSALUD y la ley de datos personales sobre el formulario de citas, que recoge datos de salud.
3. Saber de qué responde el proveedor del HIS, que opera el módulo de resultados en línea con un contrato de soporte por horas.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | El Directorio acordó encargar esta auditoría después del reclamo del paciente, y la Gerencia General la contrata |
| **Contraparte designada** | Nuestro Gerente General, con el Coordinador de TI como enlace técnico |
| **Canal único** | Toda solicitud entra y sale por el correo de la Gerencia General, con copia al Coordinador de TI y al responsable de historias clínicas |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 9 de noviembre de 2026. Trabajo de campo del 11 de noviembre de 2026 al 27 de noviembre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 30 de noviembre de 2026 y el 2 de diciembre de 2026. Informe entre el 3 de diciembre de 2026 y el 4 de diciembre de 2026 |
| **Horas que financiamos** | Hasta 188 horas de la comisión. Unas 38 de planificación, 113 de trabajo de campo, 15 de comunicación de resultados y 22 de informe. Más que eso no lo pagamos |
| **Horas que podemos dedicarles** | Nuestra área de tecnologías de la información dedica unas 64 horas al mes al proceso que van a auditar, entre sus 4 personas. No pueden pedirle más tiempo que ese |
| **Presupuesto que aprobamos** | S/ 13 630, a tarifa de referencia de S/ 110 la hora de supervisión, S/ 85 la de jefe de comisión y S/ 60 la de integrante, sin viáticos |
| **Confidencialidad** | Todo lo que les entregamos es confidencial. Lo guardan en un repositorio privado, cifrado, con la marca CONFIDENCIAL — USO ACADÉMICO, y al cierre conservan solo lo que el informe cite |
| **Lo que no autorizamos** | Ninguna prueba se ejecuta sobre nuestros sistemas en esta etapa. Lo que pedimos es un plan. Si el plan incluye pruebas, dirá cuáles y nos pedirá autorización escrita antes |
| **Las personas** | En su plan y en su informe nos nombran por el cargo, no por el nombre |

## 7. Lo que les entregamos

Lo que sigue lo entregamos **a solicitud escrita**, indicando para qué lo necesitan y qué procedimiento lo va a usar. Los documentos propios de esta materia van ya como anexos de esta solicitud. Los demás se entregan por el canal único, en la carpeta que indica la tabla.

| Documento | Qué contiene | Dónde está |
|---|---|---|
| `canal-digital-y-aplicaciones.md` | El inventario de nuestro canal digital, armado a pedido, con la arquitectura declarada, la autenticación, los certificados, los componentes de terceros y los formularios | Anexo 1 |
| `contratos-proveedores.md` | El contrato con el proveedor del portal, con o sin matriz de responsabilidad compartida | [`documentos/contratos-proveedores.md`](../../../CASOS/EMPRESA-02-clinica-san-ramon/documentos/contratos-proveedores.md) |
| `sgsi-politica-y-aplicabilidad.md` | Los controles del Anexo A que declaramos sobre el canal | [`documentos/sgsi-politica-y-aplicabilidad.md`](../../../CASOS/EMPRESA-02-clinica-san-ramon/documentos/sgsi-politica-y-aplicabilidad.md) |
| `registro-datos-y-licencias.md` | Los datos personales que cada formulario recoge, según nuestro registro de tratamiento | [`documentos/registro-datos-y-licencias.md`](../../../CASOS/EMPRESA-02-clinica-san-ramon/documentos/registro-datos-y-licencias.md) |
| `incidente-detallado.md` | El incidente del periodo | [`documentos/incidente-detallado.md`](../../../CASOS/EMPRESA-02-clinica-san-ramon/documentos/incidente-detallado.md) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/usuarios_erp.csv` | Los usuarios de nuestro sistema principal, con perfil, último acceso y segundo factor | 143 registros · 143 habilitados · 143 sin segundo factor |
| `datos/pagos.csv` | Nuestros pagos del periodo | 10129 registros · S/ 15 599 828 en total |

Atentamente,

**Gerente General, por acuerdo del Directorio**
CLÍNICA SAN RAMÓN S.A.C.

---

## Anexos

### Anexo 1 · `canal-digital-y-aplicaciones.md`

### 1. Qué es este documento

Es el inventario de lo que la organización tiene publicado en internet, con lo que se sabe de cada pieza. Lo armó TI junto con el proveedor del portal a pedido del equipo auditor. **Antes de este pedido no existía.**

> **La organización no autoriza pruebas técnicas sobre estos activos.** Autoriza entregar documentación, planos y configuraciones declaradas, y responder preguntas. Toda prueba activa requeriría una autorización escrita de Gerencia que no se ha solicitado ni otorgado. El producto de esta semana es un **plan**, no una ejecución.

### 2. Inventario del canal digital

| ID | Activo expuesto | Dirección declarada | Qué hace | Quién lo mantiene | Autenticación |
|---|---|---|---|---|---|
| AP-01 | Portal institucional | `https://www.sanramon.com.pe` | Información pública y formularios de contacto | Proveedor del portal | No |
| AP-02 | Formulario de contacto | `https://www.sanramon.com.pe/contacto` | Recoge nombre, documento, teléfono y correo | Proveedor del portal | No |
| AP-03 | Consulta en línea de la organización | Dominio del proveedor, no registrado | Formulario web publicado por el proveedor del portal | Proveedor del sistema | Usuario y contraseña |
| AP-04 | Consola de administración del portal | `https://www.sanramon.com.pe/gestor` | Publicación de contenido | Proveedor del portal | Usuario y contraseña |
| AP-05 | Correo web | `https://correo.sanramon.com.pe` | Acceso al correo del personal | Proveedor de correo | Usuario y contraseña |
| AP-06 | Servicio de archivos compartidos | `https://archivos.sanramon.com.pe` | Intercambio de archivos con terceros | TI | Enlace con clave |
| AP-07 | Tablero de indicadores de gerencia | Consola del proveedor | Hoja de cálculo publicada por un enlace de solo lectura | Proveedor | Usuario y contraseña |

> **La organización no sabe cuántos subdominios tiene publicados.** El dominio lo administra Álvaro Yufra Núñez, con la cuenta `dominios@sanramon.com.pe`, cuya contraseña «la tienen dos personas».

### 3. Arquitectura declarada

```
Internet
   │
   ├── Portal institucional (AP-01, AP-02, AP-04)  ── hosting compartido contratado
   │        └── base de datos del portal, en el mismo hosting
   │
   ├── Consulta en línea de la organización (AP-03)  ── Hosting contratado
   │        └── base de datos del sistema, en el mismo servidor que la aplicación
   │
   └── Correo y archivos (AP-05, AP-06)  ── servicios de terceros

Red interna ── sin segmentación declarada ── equipos de usuario, servidores y cámaras en la misma red
```

**Lo que la organización no puede precisar.** Dónde termina el hosting del proveedor y dónde empieza su propia responsabilidad. El contrato no tiene matriz de responsabilidad compartida.

### 4. Autenticación y gestión de sesión, tal como se declara

| Aspecto | Lo que la organización declara |
|---|---|
| Longitud mínima de contraseña | 8 caracteres |
| Complejidad exigida | «Letras y números» |
| Caducidad de la contraseña | No |
| Bloqueo por intentos fallidos | No |
| Segundo factor de autenticación | Solo en el correo, es opcional |
| Duración de la sesión | «Hasta que el usuario cierre el navegador» |
| Cierre de sesión por inactividad | No |
| Recuperación de contraseña | «Se pide a TI por teléfono o por el grupo de mensajería» |
| Registro de accesos fallidos | No se revisa |

### 5. Transporte y certificados

| Activo | Certificado | Vence | Redirección de HTTP a HTTPS | Cabeceras de seguridad declaradas |
|---|---|---|---|---|
| AP-01 Portal | Emitido por autoridad gratuita | 17 de setiembre de 2026 | No se verificó | «Las que trae el hosting» |
| AP-03 Consulta en línea de la organización | Emitido por autoridad gratuita | 12 de enero de 2026 | No | No se revisaron nunca |
| AP-05 Correo | Del proveedor | Lo gestiona el proveedor | Sí | Las del proveedor |

### 6. Componentes de terceros en el portal

Lo que el proveedor del portal reporta como instalado.

| Componente | Versión instalada | ¿Se actualiza? | ¿Quién decide actualizar? |
|---|---|---|---|
| Gestor de contenidos | 5.5 | «Cuando el proveedor avisa» | Proveedor |
| Plantilla del sitio | 1.1 | No desde la instalación | Nadie |
| Complemento de formularios | 5.3 | No | Nadie |
| Complemento de estadísticas | 2.3 | No | Nadie |
| Biblioteca de carrusel de imágenes | 2.8.3 | No | Nadie |
| Etiqueta de analítica de terceros | — | Automática | El proveedor de analítica |
| Chat de atención de terceros | — | Automática | El proveedor del chat |

> **Hay 32 componentes instalados en total.** El proveedor entregó la versión de los siete más visibles y declaró que del resto «habría que revisar en el panel».

### 7. Datos personales que recoge cada formulario

| Formulario | Campos | Finalidad declarada | Dónde se almacena | ¿Hay cláusula de consentimiento? |
|---|---|---|---|---|
| Contacto general | Nombre, documento, teléfono, correo, mensaje | «Atender la consulta» | Base del portal y correo de la cuenta de contacto | Casilla sin texto legal |
| Reclamo o queja | Nombre, documento, teléfono, correo, detalle y archivos adjuntos | «Registrar el reclamo» | Base del portal | Casilla sin texto legal |
| Postulación de personal | Nombre, documento, dirección, currículum | «Procesos de selección» | Carpeta compartida en el servicio de archivos | No |
| Suscripción a novedades | Nombre y correo | «Enviar información» | Servicio de correo masivo de un tercero | No |

### 8. Revisiones de seguridad previas

| Revisión | Cuándo | Quién la hizo | Informe |
|---|---|---|---|
| Prueba de penetración | Nunca | — | — |
| Análisis de vulnerabilidades del portal | Nunca | — | — |
| Revisión de código del Consulta en línea de la organización | Nunca | — | — |
| Revisión del proveedor del portal | Nunca | — | Correo con el resumen |

### 9. Lo que la organización responde

| Pregunta del auditor | Respuesta |
|---|---|
| ¿Quién es el responsable del portal dentro de la organización? | «Nelson Apaza Copaja coordina con el proveedor» |
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

[Semana 12](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 12·01](CASO-12-01-agroexportadora-valle-viejo.md) · **Caso 12·02** · [Caso 12·03](CASO-12-03-municipalidad-alto-selva.md) · [Encargo 12](../../ENCARGOS-UNIDAD-II/CASO-12-seguridad-del-canal-digital.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
