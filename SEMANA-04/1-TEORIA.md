[Semana 04](README.md) · **Teoría** · [Dinámica de aula](2-DINAMICA.md) · [Taller de laboratorio](3-TALLER.md)

# Teoría · Controles de Auditoría de Aplicación, Físicos, Lógicos y de Calidad · La Ley SOX en el Perú

**SI-084 · Auditoría de Sistemas** · Semana 04 · Sesión 1 en aula · 2 horas académicas, 100 min, con la dinámica incluida

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](../GLOSARIO.md).

---

## La pregunta de esta sesión

Una distribuidora audita su sistema de ventas. El auditor toma la validación que impide aplicar un descuento mayor al 20 % y comprueba, transacción por transacción, que **ninguna de las 4 100 ventas del año superó ese límite**. El control funciona. Lo documenta como efectivo y cierra el papel de trabajo.

Cuatro meses después, la empresa descubre que un vendedor aplicó descuentos del 45 % a tres clientes durante seis semanas. Las ventas están en el sistema, con su descuento, y **la validación sigue ahí, funcionando**.

> **La pregunta que ordena esta sesión.** *¿Cómo puede un control que se verificó y funciona estar fallando desde antes de que se verificara?*

## Antes de empezar

| Lo que necesita traer | De dónde sale |
|---|---|
| Los principios de mínimo privilegio, segregación de funciones y rendición de cuentas | Semana 02 |
| La estructura de un hallazgo — condición, criterio, causa, efecto, recomendación | Semana 01 |
| La noción de riesgo y de tratamiento del riesgo | Semana 03 |
| Qué es un objetivo de control y dónde vive en COBIT 2019 | Semana 03 |

> **Exploración (5 min), antes de cualquier definición.** Sin abrir apuntes, el aula responde tres preguntas y las respuestas quedan a la vista para contrastarlas al cierre. *¿Qué pudo pasar con la validación del descuento? ¿Qué habría tenido que mirar el auditor y no miró? ¿A quién le pediría usted la evidencia?* No se corrige ninguna respuesta todavía.

## Distribución del tiempo

| Momento | Minutos |
|---|---|
| El problema del descuento y la exploración inicial | 10 |
| **Bloque 1.** Qué es un control y cuándo actúa · con su microaplicación | 15 |
| **Bloque 2.** Controles generales de TI y la dependencia jerárquica · con su microaplicación | 15 |
| **Bloque 3.** Controles de aplicación sobre el ciclo del dato · con su microaplicación | 12 |
| **Bloque 4.** Controles físicos, ambientales y de calidad | 5 |
| **Bloque 5.** La Ley Sarbanes-Oxley y el régimen peruano | 5 |
| Cierre, respuesta a la pregunta de la sesión y puente a la dinámica | 3 |
| **Total de la sesión de aula** | **65** |

## Mapa de la sesión

---

## Bloque 1 · Qué es un control y cuándo actúa

> **La pregunta del bloque.** *Si un control evita el daño, ¿para qué sirven los demás?*

Un control es cualquier medida —política, procedimiento, práctica o estructura organizacional— diseñada para dar seguridad razonable de que los objetivos se alcanzarán y los eventos no deseados serán prevenidos, detectados o corregidos.

**Clasificación por momento de actuación.**

| Tipo | Actúa | Ejemplo en TI | Ventaja | Costo |
|---|---|---|---|---|
| **Preventivo** | Antes del evento | Validación de entrada, MFA, control de acceso | Evita el daño | Alto, fricciona la operación |
| **Detectivo** | Durante o después | Conciliación, revisión de bitácoras, alertas del SIEM | Descubre lo que el preventivo dejó pasar | Medio |
| **Correctivo** | Después del evento | Restauración de respaldo, plan de recuperación | Limita la consecuencia | Bajo, pero el daño ya ocurrió |
| **Disuasivo** | Sobre la voluntad | Política de sanciones, banner de monitoreo | Muy bajo costo | No impide al determinado |
| **Compensatorio** | Sustituye a uno inviable | Revisión posterior cuando no hay segregación de funciones | Viable en organizaciones pequeñas | Requiere disciplina |

> **Regla de diseño.** Un buen sistema de control combina las tres primeras categorías. Una organización con solo controles preventivos no sabe cuándo falló; una con solo detectivos vive apagando incendios.

**Ejemplo trabajado — un mismo riesgo, cinco controles.** Riesgo. *Un empleado transfiere fondos a una cuenta que no corresponde a un proveedor real.*

