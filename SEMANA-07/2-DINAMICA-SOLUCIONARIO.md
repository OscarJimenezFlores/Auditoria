# Solucionario del docente · Dinámica 07 «Las cinco decisiones»

**SI-084 · Auditoría de Sistemas** · Semana 07 · **Material del docente. No se publica ni se entrega al alumno.**

> Contiene la clave por empresa —las decisiones que se esperan, el eslabón frágil sembrado en el caso y la hoja de cálculo que hay que encontrar— más los errores recurrentes y la puntuación rápida.

---

## Cómo se usa en los 35 minutos

| Minuto | Qué hace el docente |
|---|---|
| 0–7 | Deja que extraigan decisiones sin intervenir. El error se corrige mejor cuando ya lo cometieron |
| 7–14 | **Primera corrección, la más importante.** Recorre las mesas leyendo solo la primera columna. Si dice «el ERP», «los reportes» o «la seguridad», eso no es una decisión y hay que reconducirlo ahora, no al final |
| 14–28 | Verifica que la cadena tenga los seis eslabones y que aparezca el dueño del dato con **cargo**, no con área |
| 28–35 | Ronda de cierre. Cada equipo lee **solo el eslabón más frágil**. Se comparan entre empresas. El aula descubre que la fragilidad se repite en forma de hoja de cálculo intermedia |

**La pregunta que separa la decisión del sistema.** «¿Quién firma esto y qué pasa si firma distinto?» Si no hay alguien que firme y no hay dos resultados posibles, no es una decisión.

---

## Clave por empresa

La columna **eslabón frágil** es la respuesta esperada del Producto 2. Está sembrada en la sección C o F de la ficha de cada caso, de modo que el equipo puede encontrarla sin salir del aula.

### 01 · Agroexportadora Valle Viejo

| | |
|---|---|
| **Decisiones esperadas** | A qué productor asociado se le compra y a qué precio · Qué lote se embarca y con qué certificación · Cuándo se riega y con qué dosis · Qué inversión de campaña se aprueba · A qué mercado de destino se asigna el lote |
| **Eslabón frágil** | **La trazabilidad de lote se arma a mano en Excel en cada embarque.** El dato nace en la balanza sin red, pasa a la base Access de un exempleado y termina en una hoja de cálculo que ningún sistema valida |
| **Hoja de cálculo** | Sí, y es el centro del hallazgo. Sin control de versiones, sin dueño formal, sin bitácora de cambios. Es EUC (End User Computing) puro |
| **Efecto sobre la decisión** | La certificación de origen que se entrega al comprador europeo se sostiene en un archivo que cualquiera puede editar. El reclamo de 2024 costó 11 días de reconstrucción |
| **Control que falta** | Registro de trazabilidad en el sistema con bloqueo tras el cierre del lote, y conciliación automática entre peso de balanza y peso embarcado |

### 02 · Clínica San Ramón

| | |
|---|---|
| **Decisiones esperadas** | Qué tratamiento se indica al paciente · Qué se factura a la aseguradora y por qué concepto · Qué medicamento se repone en farmacia · A qué paciente se le autoriza un procedimiento de alto costo · Qué convenio se renueva |
| **Eslabón frágil** | **La integración entre laboratorio y HIS es un archivo plano copiado a mano dos veces al día.** En 2025 se adjuntaron 34 resultados al paciente equivocado |
| **Hoja de cálculo** | El archivo plano intermedio cumple exactamente el papel del EUC. No tiene validación de identidad del paciente ni registro de quién lo copió |
| **Efecto sobre la decisión** | La decisión clínica se toma sobre un resultado que puede no ser del paciente. Es la cadena de mayor gravedad de todo el banco de casos |
| **Control que falta** | Interfaz automática con validación de identificador único de paciente y rechazo del registro que no concilie |

### 03 · Municipalidad de Alto Selva

| | |
|---|---|
| **Decisiones esperadas** | A qué contribuyente se le fiscaliza · Qué licencia se aprueba · Qué obra se prioriza en el presupuesto · A quién se le otorga la conformidad de un servicio · Qué deuda se declara incobrable |
| **Eslabón frágil** | **El registro civil opera en papel** y no alimenta ningún sistema. La recaudación depende de un catastro cuya actualización nadie audita |
| **Hoja de cálculo** | Aparece entre catastro y el reporte de recaudación que llega al Concejo. La cifra que decide el presupuesto no sale del sistema |
| **Efecto sobre la decisión** | El Concejo aprueba metas de recaudación sobre una cifra que no es rastreable hasta el padrón |
| **Control que falta** | Conciliación mensual entre el padrón de contribuyentes, lo emitido y lo recaudado, con firma del responsable de Rentas |

> **Es entidad pública.** Si el equipo no menciona la ausencia del Líder de Gobierno Digital al hablar de quién decide en TI, se le señala. La decisión no tiene dueño designado, y eso es en sí mismo el hallazgo de gobierno que pide el bloque 2.

### 04 · COOPAC Frontera Sur

| | |
|---|---|
| **Decisiones esperadas** | A quién se le otorga un crédito y por cuánto · Qué operación se reporta a la UIF · Qué provisión se constituye · Qué socio pasa a cobranza judicial · Qué tasa se fija por producto |
| **Eslabón frágil** | **El SGSI exigido por la Resolución SBS 504-2021 existe en papel desde 2022 y nunca se implementó.** La evaluación crediticia depende de una central de riesgos cuya consulta no deja registro auditable |
| **Hoja de cálculo** | En el cálculo de provisiones y en el reporte a la SBS. El dato sale del core, se ajusta en Excel y se envía |
| **Efecto sobre la decisión** | El reporte regulatorio se sostiene en un ajuste manual sin trazabilidad. Ante la SBS, un reporte que no se puede reconstruir es un incumplimiento |
| **Control que falta** | Generación del reporte regulatorio desde el core, con los ajustes registrados como asientos y no como ediciones de celda |

### 05 · Transportes Sur Andino

| | |
|---|---|
| **Decisiones esperadas** | Qué conductor sale en qué ruta · Qué unidad entra a mantenimiento · Qué ruta se abre o se cierra · Qué precio se fija por tramo y temporada · Qué encomienda se acepta |
| **Eslabón frágil** | **El control de horas de conducción y descanso se lleva en Excel y no cruza con el GPS.** SUTRAN detectó inconsistencias en 23 manifiestos en 2025 |
| **Hoja de cálculo** | Sí, y es el objeto directo de la fiscalización. El dato del GPS existe, pero la decisión se toma sobre el Excel |
| **Efecto sobre la decisión** | Se programa a un conductor sin descanso suficiente. El efecto no es contable, es un riesgo de vida y una sanción de SUTRAN |
| **Control que falta** | Bloqueo en la programación de flota cuando las horas acumuladas del GPS superan el límite, sin posibilidad de anulación manual sin autorización registrada |

### 06 · Distribuidora Andina del Sur

| | |
|---|---|
| **Decisiones esperadas** | Qué se compra y en qué cantidad · A qué cliente se le da crédito y por cuánto · Qué ruta de distribución se programa · Qué pago se libera en tesorería · Qué producto se descontinúa |
| **Eslabón frágil** | **El módulo de almacén del ERP se abandonó y las ubicaciones se sostienen en hojas de cálculo.** El inventario contable y el físico difieren en promedio 4.7 % |
| **Hoja de cálculo** | Es el sistema de facto. No es un intermediario. Reemplazó al módulo |
| **Efecto sobre la decisión** | La reposición se decide sobre un stock que se sabe erróneo en 4.7 %. Sobre 6 000 SKU, el error absoluto es cuantificable en soles y así debe expresarse |
| **Control que falta** | Conteo cíclico con conciliación obligatoria y bloqueo de la orden de compra cuando la diferencia supera el umbral |

### 07 · Instituto Vertiente Sur

| | |
|---|---|
| **Decisiones esperadas** | Qué programa se abre el próximo ciclo · A qué estudiante se le habilita la matrícula · Qué acta se cierra y se remite · A qué docente se le asigna carga · A quién se le otorga fraccionamiento de pensión |
| **Eslabón frágil** | **El aula virtual la administra un docente sin contrato de TI, sin respaldos y con administrador compartido con dos practicantes.** La nota que sustenta el acta pasa por ahí |
| **Hoja de cálculo** | Entre el aula virtual y el sistema académico, para consolidar notas antes del acta |
| **Efecto sobre la decisión** | El acta —documento con efecto legal sobre la titulación— se sostiene en una consolidación manual hecha desde un sistema sin control de acceso |
| **Control que falta** | Carga de notas al sistema académico desde el aula virtual con registro de origen, y cierre de acta que impida edición posterior sin resolución |

### 08 · EPS Aguas del Sur

