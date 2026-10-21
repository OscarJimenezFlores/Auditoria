[Semana 11](README.md) · [Teoría](1-TEORIA.md) · **Dinámica de aula** · [Taller de laboratorio](3-TALLER.md)

# Semana 11

## El flujo de datos personales

**SI-084 - Auditoría de Sistemas** - Actividad en aula, **dentro de la sesión de teoría** · calificación **cognitiva**

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](../GLOSARIO.md).

---

## Qué entregas

| | |
|---|---|
| **Archivo** | `SI084-S11-DINAMICA-Grupo<N>.pdf` |
| **Plantilla obligatoria** | [SI084-PLANTILLA-DINAMICA.docx](../PLANTILLAS/SI084-PLANTILLA-DINAMICA.docx) |
| **Formato** | PDF exportado desde la plantilla en Word, con la carátula de la UPT y los apellidos, nombres y códigos de todos los integrantes |
| **Qué va dentro** | Lo que el grupo resolvió en aula. Las tablas de la sección **Producto** van completas, con los textos redactados, y cada decisión va justificada |
| **Dónde se sube** | Aula virtual, tarea «Dinámica · Semana 11» |
| **Cuándo vence** | Según lo programado en el aula virtual. La tabla se resuelve en aula; el PDF se formatea y se sube después |
| **Exposición** | En la ronda de cierre de **esta misma sesión**. El grupo **lee y explica su resultado** ante el aula, con el documento a la vista. No se usan diapositivas |

> No se califica un trabajo entregado en `.docx`, sin carátula, sin los códigos de los integrantes o con las tablas del producto vacías.

---

## Consigna

> **«El flujo de datos personales»**
> Cada equipo debe **rastrear el recorrido completo de un dato personal** en la organización que se le asignó del banco de casos — desde que se capta hasta que se elimina, identificando en cada punto quién lo trata, con qué base legal, dónde reside físicamente y qué medida de seguridad lo protege. Luego debe **identificar los tres puntos de mayor exposición legal**.

| | |
|---|---|
| **Su papel** | **Auditor de cumplimiento** ante una organización que no tiene responsable de datos designado |
| **Misión** | Recorrer el dato desde que entra hasta que se elimina y ordenar los tres puntos de mayor exposición legal |
| **Restricción** | **La etapa de eliminación se responde igual**, aunque la respuesta sea que no existe. Ese vacío es el hallazgo |

Que el equipo siga un dato personal de principio a fin dentro de su organización y descubra que la exposición legal casi nunca está donde el dato se capta, sino en la conservación indefinida y en la compartición con terceros que nadie documentó.

## Lo que la teoría de hoy te da

Esta dinámica aplica piezas concretas de la sesión de teoría de hoy. Se usan tal cual, sin buscar nada más.

| De la teoría | Para qué se usa aquí |
|---|---|
| [Protección de datos personales](1-TEORIA.md) | Da la Ley 29733 y el D. S. 016-2024-JUS con sus obligaciones. Es la columna del producto donde se cita el artículo |
| [Auditoría de cumplimiento legal del entorno informático](1-TEORIA.md) | Fija cómo se audita el cumplimiento normativo, que es distinto de auditar un control técnico |
| [Auditoría de la función informática](1-TEORIA.md) | Sitúa quién debía responder por el tratamiento dentro de la estructura de la organización |

## Producto

**Producto 1 — El recorrido del dato.** Diagrama de flujo del dato personal seleccionado (por ejemplo, el DNI y el correo de un cliente), con estas anotaciones en cada etapa:

```
CAPTACIÓN → ALMACENAMIENTO → USO → COMPARTICIÓN → CONSERVACIÓN → ELIMINACIÓN
    │             │            │          │              │             │
  ¿base       ¿dónde      ¿para qué?  ¿con quién?    ¿por cuánto   ¿cómo se
  legal?      reside?     ¿finalidad   ¿contrato?     tiempo?      destruye?
              ¿país?      compatible?                ¿justificado?
```

**Producto 2 — Tabla de exposición legal.**

| # | Punto del flujo | Riesgo legal concreto | Artículo de la Ley 29733 o del D. S. 016-2024-JUS | Autoridad | Acción correctiva |
|---|---|---|---|---|---|

> **Dónde va.** Este producto se presenta en la **sección 2 de la [plantilla de dinámica](../PLANTILLAS/SI084-PLANTILLA-DINAMICA.docx)**, «El producto». No se copia la consigna ni la teoría. Solo el resultado y lo que lo sostiene.

## Ejemplo resuelto

*El caso de este ejemplo es distinto del que le toca a tu grupo. Sirve para que veas el nivel de detalle que se espera, no para copiarlo.*

**Un tramo del flujo y una fila de exposición legal.** El dato del ejemplo es el número de teléfono de un cliente.

*El recorrido, etapa de compartición*

