[Semana 02](README.md) · [Teoría](1-TEORIA.md) · **Dinámica de aula** · [Taller de laboratorio](3-TALLER.md)

# Dinámica de aula · El organigrama tóxico

**SI-084 · Auditoría de Sistemas** · Semana 02 · Actividad en aula, **dentro de los 100 min de la sesión de teoría** · calificación **cognitiva**

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](../GLOSARIO.md).

---

## Qué se busca con esta actividad

Que el equipo detecte, sobre datos reales de su organización, las combinaciones de accesos que permiten a una sola persona cometer y ocultar un error o un fraude, y que resuelva el problema que aparece siempre en una empresa pequeña, donde no hay gente suficiente para separar todas las funciones.

## Con qué material se trabaja

**Todo lo que se necesita está en esta página.** No se busca información en internet ni se visita ninguna empresa. Se **asigna una organización a cada equipo al iniciar la actividad**, de las diez del cuadro siguiente. Cada una tiene su propia estructura, su propio personal y sus propios accesos, de modo que **ningún equipo llega a la misma matriz de conflictos que otro**.

Cada organización trae el tamaño real de sus áreas y la relación de personas con los roles que tienen concedidos en su sistema. El trabajo del equipo no es conseguir esa relación, es **leerla como la lee un auditor**.

### Organización 1 · Agroexportadora de aceituna

*142 trabajadores · TI 3 personas · ERP de planta y comercial*

| Puesto | Persona | Roles asignados en el sistema |
|---|---|---|
| Jefe de Planta | N. Loayza | `prod.registrar_lote`, `prod.aprobar_lote`, `alm.ajustar_inventario` |
| Contador | M. Salas | `conta.registrar_asiento`, `conta.cerrar_periodo`, `conta.modificar_plan_cuentas` |
| Tesorería | L. Núñez | `teso.registrar_proveedor`, `teso.programar_pago`, `teso.aprobar_pago` |
| Compras | R. Zeña | `comp.crear_requisicion`, `comp.crear_orden`, `comp.aprobar_orden` |
| Asistente Administrativo | C. Paredes | `conta.registrar_asiento`, `teso.programar_pago` |
| Jefe de TI | A. Mamani | `admin.crear_usuario`, `admin.asignar_rol`, `conta.registrar_asiento` |
| Analista de TI | J. Ticona | `admin.crear_usuario`, `bd.consultar_directo` |
| Exportaciones | P. Vilca | `vent.crear_pedido`, `vent.aprobar_descuento`, `vent.emitir_factura` |
| Cuenta genérica `sistemas` | sin responsable | `admin.crear_usuario`, `admin.asignar_rol`, `bd.consultar_directo` |
| Ex jefe de Compras | F. Quispe *(cesó 30/09)* | `comp.crear_orden`, `comp.aprobar_orden` · **cuenta activa** |

### Organización 2 · Clínica privada de 60 camas

*310 trabajadores · TI 6 personas · sistema clínico y administrativo*

| Puesto | Persona | Roles asignados en el sistema |
|---|---|---|
| Jefe de Admisión | R. Chino | `adm.registrar_paciente`, `adm.anular_atencion`, `fact.emitir_comprobante` |
| Contador | S. Apaza | `conta.registrar_asiento`, `conta.cerrar_periodo` |
| Tesorería | D. Flores | `teso.registrar_proveedor`, `teso.aprobar_pago`, `teso.conciliar_banco` |
| Jefe de Farmacia | V. Huanca | `farm.registrar_ingreso`, `farm.registrar_salida`, `farm.ajustar_stock` |
| Químico Farmacéutico | M. Ccama | `farm.registrar_salida` |
| Jefe de TI | G. Ramos | `admin.crear_usuario`, `admin.asignar_rol`, `clin.consultar_historia` |
| Analista de Sistemas | T. Quenta | `admin.crear_usuario`, `bd.consultar_directo`, `clin.consultar_historia` |
| Facturación (2) | — | `fact.emitir_comprobante`, `fact.anular_comprobante` |
| Personal administrativo (14) | — | `clin.consultar_historia` · **acceso general concedido en 2023** |
| Cuenta genérica `auditoria` | sin responsable | `bd.consultar_directo`, `clin.consultar_historia` |

