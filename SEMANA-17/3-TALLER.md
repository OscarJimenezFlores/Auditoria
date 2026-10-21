[Semana 17](README.md) · [Teoría](1-TEORIA.md) · [Dinámica de aula](2-DINAMICA.md) · **Taller de laboratorio**

# Semana 17

## Cierre del encargo, expediente y seguimiento de recomendaciones

**SI-084 - Auditoría de Sistemas** - Sesión 2 en laboratorio · calificación **procedimental**

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](../GLOSARIO.md).

---

## Qué entregas

| | |
|---|---|
| **Archivo** | `SI084-S17-TALLER-Grupo<N>.pdf` |
| **Plantilla obligatoria** | [SI084-PLANTILLA-TALLER.docx](../PLANTILLAS/SI084-PLANTILLA-TALLER.docx) |
| **Formato** | PDF exportado desde la plantilla en Word, con la carátula de la UPT, el índice actualizado y las capturas numeradas |
| **Qué va dentro** | Las secciones de la plantilla. La **5. Resultados y evidencias** se califica contra la tabla de resultados esperados de esta guía, y **cada resultado necesita la evidencia que lo demuestre**. No se copian de aquí los objetivos, la duración ni los resultados de aprendizaje |
| **Dónde se sube** | Aula virtual, tarea «Taller · Semana 17» |
| **Cuándo vence** | Según lo programado en el aula virtual. El plazo se cuenta desde la sesión de laboratorio de la semana, se desarrolle el taller dentro de ella o fuera de ella |

> No se califica un informe entregado en `.docx`, sin carátula, sin los códigos de los integrantes o con resultados declarados sin evidencia.

---

## 1. Información sobre el evento práctico

### 1.1. Título del evento práctico

Cierre formal del encargo de auditoría de sistemas — entrega del expediente completo con su índice de referencias, ejecución del acta de cierre y destino de la información, diseño del programa de seguimiento de recomendaciones y evaluación de la calidad del propio encargo.

### 1.2. Objetivos

- **Ensamblar el expediente completo** del encargo con su índice de referencias cruzadas.
- Verificar la **integridad de la cadena de custodia** de toda la evidencia acumulada en el semestre.
- Ejecutar el **acta de cierre** y documentar el destino de la información conforme a la carta de encargo.
- Diseñar el **programa de seguimiento** de las recomendaciones con hitos, criterios de cierre y protocolo de escalamiento.
- Realizar la **autoevaluación de la calidad del encargo** conforme a los lineamientos de aseguramiento de la calidad.
- Producir el documento de **lecciones aprendidas** que alimenta el siguiente ciclo de auditoría.

### 1.3. Resultados de Aprendizaje (RA)

- **RA1** Diseña y aplica estrategias para los diversos tipos de auditoría de sistemas.
- **RA2** Descubre la importancia y diferencia entre auditor interno y externo.

### 1.4. Recursos

| Recurso | Detalle |
|---|---|
| Expediente completo | Repositorio del equipo, semanas 01 a 16 |
| **ISO 19011:2018**, cláusulas 6.6 y 6.7 | https://www.iso.org/standard/70017.html |
| **ITAF (ISACA)** — aseguramiento de la calidad y seguimiento | https://www.isaca.org/resources/frameworks-standards-and-models |
| **Python 3.11+**, **Pandoc**, **Git** | Verificación, ensamblaje y versionado |
| **GanttProject** o **LibreOffice Calc** | Programa de seguimiento |

### 1.5. Seguridad

1. El **destino de la información** se ejecuta según lo pactado en la carta de encargo. Devolución o destrucción certificada. Se deja acta firmada.
2. La destrucción de información digital exige **borrado seguro**, no simple eliminación. Se documenta el método empleado.
3. El repositorio del equipo permanece **privado** de forma indefinida. Se prohíbe hacerlo público, aunque el curso haya concluido.
4. Los papeles de trabajo se conservan por el plazo de retención acordado; nunca se eliminan antes de que la organización cierre las recomendaciones.

---

## 2. Procedimiento o Metodología

### Paso A — Verificar la integridad del expediente

