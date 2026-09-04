[Semana 01](README.md) · [Teoría](1-TEORIA.md) · **Dinámica de aula** · [Taller de laboratorio](3-TALLER.md)

# Dinámica de aula · El hallazgo de cinco líneas

**SI-084 · Auditoría de Sistemas** · Semana 01 · Actividad en aula, **dentro de los 100 min de la sesión de teoría** · calificación **cognitiva**

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](../GLOSARIO.md).

---

## Qué se busca con esta actividad

Que el equipo produzca su primer hallazgo de auditoría formal, con las cinco partes que lo hacen exigible. El objetivo no es detectar el problema técnico, que está a la vista, sino redactarlo de modo que la organización auditada no pueda discutirlo.

## Con qué material se trabaja

**Esta semana todos los equipos trabajan sobre la misma evidencia.** La asignación de organizaciones del banco de casos se define en esta sesión, así que la evidencia de hoy es común y está íntegra en la sección **Material de trabajo** de esta página. Desde la Semana 02 cada equipo trabaja con su propia organización.

## Lo que la teoría de hoy te da

Esta dinámica aplica piezas concretas de la sesión de teoría de hoy. Se usan tal cual, sin buscar nada más.

| De la teoría | Para qué se usa aquí |
|---|---|
| [El triángulo irreductible](1-TEORIA.md) | De ahí salen tres de los cinco bloques del producto. Sin criterio citado no hay hallazgo, hay opinión |
| [Qué es auditar](1-TEORIA.md) | Fija por qué la condición se redacta sin adjetivos y siempre contra un criterio externo |
| [El técnico y el auditor](1-TEORIA.md) | Es el estándar de redacción que la rúbrica exige. La columna derecha de esa tabla es el nivel esperado |

## Cómo se desarrolla · 35 minutos

| | Bloque | Quién | Minutos |
|---|---|---|---|
| **1** | **Leer la evidencia.** Se recorren los tres fragmentos entregados y se anota **solo lo que se ve**, en frases sin adjetivos. «Tres cuentas figuran en el grupo de administradores» es un hecho; «los accesos están mal gestionados» es una opinión y no entra. | Equipo | 7 |
| **2** | **Condición.** Se redacta qué se observó, con cantidades y con el sistema nombrado. La prueba de que está bien escrita es que el auditado pueda verificarla por su cuenta y llegue al mismo número. | Equipo | 7 |
| **3** | **Criterio.** Se ubica el control del Anexo A de la ISO/IEC 27001:2022 que se incumple y **se cita con su código**. Si el equipo no encuentra el control, revisa si lo que halló es realmente un incumplimiento o solo algo que le desagrada. | Equipo | 7 |
| **4** | **Causa y efecto.** La causa responde por qué ocurre, y no puede ser el síntoma otra vez. El efecto se cuantifica siempre que el dato lo permita, en soles, en horas de interrupción o en exposición legal. | Equipo | 7 |
| **5** | **Recomendación.** Acción específica, con responsable por cargo y plazo sugerido. «Mejorar la gestión de accesos» no es accionable; «revocar las tres cuentas compartidas y emitir una nominal por persona, Jefatura de TI, 15 días» sí lo es. | Equipo | 7 |

## Qué entregas

| | |
|---|---|
| **Archivo** | `SI084-S01-DINAMICA-Grupo<N>.pdf` |
| **Plantilla obligatoria** | [SI084-PLANTILLA-DINAMICA.docx](../PLANTILLAS/SI084-PLANTILLA-DINAMICA.docx) |
| **Formato** | PDF exportado desde la plantilla en Word, con la carátula de la UPT y los apellidos, nombres y códigos de todos los integrantes |
| **Qué va dentro** | Lo que el grupo resolvió en aula. Las tablas de la sección **Producto** van completas, con los textos redactados, y cada decisión va justificada |
| **Dónde se sube** | Aula virtual, tarea «Dinámica · Semana 01» |
| **Cuándo vence** | Hasta 24 h después de la sesión de teoría. La tabla se resuelve en aula; el PDF se formatea y se sube después |
| **Exposición** | En la ronda de cierre de **esta misma sesión**. El grupo **lee y explica su resultado** ante el aula, con el documento a la vista. No se usan diapositivas |

> No se califica un trabajo entregado en `.docx`, sin carátula, sin los códigos de los integrantes o con las tablas del producto vacías.

---

## Consigna

