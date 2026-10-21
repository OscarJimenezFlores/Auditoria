[Semana 07](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 07·07](CASO-07-07-instituto-vertiente-sur.md) · **Caso 07·08** · [Caso 07·09](CASO-07-09-servicios-mineros-cordillera.md) · [Encargo 07](../../ENCARGOS-UNIDAD-II/CASO-07-gobierno-y-gestion-de-ti.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>EPS AGUAS DEL SUR S.A.</strong><br>
  <em>Solicitud de auditoría · Gobierno y gestión de las tecnologías de la información</em>
</div>

---

# Solicitud de auditoría de el gobierno y la gestión de las tecnologías de la información

| | |
|---|---|
| **Documento** | Solicitud de auditoría de el gobierno y la gestión de las tecnologías de la información |
| **De** | Gerente General, EPS AGUAS DEL SUR S.A. |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 28 de setiembre de 2026 |
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

El Directorio y OTASS nos exigen un Plan de Gobierno Digital que nunca formulamos, y SUNASS tiene abierto un procedimiento por la facturación estimada. Nuestro Departamento de Tecnologías de la Información reporta a Administración, la red del SCADA se unió a la administrativa en 2023 por una decisión que no consta en ninguna acta, y la dirección se enteró por el reclamo masivo.

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

1. Saber qué nos exige el gobierno digital y qué nos exige el regulador del servicio, y quién en la empresa responde por cada cosa.
2. Saber qué pasó con las dos recomendaciones del Órgano de Control Institucional y con el procedimiento de SUNASS, y quién las tiene a cargo.
3. Saber quién decidió unir la red del SCADA con la administrativa en 2023 y si esa decisión debió pasar por la dirección.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | Pedimos este servicio de control al Órgano de Control Institucional, con conocimiento del Directorio y de OTASS |
| **Contraparte designada** | Nuestro Gerente de Administración, de quien depende el Departamento de Tecnologías de la Información |
| **Canal único** | Toda solicitud entra y sale por la mesa de partes institucional y el correo del Órgano de Control Institucional, con número de expediente por cada solicitud |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 5 de octubre de 2026. Trabajo de campo del 6 de octubre de 2026 al 26 de octubre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 27 de octubre de 2026 y el 2 de noviembre de 2026. Informe entre el 3 de noviembre de 2026 y el 9 de noviembre de 2026 |
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
| `universo-auditable-y-riesgos.md` | Nuestro inventario de procesos y sistemas, y el registro de riesgos tal como lo llevamos | Anexo 1 |
| `plan-institucional-extracto.md` | Nuestros objetivos institucionales, las actas y lo que declaramos sobre nuestro propio gobierno | Anexo 2 |
| `expedientes-de-inversion.md` | Los expedientes de las tres inversiones que cerramos en el periodo | Anexo 3 |
| `organigrama-y-accesos.md` | De quién depende nuestra área de tecnologías de la información | [`documentos/organigrama-y-accesos.md`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/documentos/organigrama-y-accesos.md) |
| `incidente-detallado.md` | El incidente del periodo, con su línea de tiempo | [`documentos/incidente-detallado.md`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/documentos/incidente-detallado.md) |
| `contratos-proveedores.md` | Nuestros contratos vigentes y vencidos con proveedores de tecnología | [`documentos/contratos-proveedores.md`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/documentos/contratos-proveedores.md) |
| `datos/presupuesto_ti.csv` | Nuestro presupuesto de tecnologías de la información del periodo, planificado contra ejecutado, por partida | Anexo 4 y [archivo](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/datos/presupuesto_ti.csv) |
| `datos/inversiones_cerradas.csv` | Las tres inversiones cerradas, con el beneficio que declaramos y el que medimos | Anexo 5 y [archivo](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/datos/inversiones_cerradas.csv) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/presupuesto_ti.csv` | Nuestro presupuesto de tecnologías de la información por partida | 7 registros |
| `datos/inversiones_cerradas.csv` | Nuestras inversiones cerradas del periodo | 3 registros |
| `datos/proveedores.csv` | Nuestro maestro de proveedores | 156 registros · 156 activos |
| `datos/pagos.csv` | Nuestros pagos del periodo | 19281 registros · S/ 28 844 992 en total |

Atentamente,

**Gerente General**
EPS AGUAS DEL SUR S.A.

---

## Anexos

### Anexo 1 · `universo-auditable-y-riesgos.md`

### 1. Qué es este documento

La organización no tiene un plan anual de auditoría. Lo que entrega es el **inventario de sus procesos y sistemas** —el universo auditable— y el **registro de riesgos** que mantiene Administración, tal como está.

Con esto el equipo construye el Plan Anual de Auditoría de TI basado en riesgo de la Semana 07.

### 2. Universo auditable

| ID | Entidad auditable | Tipo | Proceso que soporta | Responsable | Última auditoría |
|---|---|---|---|---|---|
| UA-01 | Catastro comercial de usuarios | Proceso | Catastro comercial de usuarios | Luis Choque Chura | Nunca |
| UA-02 | Lectura de medidores y facturación | Proceso | Lectura de medidores y facturación | Luis Salazar Ramos | Nunca |
| UA-03 | Cobranza y corte/reconexión | Proceso | Cobranza y corte/reconexión | Miguel Chura Ticona | Nunca |
| UA-04 | Atención de reclamos comerciales | Proceso | Atención de reclamos comerciales | Jorge Cáceres Ticona | Nunca |
| UA-05 | Operación de plantas y redes | Proceso | Operación de plantas y redes | Álvaro Calisaya Apaza | Nunca |
| UA-06 | Contrataciones y presupuesto público | Proceso | Contrataciones y presupuesto público | Jorge Condori Cutipa | Nunca |
| UA-07 | Sistema comercial | Sistema | Catastro comercial de usuarios | Teresa Mamani Peralta | 2023 |
| UA-08 | SCADA de plantas y reservorios | Sistema | Lectura de medidores y facturación | Carmen Calisaya Núñez | 2023 |
| UA-09 | Micromedición y lectura | Sistema | Cobranza y corte/reconexión | Lucía Cáceres Ticona | Nunca |
| UA-10 | SIAF y patrimonio | Sistema | Atención de reclamos comerciales | Jorge Núñez Zapana | 2023 |
| UA-11 | Atención de reclamos | Sistema | Operación de plantas y redes | Elena Rivera Salazar | Nunca |
| UA-12 | Enlace de comunicaciones y red | Infraestructura | Todos | Vanessa Chura Vargas | Nunca |
| UA-13 | Respaldos y recuperación | Infraestructura | Todos | Iván Maquera Cutipa | Nunca |
| UA-14 | Gestión de accesos | Proceso | Todos | Teresa Nina Ticona | Nunca |
| UA-15 | Proveedor de planilla | Tercero | Recursos humanos | Vanessa Chura Cutipa | Nunca |
| UA-16 | Proveedor de nube | Tercero | Todos | Julio Cáceres Núñez | Nunca |
| UA-17 | Protección de datos personales | Cumplimiento | Todos | Paola Colque Núñez | Nunca |

> **17 entidades auditables.** La capacidad del área de auditoría interna es de **779 horas-auditor al año**. No alcanza para todas. Por eso el plan debe priorizar por riesgo, no por orden de lista.

### 3. Registro de riesgos que mantiene la organización

Hoja de cálculo de Administración, última actualización 2 de diciembre de 2025. Se entrega tal como está.

| ID | Riesgo | Probabilidad | Impacto | Nivel | Tratamiento declarado | Responsable | Estado |
|---|---|---|---|---|---|---|---|
| RG-01 | Red industrial (SCADA) sin segmentación efectiva | Baja | Alto | Medio | Se está evaluando | Ana Aguilar Núñez | Abierto |
| RG-02 | Sin trazabilidad del proceso de carga de lecturas | Alta | Alto | **Extremo** | Mitigar — sin plan | Teresa Mamani Peralta | Abierto |
| RG-03 | Doble marco: gobierno digital y regulación sectorial, ninguno cubierto por completo | Baja | Medio | Bajo | Se está evaluando | Óscar Peralta Peralta | Abierto |
| RG-04 | Interrupción prolongada del sistema principal | Media | Alto | Alto | Aceptado | Carmen Aguilar Ramos | En revisión |
| RG-05 | Pérdida de información por fallo de respaldo | Media | Alto | Alto | Mitigar — sin plan | Miguel Huanca Mamani | Abierto |
| RG-06 | Sanción del regulador por incumplimiento normativo | Baja | Alto | Medio | Sin definir | Pedro Ancco Torres | Abierto |
| RG-07 | Fuga de datos personales de clientes o usuarios | Baja | Alto | Medio | Sin definir | Carlos Yufra Medina | Abierto |
| RG-08 | Dependencia de un único proveedor de servicios | Alta | Medio | Alto | Aceptado | Vanessa Chura Vargas | Abierto |
| RG-09 | Fraude interno en el ciclo de compras y pagos | Baja | Alto | Medio | Se está evaluando | Paola Cáceres Copaja | Abierto |

### 4. Lo que la organización responde

| Pregunta del auditor | Respuesta |
|---|---|
| ¿Con qué metodología se evaluó la probabilidad y el impacto? | «Con el criterio del área. No hay una escala escrita» |
| ¿Existe apetito de riesgo definido? | «No» |
| ¿Quién aprueba el tratamiento de un riesgo? | «Gerencia, cuando se le presenta» |
| ¿Se ha auditado alguna de estas entidades? | «No de forma sistemática» |
| ¿Cuántas horas-auditor hay disponibles al año? | «Depende de la carga. Nunca se ha calculado» |
| ¿Hay obligaciones de auditoría impuestas por un regulador? | «SUNASS, según su marco» |

### Anexo 2 · `plan-institucional-extracto.md`

### 1. Ficha del instrumento

| Campo | Contenido |
|---|---|
| Documento | Plan Estratégico Institucional 2024–2028 |
| Aprobado por | Concejo Municipal, sesión del 18 de marzo de 2024 |
| Vigencia | 2024 a 2028 |
| ¿Se ha revisado desde su aprobación? | No |
| ¿Tiene indicadores con línea base? | Parcialmente |

### 2. Misión declarada

> «Brindar productos y servicios de calidad que satisfagan las necesidades de nuestros clientes, con personal comprometido y tecnología adecuada, contribuyendo al desarrollo de la región.»

### 3. Visión declarada

> «Consolidarnos como una organización moderna, eficiente y sostenible, al servicio de la comunidad.»

### 4. Objetivos estratégicos vigentes

| N.º | Objetivo | Indicador declarado | Línea base | Meta | ¿Se mide hoy? |
|---|---|---|---|---|---|
| OE-01 | Incrementar la satisfacción del cliente | Porcentaje de satisfacción | No definida | 90 % | No |
| OE-02 | Mejorar la eficiencia de los procesos internos | Tiempo promedio de atención | No definida | Reducir 20 % | No |
| OE-03 | Fortalecer las competencias del personal | Horas de capacitación por trabajador | 12 h | 24 h | Sí |
| OE-04 | Modernizar la infraestructura tecnológica | Porcentaje de avance del plan de TI | No definida | 100 % | No |
| OE-05 | Asegurar la sostenibilidad económica | Margen operativo | 10 % | Incrementar 3 puntos | Sí |

> **Observación de la propia Gerencia.** «El objetivo de modernización tecnológica está en el plan desde su aprobación, pero nunca se desagregó en proyectos ni se le asignó presupuesto específico. Es lo que esperamos que salga del trabajo de este semestre.»

### 5. Actas del Concejo Municipal · extractos pertinentes a tecnología

#### Acta N.º 071-2025 · Sesión del 5 de febrero de 2025

**Asunto.** Aprobación del presupuesto anual

**Acuerdo.** Se aprueba el presupuesto de TI por S/ 1 080 000, con una reducción del 27 % respecto de lo solicitado. Se indica al área que priorice.

#### Acta N.º 051-2025 · Sesión del 21 de abril de 2025

**Asunto.** Informe sobre el incidente

**Acuerdo.** Se toma conocimiento del incidente reportado. Se dispone que el área presente un informe con medidas correctivas. **No se registra plazo.**

#### Acta N.º 055-2025 · Sesión del 17 de junio de 2025

**Asunto.** Solicitud de renovación de equipos

**Acuerdo.** Se posterga la decisión hasta contar con un plan integral de tecnología. Se encarga a Gerencia su elaboración.

#### Acta N.º 074-2025 · Sesión del 23 de agosto de 2025

**Asunto.** Contratación de personal para TI

**Acuerdo.** Se aprueba una plaza. Se deja constancia de que el área ha señalado que requiere dos.

#### Acta N.º 028-2025 · Sesión del 23 de octubre de 2025

**Asunto.** Cumplimiento normativo

**Acuerdo.** Se toma conocimiento de las obligaciones sobre protección de datos personales. Se dispone su evaluación. **No se designa responsable.**

#### Acta N.º 019-2025 · Sesión del 11 de diciembre de 2025

**Asunto.** Avance del plan estratégico

**Acuerdo.** Se presenta el avance. Se observa que el objetivo de modernización tecnológica no registra avance medible.

### 6. Lo que la organización responde

| Pregunta | Respuesta |
|---|---|
| ¿Quién hace seguimiento a los acuerdos del Concejo Municipal? | «Gerencia General, en la sesión siguiente» |
| ¿Existe un registro de acuerdos con estado? | «Está en las actas» |
| ¿El plan estratégico se articuló con un plan de TI? | «No. Es lo que falta» |
| ¿Los indicadores se reportan periódicamente? | «Dos de los cinco» |
| ¿Cómo se decidió el presupuesto de TI? | «Se tomó el del año anterior y se ajustó» |

### Anexo 3 · `expedientes-de-inversion.md`

### Presupuesto de TI del periodo

Detalle por partida en [`datos/presupuesto_ti.csv`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/datos/presupuesto_ti.csv). Total aprobado. **S/ 1 080 000** (1.46 % de la facturación).

### Los tres expedientes

#### Expediente 1 · Portal de autoservicio

| Campo | Contenido |
|---|---|
| Año | 2024 |
| Responsable | Rocío Maquera Peralta |
| Presupuesto aprobado | S/ 313 508.49 |
| Ejecutado | S/ 509 509.64 |
| Desviación | **+62.5 %** |
| Beneficio declarado en la solicitud | Disponibilidad del servicio |
| ¿Se midió el beneficio después? | **Parcial** |
| Documentos que la organización conserva | Solicitud, cotizaciones, orden de compra, factura |
| Documentos que **no** conserva | Caso de negocio con alternativas, acta de aceptación, medición posterior |

**Justificación transcrita de la solicitud original.**

> «El proveedor informó que la versión en uso deja de tener soporte. Es indispensable actualizar.»

**Lo que la organización responde.**

| Pregunta | Respuesta |
|---|---|
| ¿Se evaluaron alternativas? | «Se pidieron tres cotizaciones del mismo producto» |
| ¿Quién aprobó la desviación presupuestal? | «Administración y Finanzas» |
| ¿Se firmó un acta de aceptación? | «Se recibió conforme, sin acta» |
| ¿Se midió si el beneficio se logró? | «Parcial» |

#### Expediente 2 · Sistema de respaldo

| Campo | Contenido |
|---|---|
| Año | 2024 |
| Responsable | Nadia Ticona Cutipa |
| Presupuesto aprobado | S/ 280 369.14 |
| Ejecutado | S/ 375 784.32 |
| Desviación | **+34.0 %** |
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
| ¿Se firmó un acta de aceptación? | «No» |
| ¿Se midió si el beneficio se logró? | «No» |

#### Expediente 3 · Enlace de datos redundante

| Campo | Contenido |
|---|---|
| Año | 2023 |
| Responsable | Miguel Colque Apaza |
| Presupuesto aprobado | S/ 62 127.30 |
| Ejecutado | S/ 82 579.34 |
| Desviación | **+32.9 %** |
| Beneficio declarado en la solicitud | Cumplimiento normativo |
| ¿Se midió el beneficio después? | **No se midió** |
| Documentos que la organización conserva | Solicitud, cotizaciones, orden de compra, factura |
| Documentos que **no** conserva | Caso de negocio con alternativas, acta de aceptación, medición posterior |

**Justificación transcrita de la solicitud original.**

> «Es necesario para no detener la operación. El equipo actual está al límite de su capacidad.»

**Lo que la organización responde.**

| Pregunta | Respuesta |
|---|---|
| ¿Se evaluaron alternativas? | «Se pidieron tres cotizaciones del mismo producto» |
| ¿Quién aprobó la desviación presupuestal? | «Gerencia, verbalmente» |
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
| PT01 · Licencias y suscripciones | Operación | S/ 226 800 | S/ 155 842 | -31.3 % |
| PT02 · Soporte y mantenimiento de sistemas | Operación | S/ 205 200 | S/ 149 414 | -27.2 % |
| PT03 · Infraestructura y equipamiento | Operación | S/ 183 600 | S/ 163 155 | -11.1 % |
| PT04 · Comunicaciones y enlaces | Operación | S/ 118 800 | S/ 136 723 | 15.1 % |
| PT05 · Personal de TI | Operación | S/ 216 000 | S/ 153 491 | -28.9 % |
| PT06 · Proyectos nuevos | Inversión | S/ 86 400 | S/ 76 681 | -11.2 % |
| PT07 · Seguridad de la información | Operación | S/ 43 200 | S/ 28 322 | -34.4 % |
| **Total** | | **S/ 1 080 000** | **S/ 863 629** | **-20.0 %** |

### Anexo 5 · `datos/inversiones_cerradas.csv`

Las tres inversiones cerradas, con el beneficio que declaramos y el que medimos.

| Inversión | Año | Presupuesto | Ejecutado | Beneficio declarado | Beneficio medido | Responsable |
|---|---|---|---|---|---|---|
| INV01 · Portal de autoservicio | 2024 | S/ 313 508 | S/ 509 510 | Disponibilidad del servicio | Parcial | Rocío Maquera Peralta |
| INV02 · Sistema de respaldo | 2024 | S/ 280 369 | S/ 375 784 | Ahorro en licencias | No se midió | Nadia Ticona Cutipa |
| INV03 · Enlace de datos redundante | 2023 | S/ 62 127 | S/ 82 579 | Cumplimiento normativo | No se midió | Miguel Colque Apaza |

---

[Semana 07](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 07·07](CASO-07-07-instituto-vertiente-sur.md) · **Caso 07·08** · [Caso 07·09](CASO-07-09-servicios-mineros-cordillera.md) · [Encargo 07](../../ENCARGOS-UNIDAD-II/CASO-07-gobierno-y-gestion-de-ti.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
