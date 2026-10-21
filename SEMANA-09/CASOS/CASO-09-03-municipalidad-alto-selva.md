[Semana 09](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 09·02](CASO-09-02-clinica-san-ramon.md) · **Caso 09·03** · [Caso 09·04](CASO-09-04-coopac-frontera-sur.md) · [Encargo 09](../../ENCARGOS-UNIDAD-II/CASO-09-ciclo-de-vida-del-software.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>MUNICIPALIDAD DISTRITAL DE ALTO SELVA</strong><br>
  <em>Solicitud de auditoría · Ciclo de vida del software</em>
</div>

---

# Solicitud de auditoría de el ciclo de vida de nuestro software

| | |
|---|---|
| **Documento** | Solicitud de auditoría de el ciclo de vida de nuestro software |
| **De** | Gerente Municipal, MUNICIPALIDAD DISTRITAL DE ALTO SELVA |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 12 de octubre de 2026 |
| **Clasificación** | CONFIDENCIAL — USO ACADÉMICO |

---

## 1. Quiénes somos

Somos **MUNICIPALIDAD DISTRITAL DE ALTO SELVA**, gobierno local · municipalidad distrital, con sede en Provincia de Tacna. Funcionamos desde hace 61 años, con 178 trabajadores estables y 94 bajo CAS y locación. Nuestro presupuesto institucional es de S/ 31.2 millones y atendemos 41 800 habitantes.

Nos regulan o supervisan **PCM-SGTD (gobierno digital) · Contraloría General · MEF · ANPD · OSCE**. Somos una entidad pública, sujeta al gobierno digital y al control gubernamental.

Nuestra área de tecnologías de la información tiene **3 personas**. La encabeza nuestro jefe de la Unidad de Tecnologías de la Información, que reporta a Gerencia Municipal. Rotó tres veces en cuatro años. El presupuesto de tecnologías de la información es de **S/ 520 000**, el 1.67 % de nuestros ingresos. El objetivo que le declaramos a esa área es «Constituir el gobierno digital exigible y recuperar el control de los sistemas críticos».

**Lo que más nos cuesta.** No existe Comité de Gobierno Digital ni Líder de Gobierno Digital designado, pese a ser exigible. El Plan de Gobierno Digital nunca se formuló.

### 1.1. Los sistemas con los que operamos

| Sistema | Qué es | Dónde corre | Desde | ¿Tiene soporte vigente? |
|---|---|---|---|---|
| **SIAF-SP** | Sistema del MEF, obligatorio | Cliente local contra servidor del MEF | 2008 | MEF |
| **Trámite documentario** | Desarrollo propio en PHP, sin documentación | Servidor en la sede | 2015 | No, el desarrollador ya no trabaja aquí |
| **Rentas y catastro** | Producto adquirido por licitación | Servidor en la sede | 2019 | Vencido desde 2023 |
| **Portal de transparencia estándar** | Plataforma de la PCM | Nube del Estado | 2013 | PCM |
| **Mesa de partes virtual** | Formulario web más correo | Hosting contratado | 2020 | No |

### 1.2. Nuestros procesos

1. Trámite documentario y mesa de partes
2. Recaudación de tributos municipales
3. Licencias de funcionamiento y edificación
4. Registro civil
5. Contrataciones y logística
6. Atención al ciudadano

## 2. Por qué pedimos esta auditoría

Nuestro sistema de trámite documentario lo construyó un programador por locación de servicios que ya no trabaja con nosotros. No tiene documentación, el código se modifica en producción y la mesa de partes virtual depende de él. El Órgano de Control Institucional nos pregunta cómo controlamos un cambio en ese sistema.

## 3. Lo que ya sabemos que no está bien

Estos riesgos los tenemos identificados y no los hemos tratado.

- Incumplimiento del marco de gobierno digital
- Sistema crítico sin soporte ni código fuente documentado
- Datos personales de contribuyentes sin registro de tratamiento

**Lo que nos pasó en el periodo. Caída del servidor de rentas en campaña de amnistía tributaria.** El servidor de rentas estuvo caído nueve días hábiles durante la amnistía tributaria de 2025. No había respaldo restaurable ni contrato de soporte vigente. La recaudación de esos días se registró en cuadernos y se digitó después.

## 4. Lo que ya nos dijeron

- El Órgano de Control Institucional nos emitió en 2024 un informe de control con tres recomendaciones sobre tecnologías de la información. Respaldos del servidor de rentas, contrato de soporte del sistema de rentas y constitución del Comité de Gobierno Digital. Las tres figuran como «en proceso» desde entonces.
- La Contraloría General no ha realizado un servicio de control específico sobre sistemas en la entidad.
- El Jefe de la Unidad de Tecnologías de la Información que respondió el informe de 2024 ya no trabaja con nosotros.

## 5. Lo que queremos saber

Son las preguntas que la dirección espera que la auditoría responda. Cómo responderlas, con qué alcance, con qué criterios y con qué procedimientos, es lo que esperamos de su plan.

1. Saber si el código del trámite documentario es nuestro y si el contrato de locación nos lo entregó con documentación.
2. Saber qué riesgo corre la mesa de partes virtual, que es un servicio exigible, cuando cambia el sistema del que depende.
3. Saber cómo se controla un cambio cuando quien lo aprobó ya no trabaja aquí, porque nuestra Unidad rotó tres veces de jefe.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | Pedimos este servicio de control al Órgano de Control Institucional, que lo incluyó en su Plan Anual de Control aprobado por la Contraloría General de la República |
| **Contraparte designada** | El Gerente Municipal, designado por el Alcalde mediante memorando |
| **Canal único** | Toda solicitud entra y sale por la mesa de partes institucional y el correo del Órgano de Control Institucional, con número de expediente por cada solicitud |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 19 de octubre de 2026. Trabajo de campo del 20 de octubre de 2026 al 9 de noviembre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 10 de noviembre de 2026 y el 16 de noviembre de 2026. Informe entre el 17 de noviembre de 2026 y el 23 de noviembre de 2026 |
| **Horas que financiamos** | Hasta 171 horas de la comisión. Unas 34 de planificación, 103 de trabajo de campo, 14 de comunicación de resultados y 20 de informe. Más que eso no lo pagamos |
| **Horas que podemos dedicarles** | Nuestra área de tecnologías de la información dedica unas 120 horas al mes al proceso que van a auditar, entre sus 3 personas. No pueden pedirle más tiempo que ese |
| **Presupuesto que aprobamos** | S/ 12 398, a tarifa de referencia de S/ 110 la hora de supervisión, S/ 85 la de jefe de comisión y S/ 60 la de integrante, sin viáticos |
| **Confidencialidad** | Todo lo que les entregamos es confidencial. Lo guardan en un repositorio privado, cifrado, con la marca CONFIDENCIAL — USO ACADÉMICO, y al cierre conservan solo lo que el informe cite |
| **Lo que no autorizamos** | Ninguna prueba se ejecuta sobre nuestros sistemas en esta etapa. Lo que pedimos es un plan. Si el plan incluye pruebas, dirá cuáles y nos pedirá autorización escrita antes |
| **Las personas** | En su plan y en su informe nos nombran por el cargo, no por el nombre |

## 7. Lo que les entregamos

Lo que sigue lo entregamos **a solicitud escrita**, indicando para qué lo necesitan y qué procedimiento lo va a usar. Los documentos propios de esta materia van ya como anexos de esta solicitud. Los demás se entregan por el canal único, en la carpeta que indica la tabla.

| Documento | Qué contiene | Dónde está |
|---|---|---|
| `ciclo-de-vida-del-software.md` | El expediente de nuestro software propio, con las métricas del repositorio, los despliegues y los pedidos de cambio del periodo | Anexo 1 |
| `contratos-proveedores.md` | Lo que dicen nuestros contratos sobre la propiedad del código y el soporte | [`documentos/contratos-proveedores.md`](../../../CASOS/EMPRESA-03-municipalidad-alto-selva/documentos/contratos-proveedores.md) |
| `extracciones-y-registros.md` | Las extracciones del sistema principal y la bitácora que conservamos | [`documentos/extracciones-y-registros.md`](../../../CASOS/EMPRESA-03-municipalidad-alto-selva/documentos/extracciones-y-registros.md) |
| `narrativa-proceso-compras.md` | Cómo opera el proceso que nuestro software soporta o alimenta | [`documentos/narrativa-proceso-compras.md`](../../../CASOS/EMPRESA-03-municipalidad-alto-selva/documentos/narrativa-proceso-compras.md) |
| `organigrama-y-accesos.md` | Quién desarrolla, quién despliega y quién aprueba, según los accesos | [`documentos/organigrama-y-accesos.md`](../../../CASOS/EMPRESA-03-municipalidad-alto-selva/documentos/organigrama-y-accesos.md) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/usuarios_erp.csv` | Los usuarios de nuestro sistema principal, con perfil, último acceso y segundo factor | 124 registros · 124 habilitados · 124 sin segundo factor |
| `datos/pagos.csv` | Nuestros pagos del periodo | 8126 registros · S/ 12 980 144 en total |

Atentamente,

**Gerente Municipal**
MUNICIPALIDAD DISTRITAL DE ALTO SELVA

---

## Anexos

### Anexo 1 · `ciclo-de-vida-del-software.md`

### 1. El sistema desarrollado internamente

| Campo | Contenido |
|---|---|
| Sistema | **Trámite documentario** |
| Descripción | Desarrollo propio en PHP, sin documentación |
| En producción desde | 2015 |
| Lenguaje y plataforma | PHP 5.6 y MySQL |
| Personas que lo mantienen hoy | 2 |
| ¿Existe documentación técnica? | Solo el manual de usuario |
| ¿Existe control de versiones? | Sí, repositorio interno |
| ¿Existe ambiente de pruebas separado de producción? | No. Se prueba en producción |

> **Contexto que da la organización.** «Lo desarrolló un programador contratado bajo locación de servicios, que ya no trabaja aquí. Desde entonces se le hacen ajustes cuando algo falla o cuando el área pide un cambio.»

### 2. Métricas del repositorio

Extraídas con `git log` sobre el periodo auditado.

| Métrica | Valor |
|---|---|
| Commits en el periodo | 190 |
| Autores distintos | 3 |
| Commits del autor principal | 72 % del total |
| Ramas activas | 2 |
| Ramas sin fusionar con más de 90 días | 2 |
| Commits directos a la rama principal | **85 %** |
| Pull Requests abiertos en el periodo | 10 |
| Pull Requests con revisión de un segundo | **1** |
| Etiquetas de versión creadas | 4 |
| Commits con mensaje de una sola palabra | 34 |
| Archivos con más de 1 000 líneas | 2 |
| ¿Hay pruebas automatizadas en el repositorio? | No |

### 3. Últimos despliegues a producción

| Fecha | Versión | Qué se desplegó | ¿Hubo etiqueta? | ¿Hubo prueba previa? | ¿Se pudo revertir? |
|---|---|---|---|---|---|
| 2025-04-19 | v1.1 | Corrección urgente en producción | No | No | No |
| 2025-07-16 | — | Corrección urgente en producción | No | No | No |
| 2025-02-23 | — | Ajuste de cálculo | No | No | No |
| 2025-10-03 | v1.1 | Corrección de error en reportes | No | No | Sí |
| 2025-05-25 | v1.3 | Ajuste de cálculo | No | No | Sí |
| 2025-03-27 | v1.6 | Cambio de formato de comprobante | No | No | No |

### 4. Trazabilidad de requisitos

La organización entrega los pedidos de cambio del periodo, tal como los registra.

| N.º | Fecha | Solicitado por | Qué se pidió | ¿Especificación escrita? | ¿Aceptación formal? | ¿Se desplegó? |
|---|---|---|---|---|---|---|
| 01 | 2025-12-19 | Comercial | Permitir anular un registro | No | Verbal | No |
| 02 | 2025-04-12 | Contabilidad | Nuevo reporte mensual | No | Verbal | No |
| 03 | 2025-07-21 | Legal | Cambiar el cálculo del descuento | No | No | Sí |
| 04 | 2025-08-18 | Logística | Cambiar el cálculo del descuento | Correo | No | Sí |
| 05 | 2025-05-01 | Gerencia | Agregar un filtro al reporte | Correo | No | No |
| 06 | 2025-08-01 | Operaciones | Nuevo reporte mensual | Correo | No | Sí |
| 07 | 2025-01-15 | Operaciones | Corregir el redondeo | Correo | No | Sí |
| 08 | 2025-04-26 | Administración y Finanzas | Corregir el redondeo | No | No | Sí |

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

[Semana 09](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 09·02](CASO-09-02-clinica-san-ramon.md) · **Caso 09·03** · [Caso 09·04](CASO-09-04-coopac-frontera-sur.md) · [Encargo 09](../../ENCARGOS-UNIDAD-II/CASO-09-ciclo-de-vida-del-software.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
