# Solucionario del docente · Dinámica 08 «El criterio exacto»

**SI-084 · Auditoría de Sistemas** · Semana 08 · **Material del docente. No se publica ni se entrega al alumno.**

> Es la dinámica con más riesgo de discusión en aula, porque la respuesta correcta **cambia según si la organización del equipo es pública o privada**. Esta clave resuelve las seis condiciones en las dos variantes.

---

## Cómo se usa en los 35 minutos

| Minuto | Qué hace el docente |
|---|---|
| 0–2 | Recuerda al aula que la sección A de su ficha decide. **Es la única instrucción previa que hace falta** |
| 2–9 | Clasificación por cuerpo normativo. Corrige solo aquí el error de fondo. Confundir marco con ley |
| 9–17 | La norma exacta. Se exige numeral. Recorre las mesas pidiendo que lean el numeral en voz alta |
| 17–24 | Consecuencia. Se corrige el «es un riesgo» en el momento en que aparece |
| 24–31 | Autoridad. Es la columna que más se falla y la que esta clave resuelve por empresa |
| 31–35 | Ronda de cierre. Se pide la condición 6 de dos equipos, uno público y uno privado. **El contraste entre ambos es la lección de la sesión** |

**La regla que zanja cualquier discusión.** COBIT y la ISO no son ley. Nadie multa por incumplirlos. Obligan cuando la organización los adoptó, cuando un contrato los exige o cuando una norma peruana los incorpora. Esa distinción es el eje de la dinámica y el primer criterio de la rúbrica.

> **Sobre los numerales.** Los artículos y controles de esta clave se citan con el texto vigente al ciclo 2026-II. Antes de dictar, conviene confirmar la vigencia de los numerales de la Ley 29733 y de su reglamento, porque el D. S. 016-2024-JUS renumeró parte del articulado reglamentario. Lo que no cambia es el criterio de fondo, que es lo que la rúbrica califica.

---

## Clave de las condiciones 1 a 5

Son iguales en las diez empresas. Solo cambia el nombre del sistema principal, que la ficha de cada caso ya sustituye.

### Condición 1 · El mismo usuario registra y aprueba por encima del umbral

| | |
|---|---|
| **Cuerpo normativo** | **Norma técnica adoptada** y control interno. No es ley, salvo en los dos casos regulados que se indican abajo |
| **Norma exacta** | NTP-ISO/IEC 27001:2022 **A.5.15** Control de acceso · **A.8.3** Restricción del acceso a la información · COBIT 2019 **DSS06.03** *Manage roles, responsibilities, access privileges and levels of authority* · COSO 2013, **principio 10**, actividades de control |
| **Consecuencia** | Observación de control interno. Si además produjo un pago indebido, responsabilidad civil y eventualmente penal por el hecho, no por la configuración |
| **Autoridad** | Ninguna externa en el caso general. El destinatario es el directorio o el titular de la entidad |
| **Variantes** | **04 COOPAC** — además Resolución SBS **504-2021**, gestión de seguridad de la información; autoridad **SBS**. **03 y 08, públicas** — además responsabilidad por control interno ante la **Contraloría General de la República** |

> **El error clásico.** Escribir «Ley SOX» o «ley de segregación de funciones». No existe en el Perú una ley que imponga segregación de funciones a una empresa privada. El criterio es técnico o interno, y decirlo bien es exactamente lo que la rúbrica premia.

### Condición 2 · No hay revisión periódica de usuarios habilitados

| | |
|---|---|
| **Cuerpo normativo** | Norma técnica adoptada |
| **Norma exacta** | NTP-ISO/IEC 27001:2022 **A.5.18** Derechos de acceso · **A.5.16** Gestión de identidades · COBIT 2019 **DSS05.04** *Manage user identity and logical access* |
| **Consecuencia** | Observación de control. Si hay datos personales accesibles a quien ya no debe tenerlos, se transforma en infracción a la **Ley 29733, artículo 9**, principio de seguridad |
| **Autoridad** | Interna. La **ANPD** solo si se acredita el acceso indebido a datos personales |
| **Variantes** | **02 Clínica** — el dato es de salud, categoría sensible; la exposición agrava la calificación de la infracción. **04 COOPAC** — Resolución SBS 504-2021, autoridad **SBS** |

### Condición 3 · Respaldos que se ejecutan pero nunca se prueban