> **«El hallazgo de cinco líneas»**
> El equipo recibe un **extracto de evidencia real anonimizada**, con un fragmento de `/etc/passwd`, la matriz de usuarios de un ERP con tres cuentas compartidas y el correo del jefe de TI justificando la práctica. Debe convertir ese material en **un hallazgo de auditoría formal**.

## Material de trabajo

Trabaja sobre este extracto. Es evidencia anonimizada de un encargo real.

**Evidencia 1 — Fragmento de `/etc/passwd` del servidor `srv-erp-01`**

```
root:x:0:0:root:/root:/bin/bash
postgres:x:112:118:PostgreSQL administrator:/var/lib/postgresql:/bin/bash
erp_app:x:1001:1001:Usuario de aplicación ERP:/home/erp_app:/bin/bash
soporte:x:1002:1002:Soporte TI:/home/soporte:/bin/bash
practicante:x:1003:1002:Practicante:/home/practicante:/bin/bash
admin2:x:1004:1002:Administrador alterno:/home/admin2:/bin/bash
jperez:x:1005:1005:Juan Perez - Contabilidad:/home/jperez:/bin/bash
```

**Evidencia 2 — Extracto de la matriz de usuarios del ERP**

| Usuario del sistema | Personas que lo usan | Perfil asignado | Último cambio de contraseña |
|---|---|---|---|
| `soporte` | 4 (rotación de turnos de mesa de ayuda) | Administrador | Hace 19 meses |
| `practicante` | 2 (practicantes del semestre) | Administrador | Hace 19 meses |
| `admin2` | 3 (jefe de TI y dos analistas) | Administrador | Hace 19 meses |
| `jperez` | 1 | Contabilidad · consulta | Hace 2 meses |

**Evidencia 3 — Correo del jefe de TI, en respuesta a la consulta del equipo auditor**

> **Asunto.** RE. Consulta sobre cuentas del servidor ERP
>
> Estimados,
>
> Las cuentas `soporte`, `practicante` y `admin2` son cuentas de trabajo del área. Las usamos así desde que se instaló el servidor porque crear una cuenta por persona nos obligaría a pedir aprobación al jefe inmediato cada vez que entra alguien nuevo, y eso demora entre cinco y siete días. Con la carga que tenemos no es viable.
>
> La contraseña es la misma para las tres y la conoce el equipo. La cambiamos cuando se retira alguien, aunque reconozco que la última vez no lo hicimos porque fue un practicante y no tenía acceso a nada crítico.
>
> Cualquier movimiento raro lo vemos en los logs.
>
> Saludos,
> Jefe de Tecnologías de Información

**Evidencia 4 — Conteo de accesos de `/var/log/auth.log`, últimos 30 días**

```
$ grep "Accepted password" /var/log/auth.log | awk '{print $9}' | sort | uniq -c | sort -rn
    214 soporte
     87 admin2
     46 practicante
     31 jperez
```

**Dato de contexto.** El servidor `srv-erp-01` aloja la base de datos del ERP, que contiene la contabilidad, la planilla y el maestro de proveedores de la empresa.

## Producto

**Un solo producto**, que va en la sección 2 de la plantilla, «El producto», con exactamente cinco bloques rotulados:

| Bloque | Contenido exigido |
|---|---|
| **Condición** | Qué se observó, en términos verificables y sin adjetivos |
| **Criterio** | Norma, control o política incumplida, **citada con su código** (p. ej. ISO/IEC 27001:2022, control A.5.16 *Identity management*) |
| **Causa** | Por qué ocurre (proceso, recurso, conocimiento, incentivo) |
| **Efecto** | Consecuencia concreta y, si es posible, cuantificada |
| **Recomendación** | Acción específica, con responsable y plazo sugerido |

**Producto 2 (opcional) — ** la evidencia recortada y señalada con flechas.

> **Dónde va.** Este producto se presenta en la **sección 2 de la [plantilla de dinámica](../PLANTILLAS/SI084-PLANTILLA-DINAMICA.docx)**, «El producto». No se copia la consigna ni la teoría. Solo el resultado y lo que lo sostiene.

## Ejemplo resuelto

*El caso de este ejemplo es distinto del que le toca a tu grupo. Sirve para que veas el nivel de detalle que se espera, no para copiarlo.*

**Una fila bien resuelta.** El caso del ejemplo es una cuenta de aplicación en un sistema de gestión académica, distinto del servidor que te toca.

