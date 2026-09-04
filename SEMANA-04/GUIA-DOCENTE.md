# Guía del docente · Semana 04 · «El control que no se puede creer»

**SI-084 · Auditoría de Sistemas** · Uso interno. No se publica. Está excluida en el `.gitignore` del curso.

---

## Para qué sirve la dinámica

La teoría dice, con esas palabras, cuál es **el concepto más importante de la semana**:

> *Los controles de aplicación solo son confiables si los ITGC son efectivos.*

La narrativa de compras y pagos está construida para que eso se vea. El proceso tiene un control de aplicación excelente —el cruce automático de tres vías— y un entorno de TI que lo vuelve inauditable. Ese contraste es toda la clase.

**Todos los equipos trabajan sobre la misma narrativa.** No hay fichas distintas, así que la ronda final compara respuestas sobre el mismo caso y las discrepancias se resuelven en el acto.

**Qué se quitó de esta dinámica.** La versión anterior pedía diseñar el muestreo —tamaño de muestra, desviación tolerable, nivel de confianza, tablas de ITAF— y **nada de eso está en la teoría de la semana**. Se retiró. El muestreo se ve más adelante; hoy se clasifica y se concluye.

---

## Paso 0 · Los 7 minutos de pizarra · guion

Use el ejemplo, que es de **ventas y cobranza**, para que no le resuelva la narrativa a nadie.

**Escriba solo esto.**

```
RIESGO 1  descuentos por encima de la política
RIESGO 2  el cobrador recibe efectivo en ruta
```

**Lo que dice, en este orden.**

1. *«"Riesgo de fraude" no es un riesgo. Es una palabra. Un riesgo se redacta con dos cosas: qué puede salir mal y con qué consecuencia.»* Escriba al lado del primero. **El vendedor otorga descuentos sobre la política y se pierde margen, o se acuerda con el cliente.**
2. *«¿Qué control existe?»* → el bloqueo del 10 % en el ERP. *«¿Cuándo actúa? Antes. Es preventivo. ¿A qué objetivo sirve? Exactos.»*
3. Vaya al segundo. *«¿Qué control existe para el efectivo en ruta?»* Espere. *«Ninguno. Y "ninguno" es una respuesta de auditoría, no una rendición. Es el hallazgo.»*
4. Ahora el golpe. *«Vuelvo al primero. El bloqueo del 10 % está en el código del ERP. Si cualquiera puede cambiar el código en producción sin dejar rastro, ¿puedo yo concluir que ese control funcionó todo el año?»* Espere. *«No. Y eso no es culpa del control: es culpa del entorno. Por eso el auditor mira primero los ITGC.»*
5. **Cierre del paso 0.** *«Un control puede estar bien diseñado, haber operado siempre, y aun así no poder concluirse efectivo. Ahora búsquenlo en su narrativa.»*

---

## Solucionario de la narrativa de compras y pagos

### Los riesgos que la narrativa contiene

| # | Paso | Riesgo redactado | Control que existe | Tipo | Aserción |
|---|---|---|---|---|---|
| **A** | Aprobación de la orden de compra | El analista crea la orden y la aprueba él mismo por debajo de S/ 20 000, y compra a un proveedor con el que tiene acuerdo | Segregación en el ERP, **solo sobre S/ 20 000** | Preventivo, aplicación | **Autorizados** |
| **B** | Cambio de cuenta bancaria del proveedor | Alguien suplanta al proveedor por correo, Tesorería cambia la cuenta y el siguiente pago va a la cuenta del atacante | **Ninguno.** Tesorería actualiza directo con el correo como única fuente | — | **Válidos** |
| **C** | Propuesta de pago en hoja de cálculo | Se agregan a la hoja pagos que nunca pasaron por el ERP ni por el cruce de tres vías | Aprobación de la propuesta por correo del Jefe de Administración | Compensatorio, débil | **Válidos** y **completos** |
| **D** | Recepción de mercadería | El almacenero registra sistemáticamente hasta un 5 % de más y la diferencia no se investiga | Tolerancia del 5 % con aprobación por encima | Preventivo, aplicación | **Exactos** |
| **E** | Registro de la factura | Se paga una factura que no corresponde a una compra recibida | Cruce automático de tres vías | Preventivo, automático, aplicación | **Válidos** y **exactos** |
| **F** | Ejecución del pago en banca | Tesorería paga sola | Doble clave: la suya y el token físico que guarda el Jefe de Administración | Preventivo, ITGC de accesos | **Autorizados** |