### Organización 3 · Municipalidad distrital

*178 en planilla y 94 por CAS · TI 3 personas · SIAF, rentas y trámite*

| Puesto | Persona | Roles asignados en el sistema |
|---|---|---|
| Jefe de Rentas | E. Mamani | `rent.emitir_recibo`, `rent.anular_recibo`, `rent.condonar_deuda` |
| Cajero (2) | — | `caja.cobrar`, `caja.anular_cobro` |
| Tesorería | L. Coaquira | `teso.programar_pago`, `teso.aprobar_pago`, `teso.conciliar_banco` |
| Jefe de Abastecimiento | H. Calisaya | `abas.crear_requerimiento`, `abas.aprobar_orden`, `abas.registrar_proveedor` |
| Jefe de la Unidad de TI | W. Ancco | `admin.crear_usuario`, `admin.asignar_rol`, `rent.condonar_deuda` |
| Programador *(por locación)* | R. Sosa | `bd.consultar_directo`, `bd.modificar_directo`, `admin.crear_usuario` |
| Trámite documentario (3) | — | `tram.registrar_expediente`, `tram.derivar`, `tram.archivar` |
| Catastro | N. Ari | `cat.registrar_predio`, `cat.modificar_predio`, `rent.emitir_recibo` |
| Cuenta genérica `municipal` | sin responsable | `admin.crear_usuario`, `bd.consultar_directo` |
| Ex jefe de TI | J. Larico *(cesó 14/02)* | `admin.crear_usuario`, `admin.asignar_rol` · **cuenta activa** |

### Organización 4 · Cooperativa de ahorro y crédito

*121 trabajadores · TI 7 personas · core financiero*

| Puesto | Persona | Roles asignados en el sistema |
|---|---|---|
| Analista de Créditos (4) | — | `cred.evaluar_solicitud`, `cred.registrar_solicitud` |
| Jefe de Créditos | P. Quispe | `cred.registrar_solicitud`, `cred.aprobar_credito`, `cred.desembolsar` |
| Jefe de Operaciones | M. Cutipa | `oper.registrar_socio`, `oper.modificar_socio`, `caja.anular_operacion` |
| Cajero (5) | — | `caja.operar`, `caja.cuadrar` |
| Contador | A. Ticona | `conta.registrar_asiento`, `conta.cerrar_periodo`, `caja.anular_operacion` |
| Jefe de TI | F. Mendoza | `admin.crear_usuario`, `admin.asignar_rol`, `bd.consultar_directo` |
| Desarrollador | S. Ramos | `bd.consultar_directo`, `bd.modificar_directo` · **acceso a producción** |
| Oficial de Cumplimiento | R. Aguilar | `cump.revisar_alerta`, `cump.cerrar_alerta`, `oper.modificar_socio` |
| Cuenta de servicio `interfaz_sbs` | sin responsable | `bd.consultar_directo`, `rep.generar_reporte` |
| Recuperaciones | L. Choque | `cred.registrar_pago`, `cred.condonar_interes` |

### Organización 5 · Empresa de transporte de carga

*96 trabajadores · TI 2 personas · ERP y sistema de flota*

| Puesto | Persona | Roles asignados en el sistema |
|---|---|---|
| Jefe de Operaciones | P. Quispe | `flot.asignar_viaje`, `flot.cerrar_viaje`, `flot.aprobar_gasto` |
| Contador | M. Salas | `conta.registrar_asiento`, `conta.cerrar_periodo` |
| Tesorería | L. Núñez | `teso.registrar_proveedor`, `teso.programar_pago`, `teso.aprobar_pago`, `teso.conciliar_banco` |
| Compras | R. Zeña | `comp.crear_requisicion`, `comp.crear_orden`, `comp.aprobar_orden`, `comp.crear_proveedor` |
| Planillas | A. Torres | `rrhh.registrar_trabajador`, `rrhh.calcular_planilla`, `rrhh.aprobar_planilla` |
| Jefe de TI | D. Ávila | `admin.crear_usuario`, `admin.asignar_rol`, `conta.registrar_asiento` |
| Facturación | C. Paredes | `vent.emitir_factura`, `vent.anular_factura`, `vent.crear_cliente` |
| Jefe de Mantenimiento | G. Rivas | `mant.registrar_orden`, `mant.aprobar_orden`, `alm.registrar_salida` |
| Almacén de repuestos (2) | — | `alm.registrar_ingreso`, `alm.registrar_salida`, `alm.ajustar_inventario` |
| Cuenta genérica `consulta` | sin responsable | `todos.consultar`, `bd.consultar_directo` |