```python
# 30_papeles_trabajo/PT17_integridad_expediente.py
import hashlib, glob, os, re, pathlib

BASE = "../.."
print("=== VERIFICACIÓN DE LA CADENA DE CUSTODIA ===\n")

registrados = {}
for l in open(f"{BASE}/20_evidencia/CADENA_DE_CUSTODIA.md"):
    c = [x.strip() for x in l.split("|")]
    if len(c) > 4 and c[1].startswith("E"):
        registrados[c[2]] = c[3]          # archivo -> hash registrado

ok = alterados = faltantes = 0
for archivo, h_reg in registrados.items():
    rutas = glob.glob(f"{BASE}/20_evidencia/**/{archivo}", recursive=True)
    if not rutas:
        print(f"  ✗ FALTANTE : {archivo}"); faltantes += 1; continue
    h_act = hashlib.sha256(open(rutas[0], "rb").read()).hexdigest()
    if h_act == h_reg: ok += 1
    else:
        print(f"  ✗ ALTERADO : {archivo}\n      registrado {h_reg[:16]}…  actual {h_act[:16]}…")
        alterados += 1

print(f"\nÍntegros {ok} | Alterados {alterados} | Faltantes {faltantes}")
print("VEREDICTO:", "cadena de custodia ÍNTEGRA ✔" if not (alterados or faltantes)
      else "cadena de custodia COMPROMETIDA — documentar la causa de cada excepción")

print("\n=== COMPLETITUD DEL EXPEDIENTE ===")
EXIGIDOS = {
 "00_administracion": ["carta_encargo","independencia","confidencialidad","acta_apertura"],
 "10_planificacion":  ["PLAN_ANUAL","PLAN_INTEGRAL","programa_trabajo","pbc"],
 "20_evidencia":      ["CADENA_DE_CUSTODIA","SHA256SUMS"],
 "30_papeles_trabajo":["PT13","PT14","PT15","PT16"],
 "40_hallazgos":      ["H-1","ACTA_VALIDACION"],
 "50_informe":        ["INFORME_FINAL","seguimiento","CARTA_DISTRIBUCION"],
}
for carpeta, claves in EXIGIDOS.items():
    todo = " ".join(os.listdir(f"{BASE}/{carpeta}")) if os.path.isdir(f"{BASE}/{carpeta}") else ""
    for k in claves:
        print(f"  {'✔' if k.lower() in todo.lower() else '✗ FALTA'}  {carpeta}/{k}")

print("\n=== TRAZABILIDAD GLOBAL ===")
inf = open(f"{BASE}/50_informe/INFORME_COMPLETO.md").read()
hall = {pathlib.Path(f).stem for f in glob.glob(f"{BASE}/40_hallazgos/H-*.md")}
en_inf = set(re.findall(r"H-\d+", inf))
print(f"  Hallazgos redactados: {len(hall)} | en el informe: {len(en_inf & hall)}")
print(f"  No incorporados al informe: {sorted(hall - en_inf) or 'ninguno ✔'}")
```

### Paso B — Índice de referencias y ensamblaje final

`50_informe/INDICE_EXPEDIENTE.md` — el documento que permite a un revisor externo navegar el encargo:

| Ref. | Documento | Carpeta | Semana | Vinculado a | SHA-256 |
|---|---|---|---|---|---|
| ADM-01 | Carta de encargo | `00_administracion` | 08 | Todo el encargo | |
| ADM-02 | Declaraciones de independencia | `00_administracion` | 08 | ADM-01 | |
| ADM-03 | Acta de apertura | `00_administracion` | 08 | ADM-01 | |
| PL-01 | Los seis planes de auditoría de la Unidad II | `10_planificacion` | 07 a 12 | ADM-01 | |
| PL-02 | Programa de trabajo | `10_planificacion` | 08 | PT13-x | |
| PL-03 | Plan Integral v2.0 | `10_planificacion` | 12 | PL-01, PL-02 | |
| E-xx | Evidencia | `20_evidencia` | 01–15 | PT-xx | |
| PT-xx | Papeles de trabajo | `30_papeles_trabajo` | 13–16 | H-xxx | |
| H-xxx | Hallazgos | `40_hallazgos` | 13–15 | INF-01 Sección 4 | |
| VAL-01 | Acta de validación | `40_hallazgos` | 16 | H-xxx | |
| INF-01 | **Informe Final** | `50_informe` | 16 | Todo | |
| SEG-01 | Matriz de seguimiento | `50_informe` | 16 | INF-01 Sección 7 | |
| DIS-01 | Carta de distribución | `50_informe` | 16 | INF-01 | |
| CIE-01 | Acta de cierre | `00_administracion` | 17 | Todo | |

