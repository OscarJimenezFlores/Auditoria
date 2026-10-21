[Semana 09](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 09·07](CASO-09-07-instituto-vertiente-sur.md) · **Caso 09·08** · [Caso 09·09](CASO-09-09-servicios-mineros-cordillera.md) · [Encargo 09](../../ENCARGOS-UNIDAD-II/CASO-09-ciclo-de-vida-del-software.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>EPS AGUAS DEL SUR S.A.</strong><br>
  <em>Solicitud de auditoría · Ciclo de vida del software</em>
</div>

---

# Solicitud de auditoría de el ciclo de vida de nuestro software

| | |
|---|---|
| **Documento** | Solicitud de auditoría de el ciclo de vida de nuestro software |
| **De** | Gerente General, EPS AGUAS DEL SUR S.A. |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 12 de octubre de 2026 |
| **Clasificación** | CONFIDENCIAL — USO ACADÉMICO |

---

## 1. Quiénes somos

Somos **EPS AGUAS DEL SUR S.A.**, servicio de agua potable y alcantarillado, con sede en Tacna. Funcionamos desde hace 44 años, con 312 trabajadores estables y 58 por servicios. Nuestro presupuesto institucional es de S/ 74.1 millones y atendemos 86 000 conexiones domiciliarias.

Nos regulan o supervisan **SUNASS · OTASS · ANA · Contraloría General · PCM-SGTD · ANPD**. Somos una entidad pública, sujeta al gobierno digital y al control gubernamental.

Nuestra área de tecnologías de la información tiene **6 personas**. La encabeza nuestro jefe del Departamento de Tecnologías de la Información, que reporta a Gerencia de Administración. El presupuesto de tecnologías de la información es de **S/ 1 080 000**, el 1.46 % de nuestros ingresos. El objetivo que le declaramos a esa área es «Segmentar la red industrial y dar trazabilidad al ciclo comercial ante el regulador».

**Lo que más nos cuesta.** La red del SCADA de plantas comparte switches con la red administrativa desde una ampliación hecha en 2023, pese a que el diseño original las separaba.

### 1.1. Los sistemas con los que operamos

| Sistema | Qué es | Dónde corre | Desde | ¿Tiene soporte vigente? |
|---|---|---|---|---|
| **Sistema comercial** | Producto del sector saneamiento: catastro, facturación y cobranza | Servidor propio | 2014 | Sí |
| **SCADA de plantas y reservorios** | Sistema del proveedor de automatización | Red industrial separada | 2019 | Sí |
| **Micromedición y lectura** | Terminales portátiles del proveedor | Mixto | 2018 | Sí |
| **SIAF y patrimonio** | Sistemas del MEF | Cliente local | 2010 | MEF |
| **Atención de reclamos** | Formulario web y hoja de cálculo | Hosting propio | 2021 | No |

### 1.2. Nuestros procesos

1. Catastro comercial de usuarios
2. Lectura de medidores y facturación
3. Cobranza y corte/reconexión
4. Atención de reclamos comerciales
5. Operación de plantas y redes
6. Contrataciones y presupuesto público

## 2. Por qué pedimos esta auditoría

El formulario web de atención de reclamos y su proceso de carga los desarrolló un practicante que terminó en 2023. Con el procedimiento de SUNASS abierto, cada reclamo que se pierde es una sanción. El Órgano de Control Institucional nos recomendó conservar los archivos de carga del sistema comercial, y nadie puede decir qué código los procesa.

## 3. Lo que ya sabemos que no está bien

Estos riesgos los tenemos identificados y no los hemos tratado.

- Red industrial (SCADA) sin segmentación efectiva
- Sin trazabilidad del proceso de carga de lecturas
- **Doble marco.** Gobierno digital y regulación sectorial, ninguno cubierto por completo

**Lo que nos pasó en el periodo. Reclamo masivo por facturación estimada.** Un fallo en la carga de lecturas dejó tres ciclos de facturación estimados para 11 200 conexiones. SUNASS abrió procedimiento. No se pudo determinar qué lote de lecturas falló porque el sistema no conserva el archivo de carga original.

## 4. Lo que ya nos dijeron

- El Órgano de Control Institucional nos emitió en 2025 un informe sobre el proceso de facturación estimada, con dos recomendaciones. Conservar los archivos de carga de lecturas y segmentar la red del SCADA. Ambas abiertas.
- SUNASS tiene abierto un procedimiento por los tres ciclos de facturación estimada a 11 200 conexiones.
- OTASS evaluó nuestra gestión en 2025 y registró la ausencia de un Plan de Gobierno Digital.

## 5. Lo que queremos saber

Son las preguntas que la dirección espera que la auditoría responda. Cómo responderlas, con qué alcance, con qué criterios y con qué procedimientos, es lo que esperamos de su plan.

1. Saber si el formulario de reclamos cumple lo que el reglamento de reclamos de SUNASS exige, requisito por requisito.
2. Saber si la recomendación del Órgano de Control Institucional sobre los archivos de carga apunta a software nuestro o al producto del proveedor.
3. Saber si con seis personas en el Departamento podemos separar quien desarrolla de quien despliega.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | Pedimos este servicio de control al Órgano de Control Institucional, con conocimiento del Directorio y de OTASS |
| **Contraparte designada** | Nuestro Gerente de Administración, de quien depende el Departamento de Tecnologías de la Información |
| **Canal único** | Toda solicitud entra y sale por la mesa de partes institucional y el correo del Órgano de Control Institucional, con número de expediente por cada solicitud |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 19 de octubre de 2026. Trabajo de campo del 20 de octubre de 2026 al 9 de noviembre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 10 de noviembre de 2026 y el 16 de noviembre de 2026. Informe entre el 17 de noviembre de 2026 y el 23 de noviembre de 2026 |
| **Horas que financiamos** | Hasta 222 horas de la comisión. Unas 44 de planificación, 133 de trabajo de campo, 18 de comunicación de resultados y 27 de informe. Más que eso no lo pagamos |
| **Horas que podemos dedicarles** | Nuestra área de tecnologías de la información dedica unas 240 horas al mes al proceso que van a auditar, entre sus 6 personas. No pueden pedirle más tiempo que ese |
| **Presupuesto que aprobamos** | S/ 16 095, a tarifa de referencia de S/ 110 la hora de supervisión, S/ 85 la de jefe de comisión y S/ 60 la de integrante, sin viáticos |
| **Confidencialidad** | Todo lo que les entregamos es confidencial. Lo guardan en un repositorio privado, cifrado, con la marca CONFIDENCIAL — USO ACADÉMICO, y al cierre conservan solo lo que el informe cite |
| **Lo que no autorizamos** | Ninguna prueba se ejecuta sobre nuestros sistemas en esta etapa. Lo que pedimos es un plan. Si el plan incluye pruebas, dirá cuáles y nos pedirá autorización escrita antes |
| **Las personas** | En su plan y en su informe nos nombran por el cargo, no por el nombre |

## 7. Lo que les entregamos

Lo que sigue lo entregamos **a solicitud escrita**, indicando para qué lo necesitan y qué procedimiento lo va a usar. Los documentos propios de esta materia van ya como anexos de esta solicitud. Los demás se entregan por el canal único, en la carpeta que indica la tabla.

| Documento | Qué contiene | Dónde está |
|---|---|---|
| `ciclo-de-vida-del-software.md` | El expediente de nuestro software propio, con las métricas del repositorio, los despliegues y los pedidos de cambio del periodo | Anexo 1 |
| `contratos-proveedores.md` | Lo que dicen nuestros contratos sobre la propiedad del código y el soporte | [`documentos/contratos-proveedores.md`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/documentos/contratos-proveedores.md) |
| `extracciones-y-registros.md` | Las extracciones del sistema principal y la bitácora que conservamos | [`documentos/extracciones-y-registros.md`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/documentos/extracciones-y-registros.md) |
| `narrativa-proceso-compras.md` | Cómo opera el proceso que nuestro software soporta o alimenta | [`documentos/narrativa-proceso-compras.md`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/documentos/narrativa-proceso-compras.md) |
| `organigrama-y-accesos.md` | Quién desarrolla, quién despliega y quién aprueba, según los accesos | [`documentos/organigrama-y-accesos.md`](../../../CASOS/EMPRESA-08-eps-aguas-del-sur/documentos/organigrama-y-accesos.md) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/usuarios_erp.csv` | Los usuarios de nuestro sistema principal, con perfil, último acceso y segundo factor | 199 registros · 199 habilitados · 199 sin segundo factor |
| `datos/pagos.csv` | Nuestros pagos del periodo | 19281 registros · S/ 28 844 992 en total |

Atentamente,

**Gerente General**
EPS AGUAS DEL SUR S.A.

---

## Anexos

### Anexo 1 · `ciclo-de-vida-del-software.md`

### 1. El sistema desarrollado internamente

| Campo | Contenido |
|---|---|
| Sistema | **Atención de reclamos** |
| Descripción | Formulario web y proceso de carga a la hoja de cálculo de reclamos, desarrollados internamente |
| En producción desde | 2021 |
| Lenguaje y plataforma | PHP 7 y MySQL |
| Personas que lo mantienen hoy | 2 |
| ¿Existe documentación técnica? | No |
| ¿Existe control de versiones? | Sí, repositorio interno |
| ¿Existe ambiente de pruebas separado de producción? | Sí, pero con datos de producción copiados |

> **Contexto que da la organización.** «Lo desarrolló un practicante del departamento de TI que terminó sus prácticas en 2023. Desde entonces se le hacen ajustes cuando algo falla o cuando el área pide un cambio.»

### 2. Métricas del repositorio

Extraídas con `git log` sobre el periodo auditado.

| Métrica | Valor |
|---|---|
| Commits en el periodo | 240 |
| Autores distintos | 3 |
| Commits del autor principal | 70 % del total |
| Ramas activas | 6 |
| Ramas sin fusionar con más de 90 días | 4 |
| Commits directos a la rama principal | **84 %** |
| Pull Requests abiertos en el periodo | 8 |
| Pull Requests con revisión de un segundo | **2** |
| Etiquetas de versión creadas | 3 |
| Commits con mensaje de una sola palabra | 51 |
| Archivos con más de 1 000 líneas | 6 |
| ¿Hay pruebas automatizadas en el repositorio? | No |

### 3. Últimos despliegues a producción

| Fecha | Versión | Qué se desplegó | ¿Hubo etiqueta? | ¿Hubo prueba previa? | ¿Se pudo revertir? |
|---|---|---|---|---|---|
| 2025-05-25 | v1.8 | Cambio de formato de comprobante | No | No | No |
| 2025-02-09 | v1.6 | Corrección urgente en producción | No | Parcial | No |
| 2025-09-06 | v1.5 | Nuevo campo solicitado por el área | No | No | No |
| 2025-11-16 | v1.8 | Nuevo campo solicitado por el área | Sí | No | No |
| 2025-01-15 | — | Cambio de formato de comprobante | No | No | Sí |
| 2025-08-20 | v1.8 | Nuevo campo solicitado por el área | No | No | No |

### 4. Trazabilidad de requisitos

La organización entrega los pedidos de cambio del periodo, tal como los registra.

| N.º | Fecha | Solicitado por | Qué se pidió | ¿Especificación escrita? | ¿Aceptación formal? | ¿Se desplegó? |
|---|---|---|---|---|---|---|
| 01 | 2025-10-16 | Logística | Corregir el redondeo | No | No | Sí |
| 02 | 2025-02-12 | Gerencia | Bloquear la edición tras el cierre | No | No | No |
| 03 | 2025-10-26 | Recursos Humanos | Permitir anular un registro | No | Verbal | No |
| 04 | 2025-09-08 | Comercial | Corregir el redondeo | No | Verbal | Sí |
| 05 | 2025-03-05 | Recursos Humanos | Corregir el redondeo | Correo | No | No |
| 06 | 2025-11-27 | Recursos Humanos | Ampliar el campo de observaciones | Correo | Verbal | Sí |
| 07 | 2025-02-07 | Legal | Bloquear la edición tras el cierre | No | No | Sí |
| 08 | 2025-11-11 | Operaciones | Permitir anular un registro | No | No | Sí |

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

[Semana 09](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 09·07](CASO-09-07-instituto-vertiente-sur.md) · **Caso 09·08** · [Caso 09·09](CASO-09-09-servicios-mineros-cordillera.md) · [Encargo 09](../../ENCARGOS-UNIDAD-II/CASO-09-ciclo-de-vida-del-software.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
