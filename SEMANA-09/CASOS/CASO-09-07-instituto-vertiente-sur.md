[Semana 09](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 09·06](CASO-09-06-distribuidora-andina-sur.md) · **Caso 09·07** · [Caso 09·08](CASO-09-08-eps-aguas-del-sur.md) · [Encargo 09](../../ENCARGOS-UNIDAD-II/CASO-09-ciclo-de-vida-del-software.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

<div align="center">
  <strong>INSTITUTO SUPERIOR TECNOLÓGICO VERTIENTE SUR</strong><br>
  <em>Solicitud de auditoría · Ciclo de vida del software</em>
</div>

---

# Solicitud de auditoría de el ciclo de vida de nuestro software

| | |
|---|---|
| **Documento** | Solicitud de auditoría de el ciclo de vida de nuestro software |
| **De** | Director General, por acuerdo del Consejo Directivo, INSTITUTO SUPERIOR TECNOLÓGICO VERTIENTE SUR |
| **Para** | La comisión auditora que recibe este encargo |
| **Fecha** | 12 de octubre de 2026 |
| **Clasificación** | CONFIDENCIAL — USO ACADÉMICO |

---

## 1. Quiénes somos

Somos **INSTITUTO SUPERIOR TECNOLÓGICO VERTIENTE SUR**, educación superior tecnológica privada, con sede en Tacna. Operamos desde hace 16 años, con 88 trabajadores estables y 112 docentes por horas. Nuestros ingresos son de S/ 19.7 millones y atendemos 3 240 estudiantes en 7 carreras.

Nos regulan o supervisan **MINEDU · SUNEDU (para programas conducentes) · ANPD · SUNAT**.

Nuestra área de tecnologías de la información tiene **3 personas**. La encabeza nuestro coordinador de TI, que reporta a Dirección General. El presupuesto de tecnologías de la información es de **S/ 356 000**, el 1.81 % de nuestros ingresos. El objetivo que le declaramos a esa área es «Profesionalizar la administración de los sistemas académicos y asegurar la integridad de las actas».

**Lo que más nos cuesta.** El Moodle lo administra un docente de la carrera de computación, sin contrato de TI, sin respaldos programados y con acceso de administrador compartido con dos estudiantes practicantes.

### 1.1. Los sistemas con los que operamos

| Sistema | Qué es | Dónde corre | Desde | ¿Tiene soporte vigente? |
|---|---|---|---|---|
| **Sistema académico** | Producto para institutos, matrícula, notas y certificados | Servidor propio | 2017 | Sí |
| **Aula virtual** | Moodle autoalojado | Servidor propio | 2020 | Administrado por un docente |
| **Cobranzas y tesorería** | Módulo del sistema académico | Mismo servidor | 2017 | Sí |
| **Correo y ofimática** | Suite en nube, licencias educativas | Nube | 2019 | Proveedor |
| **Biblioteca** | Software libre, instalado en 2018 | PC de biblioteca | 2018 | No |

### 1.2. Nuestros procesos

1. Admisión y matrícula
2. Programación académica y carga docente
3. Registro de evaluaciones y actas
4. Cobranza de pensiones
5. Titulación y certificación
6. Bienestar y seguimiento estudiantil

## 2. Por qué pedimos esta auditoría

El módulo de reportes y certificados del sistema académico lo desarrolló un docente de la carrera de computación, que sigue dictando y lo mantiene sin contrato de TI. Los certificados que firma nuestro Director General salen de ese código. MINEDU nos pidió un informe sobre los controles del sistema académico y no pudimos decir quién cambia el software ni cómo.

## 3. Lo que ya sabemos que no está bien

Estos riesgos los tenemos identificados y no los hemos tratado.

- Administración de un sistema crítico por personal sin responsabilidad formal
- Sin autenticación reforzada en el sistema de notas
- Datos de menores de edad en algunos programas, sin tratamiento diferenciado

**Lo que nos pasó en el periodo. Alteración de notas en el sistema académico.** Se detectaron 17 modificaciones de notas fuera del periodo de registro, hechas con la cuenta de un docente que estaba de licencia. El sistema no exige segundo factor y la contraseña era la fecha de nacimiento del docente.

## 4. Lo que ya nos dijeron

- MINEDU supervisó en 2025 el registro de actas y notas, a raíz de la alteración detectada, y nos pidió un informe sobre los controles de acceso al sistema académico. Respondimos con un oficio sin evidencia técnica.
- Nunca nos han auditado el sistema académico ni el aula virtual.
- Nuestra licencia de funcionamiento ante MINEDU está vigente y no fue afectada.

## 5. Lo que queremos saber

Son las preguntas que la dirección espera que la auditoría responda. Cómo responderlas, con qué alcance, con qué criterios y con qué procedimientos, es lo que esperamos de su plan.

1. Saber si los certificados y los reportes a MINEDU que produce el módulo son exactos, y qué garantiza que lo sean.
2. Saber si está bien que el docente que mantiene el código sea el mismo que califica a los estudiantes cuyas notas procesa.
3. Saber qué proceso de desarrollo puede sostener un Coordinador de TI con dos personas, sin exigirnos una empresa de software.

## 6. Cómo trabajaremos con ustedes

| | |
|---|---|
| **Cómo se dispuso** | El Consejo Directivo lo pidió tras la alteración de notas y la Dirección General lo formalizó por resolución |
| **Contraparte designada** | Nuestro Director General, con el Coordinador de TI y el Secretario Académico como enlaces |
| **Canal único** | Toda solicitud entra y sale por el correo de la Dirección General, con copia a Secretaría Académica |
| **Plazo de respuesta** | Respondemos cada solicitud de información en tres días hábiles. Si no lo hacemos, pueden escalar a la contraparte y, al segundo incumplimiento, a quien firma este documento |
| **Plazo que proponemos** | Que el plan esté aprobado el 19 de octubre de 2026. Trabajo de campo del 20 de octubre de 2026 al 9 de noviembre de 2026. Reunión de cierre con acta y nuestra respuesta entre el 10 de noviembre de 2026 y el 16 de noviembre de 2026. Informe entre el 17 de noviembre de 2026 y el 23 de noviembre de 2026 |
| **Horas que financiamos** | Hasta 161 horas de la comisión. Unas 32 de planificación, 97 de trabajo de campo, 13 de comunicación de resultados y 19 de informe. Más que eso no lo pagamos |
| **Horas que podemos dedicarles** | Nuestra área de tecnologías de la información dedica unas 120 horas al mes al proceso que van a auditar, entre sus 3 personas. No pueden pedirle más tiempo que ese |
| **Presupuesto que aprobamos** | S/ 11 672, a tarifa de referencia de S/ 110 la hora de supervisión, S/ 85 la de jefe de comisión y S/ 60 la de integrante, sin viáticos |
| **Confidencialidad** | Todo lo que les entregamos es confidencial. Lo guardan en un repositorio privado, cifrado, con la marca CONFIDENCIAL — USO ACADÉMICO, y al cierre conservan solo lo que el informe cite |
| **Lo que no autorizamos** | Ninguna prueba se ejecuta sobre nuestros sistemas en esta etapa. Lo que pedimos es un plan. Si el plan incluye pruebas, dirá cuáles y nos pedirá autorización escrita antes |
| **Las personas** | En su plan y en su informe nos nombran por el cargo, no por el nombre |

## 7. Lo que les entregamos

Lo que sigue lo entregamos **a solicitud escrita**, indicando para qué lo necesitan y qué procedimiento lo va a usar. Los documentos propios de esta materia van ya como anexos de esta solicitud. Los demás se entregan por el canal único, en la carpeta que indica la tabla.

| Documento | Qué contiene | Dónde está |
|---|---|---|
| `ciclo-de-vida-del-software.md` | El expediente de nuestro software propio, con las métricas del repositorio, los despliegues y los pedidos de cambio del periodo | Anexo 1 |
| `contratos-proveedores.md` | Lo que dicen nuestros contratos sobre la propiedad del código y el soporte | [`documentos/contratos-proveedores.md`](../../../CASOS/EMPRESA-07-instituto-vertiente-sur/documentos/contratos-proveedores.md) |
| `extracciones-y-registros.md` | Las extracciones del sistema principal y la bitácora que conservamos | [`documentos/extracciones-y-registros.md`](../../../CASOS/EMPRESA-07-instituto-vertiente-sur/documentos/extracciones-y-registros.md) |
| `narrativa-proceso-compras.md` | Cómo opera el proceso que nuestro software soporta o alimenta | [`documentos/narrativa-proceso-compras.md`](../../../CASOS/EMPRESA-07-instituto-vertiente-sur/documentos/narrativa-proceso-compras.md) |
| `organigrama-y-accesos.md` | Quién desarrolla, quién despliega y quién aprueba, según los accesos | [`documentos/organigrama-y-accesos.md`](../../../CASOS/EMPRESA-07-instituto-vertiente-sur/documentos/organigrama-y-accesos.md) |

**Los datos del periodo**, con su tamaño, para que dimensionen sus procedimientos. Están tal como los tenemos.

| Archivo | Qué es | Tamaño |
|---|---|---|
| `datos/usuarios_erp.csv` | Los usuarios de nuestro sistema principal, con perfil, último acceso y segundo factor | 69 registros · 69 habilitados · 69 sin segundo factor |
| `datos/pagos.csv` | Nuestros pagos del periodo | 6013 registros · S/ 9 184 974 en total |

Atentamente,

**Director General, por acuerdo del Consejo Directivo**
INSTITUTO SUPERIOR TECNOLÓGICO VERTIENTE SUR

---

## Anexos

### Anexo 1 · `ciclo-de-vida-del-software.md`

### 1. El sistema desarrollado internamente

| Campo | Contenido |
|---|---|
| Sistema | **Reportes y certificados del sistema académico** |
| Descripción | Módulo desarrollado internamente sobre la base del sistema académico, que genera las constancias, los certificados y los reportes a MINEDU |
| En producción desde | 2019 |
| Lenguaje y plataforma | PHP 7 y MySQL |
| Personas que lo mantienen hoy | 1 |
| ¿Existe documentación técnica? | Parcial, desactualizada |
| ¿Existe control de versiones? | Sí, repositorio interno |
| ¿Existe ambiente de pruebas separado de producción? | Sí, pero con datos de producción copiados |

> **Contexto que da la organización.** «Lo desarrolló un docente de la carrera de computación, que sigue dictando y lo mantiene sin contrato de TI. Desde entonces se le hacen ajustes cuando algo falla o cuando el área pide un cambio.»

### 2. Métricas del repositorio

Extraídas con `git log` sobre el periodo auditado.

| Métrica | Valor |
|---|---|
| Commits en el periodo | 266 |
| Autores distintos | 4 |
| Commits del autor principal | 83 % del total |
| Ramas activas | 2 |
| Ramas sin fusionar con más de 90 días | 3 |
| Commits directos a la rama principal | **71 %** |
| Pull Requests abiertos en el periodo | 6 |
| Pull Requests con revisión de un segundo | **1** |
| Etiquetas de versión creadas | 2 |
| Commits con mensaje de una sola palabra | 47 |
| Archivos con más de 1 000 líneas | 7 |
| ¿Hay pruebas automatizadas en el repositorio? | No |

### 3. Últimos despliegues a producción

| Fecha | Versión | Qué se desplegó | ¿Hubo etiqueta? | ¿Hubo prueba previa? | ¿Se pudo revertir? |
|---|---|---|---|---|---|
| 2025-07-08 | — | Nuevo campo solicitado por el área | No | No | Sí |
| 2025-02-17 | v1.7 | Cambio de formato de comprobante | No | No | Sí |
| 2025-08-13 | — | Cambio de formato de comprobante | No | No | Sí |
| 2025-09-23 | v1.1 | Corrección urgente en producción | Sí | No | Sí |
| 2025-11-07 | v1.3 | Corrección urgente en producción | Sí | No | Sí |
| 2025-04-27 | v1.8 | Ajuste de cálculo | No | No | Sí |

### 4. Trazabilidad de requisitos

La organización entrega los pedidos de cambio del periodo, tal como los registra.

| N.º | Fecha | Solicitado por | Qué se pidió | ¿Especificación escrita? | ¿Aceptación formal? | ¿Se desplegó? |
|---|---|---|---|---|---|---|
| 01 | 2025-09-25 | Tecnologías de la Información | Corregir el redondeo | No | No | Sí |
| 02 | 2025-01-23 | Administración y Finanzas | Agregar un filtro al reporte | No | Verbal | No |
| 03 | 2025-03-08 | Logística | Cambiar el cálculo del descuento | No | No | Sí |
| 04 | 2025-06-02 | Almacén | Nuevo reporte mensual | No | No | No |
| 05 | 2025-06-14 | Recursos Humanos | Ampliar el campo de observaciones | No | Verbal | Sí |
| 06 | 2025-06-13 | Almacén | Permitir anular un registro | No | Verbal | Sí |
| 07 | 2025-09-21 | Tesorería | Exportar a hoja de cálculo | Correo | Verbal | No |
| 08 | 2025-03-04 | Tesorería | Ampliar el campo de observaciones | No | Verbal | No |

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

[Semana 09](../README.md) · [Taller](../3-TALLER.md) · [Los casos de la semana](README.md) · [Caso 09·06](CASO-09-06-distribuidora-andina-sur.md) · **Caso 09·07** · [Caso 09·08](CASO-09-08-eps-aguas-del-sur.md) · [Encargo 09](../../ENCARGOS-UNIDAD-II/CASO-09-ciclo-de-vida-del-software.md) · [Modelo del plan](../../MODELO-PLAN-DE-AUDITORIA.md)

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