```bash
# Empaquetado del expediente completo, con verificación
cd .. && tar -czf EXPEDIENTE_AUDITORIA_SI084_<equipo>.tar.gz \
  00_administracion 10_planificacion 20_evidencia 30_papeles_trabajo 40_hallazgos 50_informe
sha256sum EXPEDIENTE_AUDITORIA_SI084_<equipo>.tar.gz | tee EXPEDIENTE.sha256
git add . && git commit -m "CIERRE: expediente completo del encargo de auditoria"
git tag -a cierre-encargo -m "Cierre formal del encargo — SI-084 "
```

### Paso C — Acta de cierre y destino de la información

`00_administracion/ACTA_CIERRE.md`:

```markdown
# Acta de Cierre del Encargo de Auditoría de Sistemas

| Campo | Contenido |
|---|---|
| Organización auditada | |
| Encargo | Auditoría de sistemas — periodo ___ a ___ |
| Fecha de la reunión de cierre | |
| Asistentes (cargos) | |

## 1. Resultados presentados
Hallazgos por severidad: Crítico ___ · Alto ___ · Medio ___ · Bajo ___
Conclusión general comunicada: <transcripción>

## 2. Respuesta de la administración
| Hallazgo | Acepta | Responsable (cargo) | Plazo comprometido | Observación |
|---|---|---|---|---|

## 3. Discrepancias que persisten
| Hallazgo | Posición del auditor | Posición de la administración | Riesgo residual y quién lo asume |
|---|---|---|---|

## 4. Destino de la información
- [ ] Devolución de la información entregada por la organización — fecha: ____
- [ ] Destrucción certificada mediante borrado seguro — método: ____ — fecha: ____
- [ ] Conservación de los papeles de trabajo por ___ años, conforme a la cláusula ___ de la carta de encargo
- Responsable de la custodia durante el plazo de retención: ____

## 5. Seguimiento acordado
Primera verificación: ____ · Responsable: ____ · Alcance: recomendaciones críticas y altas

## 6. Evaluación del encargo por la organización auditada
| Aspecto | 1–5 | Comentario |
|---|---|---|
| Claridad de la comunicación | | |
| Pertinencia de los hallazgos | | |
| Utilidad de las recomendaciones | | |
| Profesionalismo del equipo | | |
| Interferencia con la operación | | |

## 7. Firmas
_____________________     _____________________
Auditor responsable        Representante de la organización
```

### Paso D — Programa de seguimiento

`50_informe/PROGRAMA_SEGUIMIENTO.csv`:

| ID | Recomendación | Severidad | Responsable | Plazo comprometido | Fecha de verificación | Criterio de cierre | Procedimiento de verificación | Estado | Escalamiento si vence |
|---|---|---|---|---|---|---|---|---|---|
| R-01 | | Crítico | | +30 d | +35 d | Conciliación con cero excepciones | Reejecutar el CAAT PT13-01 sobre datos actualizados | Abierto | Comité de auditoría a los 15 d de vencido |
| R-02 | | Crítico | | +60 d | +65 d | Acta de prueba con RTO < MTPD | Solicitar acta y verificar tiempos | Abierto | Comité de auditoría |
| R-03 | | Alto | | +90 d | +95 d | Prueba fallida de eliminación anticipada | Solicitar evidencia de retención | Abierto | Gerencia General |

**Protocolo de escalamiento** (`50_informe/PROTOCOLO_ESCALAMIENTO.md`):

