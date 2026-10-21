[Semana 09](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 09·03](CASO-09-03-municipalidad-alto-selva.md) · **Caso 09·04** · [Caso 09·05](CASO-09-05-transportes-sur-andino.md) · [Encargo 09](../../ENCARGOS-UNIDAD-II/CASO-09-ciclo-de-vida-del-software.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>COOPAC FRONTERA SUR</strong><br>
  <em>Solicitud de auditoría · Ciclo de vida del software</em>
</div>

---

# Solicitud de auditoría de el ciclo de vida de nuestro software

| | |
|---|---|
| **Documento** | Solicitud de auditoría de el ciclo de vida de nuestro software |
| **De** | Gerente General, por acuerdo del Consejo de Vigilancia, COOPAC FRONTERA SUR |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 12 de octubre de 2026 |
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

Los anexos que enviamos a la SBS se arman con consultas y macros que escribió un analista que pasó al área de riesgos. Cuando la SBS cambia un formato, él lo ajusta sin pedido, sin prueba y sin que nadie revise. Un anexo con un cálculo erróneo es una observación del regulador, y nuestra Unidad de Auditoría Interna quiere saber cuántas veces pudo ocurrir.

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

1. Saber si los anexos que enviamos a la SBS pueden haber salido con un cálculo erróneo, y cómo comprobarlo sobre un anexo real.
2. Saber si está bien que una persona del área de riesgos modifique y despliegue macros sobre la base del core.
3. Saber qué nos exige la Resolución SBS N.º 504-2021 sobre control de cambios y si lo cumplimos.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | El Consejo de Vigilancia lo acordó a propuesta de la Unidad de Auditoría Interna, dentro del plan anual que remitimos a la SBS |
| **Contraparte designada** | Nuestro Gerente General, con el Oficial de Seguridad de la Información como enlace |
| **Canal único** | Toda solicitud entra y sale por el correo de la Unidad de Auditoría Interna, que registra cada solicitud en su sistema de seguimiento |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 19 de octubre de 2026. Trabajo de campo del 20 de octubre de 2026 al 9 de noviembre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 10 de noviembre de 2026 y el 16 de noviembre de 2026. Informe entre el 17 de noviembre de 2026 y el 23 de noviembre de 2026 |
| **Horas que financiamos** | Hasta 185 horas de la comisión. Unas 37 de planificación, 111 de trabajo de campo, 15 de comunicación de resultados y 22 de informe. Más que eso no lo pagamos |
| **Horas que podemos dedicarles** | Nuestra área de tecnologías de la información dedica unas 200 horas al mes al proceso que van a auditar, entre sus 5 personas. No pueden pedirle más tiempo que ese |
| **Presupuesto que aprobamos** | S/ 13 412, a tarifa de referencia de S/ 110 la hora de supervisión, S/ 85 la de jefe de comisión y S/ 60 la de integrante, sin viáticos. Si necesitan ir a nuestras sedes fuera de Tacna, los pasajes y viáticos se presupuestan aparte |
| **Confidencialidad** | Todo lo que les entregamos es confidencial. Lo guardan en un repositorio privado, cifrado, con la marca CONFIDENCIAL — USO ACADÉMICO, y al cierre conservan solo lo que el informe cite |
| **Lo que no autorizamos** | Ninguna prueba se ejecuta sobre nuestros sistemas en esta etapa. Lo que pedimos es un plan. Si el plan incluye pruebas, dirá cuáles y nos pedirá autorización escrita antes |
| **Las personas** | En su plan y en su informe nos nombran por el cargo, no por el nombre |

## 7. Lo que les entregamos

Lo que sigue lo entregamos **a solicitud escrita**, indicando para qué lo necesitan y qué procedimiento lo va a usar. Los documentos propios de esta materia van ya como anexos de esta solicitud. Los demás se entregan por el canal único, en la carpeta que indica la tabla.

| Documento | Qué contiene | Dónde está |
|---|---|---|
| `ciclo-de-vida-del-software.md` | El expediente de nuestro software propio, con las métricas del repositorio, los despliegues y los pedidos de cambio del periodo | Anexo 1 |
| `contratos-proveedores.md` | Lo que dicen nuestros contratos sobre la propiedad del código y el soporte | [`documentos/contratos-proveedores.md`](../../../CASOS/EMPRESA-04-coopac-frontera-sur/documentos/contratos-proveedores.md) |
| `extracciones-y-registros.md` | Las extracciones del sistema principal y la bitácora que conservamos | [`documentos/extracciones-y-registros.md`](../../../CASOS/EMPRESA-04-coopac-frontera-sur/documentos/extracciones-y-registros.md) |
| `narrativa-proceso-compras.md` | Cómo opera el proceso que nuestro software soporta o alimenta | [`documentos/narrativa-proceso-compras.md`](../../../CASOS/EMPRESA-04-coopac-frontera-sur/documentos/narrativa-proceso-compras.md) |
| `organigrama-y-accesos.md` | Quién desarrolla, quién despliega y quién aprueba, según los accesos | [`documentos/organigrama-y-accesos.md`](../../../CASOS/EMPRESA-04-coopac-frontera-sur/documentos/organigrama-y-accesos.md) |

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

### Anexo 1 · `ciclo-de-vida-del-software.md`

### 1. El sistema desarrollado internamente

| Campo | Contenido |
|---|---|
| Sistema | **Reportes regulatorios a la SBS** |
| Descripción | Consultas y macros desarrolladas internamente sobre la base del core financiero, que arman los anexos que se envían al regulador |
| En producción desde | 2018 |
| Lenguaje y plataforma | SQL y Visual Basic para Aplicaciones |
| Personas que lo mantienen hoy | 2 |
| ¿Existe documentación técnica? | Solo el manual de usuario |
| ¿Existe control de versiones? | Sí, repositorio interno |
| ¿Existe ambiente de pruebas separado de producción? | Sí, pero con datos de producción copiados |

> **Contexto que da la organización.** «Las construyó un analista de TI que pasó al área de riesgos. Las sigue tocando cuando la SBS cambia un anexo. Desde entonces se le hacen ajustes cuando algo falla o cuando el área pide un cambio.»

### 2. Métricas del repositorio

Extraídas con `git log` sobre el periodo auditado.

| Métrica | Valor |
|---|---|
| Commits en el periodo | 256 |
| Autores distintos | 2 |
| Commits del autor principal | 63 % del total |
| Ramas activas | 8 |
| Ramas sin fusionar con más de 90 días | 2 |
| Commits directos a la rama principal | **85 %** |
| Pull Requests abiertos en el periodo | 0 |
| Pull Requests con revisión de un segundo | **1** |
| Etiquetas de versión creadas | 1 |
| Commits con mensaje de una sola palabra | 50 |
| Archivos con más de 1 000 líneas | 1 |
| ¿Hay pruebas automatizadas en el repositorio? | No |

### 3. Últimos despliegues a producción

| Fecha | Versión | Qué se desplegó | ¿Hubo etiqueta? | ¿Hubo prueba previa? | ¿Se pudo revertir? |
|---|---|---|---|---|---|
| 2025-04-08 | — | Corrección de error en reportes | No | No | No |
| 2025-06-14 | v1.8 | Ajuste de cálculo | Sí | Parcial | No |
| 2025-01-15 | v1.3 | Nuevo campo solicitado por el área | Sí | Parcial | No |
| 2025-04-16 | — | Ajuste de cálculo | No | Parcial | No |
| 2025-02-21 | — | Corrección urgente en producción | No | No | No |
| 2025-03-19 | v1.3 | Corrección de error en reportes | No | No | No |

### 4. Trazabilidad de requisitos

La organización entrega los pedidos de cambio del periodo, tal como los registra.

| N.º | Fecha | Solicitado por | Qué se pidió | ¿Especificación escrita? | ¿Aceptación formal? | ¿Se desplegó? |
|---|---|---|---|---|---|---|
| 01 | 2025-01-21 | Contabilidad | Nuevo reporte mensual | Correo | Verbal | Sí |
| 02 | 2025-01-23 | Comercial | Exportar a hoja de cálculo | No | No | Sí |
| 03 | 2025-11-10 | Operaciones | Cambiar el cálculo del descuento | No | No | Sí |
| 04 | 2025-07-23 | Compras | Nuevo reporte mensual | No | No | Sí |
| 05 | 2025-12-23 | Almacén | Nuevo reporte mensual | No | No | Sí |
| 06 | 2025-11-18 | Tecnologías de la Información | Nuevo reporte mensual | Correo | No | Sí |
| 07 | 2025-01-20 | Recursos Humanos | Bloquear la edición tras el cierre | No | No | No |
| 08 | 2025-11-13 | Gerencia | Exportar a hoja de cálculo | No | No | No |

### 5. Lo que la organización responde

| Pregunta | Respuesta |
|---|---|
| ¿Hay un procedimiento de desarrollo documentado? | «No. Se hace según la necesidad» |
| ¿Quién aprueba pasar un cambio a producción? | «El jefe de sistemas, o el mismo que lo hizo si es urgente» |
| ¿Se revisan los cambios entre pares? | «Somos pocos. No da el tiempo» |
| ¿Hay ambiente de pruebas? | «Se prueba en producción fuera de horario» |
| ¿Existe un plan de reversión? | «Si algo sale mal, se restaura el respaldo» |
| ¿Hay pruebas automatizadas? | «No» |
| ¿Qué pasa si el sistema deja de funcionar? | «No hay alternativa. Habría que operar en papel» |

### 6. Marco de referencia

| Norma | Procesos aplicables |
|---|---|
| **NTP-ISO/IEC 12207** | Procesos del ciclo de vida del software: adquisición, desarrollo, mantenimiento, gestión de la configuración, verificación y validación |
| **COBIT 2019 · BAI03** | Gestión de la identificación y construcción de soluciones |
| **COBIT 2019 · BAI06** | Gestión de cambios de TI |
| **COBIT 2019 · BAI07** | Gestión de la aceptación y transición del cambio |
| **ISO/IEC 25010** | Características de calidad del producto software |

---

[Semana 09](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 09·03](CASO-09-03-municipalidad-alto-selva.md) · **Caso 09·04** · [Caso 09·05](CASO-09-05-transportes-sur-andino.md) · [Encargo 09](../../ENCARGOS-UNIDAD-II/CASO-09-ciclo-de-vida-del-software.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
