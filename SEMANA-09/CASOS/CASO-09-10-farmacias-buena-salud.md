[Semana 09](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 09·09](CASO-09-09-servicios-mineros-cordillera.md) · **Caso 09·10** · [Encargo 09](../../ENCARGOS-UNIDAD-II/CASO-09-ciclo-de-vida-del-software.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>CADENA DE FARMACIAS BUENA SALUD E.I.R.L.</strong><br>
  <em>Solicitud de auditoría · Ciclo de vida del software</em>
</div>

---

# Solicitud de auditoría de el ciclo de vida de nuestro software

| | |
|---|---|
| **Documento** | Solicitud de auditoría de el ciclo de vida de nuestro software |
| **De** | Gerente General y titular de la empresa, CADENA DE FARMACIAS BUENA SALUD E.I.R.L. |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 12 de octubre de 2026 |
| **Clasificación** | CONFIDENCIAL — USO ACADÉMICO |

---

## 1. Quiénes somos

Somos **CADENA DE FARMACIAS BUENA SALUD E.I.R.L.**, retail farmacéutico · 23 locales, con sede en Tacna, Moquegua e Ilo. Operamos desde hace 15 años, con 196 trabajadores estables y 28 químicos farmacéuticos por turnos. Nuestros ingresos son de S/ 42.3 millones y atendemos tacna, Moquegua e Ilo.

Nos regulan o supervisan **DIGEMID · DIRESA · SUNAT · INDECOPI · ANPD**.

Nuestra área de tecnologías de la información tiene **3 personas**. La encabeza nuestro jefe de Sistemas, que reporta a Gerencia General. Es el único con conocimiento del sistema de puntos de venta. El presupuesto de tecnologías de la información es de **S/ 468 000**, el 1.11 % de nuestros ingresos. El objetivo que le declaramos a esa área es «Eliminar la dependencia de una sola persona y cumplir la trazabilidad exigida por DIGEMID».

**Lo que más nos cuesta.** La consolidación nocturna falla en promedio dos veces por semana y nadie más que el jefe de sistemas sabe reprocesarla. Cuando falla, el stock central queda desactualizado y se compra de más.

### 1.1. Los sistemas con los que operamos

| Sistema | Qué es | Dónde corre | Desde | ¿Tiene soporte vigente? |
|---|---|---|---|---|
| **Punto de venta y stock** | Producto del rubro farmacia, instalado local por local | Servidor por local, consolidación nocturna | 2016 | Sí |
| **Consolidación central** | Proceso nocturno por archivos, desarrollo propio | Servidor central | 2016 | No, lo mantiene el jefe de sistemas |
| **Programa de fidelización** | Módulo del proveedor del POS | Nube del proveedor | 2021 | Sí |
| **Compras y distribución a locales** | Hojas de cálculo y correo | — | — | No |
| **Receta digital y control de estupefacientes** | Libro físico foliado, exigido por DIGEMID | Papel | — | — |

### 1.2. Nuestros procesos

1. Compras a laboratorios y droguerías
2. Distribución a los 23 locales
3. Venta y dispensación
4. Control de productos controlados
5. Fidelización de clientes
6. Cierre de caja y consolidación

## 2. Por qué pedimos esta auditoría

La consolidación nocturna que une las ventas y el stock de nuestros 23 locales la desarrolló el Jefe de Sistemas, que sigue en el cargo y es el único que sabe reprocesarla. Falla dos veces por semana. DIGEMID nos exige reconstruir movimientos que ese proceso no conserva. Queremos saber qué pasa el día que el Jefe de Sistemas no esté.

## 3. Lo que ya sabemos que no está bien

Estos riesgos los tenemos identificados y no los hemos tratado.

- Dependencia crítica de una sola persona
- Retención de datos insuficiente frente a la exigencia regulatoria
- Datos de salud de clientes en el programa de fidelización sin base legal declarada

**Lo que nos pasó en el periodo. Diferencia de inventario en productos controlados.** Un cruce entre el libro físico de estupefacientes y el sistema arrojó una diferencia de 214 unidades en cuatro locales durante 2025. DIGEMID puede sancionar. No hay forma de reconstruir el movimiento porque el POS no conserva el detalle más allá de 90 días.

## 4. Lo que ya nos dijeron

- DIGEMID inspeccionó en 2025 cuatro de nuestros locales y levantó un acta por la diferencia de 214 unidades de productos controlados entre el libro físico y el sistema. El procedimiento sancionador está en curso.
- Nunca nos han auditado el sistema de punto de venta ni la consolidación central.
- La auditoría financiera externa de 2025 observó que valorizamos el inventario central con un stock que nosotros mismos reconocemos desactualizado.

## 5. Lo que queremos saber

Son las preguntas que la dirección espera que la auditoría responda. Cómo responderlas, con qué alcance, con qué criterios y con qué procedimientos, es lo que esperamos de su plan.

1. Saber qué parte del ciclo de vida del software aplica a un proceso por lotes que corre de noche en 23 locales y un servidor central.
2. Saber si la consolidación conserva o puede conservar los movimientos de productos controlados que DIGEMID nos exige.
3. Saber qué pasa si el Jefe de Sistemas, que escribe, despliega y aprueba el código, no está.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | Lo decidió el titular de la empresa, tras la inspección de DIGEMID, y lo formalizó por memorando |
| **Contraparte designada** | El propio Gerente General, con el Jefe de Sistemas como único enlace técnico |
| **Canal único** | Toda solicitud entra y sale por el correo de la Gerencia General, con copia al Jefe de Sistemas y al Director Técnico farmacéutico |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 19 de octubre de 2026. Trabajo de campo del 20 de octubre de 2026 al 9 de noviembre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 10 de noviembre de 2026 y el 16 de noviembre de 2026. Informe entre el 17 de noviembre de 2026 y el 23 de noviembre de 2026 |
| **Horas que financiamos** | Hasta 171 horas de la comisión. Unas 34 de planificación, 103 de trabajo de campo, 14 de comunicación de resultados y 20 de informe. Más que eso no lo pagamos |
| **Horas que podemos dedicarles** | Nuestra área de tecnologías de la información dedica unas 120 horas al mes al proceso que van a auditar, entre sus 3 personas. No pueden pedirle más tiempo que ese |
| **Presupuesto que aprobamos** | S/ 12 398, a tarifa de referencia de S/ 110 la hora de supervisión, S/ 85 la de jefe de comisión y S/ 60 la de integrante, sin viáticos. Si necesitan ir a nuestras sedes fuera de Tacna, los pasajes y viáticos se presupuestan aparte |
| **Confidencialidad** | Todo lo que les entregamos es confidencial. Lo guardan en un repositorio privado, cifrado, con la marca CONFIDENCIAL — USO ACADÉMICO, y al cierre conservan solo lo que el informe cite |
| **Lo que no autorizamos** | Ninguna prueba se ejecuta sobre nuestros sistemas en esta etapa. Lo que pedimos es un plan. Si el plan incluye pruebas, dirá cuáles y nos pedirá autorización escrita antes |
| **Las personas** | En su plan y en su informe nos nombran por el cargo, no por el nombre |

## 7. Lo que les entregamos

Lo que sigue lo entregamos **a solicitud escrita**, indicando para qué lo necesitan y qué procedimiento lo va a usar. Los documentos propios de esta materia van ya como anexos de esta solicitud. Los demás se entregan por el canal único, en la carpeta que indica la tabla.

| Documento | Qué contiene | Dónde está |
|---|---|---|
| `ciclo-de-vida-del-software.md` | El expediente de nuestro software propio, con las métricas del repositorio, los despliegues y los pedidos de cambio del periodo | Anexo 1 |
| `contratos-proveedores.md` | Lo que dicen nuestros contratos sobre la propiedad del código y el soporte | [`documentos/contratos-proveedores.md`](../../../CASOS/EMPRESA-10-farmacias-buena-salud/documentos/contratos-proveedores.md) |
| `extracciones-y-registros.md` | Las extracciones del sistema principal y la bitácora que conservamos | [`documentos/extracciones-y-registros.md`](../../../CASOS/EMPRESA-10-farmacias-buena-salud/documentos/extracciones-y-registros.md) |
| `narrativa-proceso-compras.md` | Cómo opera el proceso que nuestro software soporta o alimenta | [`documentos/narrativa-proceso-compras.md`](../../../CASOS/EMPRESA-10-farmacias-buena-salud/documentos/narrativa-proceso-compras.md) |
| `organigrama-y-accesos.md` | Quién desarrolla, quién despliega y quién aprueba, según los accesos | [`documentos/organigrama-y-accesos.md`](../../../CASOS/EMPRESA-10-farmacias-buena-salud/documentos/organigrama-y-accesos.md) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/usuarios_erp.csv` | Los usuarios de nuestro sistema principal, con perfil, último acceso y segundo factor | 132 registros · 132 habilitados · 132 sin segundo factor |
| `datos/pagos.csv` | Nuestros pagos del periodo | 11014 registros · S/ 16 747 445 en total |

Atentamente,

**Gerente General y titular de la empresa**
CADENA DE FARMACIAS BUENA SALUD E.I.R.L.

---

## Anexos

### Anexo 1 · `ciclo-de-vida-del-software.md`

### 1. El sistema desarrollado internamente

| Campo | Contenido |
|---|---|
| Sistema | **Consolidación central** |
| Descripción | Proceso nocturno por archivos, desarrollo propio, que consolida las ventas y el stock de los 23 locales |
| En producción desde | 2016 |
| Lenguaje y plataforma | Scripts por lotes y Python 2.7 |
| Personas que lo mantienen hoy | 1 |
| ¿Existe documentación técnica? | Parcial, desactualizada |
| ¿Existe control de versiones? | Sí, repositorio interno |
| ¿Existe ambiente de pruebas separado de producción? | Sí, pero con datos de producción copiados |

> **Contexto que da la organización.** «Lo desarrolló el jefe de sistemas, que sigue en el cargo y es la única persona que sabe reprocesarlo cuando falla. Desde entonces se le hacen ajustes cuando algo falla o cuando el área pide un cambio.»

### 2. Métricas del repositorio

Extraídas con `git log` sobre el periodo auditado.

| Métrica | Valor |
|---|---|
| Commits en el periodo | 323 |
| Autores distintos | 2 |
| Commits del autor principal | 60 % del total |
| Ramas activas | 6 |
| Ramas sin fusionar con más de 90 días | 2 |
| Commits directos a la rama principal | **89 %** |
| Pull Requests abiertos en el periodo | 0 |
| Pull Requests con revisión de un segundo | **3** |
| Etiquetas de versión creadas | 0 |
| Commits con mensaje de una sola palabra | 56 |
| Archivos con más de 1 000 líneas | 4 |
| ¿Hay pruebas automatizadas en el repositorio? | No |

### 3. Últimos despliegues a producción

| Fecha | Versión | Qué se desplegó | ¿Hubo etiqueta? | ¿Hubo prueba previa? | ¿Se pudo revertir? |
|---|---|---|---|---|---|
| 2025-12-05 | — | Ajuste de cálculo | No | No | No |
| 2025-09-16 | — | Cambio de formato de comprobante | No | No | No |
| 2025-11-12 | v1.4 | Corrección urgente en producción | Sí | No | Sí |
| 2025-04-19 | — | Corrección de error en reportes | No | Parcial | Sí |
| 2025-03-04 | — | Nuevo campo solicitado por el área | Sí | No | No |
| 2025-08-13 | — | Nuevo campo solicitado por el área | Sí | No | Sí |

### 4. Trazabilidad de requisitos

La organización entrega los pedidos de cambio del periodo, tal como los registra.

| N.º | Fecha | Solicitado por | Qué se pidió | ¿Especificación escrita? | ¿Aceptación formal? | ¿Se desplegó? |
|---|---|---|---|---|---|---|
| 01 | 2025-03-14 | Operaciones | Nuevo reporte mensual | Correo | No | Sí |
| 02 | 2025-02-04 | Administración y Finanzas | Ampliar el campo de observaciones | No | No | Sí |
| 03 | 2025-01-26 | Operaciones | Exportar a hoja de cálculo | Correo | Verbal | Sí |
| 04 | 2025-11-02 | Administración y Finanzas | Ampliar el campo de observaciones | No | Verbal | Sí |
| 05 | 2025-08-22 | Comercial | Permitir anular un registro | No | No | Sí |
| 06 | 2025-03-17 | Almacén | Cambiar el cálculo del descuento | Correo | No | No |
| 07 | 2025-08-11 | Gerencia | Ampliar el campo de observaciones | No | No | No |
| 08 | 2025-04-19 | Logística | Nuevo reporte mensual | Correo | No | No |

### 5. Lo que la organización responde

| Pregunta | Respuesta |
|---|---|
| ¿Hay un procedimiento de desarrollo documentado? | «No. Se hace según la necesidad» |
| ¿Quién aprueba pasar un cambio a producción? | «El jefe de sistemas, o el mismo que lo hizo si es urgente» |
| ¿Se revisan los cambios entre pares? | «Somos pocos. No da el tiempo» |
| ¿Hay ambiente de pruebas? | «Se prueba en producción fuera de horario» |
| ¿Existe un plan de reversión? | «Si algo sale mal, se restaura el respaldo» |
| ¿Hay pruebas automatizadas? | «No» |
| ¿Qué pasa si el sistema deja de funcionar? | «No hay alternativa. Habría que operar en papel» |

### 6. Marco de referencia

| Norma | Procesos aplicables |
|---|---|
| **NTP-ISO/IEC 12207** | Procesos del ciclo de vida del software: adquisición, desarrollo, mantenimiento, gestión de la configuración, verificación y validación |
| **COBIT 2019 · BAI03** | Gestión de la identificación y construcción de soluciones |
| **COBIT 2019 · BAI06** | Gestión de cambios de TI |
| **COBIT 2019 · BAI07** | Gestión de la aceptación y transición del cambio |
| **ISO/IEC 25010** | Características de calidad del producto software |

---

[Semana 09](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 09·09](CASO-09-09-servicios-mineros-cordillera.md) · **Caso 09·10** · [Encargo 09](../../ENCARGOS-UNIDAD-II/CASO-09-ciclo-de-vida-del-software.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