| Situación | Acción | Plazo | Destinatario |
|---|---|---|---|
| Recomendación crítica vencida sin avance | Comunicación formal al responsable | Inmediata | Responsable + su superior |
| Sin respuesta a los 15 días | Escalamiento al comité de auditoría | 15 d | Comité |
| Decisión de no implementar | **Registro formal de aceptación del riesgo residual, firmado por quien tiene autoridad para asumirlo** | Al momento de la decisión | Directorio |
| Recomendación implementada | Verificación conforme al criterio de cierre y **cierre formal** | Según cronograma | Responsable + comité |

### Paso E — Autoevaluación de la calidad y lecciones aprendidas

`30_papeles_trabajo/PT17_autoevaluacion.md`:

| # | Criterio de calidad del encargo | Sí / No / Parcial | Evidencia | Acción de mejora |
|---|---|---|---|---|
| 1 | ¿El alcance se cumplió íntegramente? | | | |
| 2 | ¿Todos los procedimientos del programa se ejecutaron? | | | |
| 3 | ¿Cada conclusión se sostiene en evidencia trazable? | | | |
| 4 | ¿Se respetó la independencia durante todo el encargo? | | | |
| 5 | ¿Los hallazgos se validaron antes de emitirlos? | | | |
| 6 | ¿El informe se emitió dentro del plazo comprometido? | | | |
| 7 | ¿Se mantuvo la confidencialidad en todo momento? | | | |
| 8 | ¿La cadena de custodia está íntegra? | | | |
| 9 | ¿Se documentaron las limitaciones al alcance? | | | |
| 10 | ¿El equipo tuvo la competencia necesaria para todo lo auditado? | | | |
| 11 | ¿Se usaron herramientas de IA? ¿Se verificó toda su salida? | | | |
| 12 | ¿El expediente permite que un tercero reejecute el encargo? | | | |

`50_informe/LECCIONES_APRENDIDAS.md`:

| Categoría | Qué funcionó | Qué no funcionó | Qué haríamos distinto |
|---|---|---|---|
| Planificación | | | |
| Acceso a la información | | | |
| Ejecución de pruebas | | | |
| Uso de herramientas | | | |
| Comunicación con el auditado | | | |
| Redacción del informe | | | |
| Trabajo en equipo | | | |

**Insumo para el siguiente ciclo.** Las tres materias de control que este encargo dejó fuera de cobertura y que deberían encabezar el programa de auditoría del periodo siguiente, con la justificación derivada de lo observado durante el trabajo de campo.

```bash
git add . && git commit -m "CIERRE: acta, seguimiento, autoevaluacion y lecciones aprendidas"
git tag -a curso-completo -m "SI-084 Auditoria de Sistemas  — expediente final"
git log --oneline --decorate --graph | head -25
```

---

### Paso F — Validar y corregir

El resultado no vale por estar hecho, sino por resistir una comprobación. Se ejecutan estas tres y **se corrige lo que falle antes de cerrar la sesión**.

1. Ejecutar el verificador sobre **toda** la evidencia del semestre y documentar cada excepción con su causa.
2. Comprobar que no queda ningún hallazgo redactado que no se haya incorporado al informe.
3. Verificar que el destino de la información está decidido y documentado, con método de destrucción cuando corresponda.

> Lo que no se pueda corregir hoy se anota en la sección **Problemas y mejoras** de la evidencia, con lo que faltó y por qué. Un resultado parcial documentado con honestidad vale más que uno declarado sin prueba.

### Paso G — Registrar la evidencia y cerrar

Se versiona lo producido, se anota la URL de cada resultado y se responde en dos frases la pregunta de transferencia — **qué riesgo correría una organización real si esto se hiciera mal**.

---

## 3. Resultados

