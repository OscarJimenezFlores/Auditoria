# Solucionario del docente · Dinámica 05 «El programa de trabajo del área asignada»

**SI-084 · Auditoría de Sistemas** · Semana 05 · **Material del docente. No se publica ni se entrega al alumno.**

> Este archivo existe para que el docente pueda arbitrar la dinámica **en el momento**, sin depender de que el equipo lo convenza. Contiene la clave por área auditable, los errores que se repiten y la puntuación rápida.

---

## Cómo se usa en los 35 minutos

| Minuto | Qué hace el docente |
|---|---|
| 0–3 | Asigna un área distinta a cada equipo. Con más de ocho equipos, se repite área pero **nunca con la misma empresa** |
| 3–20 | Pasa por las mesas con la tabla de la sección «Clave por área». Solo corrige el **objetivo de control**, porque si el objetivo está mal todo lo demás sale mal y ya no hay tiempo de rehacerlo |
| 20–30 | Verifica las dos obligaciones de la consigna — un procedimiento de reejecución y uno de CAAT sobre el 100 % — porque son las dos que más se omiten y las que la rúbrica castiga |
| 30–35 | Ronda de cierre. Cada equipo lee **un solo procedimiento**, el de reejecución. El aula juzga si podría ejecutarlo sin preguntar nada |

**La pregunta que ordena la mesa en diez segundos.** «¿Qué documento me vas a enseñar cuando termines este procedimiento?» Si no hay respuesta, el procedimiento está enunciado como intención y no cumple el criterio de reproducibilidad.

---

## Clave por área auditable

Para cada área, el objetivo de control que se espera, el criterio con su código, el procedimiento de reejecución y el CAAT. **No es la única respuesta correcta, pero sí el nivel exigible.**

### Función informática

| | |
|---|---|
| **Objetivo de control** | Verificar que la función de TI tiene dependencia jerárquica, comité y política aprobados, y que las decisiones de TI se toman en el órgano competente y quedan registradas |
| **Criterio** | COBIT 2019 **EDM01.01** *Evaluate the governance system* · NTP-ISO/IEC 27001:2022 **A.5.2** Roles y responsabilidades de seguridad de la información |
| **Población** | Las actas del órgano de gobierno del periodo y el organigrama vigente |
| **Reejecución** | Tomar tres decisiones de TI del periodo con impacto presupuestal y **rehacer el recorrido de aprobación** — quién lo propuso, en qué acta se aprobó, con qué monto y contra qué partida. Se contrasta con `datos/presupuesto_ti.csv` |
| **CAAT sobre el 100 %** | Cruzar la totalidad de las partidas ejecutadas de `presupuesto_ti.csv` contra las decisiones documentadas. Toda partida sin decisión que la respalde es excepción |
| **Excepción** | Una decisión de TI con impacto presupuestal ejecutada sin acta, o un gasto sin decisión previa |

> **En casi todos los casos el comité no existe y la política está en borrador.** El equipo que escribe «verificar que el comité sesiona trimestralmente» no ha leído la sección B de su ficha. **Corregir en mesa.** El objetivo no cambia, pero la condición esperada es la ausencia y el programa debe estar preparado para documentarla.

### Desarrollo de proyectos

| | |
|---|---|
| **Objetivo de control** | Verificar que todo desarrollo o adquisición pasó por una fase de requisitos aprobada, pruebas de aceptación del usuario y autorización de pase a producción |
| **Criterio** | COBIT 2019 **BAI03.05** *Build solutions* · **BAI07.05** *Perform acceptance tests* · NTP-ISO/IEC 27001:2022 **A.8.29** Pruebas de seguridad en desarrollo |
| **Población** | Los proyectos y adquisiciones de `documentos/expedientes-de-inversion.md` e `datos/inversiones_cerradas.csv` |
| **Reejecución** | Tomar dos expedientes cerrados y **rehacer el cálculo del beneficio declarado** con los datos que la organización tenía en ese momento. Se compara con el beneficio que el expediente afirma |
| **CAAT sobre el 100 %** | Sobre `inversiones_cerradas.csv`, listar todas las inversiones cuyo beneficio declarado no tiene un indicador medido asociado |
| **Excepción** | Un pase a producción sin evidencia de aceptación del usuario, o un beneficio declarado sin línea base |

### Aplicaciones

