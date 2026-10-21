[Semana 13](README.md) · [Teoría](1-TEORIA.md) · **Dinámica de aula** · [Taller de laboratorio](3-TALLER.md)

# Semana 13

## Reescribir el informe

**SI-084 - Auditoría de Sistemas** - Actividad en aula, **dentro de la sesión de teoría** · calificación **cognitiva**

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](../GLOSARIO.md).

---

## Qué entregas

| | |
|---|---|
| **Archivo** | `SI084-S13-DINAMICA-Grupo<N>.pdf` |
| **Plantilla obligatoria** | [SI084-PLANTILLA-DINAMICA.docx](../PLANTILLAS/SI084-PLANTILLA-DINAMICA.docx) |
| **Formato** | PDF exportado desde la plantilla en Word, con la carátula de la UPT y los apellidos, nombres y códigos de todos los integrantes |
| **Qué va dentro** | Lo que el grupo resolvió en aula. Las tablas de la sección **Producto** van completas, con los textos redactados, y cada decisión va justificada |
| **Dónde se sube** | Aula virtual, tarea «Dinámica · Semana 13» |
| **Cuándo vence** | Según lo programado en el aula virtual. La tabla se resuelve en aula; el PDF se formatea y se sube después |
| **Exposición** | En la ronda de cierre de **esta misma sesión**. El grupo **lee y explica su resultado** ante el aula, con el documento a la vista. No se usan diapositivas |

> No se califica un trabajo entregado en `.docx`, sin carátula, sin los códigos de los integrantes o con las tablas del producto vacías.

---

## Consigna

> **«Reescribir el informe»**
> Cada equipo recibe **cuatro hallazgos mal redactados**, tomados de informes reales anonimizados, con adjetivos en la condición, criterio genérico, causa igual al síntoma, efecto sin negocio y recomendación no accionable. Debe **reescribirlos completos** y **clasificar su severidad con justificación**.

| | |
|---|---|
| **Su papel** | **Revisor de calidad** que devuelve el informe antes de que salga de la oficina |
| **Misión** | Reescribir los cuatro hallazgos completos y clasificar su severidad con el criterio de asignación |
| **Restricción** | **Ningún adjetivo en la condición y ninguna causa que repita el síntoma.** «Falta de control» no es una causa |

## Producto

**Producto 1 — Antes y después.** Para dos de los cuatro hallazgos, la comparación lado a lado del texto original y del reescrito, señalando el defecto corregido en cada elemento.

**Producto 2 — Tabla de severidad.** Los cuatro hallazgos con severidad asignada, criterio de la asignación, plazo recomendado y responsable propuesto (por cargo, nunca por nombre).

> **Dónde va.** Este producto se presenta en la **sección 2 de la [plantilla de dinámica](../PLANTILLAS/SI084-PLANTILLA-DINAMICA.docx)**, «El producto». No se copia la consigna ni la teoría. Solo el resultado y lo que lo sostiene.

## Ejemplo resuelto

*El caso de este ejemplo es distinto del que le toca a tu grupo. Sirve para que veas el nivel de detalle que se espera, no para copiarlo.*

**Un hallazgo reescrito.** Es un quinto hallazgo, distinto de los cuatro que te tocan.

| Elemento | Original | Reescrito |
|---|---|---|
| **Condición** | «Se observó que el control de accesos a la sala de servidores es deficiente y no cumple con los estándares mínimos esperados.» | «La puerta de la sala de servidores se abre con una llave física de la que existen cuatro copias. No hay registro de a quién se entregó cada una. Durante la visita del 14 de la ejecución, la puerta permaneció abierta y sin vigilancia durante 40 minutos. El libro de visitas registra 3 ingresos en seis meses, frente a los 19 accesos de mantenimiento que constan en los tickets del período.» |
| **Criterio** | «Buenas prácticas de seguridad física.» | «ISO/IEC 27001:2022, Anexo A, **A.7.2 Physical entry** y **A.7.4 Physical security monitoring**. Política interna de seguridad física, numeral 6.1, que exige registro nominal de todo ingreso a áreas restringidas.» |
| **Causa** | «No hay un adecuado control de accesos.» *(es la condición otra vez)* | «El control de acceso se diseñó cuando la sala alojaba dos equipos y la operaba una sola persona. Al crecer a doce equipos y tres proveedores externos, no se revisó el mecanismo. No existe responsable asignado a la custodia de las llaves.» |
| **Efecto** | «Riesgo de acceso no autorizado.» | «Cualquier persona con una de las cuatro llaves puede acceder físicamente a los servidores que alojan la base de datos de clientes y el sistema de facturación, sin dejar rastro. Un acceso físico permite extraer discos o reiniciar en modo de mantenimiento, lo que anula los controles lógicos. La organización no podría determinar quién ingresó ante un incidente.» |
| **Recomendación** | «Mejorar el control de accesos a la sala de servidores.» | «Sustituir la cerradura por un control de acceso con credencial nominal y registro automático, o, si la inversión no es viable en el período, asignar la custodia de una única llave al Jefe de Infraestructura, con registro firmado de entrega y devolución por cada uso. **Responsable:** Jefe de Infraestructura. **Plazo:** 60 días. **Criterio de cierre:** el 100 % de los accesos del mes tiene registro nominal contrastable con los tickets de mantenimiento.» |

*Tabla de severidad*

| Hallazgo | Severidad | Criterio de la asignación | Plazo | Responsable |
|---|---|---|---|---|
| Acceso físico sin registro nominal a la sala de servidores | **Alta** | Afecta un activo crítico, el control es inexistente y no hay control compensatorio. No es «crítica» porque la sala está dentro de un perímetro con vigilancia y el acceso exige presencia en el local. | 60 días | Jefe de Infraestructura |

**La regla que decide la nota.** La causa nunca puede ser la condición reformulada. Si la condición es «no hay registro de accesos», la causa no es «falta registro de accesos». Es **por qué** falta.

## Reglas

- **Cero adjetivos valorativos** en las condiciones reescritas.
- Cada criterio debe llevar código de norma, control o artículo.
- Cada efecto debe estar cuantificado o, si no es posible, acotado en su magnitud.
- Una sola recomendación por hallazgo.
- La exposición es la ronda de cierre de esta misma sesión. El grupo **lee y explica su resultado**. No se usan diapositivas.

## Rúbrica cognitiva (20 puntos)

| Criterio | 5 | 3 | 1 |
|---|---|---|---|
| **Condición** | Solo hechos verificables y cuantificados en los cuatro | En dos o tres | Conserva juicios de valor |
| **Causa raíz** | Distinta del síntoma en los cuatro, con lógica de cinco porqués visible | En dos o tres | Causa = condición reformulada |
| **Efecto de negocio** | Cuantificado, con consecuencia legal o económica identificada | Consecuencia clara sin cuantificar | «Riesgo de seguridad» |
| **Severidad** | Justificada por riesgo, coherente entre los cuatro | Asignada con criterio parcial | Asignada por esfuerzo de corrección |

## Anexo · Material de trabajo

Trabaja sobre estos cuatro hallazgos. Están tomados de informes reales, anonimizados, y conservan los defectos de redacción originales.

**Hallazgo 1**

> **Condición.** Se observó que la gestión de usuarios presenta serias deficiencias y no se ajusta a lo esperado para una organización de este tamaño.
> **Criterio.** Buenas prácticas de seguridad de la información.
> **Causa.** No existe una adecuada gestión de usuarios.
> **Efecto.** Riesgo de accesos no autorizados.
> **Recomendación.** Se recomienda mejorar la gestión de usuarios.

*Datos que el papel de trabajo respalda:* de 118 cuentas activas en el ERP, 23 corresponden a personas que ya no trabajan en la empresa; la más antigua tiene 19 meses desde el cese. No existe procedimiento de baja vinculado al cese en Recursos Humanos.

**Hallazgo 2**

> **Condición.** El registro de cambios está incompleto.
> **Criterio.** COBIT.
> **Causa.** Falta de cultura de documentación en el equipo de desarrollo.
> **Efecto.** Se podrían generar errores en producción.
> **Recomendación.** Capacitar al personal en gestión de cambios y concientizar sobre la importancia de documentar.

*Datos que el papel de trabajo respalda:* de 112 despliegues a producción del último trimestre, 41 no tienen registro de aprobación previa. En 9 de esos 41, el mismo desarrollador escribió el código y ejecutó el despliegue. El sistema de tickets permite cerrar un cambio sin adjuntar la aprobación porque el campo es opcional.

**Hallazgo 3**

> **Condición.** La empresa no cuenta con un plan de continuidad del negocio debidamente formalizado y probado, lo que evidencia una preocupante falta de previsión ante escenarios de desastre.
> **Criterio.** ISO 22301.
> **Causa.** No se ha elaborado el plan.
> **Efecto.** La empresa podría verse afectada ante un desastre.
> **Recomendación.** Elaborar e implementar un plan de continuidad del negocio.

*Datos que el papel de trabajo respalda:* no existe análisis de impacto en el negocio. El respaldo del sistema de facturación se ejecuta a diario, pero la última prueba de restauración documentada tiene 14 meses. El sistema de facturación soporta el 100 % de los ingresos, que ascienden a S/ 2,1 millones mensuales. El servidor es único, sin réplica.

**Hallazgo 4**

> **Condición.** Se detectaron vulnerabilidades críticas en los servidores.
> **Criterio.** ISO/IEC 27001.
> **Causa.** Falta de gestión de parches.
> **Efecto.** Los servidores podrían ser comprometidos.
> **Recomendación.** Aplicar los parches de seguridad correspondientes a la brevedad posible.

*Datos que el papel de trabajo respalda:* el escaneo autenticado identificó 7 vulnerabilidades con CVSS igual o superior a 9,0. Seis de ellas están en el servidor del portal corporativo, expuesto a internet y sin datos sensibles. La séptima está en el gestor de base de datos del ERP, que no está expuesto a internet pero contiene la información contable y la planilla. No existe proceso de aplicación de parches con periodicidad definida.

**La escala de severidad de este curso**

| Severidad | Criterio |
|---|---|
| Crítica | Afecta un activo crítico, el control es inexistente y no hay control compensatorio |
| Alta | Afecta un activo crítico con control compensatorio parcial, o un activo relevante sin control |
| Media | Afecta un activo relevante con control compensatorio, o un activo de apoyo sin control |
| Baja | Deficiencia formal sin efecto operativo demostrable |

---

---

[Semana 13](README.md) · [Teoría](1-TEORIA.md) · **Dinámica de aula** · [Taller de laboratorio](3-TALLER.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
