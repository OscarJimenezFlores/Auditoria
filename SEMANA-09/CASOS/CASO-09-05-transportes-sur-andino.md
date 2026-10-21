[Semana 09](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 09·04](CASO-09-04-coopac-frontera-sur.md) · **Caso 09·05** · [Caso 09·06](CASO-09-06-distribuidora-andina-sur.md) · [Encargo 09](../../ENCARGOS-UNIDAD-II/CASO-09-ciclo-de-vida-del-software.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>TRANSPORTES SUR ANDINO S.A.</strong><br>
  <em>Solicitud de auditoría · Ciclo de vida del software</em>
</div>

---

# Solicitud de auditoría de el ciclo de vida de nuestro software

| | |
|---|---|
| **Documento** | Solicitud de auditoría de el ciclo de vida de nuestro software |
| **De** | Gerente General, por encargo del Directorio, TRANSPORTES SUR ANDINO S.A. |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 12 de octubre de 2026 |
| **Clasificación** | CONFIDENCIAL — USO ACADÉMICO |

---

## 1. Quiénes somos

Somos **TRANSPORTES SUR ANDINO S.A.**, transporte terrestre de pasajeros interprovincial, con sede en Tacna, con terminales en Moquegua, Arequipa y Puno. Operamos desde hace 27 años, con 268 trabajadores estables y Conductores en régimen mixto. Nuestros ingresos son de S/ 52.6 millones y atendemos corredor sur. Tacna–Arequipa–Puno–Cusco.

Nos regulan o supervisan **MTC · SUTRAN · SUNAT · ANPD · SUNAFIL**.

Nuestra área de tecnologías de la información tiene **4 personas**. La encabeza nuestro jefe de Sistemas, que reporta a Gerencia de Operaciones, no a Gerencia General. El presupuesto de tecnologías de la información es de **S/ 598 000**, el 1.14 % de nuestros ingresos. El objetivo que le declaramos a esa área es «Recuperar el control del canal en línea e integrar la operación de venta, embarque y flota».

**Lo que más nos cuesta.** El control de horas de conducción y descanso —exigible por SUTRAN— se lleva en Excel y no cruza con el GPS. Una fiscalización de 2025 detectó inconsistencias en 23 manifiestos.

### 1.1. Los sistemas con los que operamos

| Sistema | Qué es | Dónde corre | Desde | ¿Tiene soporte vigente? |
|---|---|---|---|---|
| **Venta de pasajes y manifiesto** | Producto del rubro, terminales en counter | Servidor central en Tacna | 2016 | Sí |
| **Venta en línea y app de pasajeros** | Desarrollo tercerizado en 2021 | Nube pública | 2021 | Contrato vencido |
| **GPS y control de flota** | Servicio del proveedor de rastreo | SaaS | 2019 | Sí |
| **Mantenimiento de unidades** | Hojas de cálculo compartidas | Drive corporativo | 2018 | No |
| **Planillas y control de descanso de conductores** | Sistema local | PC de RR. HH. | 2017 | No |

### 1.2. Nuestros procesos

1. Programación de flota y rutas
2. Venta de pasajes en counter y en línea
3. Embarque y manifiesto de pasajeros
4. Mantenimiento de unidades
5. Control de conductores y descansos
6. Encomiendas y carga

## 2. Por qué pedimos esta auditoría

El control de horas de conducción y descanso que nos exige SUTRAN se calcula en un libro de cálculo con macros que circula por correo. La fiscalización de 2025 encontró 23 manifiestos inconsistentes. Nadie sabe qué versión del libro produjo cada manifiesto, y el canal en línea tercerizado no tiene código en nuestro poder.

## 3. Lo que ya sabemos que no está bien

Estos riesgos los tenemos identificados y no los hemos tratado.

- Sistema en línea sin proveedor ni código fuente en poder de la empresa
- Datos personales de pasajeros en un servicio sin contrato vigente
- Sin control automatizado de jornada de conductores

**Lo que nos pasó en el periodo. Venta duplicada de asientos en feriado largo.** El sistema de venta en línea y el de counter no comparten bloqueo de asiento. En el feriado de julio de 2025 se vendieron 78 asientos duplicados. Se resolvió con reembolsos y una crisis en terminal. El proveedor del sistema en línea no responde desde marzo.

## 4. Lo que ya nos dijeron

- SUTRAN fiscalizó en 2025 el control de horas de conducción y encontró inconsistencias en 23 manifiestos. El procedimiento sancionador está en curso.
- Nunca nos han auditado el área de sistemas. El incidente de los 78 asientos duplicados lo resolvimos con reembolsos y no produjo ninguna revisión.
- La auditoría financiera externa observó en 2025 que la venta en línea no concilia con la contabilidad de forma automática.

## 5. Lo que queremos saber

Son las preguntas que la dirección espera que la auditoría responda. Cómo responderlas, con qué alcance, con qué criterios y con qué procedimientos, es lo que esperamos de su plan.

1. Saber qué podemos auditar del libro de cálculo de descansos y qué podemos auditar del canal en línea, que no tiene código en nuestro poder.
2. Saber si el libro de cálculo cumple lo que SUTRAN exige sobre jornada de conductores, versión por versión.
3. Saber cómo se cambió el libro la última vez y si alguien lo probó antes de usarlo.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | El Directorio lo pidió después de la fiscalización de SUTRAN y la Gerencia General contrata el servicio |
| **Contraparte designada** | Nuestro Gerente de Operaciones, de quien depende el Jefe de Sistemas |
| **Canal único** | Toda solicitud entra y sale por el correo de la Gerencia de Operaciones, con copia al Jefe de Sistemas |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 19 de octubre de 2026. Trabajo de campo del 20 de octubre de 2026 al 9 de noviembre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 10 de noviembre de 2026 y el 16 de noviembre de 2026. Informe entre el 17 de noviembre de 2026 y el 23 de noviembre de 2026 |
| **Horas que financiamos** | Hasta 193 horas de la comisión. Unas 39 de planificación, 116 de trabajo de campo, 15 de comunicación de resultados y 23 de informe. Más que eso no lo pagamos |
| **Horas que podemos dedicarles** | Nuestra área de tecnologías de la información dedica unas 160 horas al mes al proceso que van a auditar, entre sus 4 personas. No pueden pedirle más tiempo que ese |
| **Presupuesto que aprobamos** | S/ 13 992, a tarifa de referencia de S/ 110 la hora de supervisión, S/ 85 la de jefe de comisión y S/ 60 la de integrante, sin viáticos. Si necesitan ir a nuestras sedes fuera de Tacna, los pasajes y viáticos se presupuestan aparte |
| **Confidencialidad** | Todo lo que les entregamos es confidencial. Lo guardan en un repositorio privado, cifrado, con la marca CONFIDENCIAL — USO ACADÉMICO, y al cierre conservan solo lo que el informe cite |
| **Lo que no autorizamos** | Ninguna prueba se ejecuta sobre nuestros sistemas en esta etapa. Lo que pedimos es un plan. Si el plan incluye pruebas, dirá cuáles y nos pedirá autorización escrita antes |
| **Las personas** | En su plan y en su informe nos nombran por el cargo, no por el nombre |

## 7. Lo que les entregamos

Lo que sigue lo entregamos **a solicitud escrita**, indicando para qué lo necesitan y qué procedimiento lo va a usar. Los documentos propios de esta materia van ya como anexos de esta solicitud. Los demás se entregan por el canal único, en la carpeta que indica la tabla.

| Documento | Qué contiene | Dónde está |
|---|---|---|
| `ciclo-de-vida-del-software.md` | El expediente de nuestro software propio, con las métricas del repositorio, los despliegues y los pedidos de cambio del periodo | Anexo 1 |
| `contratos-proveedores.md` | Lo que dicen nuestros contratos sobre la propiedad del código y el soporte | [`documentos/contratos-proveedores.md`](../../../CASOS/EMPRESA-05-transportes-sur-andino/documentos/contratos-proveedores.md) |
| `extracciones-y-registros.md` | Las extracciones del sistema principal y la bitácora que conservamos | [`documentos/extracciones-y-registros.md`](../../../CASOS/EMPRESA-05-transportes-sur-andino/documentos/extracciones-y-registros.md) |
| `narrativa-proceso-compras.md` | Cómo opera el proceso que nuestro software soporta o alimenta | [`documentos/narrativa-proceso-compras.md`](../../../CASOS/EMPRESA-05-transportes-sur-andino/documentos/narrativa-proceso-compras.md) |
| `organigrama-y-accesos.md` | Quién desarrolla, quién despliega y quién aprueba, según los accesos | [`documentos/organigrama-y-accesos.md`](../../../CASOS/EMPRESA-05-transportes-sur-andino/documentos/organigrama-y-accesos.md) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/usuarios_erp.csv` | Los usuarios de nuestro sistema principal, con perfil, último acceso y segundo factor | 181 registros · 181 habilitados · 181 sin segundo factor |
| `datos/pagos.csv` | Nuestros pagos del periodo | 13694 registros · S/ 20 728 005 en total |

Atentamente,

**Gerente General, por encargo del Directorio**
TRANSPORTES SUR ANDINO S.A.

---

## Anexos

### Anexo 1 · `ciclo-de-vida-del-software.md`

### 1. El sistema desarrollado internamente

| Campo | Contenido |
|---|---|
| Sistema | **Control de horas de conducción y descanso** |
| Descripción | Libro de cálculo con macros desarrollado internamente, que consolida los manifiestos y calcula los descansos que exige SUTRAN |
| En producción desde | 2018 |
| Lenguaje y plataforma | Visual Basic para Aplicaciones sobre Microsoft Excel |
| Personas que lo mantienen hoy | 1 |
| ¿Existe documentación técnica? | Solo el manual de usuario |
| ¿Existe control de versiones? | Sí, repositorio interno |
| ¿Existe ambiente de pruebas separado de producción? | Sí, pero con datos de producción copiados |

> **Contexto que da la organización.** «Lo armó un asistente de operaciones que ya no trabaja aquí. No hay otra versión que la que circula por correo. Desde entonces se le hacen ajustes cuando algo falla o cuando el área pide un cambio.»

### 2. Métricas del repositorio

Extraídas con `git log` sobre el periodo auditado.

| Métrica | Valor |
|---|---|
| Commits en el periodo | 161 |
| Autores distintos | 4 |
| Commits del autor principal | 61 % del total |
| Ramas activas | 7 |
| Ramas sin fusionar con más de 90 días | 4 |
| Commits directos a la rama principal | **95 %** |
| Pull Requests abiertos en el periodo | 13 |
| Pull Requests con revisión de un segundo | **3** |
| Etiquetas de versión creadas | 1 |
| Commits con mensaje de una sola palabra | 34 |
| Archivos con más de 1 000 líneas | 4 |
| ¿Hay pruebas automatizadas en el repositorio? | Sí, 3 archivos de prueba sin ejecutarse desde 2023 |

### 3. Últimos despliegues a producción

| Fecha | Versión | Qué se desplegó | ¿Hubo etiqueta? | ¿Hubo prueba previa? | ¿Se pudo revertir? |
|---|---|---|---|---|---|
| 2025-09-09 | v1.6 | Ajuste de cálculo | No | Parcial | Sí |
| 2025-10-09 | v1.7 | Corrección urgente en producción | Sí | No | No |
| 2025-12-22 | v1.2 | Corrección urgente en producción | No | Parcial | Sí |
| 2025-04-21 | v1.2 | Nuevo campo solicitado por el área | No | Parcial | Sí |
| 2025-06-20 | v1.3 | Corrección de error en reportes | No | No | No |
| 2025-07-03 | — | Corrección de error en reportes | No | No | No |

### 4. Trazabilidad de requisitos

La organización entrega los pedidos de cambio del periodo, tal como los registra.

| N.º | Fecha | Solicitado por | Qué se pidió | ¿Especificación escrita? | ¿Aceptación formal? | ¿Se desplegó? |
|---|---|---|---|---|---|---|
| 01 | 2025-06-25 | Operaciones | Exportar a hoja de cálculo | No | Verbal | No |
| 02 | 2025-09-24 | Almacén | Bloquear la edición tras el cierre | No | No | Sí |
| 03 | 2025-05-18 | Comercial | Agregar un filtro al reporte | No | No | Sí |
| 04 | 2025-06-17 | Administración y Finanzas | Corregir el redondeo | Correo | No | Sí |
| 05 | 2025-04-16 | Contabilidad | Cambiar el cálculo del descuento | No | No | Sí |
| 06 | 2025-08-14 | Recursos Humanos | Exportar a hoja de cálculo | No | No | Sí |
| 07 | 2025-07-11 | Administración y Finanzas | Agregar un filtro al reporte | No | Verbal | No |
| 08 | 2025-06-08 | Operaciones | Cambiar el cálculo del descuento | Correo | No | No |

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

[Semana 09](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 09·04](CASO-09-04-coopac-frontera-sur.md) · **Caso 09·05** · [Caso 09·06](CASO-09-06-distribuidora-andina-sur.md) · [Encargo 09](../../ENCARGOS-UNIDAD-II/CASO-09-ciclo-de-vida-del-software.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