| Tipo | Control concreto | Qué pasa si es el único que existe |
|---|---|---|
| Preventivo | El alta de un proveedor exige validación del RUC contra el padrón de la SUNAT y aprobación de un segundo | El determinado puede coludirse con quien aprueba |
| Detectivo | Reporte semanal de proveedores nuevos, revisado por Contraloría interna | El fraude ocurre y se descubre después; el dinero puede haber salido |
| Correctivo | Procedimiento de reversión de transferencia dentro de las 24 h | Solo sirve si el detectivo actuó a tiempo |
| Disuasivo | Cláusula de sanción en el reglamento interno, firmada por el trabajador | No detiene a quien ya decidió hacerlo |
| Compensatorio | En una empresa de 6 personas donde no hay segundo aprobador. Revisión mensual de todos los pagos por el contador externo | Depende de que el externo efectivamente revise |

Fíjese en que **ninguno alcanza solo**. Ese es el argumento de por qué el auditor evalúa el conjunto y no controla uno por uno.

> **Microaplicación (4 min) · clasificar en voz alta.** El docente lanza los tres casos y el aula responde levantando la mano por categoría antes de que se diga la respuesta. Sirve para que el error salga a la luz mientras aún se puede corregir.

| Caso | Qué debe contener una buena respuesta |
|---|---|
| Un banco tiene MFA en todas sus aplicaciones y ningún control detectivo. ¿Qué riesgo asume? | Que no se entera de los accesos indebidos que el MFA no evitó. Credenciales robadas con el segundo factor comprometido, o abuso por parte de un usuario legítimo |
| ¿Un respaldo es un control preventivo, detectivo o correctivo? | Correctivo. No evita el incidente ni lo detecta: limita la consecuencia. Quien lo llama preventivo confunde el momento en que actúa |
| ¿Cuándo es legítimo apoyarse en un control compensatorio? | Cuando el control ideal es inviable por tamaño o costo, la compensación cubre el mismo objetivo y **queda documentada la razón**. Nunca como excusa permanente |

> **El error frecuente del bloque.** Llamar preventivo al respaldo. Es el más repetido y revela la confusión de fondo — se clasifica por **lo que el control protege** en lugar de por **cuándo actúa**. Un respaldo protege el dato, sí, pero actúa después del incidente. La pregunta que desarma el error es siempre la misma — *¿el daño ya ocurrió cuando este control entra en juego?*

**Clasificación por naturaleza.**

| Categoría | Alcance | Quién los evalúa |
|---|---|---|
| **Controles generales de TI (ITGC)** | Aplican a **todo** el ambiente de TI | Auditor de sistemas |
| **Controles de aplicación** | Aplican a **una** transacción o proceso de negocio | Auditor de sistemas junto al auditor de proceso |

**La dependencia jerárquica** es el concepto más importante de la semana. **Los controles de aplicación solo son confiables si los ITGC son efectivos**. Si cualquier desarrollador puede modificar el código en producción (ITGC de gestión de cambios roto), entonces la validación de que «el descuento no puede superar el 20 %» es irrelevante. Alguien pudo cambiarla ayer y devolverla hoy. Por eso el auditor **siempre evalúa primero los ITGC**.

## Bloque 2 · Controles generales de TI y la dependencia jerárquica

> **La pregunta del bloque.** *¿Por qué el auditor no puede concluir sobre la validación del descuento sin mirar antes otra cosa?*

| Dominio ITGC | Qué asegura | Pruebas típicas | COBIT 2019 | ISO/IEC 27001:2022 |
|---|---|---|---|---|
| **Gestión de accesos** | Solo los autorizados acceden y solo a lo que necesitan | Revisión de altas/bajas, permisos efectivos, cuentas privilegiadas, revisión periódica | DSS05, DSS06 | A.5.15–A.5.18, A.8.2–A.8.5 |
| **Gestión de cambios** | Todo cambio a producción es autorizado, probado y trazable | Muestra de cambios: ¿aprobación? ¿evidencia de prueba? ¿segregación desarrollo-producción? ¿plan de reversión? | BAI06, BAI07 | A.8.32, A.8.31 |
| **Operaciones de TI** | Los procesos programados se ejecutan y los incidentes se gestionan | Revisión de *jobs* fallidos, respaldo y restauración, gestión de incidentes | DSS01, DSS02, DSS04 | A.8.13, A.8.14, A.5.24–A.5.26 |
| **Desarrollo y adquisición** | El software cumple los requisitos y no introduce riesgos | Metodología, pruebas, aceptación del usuario, revisión de código | BAI03, BAI05 | A.8.25–A.8.31 |

**Prueba de diseño vs. prueba de eficacia operativa.** Son dos pruebas distintas y el informe debe distinguirlas:

- **Diseño.** ¿El control, tal como está definido, mitigaría el riesgo si se ejecutara siempre? Se evalúa leyendo el procedimiento y entrevistando.
- **Eficacia operativa.** ¿El control **efectivamente se ejecutó** durante todo el periodo auditado? Se evalúa con muestreo y evidencia de cada ejecución.

Un control bien diseñado que se ejecutó 8 de 12 meses **falla la prueba de eficacia operativa**, y ese es un hallazgo distinto —y a menudo más grave— que un control mal diseñado.

**Ejemplo trabajado — el mismo control, las dos pruebas.** Control. *Todo cambio a producción requiere aprobación del jefe de sistemas antes de aplicarse.*

| | Prueba de diseño | Prueba de eficacia operativa |
|---|---|---|
| **Qué se pregunta** | ¿El procedimiento, tal como está escrito, evitaría un cambio no autorizado? | ¿Se aprobaron efectivamente los cambios del periodo, antes de aplicarse? |
| **Cómo se prueba** | Se lee el procedimiento y se entrevista al responsable | Se toma la población de cambios del periodo y se verifica la evidencia de aprobación de cada uno |
| **Evidencia** | El procedimiento firmado | El registro de cambios, contrastado con los despliegues reales del sistema |
| **Resultado posible A** | Diseño adecuado | 14 de 14 cambios aprobados → **el control opera** |
| **Resultado posible B** | Diseño adecuado | 9 de 14 aprobados, y 3 de los 5 sin aprobar son de urgencia → **falla la eficacia operativa** |
| **Resultado posible C** | El procedimiento permite que el mismo desarrollador apruebe → **falla el diseño** | **Irrelevante.** Si el diseño falla, no se prueba la eficacia |

> **El orden importa.** Si el diseño falla, la prueba de eficacia no se ejecuta. No tiene sentido verificar la operación de un control que no mitigaría el riesgo aunque operara siempre.

> **Microaplicación (5 min) · el caso del descuento, resuelto.** Se vuelve al problema con el que abrió la sesión y el aula responde en parejas, por escrito y en una línea, *¿qué ITGC falló para que la validación del 20 % dejara de proteger?* Se recogen dos o tres respuestas antes de dar la correcta.

| Caso | Qué debe contener una buena respuesta |
|---|---|
| El auditado dice: «el control existe, lo que pasa es que no lo documentamos». ¿Es un hallazgo? | Sí. Un control que no deja rastro no puede verificarse. La condición no es que el control no exista, sino que **no hay evidencia de su operación** durante el periodo |
| En una empresa de 8 personas, el jefe de sistemas desarrolla, prueba y despliega. ¿Qué se recomienda? | No «contratar más gente». Un control compensatorio: revisión posterior por un tercero —el contador externo o la gerencia— de los cambios aplicados, con registro. Se declara como compensatorio y por qué |
| ¿Por qué el auditor evalúa primero los ITGC y no los controles de aplicación? | Porque si los ITGC fallan, cualquier conclusión sobre los controles de aplicación pierde sustento. La validación pudo alterarse sin dejar rastro |

> **La respuesta al problema de la sesión.** El vendedor no burló la validación. **Alguien con acceso al código la desactivó, aplicó los descuentos y la devolvió.** El ITGC de gestión de cambios estaba roto —cualquiera podía desplegar sin aprobación ni rastro— y por eso el control de aplicación era inauditable desde el principio. El auditor verificó 4 100 transacciones contra una regla que no sabía si había estado vigente durante el periodo. **Probó la fotografía de hoy y concluyó sobre el año.**

> **El error frecuente del bloque.** Probar la eficacia operativa de un control cuyo diseño no se ha evaluado. Si el diseño falla, la prueba de operación es trabajo perdido, y peor aún, produce una conclusión favorable sobre un control que no protege.

## Bloque 3 · Controles de aplicación sobre el ciclo del dato

> **La pregunta del bloque.** *El dato entra bien. ¿Dónde puede estropearse después?*

Se organizan siguiendo el recorrido del dato dentro del sistema:

| Etapa | Objetivo de control | Controles concretos |
|---|---|---|
| **Entrada** | Que el dato ingrese completo, exacto y una sola vez | Validación de formato, rango y tipo; dígito verificador (p. ej. el del RUC); listas de valores; campos obligatorios; **control de duplicados**; autorización previa a la captura |
| **Procesamiento** | Que el cálculo sea correcto y no se pierdan ni dupliquen registros | Totales de control (*hash totals*, *record counts*); conciliación entrada-salida; control de secuencia; manejo de excepciones a un archivo de rechazos revisable; reproceso controlado |
| **Salida** | Que el resultado llegue completo y solo a quien corresponde | Conciliación de totales; distribución controlada de reportes; marcado de clasificación; registro de impresión y exportación |
| **Archivo y datos maestros** | Que los datos permanentes sean íntegros | Restricciones referenciales; autorización dual para cambios de datos maestros (proveedores, cuentas bancarias); bitácora de cambios |
| **Pistas de auditoría** | Que toda transacción sea reconstruible | Registro inalterable de quién, qué, cuándo y desde dónde |

**Los seis objetivos de aserción.** El auditor pregunta, para cada aplicación — ¿los datos son **completos**, **exactos**, **válidos**, **autorizados**, **oportunos** y **restringidos**? Cada control de aplicación sirve a al menos uno de estos seis objetivos, y todo control que no sirva a ninguno es un control decorativo.

**Ejemplo trabajado — control de cambio de cuenta bancaria del proveedor.** Es el vector del fraude BEC (*Business Email Compromise*), uno de los de mayor pérdida económica global:

| Objetivo | Control | Prueba de auditoría |
|---|---|---|
| Autorizado | Doble aprobación fuera del canal de solicitud (llamada al contacto registrado) | Muestrear 25 cambios y verificar evidencia de la verificación telefónica |
| Trazable | Bitácora inalterable del cambio con valor anterior y nuevo | Consultar la tabla de auditoría y verificar que no sea editable |
| Detectivo | Reporte semanal de cambios de datos bancarios revisado por Tesorería | Verificar firma o registro de revisión en 12 semanas del periodo |
| Preventivo | Bloqueo de pagos durante 48 h tras un cambio de cuenta | Intentar un pago inmediato en el ambiente de pruebas |

> **Microaplicación (3 min) · el control decorativo.** El docente enuncia un control real de un sistema conocido —«el sistema exige que el campo de observaciones tenga al menos diez caracteres»— y el aula responde a mano alzada *¿a cuál de los seis objetivos de aserción sirve?* La respuesta correcta es que a ninguno, y ese es el punto.

> **El error frecuente del bloque.** Auditar la entrada del dato y detenerse ahí. La entrada es donde están los controles visibles y donde el auditado enseña sus validaciones con orgullo. El fraude de cuenta bancaria del ejemplo **no ocurre en la entrada**. Ocurre en los datos maestros, que casi nadie mira.

## Bloque 4 · Controles físicos, ambientales y de calidad

**Físicos y ambientales (ISO/IEC 27001:2022, tema A.7).** Aunque muchas empresas migraron a la nube, el control físico no desaparece — **se transfiere al proveedor y debe auditarse por certificación de tercero** (informe SOC 2 Tipo II, certificado ISO/IEC 27001 con su alcance leído en detalle). En lo que permanece en las instalaciones —oficinas, dispositivos de usuario, cableado, respaldos en cinta— se auditan — perímetro (A.7.1), controles de entrada (A.7.2), protección contra amenazas físicas y ambientales (A.7.5), **escritorio y pantalla limpios** (A.7.7), seguridad del cableado (A.7.12), mantenimiento (A.7.13) y **eliminación o reutilización segura de equipos** (A.7.14).

**Controles de calidad del software.** La NTP-ISO/IEC 12207 estructura los procesos del ciclo de vida y la serie ISO/IEC 25000 (SQuaRE) define el modelo de calidad del producto con ocho características — adecuación funcional, eficiencia de desempeño, compatibilidad, usabilidad, fiabilidad, **seguridad**, mantenibilidad y portabilidad. Para el auditor, la calidad es auditable cuando existe una métrica, un umbral aceptado y evidencia de medición — «cobertura de pruebas ≥ 70 %», «cero vulnerabilidades críticas en el análisis de dependencias antes del despliegue», «defectos en producción por versión ≤ 3».

## Bloque 5 · La Ley Sarbanes-Oxley y el régimen peruano

**Qué es SOX.** La *Sarbanes-Oxley Act of 2002* fue la respuesta legislativa de los Estados Unidos a los fraudes contables de Enron, WorldCom y Tyco. Dos secciones concentran el impacto sobre TI:

| Sección | Exigencia | Consecuencia para TI |
|---|---|---|
| **302** | El CEO y el CFO **certifican personalmente** la veracidad de los estados financieros y la efectividad de los controles de divulgación | La certificación depende de que los sistemas que producen la cifra sean confiables |
| **404** | La dirección debe evaluar y **el auditor externo debe atestiguar** la efectividad del control interno sobre el reporte financiero (ICFR) | Los **ITGC** de los sistemas que alimentan los estados financieros entran en el alcance obligatorio |