| Pregunta | Respuesta |
|---|---|
| ¿Base legal? | Ejecución del contrato para el envío de la guía de despacho. Para el envío de promociones **no** hay base contractual. Exige consentimiento específico, que hoy no se recoge por separado. |
| ¿Dónde reside? | Base de datos del ERP, en un servidor del proveedor de nube, con centro de datos en Estados Unidos. |
| ¿Con quién se comparte? | Con el operador logístico, mediante un archivo diario en texto plano por correo, y con una plataforma de mensajería para las campañas comerciales. |
| ¿Hay contrato? | Con el operador logístico existe contrato de servicios, pero **sin cláusula de encargo de tratamiento**. Con la plataforma de mensajería solo hay aceptación de términos en línea. |
| ¿Por cuánto tiempo? | Indefinido. No existe política de conservación. |
| ¿Cómo se destruye? | No se destruye. |

*Tabla de exposición legal*

| # | Punto del flujo | Riesgo legal concreto | Artículo aplicable | Autoridad | Acción correctiva |
|---|---|---|---|---|---|
| 1 | Compartición con el operador logístico | Se transfieren datos personales a un tercero sin contrato de encargo de tratamiento, y por un canal sin cifrado. Ante una fuga, la responsabilidad recae íntegra en la organización. | Ley 29733, artículo 2 numeral 6 y artículo 28. Decreto Supremo 016-2024-JUS, sobre obligaciones del encargado de tratamiento. | Autoridad Nacional de Protección de Datos Personales | Suscribir adenda de encargo de tratamiento con obligaciones de seguridad y de eliminación, y sustituir el envío por correo por una transferencia cifrada |
| 2 | Flujo transfronterizo hacia el centro de datos | El almacenamiento fuera del país constituye flujo transfronterizo y exige garantías y registro. | Ley 29733, artículo 15 | Autoridad Nacional de Protección de Datos Personales | Documentar el flujo, verificar las garantías del proveedor e inscribir el banco de datos |
| 3 | Conservación indefinida | Se conservan datos más allá de la finalidad que justificó su recogida. | Ley 29733, artículo 8 (principio de calidad) | Autoridad Nacional de Protección de Datos Personales | Definir plazo de conservación por finalidad y procedimiento de eliminación verificable |

**La diferencia entre aprobar y no aprobar.**

| Así no | Así sí |
|---|---|
| «Se comparten datos con terceros.» | «Archivo diario en texto plano por correo al operador logístico, sin cláusula de encargo de tratamiento.» |
| «Incumple la Ley de Protección de Datos.» | «Ley 29733, artículo 15: el almacenamiento fuera del país es flujo transfronterizo y exige garantías y registro.» |
| «Se recomienda mejorar la seguridad.» | «Adenda de encargo de tratamiento y sustitución del correo por transferencia cifrada.» |

## Reglas

- Obligatorio identificar **al menos un flujo transfronterizo** (casi toda empresa usa un servicio de nube o de correo con servidores en el extranjero).
- Obligatorio identificar **al menos un encargado del tratamiento** y verificar si existe cláusula contractual.
- Se debe citar artículo, no solo la ley.
- La exposición es la ronda de cierre de esta misma sesión. El grupo **lee y explica su resultado**. No se usan diapositivas.

## Rúbrica cognitiva (20 puntos)

| Criterio | 5 | 3 | 1 |
|---|---|---|---|
| **Completitud del flujo** | Recorre las seis etapas, incluida eliminación | Recorre cuatro o cinco | Se detiene en el almacenamiento |
| **Base legal** | Identifica la base legal correcta por etapa y distingue consentimiento de otras bases | Base legal identificada de forma general | Asume consentimiento en todo |
| **Flujo transfronterizo y encargados** | Identifica ambos y evalúa las garantías existentes | Identifica uno de los dos | No los detecta |
| **Precisión normativa** | Cita artículos específicos y la autoridad competente | Cita la norma sin artículo | Referencia genérica |

## Anexo · Material de trabajo

**No se busca información fuera del aula.** Cada equipo trabaja con la organización que se le asignó del banco de casos, en `CASOS/EMPRESA-<NN>-<slug>/`. Las diez organizaciones tienen cifras, personas y documentos distintos, de modo que ningún equipo puede reutilizar el resultado de otro.

| Para qué | Archivo del caso | Qué contiene |
|---|---|---|
| Qué datos trata y con qué base | `documentos/registro-datos-y-licencias.md` | Datos personales tratados, finalidad declarada, dónde residen y el estado del consentimiento |
| A quién se los entrega | `documentos/contratos-proveedores.md` | Proveedores que acceden a datos, con sus cláusulas y la existencia o ausencia de acuerdo de encargo de tratamiento |
| El dato en concreto | `datos/empleados.csv` | Personal con su documento y sus datos de contacto, que es el flujo más fácil de rastrear entero |
| Quién puede verlo | `datos/usuarios_erp.csv` | Usuarios habilitados sobre el sistema que contiene el dato, para medir el alcance del acceso |
| Contexto regulatorio | `FICHA.md` | Naturaleza de la organización y entidades que la supervisan, sección A |

---

---

[Semana 11](README.md) · [Teoría](1-TEORIA.md) · **Dinámica de aula** · [Taller de laboratorio](3-TALLER.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
