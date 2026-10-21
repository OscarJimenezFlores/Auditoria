[Semana 07](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 07·03](CASO-07-03-municipalidad-alto-selva.md) · **Caso 07·04** · [Caso 07·05](CASO-07-05-transportes-sur-andino.md) · [Encargo 07](../../ENCARGOS-UNIDAD-II/CASO-07-gobierno-y-gestion-de-ti.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>COOPAC FRONTERA SUR</strong><br>
  <em>Solicitud de auditoría · Gobierno y gestión de las tecnologías de la información</em>
</div>

---

# Solicitud de auditoría de el gobierno y la gestión de las tecnologías de la información

| | |
|---|---|
| **Documento** | Solicitud de auditoría de el gobierno y la gestión de las tecnologías de la información |
| **De** | Gerente General, por acuerdo del Consejo de Vigilancia, COOPAC FRONTERA SUR |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 28 de setiembre de 2026 |
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

Nuestro Consejo de Administración debe responder a la SBS por las cuatro observaciones abiertas de 2024, y la Resolución SBS N.º 504-2021 le atribuye a él, no al Jefe de TI, la responsabilidad del sistema de gestión de seguridad. El Consejo quiere saber si gobierna la tecnología o solo aprueba su presupuesto.

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

1. Saber si el Consejo de Administración está cumpliendo lo que la Resolución SBS N.º 504-2021 le atribuye, y qué nos falta para cerrar las cuatro observaciones de la SBS.
2. Saber qué papel tienen hoy la Unidad de Auditoría Interna y el Oficial de Seguridad de la Información en las decisiones sobre tecnología, y cuál deberían tener.
3. Saber si el presupuesto de tecnologías de la información, que es el 2.9 % de nuestros gastos operativos, se decide con un criterio o solo se aprueba.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | El Consejo de Vigilancia lo acordó a propuesta de la Unidad de Auditoría Interna, dentro del plan anual que remitimos a la SBS |
| **Contraparte designada** | Nuestro Gerente General, con el Oficial de Seguridad de la Información como enlace |
| **Canal único** | Toda solicitud entra y sale por el correo de la Unidad de Auditoría Interna, que registra cada solicitud en su sistema de seguimiento |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 5 de octubre de 2026. Trabajo de campo del 6 de octubre de 2026 al 26 de octubre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 27 de octubre de 2026 y el 2 de noviembre de 2026. Informe entre el 3 de noviembre de 2026 y el 9 de noviembre de 2026 |
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
| `universo-auditable-y-riesgos.md` | Nuestro inventario de procesos y sistemas, y el registro de riesgos tal como lo llevamos | Anexo 1 |
| `plan-institucional-extracto.md` | Nuestros objetivos institucionales, las actas y lo que declaramos sobre nuestro propio gobierno | Anexo 2 |
| `expedientes-de-inversion.md` | Los expedientes de las tres inversiones que cerramos en el periodo | Anexo 3 |
| `organigrama-y-accesos.md` | De quién depende nuestra área de tecnologías de la información | [`documentos/organigrama-y-accesos.md`](../../../CASOS/EMPRESA-04-coopac-frontera-sur/documentos/organigrama-y-accesos.md) |
| `incidente-detallado.md` | El incidente del periodo, con su línea de tiempo | [`documentos/incidente-detallado.md`](../../../CASOS/EMPRESA-04-coopac-frontera-sur/documentos/incidente-detallado.md) |
| `contratos-proveedores.md` | Nuestros contratos vigentes y vencidos con proveedores de tecnología | [`documentos/contratos-proveedores.md`](../../../CASOS/EMPRESA-04-coopac-frontera-sur/documentos/contratos-proveedores.md) |
| `datos/presupuesto_ti.csv` | Nuestro presupuesto de tecnologías de la información del periodo, planificado contra ejecutado, por partida | Anexo 4 y [archivo](../../../CASOS/EMPRESA-04-coopac-frontera-sur/datos/presupuesto_ti.csv) |
| `datos/inversiones_cerradas.csv` | Las tres inversiones cerradas, con el beneficio que declaramos y el que medimos | Anexo 5 y [archivo](../../../CASOS/EMPRESA-04-coopac-frontera-sur/datos/inversiones_cerradas.csv) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/presupuesto_ti.csv` | Nuestro presupuesto de tecnologías de la información por partida | 7 registros |
| `datos/inversiones_cerradas.csv` | Nuestras inversiones cerradas del periodo | 3 registros |
| `datos/proveedores.csv` | Nuestro maestro de proveedores | 60 registros · 60 activos |
| `datos/pagos.csv` | Nuestros pagos del periodo | 28016 registros · S/ 42 214 064 en total |

Atentamente,

**Gerente General, por acuerdo del Consejo de Vigilancia**
COOPAC FRONTERA SUR

---

## Anexos

### Anexo 1 · `universo-auditable-y-riesgos.md`

### 1. Qué es este documento

La organización no tiene un plan anual de auditoría. Lo que entrega es el **inventario de sus procesos y sistemas** —el universo auditable— y el **registro de riesgos** que mantiene Administración, tal como está.

Con esto el equipo construye el Plan Anual de Auditoría de TI basado en riesgo de la Semana 07.

### 2. Universo auditable

| ID | Entidad auditable | Tipo | Proceso que soporta | Responsable | Última auditoría |
|---|---|---|---|---|---|
| UA-01 | Captación de ahorros | Proceso | Captación de ahorros | Fernando Zapana Apaza | Nunca |
| UA-02 | Evaluación y otorgamiento de créditos | Proceso | Evaluación y otorgamiento de créditos | Iván Bravo Peralta | Nunca |
| UA-03 | Recuperaciones y cobranza | Proceso | Recuperaciones y cobranza | Fernando Zapana Apaza | Nunca |
| UA-04 | Prevención de lavado de activos | Proceso | Prevención de lavado de activos | Gabriela Maquera Salazar | Nunca |
| UA-05 | Atención al socio en agencias | Proceso | Atención al socio en agencias | Paola Condori Nina | Nunca |
| UA-06 | Cierre contable y reportes a la SBS | Proceso | Cierre contable y reportes a la SBS | Fernando Paredes Laura | Nunca |
| UA-07 | Core financiero | Sistema | Captación de ahorros | Nadia Rivera Copaja | Nunca |
| UA-08 | Banca por internet para socios | Sistema | Evaluación y otorgamiento de créditos | Nelson Aguilar Calisaya | Nunca |
| UA-09 | Prevención de lavado de activos | Sistema | Recuperaciones y cobranza | Julio Colque Peralta | 2023 |
| UA-10 | Central de riesgos | Sistema | Prevención de lavado de activos | Gabriela Maquera Salazar | Nunca |
| UA-11 | Gestión documental de expedientes de crédito | Sistema | Atención al socio en agencias | Ana Chura Vargas | Nunca |
| UA-12 | Enlace de comunicaciones y red | Infraestructura | Todos | Miguel Condori Ramos | Nunca |
| UA-13 | Respaldos y recuperación | Infraestructura | Todos | Paola Núñez Rivera | Nunca |
| UA-14 | Gestión de accesos | Proceso | Todos | Teresa Colque Zapana | Nunca |
| UA-15 | Proveedor de planilla | Tercero | Recursos humanos | Carlos Chura Colque | Nunca |
| UA-16 | Proveedor de nube | Tercero | Todos | Gabriela Nina Vargas | Nunca |
| UA-17 | Protección de datos personales | Cumplimiento | Todos | Carlos Núñez Mamani | Nunca |

> **17 entidades auditables.** La capacidad del área de auditoría interna es de **310 horas-auditor al año**. No alcanza para todas. Por eso el plan debe priorizar por riesgo, no por orden de lista.

### 3. Registro de riesgos que mantiene la organización

Hoja de cálculo de Administración, última actualización 5 de mayo de 2025. Se entrega tal como está.

| ID | Riesgo | Probabilidad | Impacto | Nivel | Tratamiento declarado | Responsable | Estado |
|---|---|---|---|---|---|---|---|
| RG-01 | Incumplimiento verificable de la Resolución SBS 504-2021 | Baja | Medio | Bajo | Mitigar — sin plan | Nelson Vargas Zapana | Abierto |
| RG-02 | Sin registro de accesos de lectura a información de socios | Alta | Alto | **Extremo** | Aceptado | Gabriela Choque Ticona | Abierto |
| RG-03 | Plan de continuidad sin pruebas documentadas | Media | Medio | Medio | Mitigar — sin plan | Nelson Aguilar Calisaya | Abierto |
| RG-04 | Interrupción prolongada del sistema principal | Media | Alto | Alto | Sin definir | Julio Colque Peralta | Abierto |
| RG-05 | Pérdida de información por fallo de respaldo | Media | Alto | Alto | Mitigar — sin plan | Raúl Choque Choque | Abierto |
| RG-06 | Sanción del regulador por incumplimiento normativo | Baja | Alto | Medio | Sin definir | Vanessa Maquera Peralta | Abierto |
| RG-07 | Fuga de datos personales de clientes o usuarios | Baja | Alto | Medio | Aceptado | Julio Ticona Yufra | Abierto |
| RG-08 | Dependencia de un único proveedor de servicios | Alta | Medio | Alto | Sin definir | Ricardo Nina Ticona | Abierto |
| RG-09 | Fraude interno en el ciclo de compras y pagos | Baja | Alto | Medio | Aceptado | Miguel Condori Ramos | En revisión |

### 4. Lo que la organización responde

| Pregunta del auditor | Respuesta |
|---|---|
| ¿Con qué metodología se evaluó la probabilidad y el impacto? | «Con el criterio del área. No hay una escala escrita» |
| ¿Existe apetito de riesgo definido? | «No» |
| ¿Quién aprueba el tratamiento de un riesgo? | «Gerencia, cuando se le presenta» |
| ¿Se ha auditado alguna de estas entidades? | «No de forma sistemática» |
| ¿Cuántas horas-auditor hay disponibles al año? | «Depende de la carga. Nunca se ha calculado» |
| ¿Hay obligaciones de auditoría impuestas por un regulador? | «El regulador sectorial exige algunas revisiones. No están calendarizadas» |

### Anexo 2 · `plan-institucional-extracto.md`

### 1. Ficha del instrumento

| Campo | Contenido |
|---|---|
| Documento | Plan Estratégico 2024–2028 |
| Aprobado por | Directorio, sesión del 18 de marzo de 2024 |
| Vigencia | 2024 a 2028 |
| ¿Se ha revisado desde su aprobación? | No |
| ¿Tiene indicadores con línea base? | Parcialmente |

### 2. Misión declarada

> «Satisfacer las expectativas de nuestros usuarios mediante servicios eficientes y personal calificado, generando valor para la sociedad.»

### 3. Visión declarada

> «Consolidarnos como una organización moderna, eficiente y sostenible, al servicio de la comunidad.»

### 4. Objetivos estratégicos vigentes

| N.º | Objetivo | Indicador declarado | Línea base | Meta | ¿Se mide hoy? |
|---|---|---|---|---|---|
| OE-01 | Incrementar la satisfacción del cliente | Porcentaje de satisfacción | No definida | 90 % | No |
| OE-02 | Mejorar la eficiencia de los procesos internos | Tiempo promedio de atención | No definida | Reducir 20 % | No |
| OE-03 | Fortalecer las competencias del personal | Horas de capacitación por trabajador | 12 h | 24 h | Sí |
| OE-04 | Modernizar la infraestructura tecnológica | Porcentaje de avance del plan de TI | No definida | 100 % | No |
| OE-05 | Asegurar la sostenibilidad económica | Margen operativo | 13 % | Incrementar 3 puntos | Sí |

> **Observación de la propia Gerencia.** «El objetivo de modernización tecnológica está en el plan desde su aprobación, pero nunca se desagregó en proyectos ni se le asignó presupuesto específico. Es lo que esperamos que salga del trabajo de este semestre.»

### 5. Actas del Directorio · extractos pertinentes a tecnología

#### Acta N.º 053-2025 · Sesión del 5 de febrero de 2025

**Asunto.** Aprobación del presupuesto anual

**Acuerdo.** Se aprueba el presupuesto de TI por S/ 1 240 000, con una reducción del 31 % respecto de lo solicitado. Se indica al área que priorice.

#### Acta N.º 059-2025 · Sesión del 4 de abril de 2025

**Asunto.** Informe sobre el incidente

**Acuerdo.** Se toma conocimiento del incidente reportado. Se dispone que el área presente un informe con medidas correctivas. **No se registra plazo.**

#### Acta N.º 029-2025 · Sesión del 9 de junio de 2025

**Asunto.** Solicitud de renovación de equipos

**Acuerdo.** Se posterga la decisión hasta contar con un plan integral de tecnología. Se encarga a Gerencia su elaboración.

#### Acta N.º 012-2025 · Sesión del 5 de agosto de 2025

**Asunto.** Contratación de personal para TI

**Acuerdo.** Se aprueba una plaza. Se deja constancia de que el área ha señalado que requiere dos.

#### Acta N.º 021-2025 · Sesión del 22 de octubre de 2025

**Asunto.** Cumplimiento normativo

**Acuerdo.** Se toma conocimiento de las obligaciones sobre protección de datos personales. Se dispone su evaluación. **No se designa responsable.**

#### Acta N.º 074-2025 · Sesión del 11 de diciembre de 2025

**Asunto.** Avance del plan estratégico

**Acuerdo.** Se presenta el avance. Se observa que el objetivo de modernización tecnológica no registra avance medible.

### 6. Lo que la organización responde

| Pregunta | Respuesta |
|---|---|
| ¿Quién hace seguimiento a los acuerdos del Directorio? | «Gerencia General, en la sesión siguiente» |
| ¿Existe un registro de acuerdos con estado? | «Está en las actas» |
| ¿El plan estratégico se articuló con un plan de TI? | «No. Es lo que falta» |
| ¿Los indicadores se reportan periódicamente? | «Dos de los cinco» |
| ¿Cómo se decidió el presupuesto de TI? | «Se tomó el del año anterior y se ajustó» |

### Anexo 3 · `expedientes-de-inversion.md`

### Presupuesto de TI del periodo

Detalle por partida en [`datos/presupuesto_ti.csv`](../../../CASOS/EMPRESA-04-coopac-frontera-sur/datos/presupuesto_ti.csv). Total aprobado. **S/ 1 240 000** (2.9 % de gastos operativos de la facturación).

### Los tres expedientes

#### Expediente 1 · Videovigilancia

| Campo | Contenido |
|---|---|
| Año | 2025 |
| Responsable | Nelson Condori Salazar |
| Presupuesto aprobado | S/ 161 321.34 |
| Ejecutado | S/ 153 280.11 |
| Desviación | **-5.0 %** |
| Beneficio declarado en la solicitud | Disponibilidad del servicio |
| ¿Se midió el beneficio después? | **No se midió** |
| Documentos que la organización conserva | Solicitud, cotizaciones, orden de compra, factura |
| Documentos que **no** conserva | Caso de negocio con alternativas, acta de aceptación, medición posterior |

**Justificación transcrita de la solicitud original.**

> «Lo solicitó el área usuaria por los problemas recurrentes que viene reportando.»

**Lo que la organización responde.**

| Pregunta | Respuesta |
|---|---|
| ¿Se evaluaron alternativas? | «Se comparó con una alternativa, verbalmente» |
| ¿Quién aprobó la desviación presupuestal? | «Gerencia, verbalmente» |
| ¿Se firmó un acta de aceptación? | «Se recibió conforme, sin acta» |
| ¿Se midió si el beneficio se logró? | «No» |

#### Expediente 2 · Renovación de servidores

| Campo | Contenido |
|---|---|
| Año | 2024 |
| Responsable | Ana Torres Medina |
| Presupuesto aprobado | S/ 116 107.29 |
| Ejecutado | S/ 170 158.62 |
| Desviación | **+46.6 %** |
| Beneficio declarado en la solicitud | Ahorro en licencias |
| ¿Se midió el beneficio después? | **No se midió** |
| Documentos que la organización conserva | Solicitud, cotizaciones, orden de compra, factura |
| Documentos que **no** conserva | Caso de negocio con alternativas, acta de aceptación, medición posterior |

**Justificación transcrita de la solicitud original.**

> «Es necesario para no detener la operación. El equipo actual está al límite de su capacidad.»

**Lo que la organización responde.**

| Pregunta | Respuesta |
|---|---|
| ¿Se evaluaron alternativas? | «Se comparó con una alternativa, verbalmente» |
| ¿Quién aprobó la desviación presupuestal? | «Gerencia, verbalmente» |
| ¿Se firmó un acta de aceptación? | «No recordamos» |
| ¿Se midió si el beneficio se logró? | «No» |

#### Expediente 3 · Sistema de respaldo

| Campo | Contenido |
|---|---|
| Año | 2025 |
| Responsable | Marta Colque Apaza |
| Presupuesto aprobado | S/ 193 409.68 |
| Ejecutado | S/ 254 711.93 |
| Desviación | **+31.7 %** |
| Beneficio declarado en la solicitud | Cumplimiento normativo |
| ¿Se midió el beneficio después? | **No se midió** |
| Documentos que la organización conserva | Solicitud, cotizaciones, orden de compra, factura |
| Documentos que **no** conserva | Caso de negocio con alternativas, acta de aceptación, medición posterior |

**Justificación transcrita de la solicitud original.**

> «Es necesario para no detener la operación. El equipo actual está al límite de su capacidad.»

**Lo que la organización responde.**

| Pregunta | Respuesta |
|---|---|
| ¿Se evaluaron alternativas? | «No. Se fue con el proveedor habitual» |
| ¿Quién aprobó la desviación presupuestal? | «Administración y Finanzas» |
| ¿Se firmó un acta de aceptación? | «Se recibió conforme, sin acta» |
| ¿Se midió si el beneficio se logró? | «No» |

### Marco de referencia

| Marco | Qué aporta |
|---|---|
| **COBIT 2019 · EDM02** | Asegurar la entrega de beneficios de la inversión en TI |
| **COBIT 2019 · APO05** | Gestión del portafolio de inversiones |
| **Val IT** | Evaluación del valor entregado por una inversión ya ejecutada |

### Anexo 4 · `datos/presupuesto_ti.csv`

Nuestro presupuesto de tecnologías de la información del periodo, planificado contra ejecutado, por partida.

| Partida | Tipo | Planificado | Ejecutado | Desviación |
|---|---|---|---|---|
| PT01 · Licencias y suscripciones | Operación | S/ 260 400 | S/ 235 789 | -9.5 % |
| PT02 · Soporte y mantenimiento de sistemas | Operación | S/ 235 600 | S/ 149 613 | -36.5 % |
| PT03 · Infraestructura y equipamiento | Operación | S/ 210 800 | S/ 221 418 | 5.0 % |
| PT04 · Comunicaciones y enlaces | Operación | S/ 136 400 | S/ 128 514 | -5.8 % |
| PT05 · Personal de TI | Operación | S/ 248 000 | S/ 238 528 | -3.8 % |
| PT06 · Proyectos nuevos | Inversión | S/ 99 200 | S/ 113 754 | 14.7 % |
| PT07 · Seguridad de la información | Operación | S/ 49 600 | S/ 57 111 | 15.1 % |
| **Total** | | **S/ 1 240 000** | **S/ 1 144 727** | **-7.7 %** |

### Anexo 5 · `datos/inversiones_cerradas.csv`

Las tres inversiones cerradas, con el beneficio que declaramos y el que medimos.

| Inversión | Año | Presupuesto | Ejecutado | Beneficio declarado | Beneficio medido | Responsable |
|---|---|---|---|---|---|---|
| INV01 · Videovigilancia | 2025 | S/ 161 321 | S/ 153 280 | Disponibilidad del servicio | No se midió | Nelson Condori Salazar |
| INV02 · Renovación de servidores | 2024 | S/ 116 107 | S/ 170 159 | Ahorro en licencias | No se midió | Ana Torres Medina |
| INV03 · Sistema de respaldo | 2025 | S/ 193 410 | S/ 254 712 | Cumplimiento normativo | No se midió | Marta Colque Apaza |

---

[Semana 07](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 07·03](CASO-07-03-municipalidad-alto-selva.md) · **Caso 07·04** · [Caso 07·05](CASO-07-05-transportes-sur-andino.md) · [Encargo 07](../../ENCARGOS-UNIDAD-II/CASO-07-gobierno-y-gestion-de-ti.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