| Bloque | Contenido |
|---|---|
| **Condición** | El sistema de gestión académica se conecta a su base de datos con la cuenta `sa`, que es la cuenta de administrador del gestor. La cadena de conexión está en el archivo `web.config` del servidor de aplicaciones, en texto claro, y ese archivo es legible por los cuatro usuarios del grupo `IIS_Users`. La contraseña no ha cambiado desde la instalación, hace 4 años y 2 meses, según la fecha de modificación del archivo. |
| **Criterio** | ISO/IEC 27001:2022, Anexo A, control **A.8.2 Privileged access rights**, que exige restringir y controlar la asignación de derechos privilegiados, y **A.5.17 Authentication information**, sobre la gestión de la información de autenticación. Guía de aseguramiento del fabricante del gestor, que prohíbe el uso de la cuenta de administrador para la conexión de aplicaciones. |
| **Causa** | La aplicación se instaló con la configuración por defecto del proveedor, que usa la cuenta de administrador para simplificar la puesta en marcha. No existe procedimiento de aseguramiento posterior a la instalación, ni revisión de las cuentas de servicio. |
| **Efecto** | Cualquier persona con acceso al servidor de aplicaciones obtiene una credencial con control total sobre la base de datos académica, que contiene las notas y los datos personales de 3 400 estudiantes. Con esa cuenta se puede modificar una nota sin dejar rastro atribuible, porque todas las operaciones de la aplicación se registran bajo el mismo usuario. |
| **Recomendación** | Crear una cuenta de servicio con los permisos mínimos que la aplicación necesita —lectura y escritura sobre sus esquemas, sin permisos administrativos—, cambiar la cadena de conexión y cifrar la sección de configuración. Rotar la contraseña de la cuenta de administrador y restringir su uso. **Responsable:** Jefe de Sistemas. **Plazo:** 45 días. **Criterio de cierre:** la cadena de conexión no contiene una cuenta con rol de administrador, verificado en la revisión de configuración del trimestre siguiente. |

**La diferencia entre aprobar y no aprobar.**

| Elemento | Así no | Así sí |
|---|---|---|
| Condición | «El manejo de credenciales es deficiente y preocupante.» | «La aplicación se conecta con la cuenta `sa`. La contraseña está en texto claro en `web.config` y no cambia desde hace 4 años.» |
| Criterio | «Se incumplen las buenas prácticas de seguridad.» | «ISO/IEC 27001:2022, control A.8.2 *Privileged access rights*.» |
| Causa | «No se configuró bien la aplicación.» *(es el síntoma otra vez)* | «Se instaló con la configuración por defecto del proveedor y no existe procedimiento de aseguramiento posterior.» |
| Efecto | «Riesgo de acceso no autorizado.» | «Control total sobre la base de datos con las notas de 3 400 estudiantes. Una nota se modifica sin rastro atribuible.» |
| Recomendación | «Mejorar la gestión de credenciales.» | «Cuenta de servicio con permisos mínimos. Responsable: Jefe de Sistemas. Plazo: 45 días. Cierre: la cadena de conexión no usa cuenta administrativa.» |

## Reglas

- 35 min en aula, dentro de la sesión de teoría.
- La exposición es la ronda de cierre de esta misma sesión. El grupo **lee y explica su resultado**. No se usan diapositivas. **Expone un integrante elegido al azar**, así que todos deben dominar el producto.
- Prohibido el adjetivo sin dato. «El control es débil» no es una condición; «tres cuentas de administrador son compartidas por siete personas y no existe registro de quién ejecutó cada acción» sí lo es.

## Rúbrica cognitiva (20 puntos)

| Criterio | 5 (Excelente) | 3 (Suficiente) | 1 (Insuficiente) |
|---|---|---|---|
| **Criterio citado** | Norma y control identificados con código exacto y pertinente | Norma correcta sin código específico | Sin norma o norma inaplicable |
| **Condición verificable** | Redactada solo con hechos observables y cuantificados | Hechos correctos pero con adjetivos valorativos | Opinión sin sustento en la evidencia |
| **Causa y efecto** | Causa raíz distinta del síntoma; efecto con impacto de negocio | Causa plausible; efecto genérico | Causa = condición repetida |
| **Recomendación** | Específica, accionable, con responsable y plazo | Específica pero sin responsable ni plazo | «Mejorar la seguridad» |

---

---

[Semana 01](README.md) · [Teoría](1-TEORIA.md) · **Dinámica de aula** · [Taller de laboratorio](3-TALLER.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