### Organización 6 · Distribuidora mayorista

*157 trabajadores · TI 4 personas · ERP comercial*

| Puesto | Persona | Roles asignados en el sistema |
|---|---|---|
| Jefe de Almacén | J. Mamani | `alm.registrar_ingreso`, `alm.registrar_salida`, `alm.ajustar_inventario` |
| Auxiliares de almacén (4) | — | `alm.registrar_ingreso`, `alm.registrar_salida` |
| Compras | K. Condori | `comp.crear_requisicion`, `comp.crear_orden`, `comp.aprobar_orden`, `comp.crear_proveedor` |
| Tesorería | K. Huanca | `teso.programar_pago`, `teso.aprobar_pago`, `teso.registrar_proveedor` |
| Contador | M. Maquera | `conta.registrar_asiento`, `conta.cerrar_periodo`, `alm.ajustar_inventario` |
| Jefe de Sistemas | R. Copaja | `admin.crear_usuario`, `admin.asignar_rol`, `bd.modificar_directo` |
| Jefe Comercial | D. Ávila | `vent.crear_pedido`, `vent.aprobar_descuento`, `vent.anular_factura` |
| Facturación (2) | — | `vent.emitir_factura`, `vent.anular_factura`, `vent.crear_cliente` |
| Vendedores (11) | — | `vent.crear_pedido`, `vent.crear_cliente` |
| Cuenta genérica `portal_web` | sin responsable | `bd.consultar_directo` · **la usa el portal de pedidos sin soporte** |

### Organización 7 · Instituto de educación superior

*94 trabajadores · TI 3 personas · sistema académico*

| Puesto | Persona | Roles asignados en el sistema |
|---|---|---|
| Secretaría Académica | N. Apaza | `acad.registrar_nota`, `acad.modificar_nota`, `acad.cerrar_acta` |
| Docentes (38) | — | `acad.registrar_nota` |
| Jefe de Registros | V. Ccalla | `acad.modificar_nota`, `acad.cerrar_acta`, `acad.emitir_certificado` |
| Tesorería | L. Puma | `teso.registrar_pago`, `teso.anular_pago`, `teso.conciliar_banco` |
| Contador | S. Rojas | `conta.registrar_asiento`, `conta.cerrar_periodo` |
| Jefe de TI | E. Chambi | `admin.crear_usuario`, `admin.asignar_rol`, `acad.modificar_nota` |
| Soporte técnico | M. Hancco | `admin.crear_usuario`, `bd.consultar_directo` |
| Admisión | T. Yucra | `adm.registrar_postulante`, `adm.registrar_pago`, `acad.matricular` |
| Cuenta genérica `campus` | sin responsable | `acad.consultar`, `bd.consultar_directo` |
| Ex secretaria académica | R. Nina *(cesó 31/07)* | `acad.modificar_nota`, `acad.cerrar_acta` · **cuenta activa** |

### Organización 8 · Empresa de saneamiento

*204 trabajadores · TI 5 personas · comercial y catastro*