| | |
|---|---|
| **Objetivo de control** | Verificar que los controles de entrada, proceso y salida de la aplicación impiden que una transacción sea registrada y aprobada por la misma persona por encima del umbral |
| **Criterio** | COBIT 2019 **DSS06.03** *Manage roles, responsibilities, access privileges* · NTP-ISO/IEC 27001:2022 **A.5.15** Control de acceso · **A.8.3** Restricción del acceso a la información |
| **Población** | Las operaciones del periodo en `datos/pagos.csv` y los perfiles de `datos/usuarios_erp.csv` |
| **Reejecución** | Tomar cinco operaciones por encima del umbral y **volver a ejecutar la regla de aprobación** con los perfiles vigentes en la fecha de la operación. Si la regla permite el mismo usuario en registro y aprobación, el control es inefectivo por diseño |
| **CAAT sobre el 100 %** | Sobre el cruce completo de `pagos.csv` y `usuarios_erp.csv`, listar toda operación donde el registrador y el aprobador coinciden. Es la prueba que sostiene la condición 1 de la Semana 08 |
| **Excepción** | Una sola operación con registrador igual a aprobador por encima del umbral |

### Explotación

Es el área del **ejemplo resuelto publicado**. Si un equipo la recibe, se le exige un objetivo distinto del que el ejemplo desarrolla —cierre de periodo en lugar de procesos programados— para que no copie.

| | |
|---|---|
| **Objetivo de control alternativo** | Verificar que el cierre de periodo se ejecuta sobre datos completos, que los ajustes posteriores al cierre están autorizados y que existe evidencia de la conciliación |
| **Criterio** | COBIT 2019 **DSS01.01** *Perform operational procedures* · NTP-ISO/IEC 27001:2022 **A.8.16** Actividades de monitoreo |
| **Reejecución** | Rehacer la conciliación de un periodo cerrado a partir de los movimientos, y comparar con el saldo que el sistema reporta |
| **CAAT sobre el 100 %** | Listar todos los asientos con fecha de registro posterior a la fecha de cierre del periodo al que afectan |

### Infraestructura

| | |
|---|---|
| **Objetivo de control** | Verificar que los activos de TI en producción están inventariados, tienen soporte vigente y que su capacidad se monitorea contra un umbral definido |
| **Criterio** | COBIT 2019 **BAI09.01** *Identify and record current assets* · **BAI04.03** *Plan for new or changed capacity* · NTP-ISO/IEC 27001:2022 **A.5.9** Inventario de activos · **A.8.6** Gestión de capacidad |
| **Población** | Los sistemas de la sección C de `FICHA.md` y los contratos de `documentos/contratos-proveedores.md` |
| **Reejecución** | Tomar el inventario declarado y **recorrer físicamente** tres activos, verificando que existen, que están donde el inventario dice y que su versión coincide |
| **CAAT sobre el 100 %** | Cruzar la totalidad de los sistemas de la sección C contra `documentos/contratos-proveedores.md`. Todo sistema en producción sin contrato vigente es excepción |
| **Excepción** | Un sistema en producción ausente del inventario, o con soporte vencido y servicio en curso |

> **En todos los casos hay al menos un sistema sin soporte vigente y un inventario desactualizado.** El CAAT lo encuentra en un minuto. Es el resultado esperado.

### Seguridad

| | |
|---|---|
| **Objetivo de control** | Verificar que las altas, bajas y modificaciones de usuarios están autorizadas, que se revisan periódicamente y que ningún usuario conserva accesos tras su desvinculación |
| **Criterio** | COBIT 2019 **DSS05.04** *Manage user identity and logical access* · NTP-ISO/IEC 27001:2022 **A.5.16** Gestión de identidades · **A.5.18** Derechos de acceso |
| **Población** | La totalidad de `datos/usuarios_erp.csv`, contrastada con `datos/empleados.csv` |
| **Reejecución** | Tomar tres altas del periodo y **rehacer el trámite** — solicitud, autorización del jefe del área, perfil concedido y comparación con el perfil solicitado |
| **CAAT sobre el 100 %** | Cruce completo de `usuarios_erp.csv` contra `empleados.csv` por documento de identidad. Devuelve usuarios activos sin vínculo laboral vigente, cuentas genéricas y cuentas sin último acceso registrado |
| **Excepción** | Un usuario activo cuyo cese figura en `empleados.csv`; una cuenta compartida; un perfil concedido por encima del solicitado |

> **El cruce siempre devuelve resultados.** Es la anomalía sembrada en las diez empresas. Un equipo que reporta cero excepciones no ejecutó el cruce. Hizo una inspección visual del CSV.

### Continuidad