| | |
|---|---|
| **Cuerpo normativo** | Norma técnica adoptada |
| **Norma exacta** | NTP-ISO/IEC 27001:2022 **A.8.13** Respaldo de la información · **A.5.30** Preparación de las TIC para la continuidad del negocio · COBIT 2019 **DSS04.04** *Exercise, test and review the business continuity plan* |
| **Consecuencia** | Observación de control. El efecto se cuantifica con el RTO del BIA. La organización declara recuperarse en un plazo que no ha demostrado poder cumplir |
| **Autoridad** | Interna |
| **Variantes** | **04 COOPAC** — la continuidad es exigencia de la **SBS**. **08 EPS** — la continuidad del servicio de agua es exigible por **SUNASS**, y la Contraloría puede observarla como control interno |

> **La respuesta que vale 5** no se queda en «falta probar el respaldo». **Dice.** *El BIA declara un RTO de N horas para tal actividad y no existe evidencia de que la restauración se haya ejecutado nunca; el objetivo declarado no está sustentado*. Ese salto de la condición al efecto medido es lo que se busca.

### Condición 4 · Sistema en producción con contrato de soporte vencido

| | |
|---|---|
| **Cuerpo normativo** | **Obligación contractual**, y su ausencia. Este es el punto. No hay contrato que incumplir, y esa es la irregularidad |
| **Norma exacta** | NTP-ISO/IEC 27001:2022 **A.5.19** Seguridad de la información en las relaciones con proveedores · **A.5.20** Tratamiento de la seguridad dentro de los acuerdos con proveedores · COBIT 2019 **APO10.04** *Manage supplier risk* · Código Civil, artículos **1361** y **1362**, sobre la fuerza obligatoria del contrato y la buena fe |
| **Consecuencia** | Incumplimiento contractual y desprotección jurídica. Si el servicio falla, la organización no tiene título para exigir el nivel de servicio ni la indemnización |
| **Autoridad** | Ninguna administrativa. Se resuelve en sede judicial o arbitral |
| **Variantes** | **03 y 08, públicas** — la continuidad del servicio sin contrato vigente es además observación de la **Contraloría** y puede infringir la normativa de contrataciones del Estado; el **OSCE** interviene en lo referido al procedimiento |

> **El error clásico.** Clasificarla como norma técnica. La condición 4 es la única de las seis cuyo cuerpo normativo es contractual, y por eso está en la lista. Si un equipo clasifica las seis como norma técnica, ya perdió el primer criterio.

### Condición 5 · Sin registro de incidentes con severidad ni tiempo de atención

| | |
|---|---|
| **Cuerpo normativo** | Norma técnica adoptada. Se convierte en legal cuando existe deber de notificar |
| **Norma exacta** | NTP-ISO/IEC 27001:2022 **A.5.24** Planificación y preparación de la gestión de incidentes de seguridad de la información · **A.5.25** Evaluación y decisión sobre eventos · COBIT 2019 **DSS02.02** *Record, classify and prioritise requests and incidents* |
| **Consecuencia** | Observación de control. Sin clasificación no hay forma de saber si se cumplió un deber de notificación, lo que agrava cualquier incidente posterior |
| **Autoridad** | Interna, con las excepciones siguientes |
| **Variantes** | **04 COOPAC** — deber de reportar incidentes a la **SBS** conforme a la Resolución 504-2021. **03 y 08, públicas** — deber de notificar al **CNSD** de la PCM en el marco del D. U. 007-2020 y su reglamento. **02 Clínica** — un incidente sobre datos de salud activa deberes ante la **ANPD** |

---

## Clave de la condición 6, que cambia por empresa