| Puesto | Persona | Roles asignados en el sistema |
|---|---|---|
| Jefe Comercial | H. Larico | `com.emitir_facturacion`, `com.anular_recibo`, `com.aplicar_descuento` |
| Lecturistas (12) | — | `com.registrar_lectura` |
| Supervisor de Lecturas | R. Ari | `com.registrar_lectura`, `com.modificar_lectura`, `com.emitir_facturacion` |
| Catastro | P. Ccama | `cat.registrar_conexion`, `cat.modificar_conexion`, `com.aplicar_descuento` |
| Tesorería | M. Coila | `teso.registrar_cobro`, `teso.anular_cobro`, `teso.conciliar_banco` |
| Contador | J. Vilca | `conta.registrar_asiento`, `conta.cerrar_periodo` |
| Jefe de TI | A. Quenta | `admin.crear_usuario`, `admin.asignar_rol`, `bd.modificar_directo` |
| Reclamos (3) | — | `rec.registrar_reclamo`, `rec.cerrar_reclamo` |
| Jefe de Reclamos | L. Chino | `rec.cerrar_reclamo`, `com.anular_recibo`, `com.aplicar_descuento` |
| Cuenta de servicio `interfaz_bancos` | sin responsable | `teso.registrar_cobro`, `bd.consultar_directo` |

### Organización 9 · Servicios de ingeniería para minería

*88 trabajadores · TI 4 personas · ERP y plataforma técnica*

| Puesto | Persona | Roles asignados en el sistema |
|---|---|---|
| Jefe de Proyectos | C. Sucari | `proy.crear_proyecto`, `proy.aprobar_valorizacion`, `proy.cerrar_proyecto` |
| Ingenieros de proyecto (9) | — | `proy.registrar_avance`, `proy.crear_valorizacion` |
| Administración | M. Layme | `comp.crear_orden`, `comp.aprobar_orden`, `teso.programar_pago` |
| Tesorería | F. Nina | `teso.programar_pago`, `teso.aprobar_pago` |
| Contador | G. Pari | `conta.registrar_asiento`, `conta.cerrar_periodo`, `proy.aprobar_valorizacion` |
| Jefe de TI | R. Aro | `admin.crear_usuario`, `admin.asignar_rol`, `tel.configurar_sensor` |
| Desarrollador de telemetría | S. Huisa | `tel.configurar_sensor`, `tel.modificar_lectura`, `bd.modificar_directo` |
| Laboratorio de datos (2) | — | `tel.consultar_lectura`, `bd.consultar_directo` |
| Recursos Humanos | D. Ala | `rrhh.registrar_trabajador`, `rrhh.calcular_planilla`, `rrhh.aprobar_planilla` |
| Cuenta genérica `telemetria` | sin responsable | `tel.modificar_lectura`, `bd.modificar_directo` |

### Organización 10 · Cadena regional de farmacias

*268 trabajadores · TI 5 personas · punto de venta y ERP*

| Puesto | Persona | Roles asignados en el sistema |
|---|---|---|
| Jefe de Local (34) | — | `pos.vender`, `pos.anular_venta`, `alm.ajustar_stock` |
| Químicos farmacéuticos (34) | — | `pos.vender`, `farm.registrar_receta` |
| Jefe de Compras | N. Mamani | `comp.crear_orden`, `comp.aprobar_orden`, `comp.crear_proveedor` |
| Reposición automática | cuenta de servicio | `comp.crear_orden`, `alm.ajustar_stock` · **sin responsable nombrado** |
| Tesorería | L. Cutipa | `teso.programar_pago`, `teso.aprobar_pago`, `teso.conciliar_banco` |
| Contador | R. Sosa | `conta.registrar_asiento`, `conta.cerrar_periodo`, `pos.anular_venta` |
| Jefe de TI | V. Ramos | `admin.crear_usuario`, `admin.asignar_rol`, `pos.anular_venta` |
| Soporte de tienda (2) | — | `admin.crear_usuario`, `pos.anular_venta` |
| Marketing | T. Flores | `fid.consultar_cliente`, `fid.exportar_base` · **exporta la base de clientes** |
| Ex jefe de local | J. Apaza *(cesó 12/05)* | `pos.vender`, `pos.anular_venta` · **cuenta activa** |

> **El tamaño manda.** En varias de estas organizaciones separar todas las funciones es imposible porque no hay personal suficiente. Un equipo que exija eliminar todos los conflictos no ha resuelto el problema, lo ha trasladado. **La respuesta profesional es el control compensatorio**, y por eso el producto exige al menos un conflicto que el equipo decida no eliminar.

## Lo que la teoría de hoy te da

Esta dinámica aplica piezas concretas de la sesión de teoría de hoy. Se usan tal cual, sin buscar nada más.

| De la teoría | Para qué se usa aquí |
|---|---|
| [Los principios que sostienen el diseño de controles](1-TEORIA.md) | Segregación de funciones y mínimo privilegio son el criterio que permite llamar tóxica a una combinación. Sin ese criterio la matriz es una opinión |
| [Roles y responsabilidades en seguridad de la información](1-TEORIA.md) | Define quién debe responder por cada acceso, que es la columna que convierte el conflicto en algo exigible |
| [Información y seguridad de la información](1-TEORIA.md) | Integridad y trazabilidad son las propiedades que un conflicto de segregación destruye, y así se enuncia el riesgo |

## Cómo se desarrolla · 35 minutos

| | Bloque | Quién | Minutos |
|---|---|---|---|
| **1** | **Leer la estructura.** Se lee la cabecera de la organización asignada y se anota el número real de personas por área. **El tamaño manda**: con dos personas en un área, separar cuatro funciones es imposible y el análisis debe reconocerlo desde el principio. | Equipo | 7 |
| **2** | **Cruzar personas y roles.** Sobre la tabla de accesos se marca a cada persona que reúne un rol de **registrar** y un rol de **aprobar** dentro del mismo ciclo, o de **crear el maestro** y **operar sobre él**. Se revisan además las cuentas genéricas sin responsable y las cuentas de personas que ya cesaron. | Equipo | 7 |
| **3** | **Enunciar el riesgo.** Por cada combinación se escribe qué podría hacer esa persona sola y sin que nadie lo note. Un conflicto sin riesgo redactado no se califica, porque no se puede discutir con la gerencia. | Equipo | 7 |
| **4** | **Decidir qué no se elimina.** Se elige al menos un conflicto que el equipo **decide mantener** por falta de personal, y se diseña su control compensatorio con frecuencia, responsable y la evidencia que dejaría. | Equipo | 7 |
| **5** | **Severidad.** Se ordena la matriz por severidad, justificando el orden con lo que cada conflicto pone en juego en esa organización concreta. | Equipo | 7 |

## Qué entregas

| | |
|---|---|
| **Archivo** | `SI084-S02-DINAMICA-Grupo<N>.pdf` |
| **Plantilla obligatoria** | [SI084-PLANTILLA-DINAMICA.docx](../PLANTILLAS/SI084-PLANTILLA-DINAMICA.docx) |
| **Formato** | PDF exportado desde la plantilla en Word, con la carátula de la UPT y los apellidos, nombres y códigos de todos los integrantes |
| **Qué va dentro** | Lo que el grupo resolvió en aula. Las tablas de la sección **Producto** van completas, con los textos redactados, y cada decisión va justificada |
| **Dónde se sube** | Aula virtual, tarea «Dinámica · Semana 02» |
| **Cuándo vence** | Hasta 24 h después de la sesión de teoría. La tabla se resuelve en aula; el PDF se formatea y se sube después |
| **Exposición** | En la ronda de cierre de **esta misma sesión**. El grupo **lee y explica su resultado** ante el aula, con el documento a la vista. No se usan diapositivas |

> No se califica un trabajo entregado en `.docx`, sin carátula, sin los códigos de los integrantes o con las tablas del producto vacías.

---

## Consigna

> **«El organigrama tóxico»**
> Cada equipo recibe **la estructura y la matriz de accesos de una de las diez organizaciones** de esta página (está en la sección **Con qué material se trabaja** de esta página), con el detalle de qué roles del ERP tiene asignado cada persona. El equipo debe **detectar las combinaciones tóxicas de segregación de funciones y proponer controles compensatorios viables para el tamaño de la empresa**.

## Producto

**Producto 1 — Matriz de conflictos.**

| Persona | Rol A | Rol B en conflicto | Riesgo concreto | Severidad |
|---|---|---|---|---|

**Producto 2 — Controles compensatorios.** Para cada conflicto que **no pueda eliminarse** por falta de personal, un control compensatorio con descripción, frecuencia, responsable de ejecución y evidencia que dejaría.

> **Dónde va.** Este producto se presenta en la **sección 2 de la [plantilla de dinámica](../PLANTILLAS/SI084-PLANTILLA-DINAMICA.docx)**, «El producto». No se copia la consigna ni la teoría. Solo el resultado y lo que lo sostiene.

## Ejemplo resuelto

*El caso de este ejemplo es distinto del que le toca a tu grupo. Sirve para que veas el nivel de detalle que se espera, no para copiarlo.*

**Una fila bien resuelta de cada tabla.** El ejemplo es de otra empresa y de un conflicto distinto de los que hay en tu material.

*Matriz de conflictos*

| Persona | Rol A | Rol B en conflicto | Riesgo concreto | Severidad |
|---|---|---|---|---|
| Jefe de Almacén (empresa de 30 personas) | `alm.registrar_salida` | `alm.ajustar_inventario` | Puede sacar mercadería del almacén y, acto seguido, ajustar el inventario para que el faltante no aparezca. El ERP no exige justificación ni aprobación para el ajuste, y la diferencia solo se detectaría en el inventario físico anual. | Crítica |

*Control compensatorio*

| Campo | Contenido |
|---|---|
| Conflicto que no se elimina | El almacén tiene un solo jefe y cuatro operarios sin perfil administrativo. Separar el ajuste de inventario exige un puesto de control de existencias que la empresa no puede financiar. |
| Control compensatorio | Revisión quincenal, por el Contador, del reporte de ajustes de inventario del período, con verificación física por muestreo de los cinco ajustes de mayor valor. |
| Frecuencia | Quincenal, dentro de los tres días hábiles siguientes al corte. |
| Responsable de ejecución | Contador, que no tiene acceso al módulo de almacén. |
| Evidencia que deja | Reporte de ajustes firmado, con el detalle del conteo físico de los cinco ajustes verificados y la explicación de cada diferencia. |
| Control ISO que lo sustenta | ISO/IEC 27001:2022, **A.5.3 Segregation of duties**, y objetivo COBIT 2019 **DSS06.03 Manage roles, responsibilities, access privileges and levels of authority**. |

**La diferencia entre aprobar y no aprobar.**

| Así no | Así sí |
|---|---|
| «Riesgo de fraude en almacén.» | «Puede sacar mercadería y ajustar el inventario para que el faltante no aparezca. El ajuste no exige justificación ni aprobación.» |
| «Se recomienda contratar más personal.» | «Revisión quincenal del Contador, con verificación física de los cinco ajustes de mayor valor, porque el puesto de control de existencias no es financiable.» |
| «El jefe supervisa.» | «Contador, que no tiene acceso al módulo de almacén, dentro de los tres días hábiles siguientes al corte.» |

## Reglas

- 35 min en aula, dentro de la sesión de teoría.
- Se exige al menos **un conflicto que el equipo decida NO eliminar**, justificando por qué el control compensatorio es más eficiente que contratar personal.
- La exposición es la ronda de cierre de esta misma sesión. El grupo **lee y explica su resultado**. No se usan diapositivas.

## Rúbrica cognitiva (20 puntos)

| Criterio | 5 | 3 | 1 |
|---|---|---|---|
| **Detección de conflictos** | Identifica conflictos no evidentes (p. ej. desarrollo + despliegue) además de los obvios | Identifica solo los conflictos evidentes | Confunde jerarquía con conflicto de funciones |
| **Riesgo concreto** | Describe el fraude o error específico posible y su límite económico | Riesgo genérico pero pertinente | «Riesgo de seguridad» |
| **Control compensatorio** | Viable, con frecuencia, responsable y evidencia verificable | Viable pero incompleto | Propone contratar personal como única salida |
| **Criterio normativo** | Cita el control ISO o el objetivo COBIT aplicable | Menciona la norma sin el control | Sin referencia normativa |

---

---

[Semana 02](README.md) · [Teoría](1-TEORIA.md) · **Dinámica de aula** · [Taller de laboratorio](3-TALLER.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