| | |
|---|---|
| **Objetivo de control** | Verificar que los objetivos de tiempo de recuperación declarados en el BIA están respaldados por una capacidad de restauración probada |
| **Criterio** | COBIT 2019 **DSS04.03** *Develop and implement a business continuity response* · **DSS04.04** *Exercise, test and review the BCP* · NTP-ISO/IEC 27001:2022 **A.5.30** Preparación de las TIC para la continuidad · **A.8.13** Respaldo de la información |
| **Población** | Las actividades de `datos/bia.csv` y los respaldos ejecutados según `documentos/politica-de-respaldo.md` |
| **Reejecución** | **Solicitar una restauración real** de un respaldo elegido por el auditor, cronometrarla y comparar el tiempo obtenido con el RTO declarado en el BIA |
| **CAAT sobre el 100 %** | Sobre `bia.csv`, listar todas las actividades cuyo RTO declarado es menor que la periodicidad del respaldo que las cubre. Es una imposibilidad aritmética y sostiene el hallazgo sin necesidad de la prueba de restauración |
| **Excepción** | Una actividad crítica cuyo RTO es inferior al intervalo entre respaldos; la ausencia de cualquier prueba de restauración en el periodo |

> **Este es el CAAT más potente de la dinámica** y casi ningún equipo lo encuentra solo. Si a los 20 minutos el equipo de continuidad sigue sin él, se le da la pista. «Compara la columna de RTO con cada cuánto se respalda».

### Jurídica

| | |
|---|---|
| **Objetivo de control** | Verificar que el tratamiento de datos personales y el uso de licencias de software cuentan con base legal y título habilitante suficientes |
| **Criterio** | Ley 29733, **artículos 13 y 14** · D. S. 016-2024-JUS · Decreto Legislativo 822 sobre derecho de autor, **artículo 183** · NTP-ISO/IEC 27001:2022 **A.5.32** Derechos de propiedad intelectual · **A.5.34** Privacidad y protección de datos personales |
| **Población** | `documentos/registro-datos-y-licencias.md` completo |
| **Reejecución** | Tomar tres tratamientos declarados y **rehacer el rastreo de su base legal** hasta el documento que la sustenta. Consentimiento firmado, contrato o norma que lo habilite |
| **CAAT sobre el 100 %** | Contar puestos instalados contra licencias adquiridas para la totalidad del software del registro. La diferencia es la excepción, y es cuantificable en soles |
| **Excepción** | Un tratamiento sin base legal identificable; más puestos instalados que licencias adquiridas; un banco de datos personales no inscrito |

---

## Los cuatro errores que se repiten y cómo se corrigen en la mesa

| Lo que escriben | Por qué no sirve | Qué se les dice, literalmente |
|---|---|---|
| «Verificar que existan controles de acceso» | Es la actividad, no el objetivo. No dice qué debe ser cierto al final | «Termina la frase: verificar que **ningún** usuario… ¿qué?» |
| «Muestra: 10 usuarios» | Sin población y sin regla, el 10 es un número inventado | «¿Diez sobre cuántos, y por qué diez y no cuatro?» |
| «Entrevistar al jefe de sistemas para confirmar» como único sustento | La indagación está prohibida como sustento único por la consigna | «Eso es lo que él dice. ¿Qué vas a mirar tú?» |
| «Excepción: que el control no funcione» | Circular. No permite decidir en campo si lo observado es o no una excepción | «Dime una fila del CSV que, si la ves, ya es excepción» |

---

## Puntuación rápida

Se recorre en menos de dos minutos por equipo.

| Criterio | 5 si… | 1 si… |
|---|---|---|
| **Objetivo y criterio** | El código del criterio existe y corresponde al área. Se verifica contra la clave de arriba | Cita «ISO 27001» sin control, o cita un control de otra área |
| **Fuerza de la evidencia** | Aparecen el procedimiento de reejecución **y** el CAAT sobre el 100 % | Tres o más procedimientos empiezan con «entrevistar», «consultar» o «preguntar» |
| **Muestreo** | Hay población con número, muestra con número y una razón que las une | Falta cualquiera de los tres |
| **Reproducibilidad** | Cada procedimiento nombra el archivo o documento del que sale la evidencia | Los procedimientos son verbos sin objeto |

**Nota de cierre.** Un programa con cinco procedimientos correctos pero sin reejecución ni CAAT **no pasa de 12**, por más pulcro que se vea. La consigna lo declara obligatorio y la rúbrica lo mide en el segundo criterio.