| Empresa | Naturaleza | Condición 6 | Cuerpo normativo | Norma exacta | Consecuencia | Autoridad |
|---|---|---|---|---|---|---|
| **01** Agroexportadora | Privada | Sin inventario de datos personales ni registro de finalidades | **Legal** | Ley 29733, **art. 28** obligaciones del titular del banco de datos, y **art. 32** Registro Nacional · D. S. 016-2024-JUS | Infracción sancionable con multa en UIT según **arts. 38 y 39** | **ANPD** — MINJUSDH |
| **02** Clínica San Ramón | Privada | Ídem | **Legal, agravada** | Ídem, más **art. 13.5** sobre datos sensibles de salud | Infracción de mayor gravedad por tratarse de datos sensibles | **ANPD**; **SUSALUD** en lo referido a la historia clínica |
| **03** Municipalidad | **Pública** | **Sin Líder de Gobierno Digital ni Comité constituido** | **Legal** | D. Leg. **1412**, Ley de Gobierno Digital, y su reglamento **D. S. 029-2021-PCM** · R. M. **119-2018-PCM**, que crea el Comité y el Líder | Incumplimiento de norma de obligatorio cumplimiento. Responsabilidad administrativa funcional del titular | **PCM — Secretaría de Gobierno y Transformación Digital**; **Contraloría General** por la responsabilidad funcional |
| **04** COOPAC | Privada supervisada | Sin inventario de datos personales | **Legal**, concurrente | Ley 29733, arts. 28 y 32 · Resolución **SBS 504-2021** | Multa de la ANPD y observación de la SBS, que concurren | **ANPD** y **SBS** |
| **05** Transportes | Privada | Sin inventario de datos personales | **Legal** | Ley 29733, arts. 28 y 32 | Multa en UIT | **ANPD** |
| **06** Distribuidora | Privada | Ídem | **Legal** | Ídem | Multa en UIT | **ANPD** |
| **07** Instituto | Privada | Ídem, sobre datos de estudiantes | **Legal** | Ley 29733, arts. 28 y 32. Si hay menores de edad, tratamiento con reglas propias | Multa en UIT | **ANPD**; **MINEDU** en lo académico |
| **08** EPS Aguas del Sur | **Pública** | **Sin Líder de Gobierno Digital ni Comité constituido** | **Legal** | D. Leg. 1412 · D. S. 029-2021-PCM · R. M. 119-2018-PCM | Incumplimiento y responsabilidad administrativa funcional | **PCM — SGTD**; **Contraloría General** |
| **09** Servicios Mineros | Privada | Sin inventario de datos personales | **Legal**, y además **contractual** | Ley 29733, arts. 28 y 32, más la exigencia de homologación del cliente minero | Multa en UIT y pérdida de la homologación, que termina el contrato | **ANPD**; el **cliente** como parte contractual |
| **10** Farmacias | Privada | Ídem, con datos de salud en el programa de fidelización | **Legal, agravada** | Ley 29733, arts. 28 y 32, más **art. 13.5** si el programa infiere condición de salud a partir de la compra | Infracción de mayor gravedad | **ANPD**; **DIGEMID** por productos controlados |

> **El contraste que cierra la sesión.** Las ocho empresas privadas responden ante la ANPD por un inventario de datos que no existe. Las dos públicas responden ante la PCM y la Contraloría por un cargo que no se designó. Misma ausencia de gobierno, dos cuerpos normativos, dos autoridades. Si el aula se lleva solo eso, la dinámica cumplió.

---

## Los errores que se repiten

| Lo que escriben | Por qué está mal | Corrección en una frase |
|---|---|---|
| «Incumple la ISO 27001» en una empresa privada que no está certificada | La ISO no obliga por sí misma | «¿Quién te multa por eso? Nadie. Entonces no es ley, es criterio técnico» |
| «Autoridad: OSIPTEL» o «la SUNAT» por defecto | Se elige el regulador conocido, no el competente | «Lee la sección A de tu ficha y dime quién te supervisa» |
| «Consecuencia: riesgo de pérdida de información» | No es consecuencia jurídica | «Eso es el efecto técnico. ¿Qué te pasa **ante la autoridad**?» |
| Citan «la Ley de Protección de Datos» sin artículo | La consigna exige numeral y la rúbrica lo mide | «Ley 29733 tiene 40 artículos. ¿Cuál?» |
| Fuerzan la condición 6 pública hacia la Ley 29733 | Aplicable, pero no es lo que la condición describe | «La condición dice que no se designó un cargo. ¿Qué norma manda designarlo?» |

---

## Puntuación rápida

| Criterio | 5 si… | 1 si… |
|---|---|---|
| **Cuerpo normativo** | Las seis bien clasificadas, con la 4 como contractual y la 6 como legal | Clasifica COBIT o la ISO como ley |
| **Precisión del criterio** | Numeral en al menos cinco de las seis | Cita normas por su nombre común |
| **Consecuencia** | Distingue multa administrativa, responsabilidad funcional, incumplimiento contractual y delito | «Es un riesgo» |
| **Autoridad** | Coincide con la columna de la tabla de la condición 6 y con las variantes de la 1 a la 5 | Repite la misma autoridad en las seis filas |

**Nota de cierre.** Un equipo de empresa pública que no nombra a la Contraloría en ninguna de las seis filas no ha entendido la naturaleza de su organización, y eso limita el cuarto criterio a 1 aunque las normas citadas sean correctas.
