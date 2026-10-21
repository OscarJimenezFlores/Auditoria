[Semana 09](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 09·05](CASO-09-05-transportes-sur-andino.md) · **Caso 09·06** · [Caso 09·07](CASO-09-07-instituto-vertiente-sur.md) · [Encargo 09](../../ENCARGOS-UNIDAD-II/CASO-09-ciclo-de-vida-del-software.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>DISTRIBUIDORA ANDINA DEL SUR S.A.C.</strong><br>
  <em>Solicitud de auditoría · Ciclo de vida del software</em>
</div>

---

# Solicitud de auditoría de el ciclo de vida de nuestro software

| | |
|---|---|
| **Documento** | Solicitud de auditoría de el ciclo de vida de nuestro software |
| **De** | Gerente General, por acuerdo de la Junta General de Accionistas, DISTRIBUIDORA ANDINA DEL SUR S.A.C. |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 12 de octubre de 2026 |
| **Clasificación** | CONFIDENCIAL — USO ACADÉMICO |

---

## 1. Quiénes somos

Somos **DISTRIBUIDORA ANDINA DEL SUR S.A.C.**, distribución mayorista de consumo masivo, con sede en Tacna, con almacenes en Tacna e Ilo. Operamos desde hace 21 años, con 157 trabajadores estables y 34 en temporada alta. Nuestros ingresos son de S/ 68.4 millones y atendemos tacna, Moquegua y frontera.

Nos regulan o supervisan **SUNAT · INDECOPI · SUNAFIL · ANPD**.

Nuestra área de tecnologías de la información tiene **4 personas**. La encabeza nuestro jefe de Sistemas, que reporta a Gerencia de Administración y Finanzas. El presupuesto de tecnologías de la información es de **S/ 742 000**, el 1.08 % de nuestros ingresos. El objetivo que le declaramos a esa área es «Restablecer el control interno sobre el ciclo de compras y pagos y conciliar el inventario».

**Lo que más nos cuesta.** El módulo de almacén del ERP se dejó de usar para la gestión de ubicaciones y se sostiene en hojas de cálculo. El inventario contable y el físico difieren en promedio 4.7 %.

### 1.1. Los sistemas con los que operamos

| Sistema | Qué es | Dónde corre | Desde | ¿Tiene soporte vigente? |
|---|---|---|---|---|
| **ERP comercial** | Producto peruano con módulos de compras, ventas, almacén, tesorería y contabilidad | Servidor propio | 2015 | Sí |
| **Fuerza de ventas móvil** | App del proveedor del ERP | Nube del proveedor | 2020 | Sí |
| **Facturación electrónica** | OSE contratado | SaaS | 2018 | Sí |
| **Gestión de almacén** | Módulo del ERP más hojas de cálculo paralelas | Mixto | 2015 | Parcial |
| **Portal de pedidos para clientes** | Desarrollo propio | Hosting compartido | 2022 | No |

### 1.2. Nuestros procesos

1. Compras a proveedores y reposición
2. Almacenamiento y despacho
3. Venta y distribución en ruta
4. Cobranza y crédito a clientes
5. Tesorería y pagos
6. Contabilidad y cierre

## 2. Por qué pedimos esta auditoría

El portal de pedidos para clientes lo desarrolló un practicante en 2022 y se publica en un hosting compartido. Recibe cambios directos en producción cuando un cliente se queja. Aprobamos esta auditoría después de que un cambio en el portal dejara de registrar pedidos durante un fin de semana.

## 3. Lo que ya sabemos que no está bien

Estos riesgos los tenemos identificados y no los hemos tratado.

- Segregación de funciones inexistente en compras y pagos
- Inventario sin conciliación sistemática
- Portal de clientes sin mantenimiento ni pruebas de seguridad

**Lo que nos pasó en el periodo. Fraccionamiento de compras bajo el umbral de aprobación.** Una revisión interna detectó órdenes de compra fraccionadas sistemáticamente bajo el umbral de S/ 5 000 que exige aprobación de gerencia. El mismo usuario registraba y aprobaba. El ERP lo permitía por configuración de perfiles.

## 4. Lo que ya nos dijeron

- Nuestra revisión interna de 2025, hecha por Contabilidad a pedido de la gerencia, detectó el fraccionamiento de compras y la autoaprobación en el ERP. No tuvo forma de informe y no generó un plan de acción.
- La auditoría financiera externa de 2025 nos recomendó segregar el registro y la aprobación de pagos. La recomendación está abierta.
- Nunca nos han auditado el ERP ni el portal de pedidos.

## 5. Lo que queremos saber

Son las preguntas que la dirección espera que la auditoría responda. Cómo responderlas, con qué alcance, con qué criterios y con qué procedimientos, es lo que esperamos de su plan.

1. Saber cómo se construye y cómo se cambia el portal de pedidos, y qué debió evitar que dejara de registrar pedidos un fin de semana.
2. Saber si la configuración de perfiles del ERP, que hacemos nosotros, es parte del ciclo de vida del software o del control de accesos.
3. Saber contra qué se nos audita si ninguna norma nos exige control de cambios.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | La Junta General de Accionistas dispuso una auditoría externa del control interno sobre tecnologías de la información, tras la revisión interna que detectó el fraccionamiento |
| **Contraparte designada** | Nuestro Gerente de Administración y Finanzas, de quien depende el Jefe de Sistemas |
| **Canal único** | Toda solicitud entra y sale por el correo de la Gerencia de Administración y Finanzas, con copia a Contabilidad y al Jefe de Sistemas |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 19 de octubre de 2026. Trabajo de campo del 20 de octubre de 2026 al 9 de noviembre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 10 de noviembre de 2026 y el 16 de noviembre de 2026. Informe entre el 17 de noviembre de 2026 y el 23 de noviembre de 2026 |
| **Horas que financiamos** | Hasta 183 horas de la comisión. Unas 37 de planificación, 110 de trabajo de campo, 15 de comunicación de resultados y 21 de informe. Más que eso no lo pagamos |
| **Horas que podemos dedicarles** | Nuestra área de tecnologías de la información dedica unas 160 horas al mes al proceso que van a auditar, entre sus 4 personas. No pueden pedirle más tiempo que ese |
| **Presupuesto que aprobamos** | S/ 13 268, a tarifa de referencia de S/ 110 la hora de supervisión, S/ 85 la de jefe de comisión y S/ 60 la de integrante, sin viáticos. Si necesitan ir a nuestras sedes fuera de Tacna, los pasajes y viáticos se presupuestan aparte |
| **Confidencialidad** | Todo lo que les entregamos es confidencial. Lo guardan en un repositorio privado, cifrado, con la marca CONFIDENCIAL — USO ACADÉMICO, y al cierre conservan solo lo que el informe cite |
| **Lo que no autorizamos** | Ninguna prueba se ejecuta sobre nuestros sistemas en esta etapa. Lo que pedimos es un plan. Si el plan incluye pruebas, dirá cuáles y nos pedirá autorización escrita antes |
| **Las personas** | En su plan y en su informe nos nombran por el cargo, no por el nombre |

## 7. Lo que les entregamos

Lo que sigue lo entregamos **a solicitud escrita**, indicando para qué lo necesitan y qué procedimiento lo va a usar. Los documentos propios de esta materia van ya como anexos de esta solicitud. Los demás se entregan por el canal único, en la carpeta que indica la tabla.

| Documento | Qué contiene | Dónde está |
|---|---|---|
| `ciclo-de-vida-del-software.md` | El expediente de nuestro software propio, con las métricas del repositorio, los despliegues y los pedidos de cambio del periodo | Anexo 1 |
| `contratos-proveedores.md` | Lo que dicen nuestros contratos sobre la propiedad del código y el soporte | [`documentos/contratos-proveedores.md`](../../../CASOS/EMPRESA-06-distribuidora-andina-sur/documentos/contratos-proveedores.md) |
| `extracciones-y-registros.md` | Las extracciones del sistema principal y la bitácora que conservamos | [`documentos/extracciones-y-registros.md`](../../../CASOS/EMPRESA-06-distribuidora-andina-sur/documentos/extracciones-y-registros.md) |
| `narrativa-proceso-compras.md` | Cómo opera el proceso que nuestro software soporta o alimenta | [`documentos/narrativa-proceso-compras.md`](../../../CASOS/EMPRESA-06-distribuidora-andina-sur/documentos/narrativa-proceso-compras.md) |
| `organigrama-y-accesos.md` | Quién desarrolla, quién despliega y quién aprueba, según los accesos | [`documentos/organigrama-y-accesos.md`](../../../CASOS/EMPRESA-06-distribuidora-andina-sur/documentos/organigrama-y-accesos.md) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/usuarios_erp.csv` | Los usuarios de nuestro sistema principal, con perfil, último acceso y segundo factor | 119 registros · 119 habilitados · 119 sin segundo factor |
| `datos/pagos.csv` | Nuestros pagos del periodo | 17798 registros · S/ 26 668 856 en total |

Atentamente,

**Gerente General, por acuerdo de la Junta General de Accionistas**
DISTRIBUIDORA ANDINA DEL SUR S.A.C.

---

## Anexos

### Anexo 1 · `ciclo-de-vida-del-software.md`

### 1. El sistema desarrollado internamente

| Campo | Contenido |
|---|---|
| Sistema | **Portal de pedidos para clientes** |
| Descripción | Desarrollo propio, publicado en un hosting compartido |
| En producción desde | 2022 |
| Lenguaje y plataforma | PHP 7.4 y MariaDB |
| Personas que lo mantienen hoy | 2 |
| ¿Existe documentación técnica? | No |
| ¿Existe control de versiones? | Sí, repositorio interno |
| ¿Existe ambiente de pruebas separado de producción? | Sí, pero con datos de producción copiados |

> **Contexto que da la organización.** «Lo desarrolló un practicante en 2022. Ya no trabaja aquí. Desde entonces se le hacen ajustes cuando algo falla o cuando el área pide un cambio.»

### 2. Métricas del repositorio

Extraídas con `git log` sobre el periodo auditado.

| Métrica | Valor |
|---|---|
| Commits en el periodo | 262 |
| Autores distintos | 3 |
| Commits del autor principal | 63 % del total |
| Ramas activas | 8 |
| Ramas sin fusionar con más de 90 días | 1 |
| Commits directos a la rama principal | **86 %** |
| Pull Requests abiertos en el periodo | 3 |
| Pull Requests con revisión de un segundo | **3** |
| Etiquetas de versión creadas | 0 |
| Commits con mensaje de una sola palabra | 30 |
| Archivos con más de 1 000 líneas | 2 |
| ¿Hay pruebas automatizadas en el repositorio? | No |

### 3. Últimos despliegues a producción

| Fecha | Versión | Qué se desplegó | ¿Hubo etiqueta? | ¿Hubo prueba previa? | ¿Se pudo revertir? |
|---|---|---|---|---|---|
| 2025-06-19 | — | Cambio de formato de comprobante | No | No | No |
| 2025-03-22 | v1.4 | Ajuste de cálculo | Sí | No | No |
| 2025-04-08 | v1.8 | Ajuste de cálculo | Sí | No | Sí |
| 2025-05-18 | — | Corrección de error en reportes | No | No | Sí |
| 2025-04-13 | — | Nuevo campo solicitado por el área | No | Parcial | Sí |
| 2025-08-22 | v1.2 | Cambio de formato de comprobante | Sí | Parcial | No |

### 4. Trazabilidad de requisitos

La organización entrega los pedidos de cambio del periodo, tal como los registra.

| N.º | Fecha | Solicitado por | Qué se pidió | ¿Especificación escrita? | ¿Aceptación formal? | ¿Se desplegó? |
|---|---|---|---|---|---|---|
| 01 | 2025-06-04 | Tesorería | Ampliar el campo de observaciones | No | No | No |
| 02 | 2025-09-16 | Administración y Finanzas | Ampliar el campo de observaciones | No | No | Sí |
| 03 | 2025-11-22 | Logística | Agregar un filtro al reporte | No | No | Sí |
| 04 | 2025-04-23 | Legal | Ampliar el campo de observaciones | Correo | No | Sí |
| 05 | 2025-03-21 | Contabilidad | Corregir el redondeo | No | No | No |
| 06 | 2025-04-27 | Operaciones | Corregir el redondeo | No | No | Sí |
| 07 | 2025-07-27 | Almacén | Exportar a hoja de cálculo | Correo | Verbal | Sí |
| 08 | 2025-03-03 | Legal | Cambiar el cálculo del descuento | No | No | No |

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

[Semana 09](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 09·05](CASO-09-05-transportes-sur-andino.md) · **Caso 09·06** · [Caso 09·07](CASO-09-07-instituto-vertiente-sur.md) · [Encargo 09](../../ENCARGOS-UNIDAD-II/CASO-09-ciclo-de-vida-del-software.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