**Los tres que debe traer un buen trabajo son A, B y C.** El **B** es el riesgo sin control y es el que se pide expresamente. El **D**, **E** y **F** son correctos pero de menor severidad.

### Los datos del período que miden cada hallazgo

| Hallazgo | El dato que lo dimensiona |
|---|---|
| **A** autoaprobación | **1 108 de 1 240 órdenes** están por debajo de S/ 20 000. El control cubre el 11 % de las órdenes |
| **B** cuenta bancaria | **12 cambios** de cuenta en el período, ninguno con verificación fuera del canal del correo |
| **C** pagos fuera del ERP | **519 de 2 310 pagos**, el 22 %, no provienen del ERP y no pasaron por el cruce de tres vías |
| **E** cruce de tres vías | 63 facturas observadas de 1 795. El control **sí actúa**; el problema es otro |

### Las dos conclusiones

> **La dependencia.** El **cruce automático de tres vías** (E) es el mejor control del proceso y **no se puede concluir efectivo**, porque el ITGC de **gestión de cambios** está roto. El proveedor externo aplica cambios en producción sin aprobación registrada y sin ambiente de pruebas. La regla pudo desactivarse y volver a activarse sin dejar rastro. **El auditor no puede apoyarse en él, por bien diseñado que esté.**

> **Diseño o eficacia.** Son dos controles distintos, y esa es la gracia:
> - Falla el **diseño**. La segregación de crear y aprobar la orden (A). Aunque operara sin excepción, deja fuera el 89 % de las órdenes. Un control que no mitigaría el riesgo ni operando siempre falla el diseño, y por eso **no se prueba su eficacia**.
> - Falla la **eficacia operativa** — la baja de usuarios. El procedimiento existe y es adecuado, pero hubo **7 ceses y 3 usuarios seguían activos** al cierre. Diseño correcto, operación incompleta.

### Lo que le van a discutir

| Lo que dirán | Cómo se resuelve |
|---|---|
| «El cruce de tres vías está bien, no es hallazgo.» | Correcto: el control está bien diseñado. El hallazgo no es sobre el control, es sobre el **entorno** que impide concluir sobre él. Es la distinción central de la semana |
| «La autoaprobación falla la eficacia operativa.» | No. El control **hace lo que dice que hace**: bloquea sobre S/ 20 000. Lo que está mal es el umbral, y el umbral es diseño |
| «El riesgo del cambio de cuenta es muy rebuscado.» | Es el fraude BEC, y la teoría de la semana le dedica un ejemplo trabajado completo. Remítalos a él |
| «La aprobación por correo del Jefe sirve como control.» | Pregunte qué aprobó exactamente. La hoja de cálculo cambia después de exportada y el correo no deja constancia de qué versión se aprobó. Es compensatorio y débil, no preventivo |
| «El respaldo diario es un buen control.» | Correctivo, y **no se puede concluir efectivo**: la restauración se probó una vez en 2023. Un respaldo que nunca se restauró es una copia, no un control |

---

## Paso 4 · La ronda y el cierre · 6 minutos

Pida a **tres equipos solo el riesgo sin control**. Casi todos dirán el **B**. Si alguno dice el **C**, mejor todavía. Haga que el aula decida si la aprobación por correo cuenta como control.

Repregunta única. **«¿Con qué dato del período lo dimensiona?»**

**Cierre, dos minutos.**

> *«Fíjense en el orden en que trabajamos. Primero los controles del proceso, y al final el entorno. En una auditoría real es al revés: se miran primero los ITGC, porque si están rotos, todo lo que concluyan sobre los controles de aplicación no se sostiene. Hoy lo hicimos al revés a propósito, para que sintieran lo que se pierde. La próxima vez empiecen por arriba.»*

---

## Si el tiempo se acorta

| Situación | Qué se recorta |
|---|---|
| La teoría se pasó | Pida dos riesgos en vez de tres, y que uno sea el que no tiene control |
| Los equipos se atascan en la clasificación | Escriba en la pizarra los seis objetivos de aserción y déjelos ahí. Es lo que más cuesta |
| Sobra tiempo | Pregunte cuál de los seis controles **no depende** de ningún ITGC. Respuesta, el F: el token físico está fuera del sistema, y por eso es el más confiable del proceso |

---

**Docente** · Dr. Oscar Juan Jimenez Flores · Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna
