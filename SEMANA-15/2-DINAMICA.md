[Semana 15](README.md) · [Teoría](1-TEORIA.md) · **Dinámica de aula** · [Taller de laboratorio](3-TALLER.md)

# Semana 15

## El BIA de una actividad

**SI-084 - Auditoría de Sistemas** - Actividad en aula, **dentro de la sesión de teoría** · calificación **cognitiva**

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](../GLOSARIO.md).

---

## Qué entregas

| | |
|---|---|
| **Archivo** | `SI084-S15-DINAMICA-Grupo<N>.pdf` |
| **Plantilla obligatoria** | [SI084-PLANTILLA-DINAMICA.docx](../PLANTILLAS/SI084-PLANTILLA-DINAMICA.docx) |
| **Formato** | PDF exportado desde la plantilla en Word, con la carátula de la UPT y los apellidos, nombres y códigos de todos los integrantes |
| **Qué va dentro** | Lo que el grupo resolvió en aula. Las tablas de la sección **Producto** van completas, con los textos redactados, y cada decisión va justificada |
| **Dónde se sube** | Aula virtual, tarea «Dinámica · Semana 15» |
| **Cuándo vence** | Según lo programado en el aula virtual. La tabla se resuelve en aula; el PDF se formatea y se sube después |
| **Exposición** | En la ronda de cierre de **esta misma sesión**. El grupo **lee y explica su resultado** ante el aula, con el documento a la vista. No se usan diapositivas |

> No se califica un trabajo entregado en `.docx`, sin carátula, sin los códigos de los integrantes o con las tablas del producto vacías.

---

## Consigna

> **«El BIA de una actividad»**
> Cada equipo elige **una actividad de negocio real de su empresa auditada** (facturar, despachar, cobrar, pagar la planilla, atender al cliente) y **construye su BIA completo** siguiendo los ocho pasos, terminando con la estrategia de continuidad que recomendaría y su justificación económica.

| | |
|---|---|
| **Su papel** | **Analista de continuidad** que debe justificar la inversión ante finanzas |
| **Misión** | Construir el BIA completo de la actividad y recomendar la estrategia con su justificación económica |
| **Restricción** | **El objetivo de tiempo de recuperación se sustenta en el costo de la interrupción**, no en lo que sería deseable tener |

## Producto

**Producto 1 — Impacto en el tiempo.** Tabla del impacto de la interrupción de la actividad:

| Horizonte | Impacto financiero | Impacto operativo | Impacto legal / regulatorio | Impacto reputacional |
|---|---|---|---|---|
| 4 horas | | | | |
| 24 horas | | | | |
| 3 días | | | | |
| 1 semana | | | | |

Con la conclusión **MTPD = ___ · RTO propuesto = ___ · RPO = ___ · MBCO = ___**, cada uno justificado.

**Producto 2 — Recursos y estrategia.**

| Recurso requerido | Detalle | Estado actual | Brecha |
|---|---|---|---|
| Personas (roles mínimos) | | | |
| Sistemas | | | |
| Datos y su RPO | | | |
| Instalaciones | | | |
| Proveedores críticos | | | |

Más la **estrategia recomendada**, su costo estimado y la comparación con el impacto que evita.

> **Dónde va.** Este producto se presenta en la **sección 2 de la [plantilla de dinámica](../PLANTILLAS/SI084-PLANTILLA-DINAMICA.docx)**, «El producto». No se copia la consigna ni la teoría. Solo el resultado y lo que lo sostiene.

## Ejemplo resuelto

*El caso de este ejemplo es distinto del que le toca a tu grupo. Sirve para que veas el nivel de detalle que se espera, no para copiarlo.*

**Un BIA (*Business Impact Analysis*, análisis de impacto al negocio) bien resuelto.** La actividad del ejemplo es la emisión de comprobantes electrónicos.

*Impacto en el tiempo*

| Horizonte | Impacto financiero | Impacto operativo | Impacto legal o regulatorio | Impacto reputacional |
|---|---|---|---|---|
| 4 horas | S/ 18 000 en ventas no facturadas, recuperables | Se emite en contingencia con talonario físico. 3 personas dedicadas a la digitación posterior | **Ninguno.** La SUNAT admite la contingencia | Bajo. Demora en caja perceptible |
| 24 horas | S/ 105 000 | El talonario de contingencia alcanza para 400 comprobantes; se agota a las 14 horas. A partir de ahí no se puede despachar | Riesgo de incumplimiento del plazo de envío de comprobantes | Medio. Clientes mayoristas reclaman |
| 3 días | S/ 315 000 | Operación detenida. Personal de almacén sin actividad | Incumplimiento formal del plazo de remisión a la SUNAT, con multa | Alto. Dos clientes mayoristas consultan a la competencia |
| 1 semana | S/ 735 000 | Pérdida de la campaña del mes | Multa y posible fiscalización | Alto e irreversible con los mayoristas |

**MTPD = 3 días** · **RTO propuesto = 8 horas** · **RPO = 15 minutos** · **MBCO = 60 % del volumen diario**

*Justificación de cada cifra.* El MTPD es de 3 días porque a partir de ahí el daño reputacional con los mayoristas deja de ser recuperable y aparece la multa. El RTO se fija en 8 horas, por debajo de las 14 en que se agota el talonario de contingencia, para no llegar nunca a la detención del despacho. El RPO de 15 minutos corresponde al intervalo máximo de pérdida de comprobantes emitidos que se puede reconstruir a mano con el reporte de caja. El MBCO del 60 % es el volumen que permite atender a los mayoristas, que representan el 60 % de la facturación.

*Recursos y estrategia*

| Recurso requerido | Detalle | Estado actual | Brecha |
|---|---|---|---|
| Personas | 1 operador de caja y 1 responsable de facturación con clave de contingencia | Existe, pero la clave la conoce solo una persona | Sin respaldo humano |
| Sistemas | Servidor de facturación y conexión con el proveedor de servicios electrónicos | Servidor único, sin réplica | No hay alternativa técnica |
| Datos y su RPO | Comprobantes emitidos | Respaldo diario a las 23:00 | RPO real de 24 horas frente a los 15 minutos requeridos |
| Instalaciones | Local principal | Único | Sin sede alterna |
| Proveedores críticos | Proveedor de servicios electrónicos | Contrato sin nivel de servicio comprometido | Sin exigencia contractual de disponibilidad |

**Estrategia recomendada.** Réplica del servidor de facturación en el proveedor de nube ya contratado, con conmutación manual, más respaldo transaccional cada 15 minutos y una segunda persona con clave de contingencia. **Costo estimado.** S/ 34 000 de inversión y S/ 9 600 anuales. **Comparación.** El impacto de una sola interrupción de 24 horas es de S/ 105 000, tres veces la inversión.

**La diferencia entre aprobar y no aprobar.**

| Así no | Así sí |
|---|---|
| «RTO: 4 horas, porque es lo razonable.» | «RTO 8 horas, por debajo de las 14 en que se agota el talonario de contingencia.» |
| «Impacto: alto.» | «S/ 105 000 a las 24 horas, y a las 14 horas se detiene el despacho.» |
| «Se recomienda mejorar la continuidad.» | «Réplica en nube con conmutación manual. S/ 34 000 de inversión frente a S/ 105 000 de impacto por una sola interrupción de 24 horas.» |

## Reglas

- **Se parte de la actividad de negocio, nunca del sistema.** Un BIA que empieza nombrando servidores no se califica.
- El MTPD debe justificarse con el momento en que el impacto se vuelve inaceptable, no con una cifra redonda.
- La estrategia recomendada debe compararse económicamente con el impacto que evita.
- La exposición es la ronda de cierre de esta misma sesión. El grupo **lee y explica su resultado**. No se usan diapositivas.

## Rúbrica cognitiva (20 puntos)

| Criterio | 5 | 3 | 1 |
|---|---|---|---|
| **Enfoque de actividad** | Parte de la actividad de negocio y llega a los sistemas al final | Mezcla actividad y sistemas | Parte de los sistemas |
| **Impacto en el tiempo** | Las cuatro dimensiones en los cuatro horizontes, con cifras | Impactos descritos sin cuantificar | Impacto genérico |
| **Coherencia de los tiempos** | RTO < MTPD, RPO justificado, MBCO definido | Tiempos correctos sin justificación | RTO ≥ MTPD o tiempos ausentes |
| **Justificación económica** | Compara el costo de la estrategia con el impacto evitado | Menciona el costo sin comparar | Recomienda la estrategia más cara sin justificar |

---

---

[Semana 15](README.md) · [Teoría](1-TEORIA.md) · **Dinámica de aula** · [Taller de laboratorio](3-TALLER.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