| | |
|---|---|
| **Decisiones esperadas** | Qué usuario se corta por deuda · Qué reclamo se declara fundado · Qué obra de red se prioriza · Qué tarifa se aplica por categoría · Qué planta se opera a qué caudal |
| **Eslabón frágil** | **La red del SCADA comparte switches con la red administrativa desde 2023**, pese a que el diseño original las separaba. La decisión de operación de planta depende de una red que no está aislada |
| **Hoja de cálculo** | En la atención de reclamos, que se lleva con formulario web y hoja de cálculo. El plazo de SUNASS se controla ahí |
| **Efecto sobre la decisión** | Un reclamo vencido sin respuesta se convierte en silencio administrativo positivo. El control del plazo depende de un archivo sin alertas |
| **Control que falta** | Segmentación de la red SCADA con regla de firewall documentada, y control automático de plazo en el sistema de reclamos |

> **Es entidad pública.** Concurren SUNASS como regulador sectorial y la Contraloría como control gubernamental. Si el equipo solo nombra a uno, está incompleto.

### 09 · Servicios Mineros Cordillera

| | |
|---|---|
| **Decisiones esperadas** | A qué licitación se presenta y con qué precio · Qué personal entra a campamento · Qué equipo entra a mantenimiento · Qué valorización se factura al cliente · Qué observación de homologación se atiende primero |
| **Eslabón frágil** | **La homologación anual del cliente minero se aprobó con nueve observaciones y ninguna se cerró.** La decisión de seguir operando se toma ignorando el estado real del compromiso contractual |
| **Hoja de cálculo** | En la valorización que se factura al cliente, armada fuera del ERP a partir del control de personal en campamento |
| **Efecto sobre la decisión** | Se factura sobre horas que el cliente puede objetar, y la pérdida de homologación pondría fin al contrato. Aquí el criterio es **contractual**, no legal |
| **Control que falta** | Registro de observaciones de homologación con responsable, plazo y evidencia de cierre, revisado en el comité antes de cada valorización |

### 10 · Farmacias Buena Salud

| | |
|---|---|
| **Decisiones esperadas** | Qué se compra a laboratorios y en qué volumen · Qué se distribuye a cada uno de los 23 locales · Qué producto controlado se dispensa y contra qué receta · Qué promoción se lanza · Qué local se abre o se cierra |
| **Eslabón frágil** | **La consolidación nocturna falla dos veces por semana y solo el jefe de sistemas sabe reprocesarla.** Cuando falla, el stock central queda desactualizado y se compra de más |
| **Hoja de cálculo** | En el reproceso manual de la consolidación fallida y en el control de productos controlados exigido por DIGEMID |
| **Efecto sobre la decisión** | La compra se decide sobre un stock que se sabe incorrecto dos veces por semana. Y la dependencia de una sola persona es un riesgo de continuidad nombrable como tal |
| **Control que falta** | Alerta de fallo de consolidación con escalamiento, procedimiento de reproceso documentado y ejecutable por un segundo responsable |

---

## Los errores que se repiten

| Lo que escriben | Por qué no sirve | Qué se les dice |
|---|---|---|
| «Decisión: usar el ERP» | Es un sistema. La rúbrica lo llama «lista de sistemas disfrazada de decisiones» y da 1 punto | «¿Quién firma eso y cuándo?» |
| «Quién la toma: el área de TI» | TI no toma decisiones de negocio. Nombrar el área en vez del cargo oculta que la decisión no tiene dueño | «Un cargo, no un área. Y si no lo hay, escríbelo: eso ya es un hallazgo» |
| Saltan de «sistema» a «decisión» sin pasar por hecho ni dato | Es el segundo criterio de la rúbrica y el más fallado | «¿Dónde nace el hecho? ¿Alguien lo teclea o lo captura un equipo?» |
| «Riesgo: falta de seguridad informática» | Riesgo genérico de TI. Da 1 punto en el tercer criterio | «¿Qué decisión sale mal, en concreto, y cuánto cuesta?» |
| No mencionan hoja de cálculo | Cuarto criterio de la rúbrica, ausente, 0 | «¿En algún punto alguien abre un Excel? Búscalo, está en tu caso» |

---

## Puntuación rápida

| Criterio | 5 si… | 1 si… |
|---|---|---|
| **Decisiones identificadas** | Cinco decisiones con verbo de decisión y frecuencia declarada | Aparece un nombre de sistema en la primera columna |
| **Trazado de la cadena** | Los seis eslabones y el dueño del dato con cargo | Va de sistema a decisión sin hecho ni dato |
| **Eslabón débil** | Coincide con el sembrado en el caso, o es otro igual de específico, y dice qué decisión queda mal fundada | Riesgo genérico de TI |
| **Hoja de cálculo** | La identifica y nombra al menos dos controles ausentes —versión, dueño, bitácora, validación de entrada— | No aparece |

**Nota de cierre.** Un equipo que no encuentra la hoja de cálculo no pasa de 15, porque el cuarto criterio queda en 1. Está sembrada en los diez casos sin excepción.