> **Evidencia obligatoria en GitHub.** Todo resultado de este taller se versiona en el repositorio del equipo. El informe **no consigna capturas sueltas**. Consigna la **URL** del artefacto en GitHub. Una captura no permite verificar autoría, fecha ni contenido; un enlace sí.
>
> | Qué se entrega | Dónde vive | Qué se escribe en el informe |
> |---|---|---|
> | Código y archivos de configuración | Rama del taller, fusionada a `develop` vía Pull Request | URL del Pull Request |
> | Documentos y matrices | `docs/`, en formato de texto versionable | URL del archivo en la rama |
> | Capturas y videos que el taller exija | `docs/evidencias/S17/` | URL del archivo |
> | Salida de comandos | `docs/evidencias/S17/salidas/*.txt` | URL del archivo |
>
> **Etiqueta del taller.** Al cerrar el taller se crea la etiqueta `taller-17` sobre el commit entregado:
>
> ```bash
> git tag -a taller-17 -m "Taller 17 · SI084"
> git push origin taller-17
> ```
>
> La URL que se consigna en el informe apunta a esa etiqueta:
> `https://github.com/<organizacion>/<repositorio>/tree/taller-17`
>
> **El informe es lo que se califica; el repositorio es lo que lo prueba.** Cada resultado de la sección 3 del informe lleva la URL con la que se verifica, y **un resultado sin su URL se califica como no logrado**, por bien redactado que esté. Lo que no se puede abrir no se puede dar por hecho.

### 3.1. Los tres resultados que se califican

Son los que la rúbrica evalúa. El resto de la lista tiene que existir, pero no se califica fila por fila.

| Resultado | Qué demuestra | Dónde está |
|---|---|---|
| **La integridad del expediente** | El verificador ejecutado sobre todo el semestre, con veredicto | Salida de `PT17_integridad_expediente.py` |
| **El acta de cierre** | Las siete secciones, con el destino de la información decidido | `ACTA_CIERRE.md` |
| **El programa de seguimiento** | Criterio de cierre y procedimiento de verificación por recomendación | `PROGRAMA_SEGUIMIENTO.csv` |

### 3.2. Lista de comprobación del taller

Todo esto debe existir al cerrar la sesión.

| # | Resultado esperado | Verificación |
|---|---|---|
| 1 | Verificador de integridad ejecutado sobre **toda** la evidencia del semestre | Salida de `PT17_integridad_expediente.py` |
| 2 | Veredicto de cadena de custodia **íntegra**, o cada excepción documentada con su causa | Salida del verificador |
| 3 | Verificación de completitud del expediente. **Cero documentos faltantes** | Salida del verificador |
| 4 | **Cero hallazgos redactados que no fueron incorporados al informe** | Trazabilidad global |
| 5 | Índice de referencias cruzadas completo, con hash por documento | `INDICE_EXPEDIENTE.md` |
| 6 | Expediente empaquetado con su hash verificable | `EXPEDIENTE.sha256` |
| 7 | Acta de cierre con las siete secciones, incluida la evaluación de la organización | `ACTA_CIERRE.md` |
| 8 | **Destino de la información decidido y documentado**, con método de destrucción si aplica | Sección 4 del acta |
| 9 | Programa de seguimiento con criterio de cierre y **procedimiento de verificación** por recomendación | `PROGRAMA_SEGUIMIENTO.csv` |
| 10 | Protocolo de escalamiento con la figura de **aceptación formal del riesgo residual** | `PROTOCOLO_ESCALAMIENTO.md` |
| 11 | Autoevaluación de los 12 criterios de calidad, con acción de mejora en los no conformes | `PT17_autoevaluacion.md` |
| 12 | Lecciones aprendidas por las siete categorías | `LECCIONES_APRENDIDAS.md` |
| 13 | Tres materias de control propuestas para el programa del periodo siguiente, con justificación | `LECCIONES_APRENDIDAS.md` |
| 14 | Etiquetas `cierre-encargo` y `curso-completo` en Git | `git tag` |

## Rúbrica procedimental (20 puntos)

Se aplica sobre el informe entregado y la evidencia enlazada en el repositorio. **Cada criterio se califica de forma independiente.**

| Criterio | 4 — Logrado | 2 — En proceso | 0 — Insuficiente |
|---|---|---|---|
| **Verificar la integridad del expediente** | Completo y correcto, con la evidencia que lo respalda | Completo con errores menores, o correcto pero sin toda la evidencia | Incompleto, o entregado sin ejecutar |
| **Índice de referencias y ensamblaje final** | Completo y correcto, con la evidencia que lo respalda | Completo con errores menores, o correcto pero sin toda la evidencia | Incompleto, o entregado sin ejecutar |
| **Evidencia verificable en el repositorio** | Cada resultado tiene su URL sobre la etiqueta `taller-NN`, y el enlace abre lo que dice | La mayoría tiene URL; alguna evidencia es una captura suelta | Se declaran resultados sin enlace, o el enlace no corresponde |
| **Trazabilidad de la evidencia** | Todo hallazgo o dato se rastrea hasta el archivo, registro y fecha que lo sustenta | Rastreable en su mayoría; algún dato sin origen | Se afirman hechos sin poder ubicarlos en la evidencia |
| **La evidencia entregada** | Las secciones de la plantilla completas; los papeles de trabajo quedan archivados y referenciados | Secciones completas con papeles de trabajo incompletos | Faltan secciones o no hay papeles de trabajo |

| Puntaje | Equivalencia |
|---|---|
| 18 – 20 | Destacado |
| 14 – 17 | Logrado |
| 6 – 13 | En proceso |
| 0 – 5 | Insuficiente |

> **Un resultado declarado sin evidencia enlazada no se califica**, aunque el trabajo se haya hecho. La tabla de la sección 3.1 es la lista de cotejo; esta rúbrica es lo que determina la nota.

## 4. Conclusiones

Mínimo tres. Líneas argumentales esperadas:

1. Un encargo de auditoría no termina con la entrega del informe sino con el seguimiento de las recomendaciones. Sin verificación posterior, el informe documenta problemas en lugar de resolverlos.
2. La integridad verificable del expediente es lo que permite que un tercero —un regulador, un auditor externo, un tribunal— reconstruya el trabajo y llegue a la misma conclusión; sin ella, el informe vale lo que vale la palabra de quien lo firmó.
3. La aceptación formal del riesgo residual, firmada por quien tiene autoridad para asumirlo, es el mecanismo que transfiere la responsabilidad de la decisión desde el auditor hacia el órgano que efectivamente la toma.

## 5. Referencias Bibliográficas

- ISO 19011:2018, cláusulas 6.6 «Finalización de la auditoría» y 6.7 «Realización del seguimiento». https://www.iso.org/standard/70017.html
- ISACA. *ITAF: A Professional Practices Framework for IS Audit/Assurance* (5.ª ed.) — aseguramiento de la calidad, documentación y seguimiento. https://www.isaca.org/resources/frameworks-standards-and-models
- ISACA. *Code of Professional Ethics*. https://www.isaca.org/credentialing/code-of-professional-ethics
- The Institute of Internal Auditors. *Global Internal Audit Standards* — dominio de gestión de la calidad y seguimiento del progreso. https://www.theiia.org/en/standards/
- COSO (*Committee of Sponsoring Organizations of the Treadway Commission*). (2013). *Internal Control — Integrated Framework*. https://www.coso.org/guidance-on-ic
- ISO/IEC 27001:2022, control A.8.10 *Information deletion*. https://www.iso.org/standard/27001
- Ley 29733 y D. S. 016-2024-JUS — obligaciones de conservación y supresión de datos personales. https://www.gob.pe/institucion/anpd
- Contraloría General de la República del Perú. *Normas Generales de Control Gubernamental*. https://www.gob.pe/contraloria
- Piattini Velthuis, M., Del Peso Navarro, E. y Del Peso Ruiz, M. (2009). *Auditoría de tecnologías y sistemas de información* (6.ª ed.). Alfaomega / Ra-Ma.

## 6. Anexos

- `anexo_A_indice_expediente.pdf`
- `anexo_B_acta_cierre.pdf`
- `anexo_C_programa_seguimiento.xlsx`
- `anexo_D_autoevaluacion.pdf`
- `anexo_E_lecciones_aprendidas.pdf`
- `anexo_F_verificacion_integridad.pdf`

---

---

[Semana 17](README.md) · [Teoría](1-TEORIA.md) · [Dinámica de aula](2-DINAMICA.md) · **Taller de laboratorio**

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