El marco de referencia usado es **COSO (*Committee of Sponsoring Organizations of the Treadway Commission*) Internal Control — Integrated Framework (2013)**, con sus cinco componentes — ambiente de control, evaluación de riesgos, actividades de control, información y comunicación, y actividades de supervisión.

**Por qué importa en el Perú.** SOX no es ley peruana, pero alcanza al país por tres vías:

1. **Subsidiarias de empresas listadas en EE. UU.** Mineras, bancos y compañías de consumo masivo con matriz listada en NYSE o NASDAQ aplican SOX a sus operaciones peruanas. Los ITGC del ERP en Lima son evaluados por el auditor externo de la matriz.
2. **Empresas peruanas con ADR (*American Depositary Receipt*) o emisión de deuda en mercados estadounidenses.**
3. **Efecto de arrastre normativo.** El diseño de control interno de SOX se convirtió en el estándar de facto para las auditorías externas y los directorios.

**El marco peruano equivalente.** El Perú construyó su propia arquitectura de control:

| Ámbito | Norma | Exigencia relevante |
|---|---|---|
| **Sistema financiero, de seguros y AFP** | **Resolución SBS N.º 504-2021** (vigente desde el 1 de julio de 2021; modificada por las Resoluciones SBS 1515-2021 y 3797-2023) | Obliga a implementar un **Sistema de Gestión de Seguridad de la Información y Ciberseguridad (SGSI-C)**, con roles definidos, gestión de incidentes, autenticación reforzada y reporte a la SBS. Modificó además los Reglamentos de Auditoría Interna y de Auditoría Externa |
| **Mercado de valores** | Código de Buen Gobierno Corporativo para las Sociedades Peruanas (SMV) y reporte anual de cumplimiento | Divulgación del sistema de control interno y de la gestión de riesgos |
| **Sector público** | Ley 28716 de Control Interno de las Entidades del Estado y directivas de la Contraloría General de la República | Implementación y evaluación del sistema de control interno; el Órgano de Control Institucional audita TI |
| **Gobierno digital** | Decreto Legislativo 1412 y D. S. 029-2021-PCM | Líder de Gobierno Digital, Oficial de Seguridad de la Información, uso obligatorio de la NTP-ISO/IEC 27001 vigente |

> **Conclusión operativa.** Cuando un estudiante audite una empresa peruana debe preguntar primero **a qué régimen pertenece** — financiero (SBS), mercado de valores (SMV), público (Contraloría) o privado no regulado. El criterio de auditoría cambia por completo, y aplicar el criterio equivocado invalida el hallazgo.

## Cierre · qué se lleva de aquí

**La respuesta a la pregunta con la que abrimos.** Un control puede estar funcionando el día que se mira y haber estado desactivado el día que importaba. Verificar un control de aplicación sin haber evaluado antes los controles generales de TI **no es una auditoría incompleta, es una conclusión sin sustento**, porque el auditor no puede saber si lo que probó estuvo vigente durante el periodo.

**Las tres ideas que deben quedar.**

| Idea | Por qué importa en el ejercicio profesional |
|---|---|
| Un control se clasifica por **cuándo actúa**, no por lo que protege | Determina qué se puede concluir de él. Un correctivo nunca demuestra que el riesgo no se materializó |
| **Los controles de aplicación solo son confiables si los ITGC son efectivos** | Fija el orden del encargo. Es la razón por la que el programa de trabajo empieza siempre por accesos y cambios |
| Diseño y eficacia operativa son **dos pruebas distintas**, y el orden no es negociable | Un control bien diseñado que operó ocho de doce meses produce un hallazgo distinto —y a menudo más grave— que uno mal diseñado |

**Volviendo a la exploración del inicio.** Se releen las respuestas que el aula dio antes de la teoría. La pregunta que casi nadie hizo —*¿estuvo esa validación vigente todo el año?*— es exactamente la que separa a un técnico que revisa de un auditor que concluye.

**Lo que sigue.** La [dinámica de esta sesión](2-DINAMICA.md) entrega la narrativa del proceso de compras y pagos de su organización, y pide dos cosas que solo se pueden responder con lo visto aquí — **qué control no se puede concluir efectivo por culpa del entorno de TI**, y **cuál falla el diseño y cuál la eficacia operativa**. La distinción que acaba de aprender es literalmente el producto que va a entregar.

---

---

[Semana 04](README.md) · **Teoría** · [Dinámica de aula](2-DINAMICA.md) · [Taller de laboratorio](3-TALLER.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
