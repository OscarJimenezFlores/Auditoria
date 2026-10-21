[Semana 15](README.md) · [Teoría](1-TEORIA.md) · [Dinámica de aula](2-DINAMICA.md) · **Taller de laboratorio**

# Semana 15

## Auditoría del plan de continuidad con BIA, RTO, RPO y prueba de restauración

**SI-084 - Auditoría de Sistemas** - Sesión 2 en laboratorio · calificación **procedimental**

> ¿Un término no le resulta claro? Está definido en el [glosario técnico del curso](../GLOSARIO.md).

---

## Qué entregas

| | |
|---|---|
| **Archivo** | `SI084-S15-TALLER-Grupo<N>.pdf` |
| **Plantilla obligatoria** | [SI084-PLANTILLA-TALLER.docx](../PLANTILLAS/SI084-PLANTILLA-TALLER.docx) |
| **Formato** | PDF exportado desde la plantilla en Word, con la carátula de la UPT, el índice actualizado y las capturas numeradas |
| **Qué va dentro** | Las secciones de la plantilla. La **5. Resultados y evidencias** se califica contra la tabla de resultados esperados de esta guía, y **cada resultado necesita la evidencia que lo demuestre**. No se copian de aquí los objetivos, la duración ni los resultados de aprendizaje |
| **Dónde se sube** | Aula virtual, tarea «Taller · Semana 15» |
| **Cuándo vence** | Según lo programado en el aula virtual |

> No se califica un informe entregado en `.docx`, sin carátula, sin los códigos de los integrantes o con resultados declarados sin evidencia.

---

## 1. Información sobre el evento práctico

### 1.1. Título del evento práctico

Auditoría del sistema de gestión de continuidad del negocio de la organización conforme a la ISO 22301:2019, con verificación de la coherencia de los objetivos temporales y ejecución de una prueba real de restauración que mide el tiempo efectivo de recuperación.

### 1.2. Objetivos

- Auditar la existencia, vigencia y calidad del **BIA (*Business Impact Analysis*, análisis de impacto al negocio)**, verificando que se construyó por actividad de negocio.
- Verificar la **coherencia matemática** de los objetivos temporales — RPO, RTO, MTPD y MBCO.
- Auditar la **arquitectura de respaldo** contra la regla 3-2-1 extendida, con foco en la copia inmutable.
- Evaluar el **programa de ejercicios y pruebas** exigido por la cláusula 8.5.
- **Ejecutar una prueba real de restauración**, medir el tiempo efectivo y contrastarlo con el RTO declarado.
- Verificar la existencia de **autoridad definida para activar el plan** y del plan de comunicación de crisis.
- Producir el **hallazgo de continuidad** con evidencia de la prueba.

### 1.3. Resultados de Aprendizaje (RA)

- **RA1** Diseña y aplica estrategias para los diversos tipos de auditoría de sistemas.
- **RA2** Descubre la importancia y diferencia entre auditor interno y externo.

### 1.4. Recursos

| Recurso | Detalle |
|---|---|
| **ISO 22301:2019** | https://www.iso.org/standard/75106.html |
| **ISO/IEC 27031** — preparación TIC para la continuidad | https://www.iso.org/standard/83507.html |
| **restic** | https://restic.net/ — respaldo con verificación e inmutabilidad |
| **Duplicati** | https://duplicati.com/ — alternativa con interfaz gráfica |
| **MinIO** | https://min.io/ — almacenamiento compatible S3 con *object lock* para probar inmutabilidad |
| Entorno `si084-lab` | Base de datos `si084_db` como sistema a restaurar |
| Documentos de la empresa | BCP, DRP, BIA, política de respaldo, actas de simulacro |
| **Python 3.11+** | Verificación de coherencia y análisis |

### 1.5. Seguridad

1. **La prueba de restauración se ejecuta exclusivamente en un ambiente aislado**, nunca sobre producción. Restaurar sobre producción puede destruir datos vigentes.
2. Se coordina con TI de la empresa **por escrito**, indicando fecha, hora, sistema y aislamiento. Si la empresa no autoriza, la prueba se ejecuta sobre el entorno de laboratorio y se documenta la limitación de alcance.
3. Los respaldos de la empresa pueden contener datos personales — si se manipulan, se aplican las medidas del registro de tratamiento de la Semana 11 y se destruyen al terminar, dejando acta.
4. La prueba debe poder **abortarse en cualquier momento** sin efecto sobre la operación.

---

## 2. Procedimiento o Metodología

> **Documento del caso para esta semana.** La organización entrega **Política de respaldo y el BIA vigente**, en `CASOS/EMPRESA-<NN>-<slug>/documentos/politica-de-respaldo.md`. Es consistente con los datos de `datos/`. Las personas, usuarios y proveedores que menciona existen en los archivos. **No señala sus debilidades**; declara lo que la organización dice hacer.

### Paso A — Auditar el BIA

`30_papeles_trabajo/PT15-01_bia.md`:

| Proc. | Objetivo de control | Criterio | Procedimiento | Excepción |
|---|---|---|---|---|
| **C-01** | Existe un BIA vigente | ISO 22301:2019, 8.2.2 | Solicitar el BIA; verificar fecha de elaboración y de última revisión | No existe, o antigüedad > 12 meses sin revisión |
| **C-02** | El BIA se construyó por **actividad de negocio** | ISO 22301:2019, 8.2.2 | Revisar la unidad de análisis del BIA | El BIA lista sistemas o servidores en lugar de actividades |
| **C-03** | Participó el negocio, no solo TI | ISO 22301:2019, 5.3, 7.4 | Revisar la lista de participantes y las actas de los talleres del BIA | Elaborado exclusivamente por TI |
| **C-04** | El impacto se evalúa **en el tiempo** y en varias dimensiones | ISO 22301:2019, 8.2.2 | Verificar que existan horizontes temporales y las dimensiones financiera, operativa, legal y reputacional | Impacto evaluado en un solo momento o en una sola dimensión |
| **C-05** | Cada actividad tiene MTPD, RTO, RPO y MBCO | ISO 22301:2019, 8.2.2 | Revisar la tabla de objetivos temporales | Actividad crítica sin objetivos definidos |
| **C-06** | Los objetivos son **coherentes** | ISO 22301:2019, 8.2.2 y 8.3 | Ejecutar el verificador de coherencia | RTO ≥ MTPD, o RPO mayor que la frecuencia real de respaldo |

```python
# 30_papeles_trabajo/PT15_coherencia.py
import pandas as pd

bia = pd.read_csv("../20_evidencia/E15_bcp/bia_empresa.csv")
# columnas · actividad, mtpd_h, rto_h, rpo_h, mbco, frecuencia_respaldo_h, estrategia_actual, rto_real_h

print("=== VERIFICACIÓN DE COHERENCIA DE OBJETIVOS TEMPORALES ===\n")
for _, a in bia.iterrows():
    p = []
    if a.rto_h >= a.mtpd_h:
        p.append(f"CRÍTICO: RTO ({a.rto_h} h) ≥ MTPD ({a.mtpd_h} h) → el plan NO PROTEGE la actividad")
    if a.rpo_h < a.frecuencia_respaldo_h:
        p.append(f"CRÍTICO: RPO declarado ({a.rpo_h} h) es MENOR que la frecuencia real de "
                 f"respaldo ({a.frecuencia_respaldo_h} h) → el RPO es inalcanzable")
    if pd.notna(a.get("rto_real_h")) and a.rto_real_h > a.rto_h:
        p.append(f"El RTO real medido ({a.rto_real_h} h) excede el declarado ({a.rto_h} h) "
                 f"en {a.rto_real_h - a.rto_h:.1f} h")
    if pd.isna(a.mbco) or str(a.mbco).strip() == "":
        p.append("Sin MBCO definido: no se sabe qué nivel mínimo de servicio se debe sostener")
    print(f"{a.actividad}\n   MTPD {a.mtpd_h} h | RTO {a.rto_h} h | RPO {a.rpo_h} h")
    print("   " + ("✔ Coherente" if not p else "\n   ".join("✗ " + x for x in p)) + "\n")

criticos = bia[bia.rto_h >= bia.mtpd_h]
print(f"RESUMEN: {len(criticos)} de {len(bia)} actividades con plan que no protege.")
```

### Paso B — Auditar la arquitectura de respaldo

| Proc. | Objetivo | Criterio | Procedimiento | Excepción |
|---|---|---|---|---|
| **C-07** | Existen al menos 3 copias | Regla 3-2-1; ISO/IEC 27001:2022 A.8.13 | Inventariar las copias existentes por sistema crítico | Menos de 3 copias |
| **C-08** | En al menos 2 medios distintos | Regla 3-2-1 | Verificar la tecnología de cada copia | Todas en el mismo medio |
| **C-09** | Al menos 1 copia fuera de sitio | Regla 3-2-1 · A.8.13 | Verificar ubicación física o región de nube | Todas en la misma ubicación |
| **C-10** | **Al menos 1 copia inmutable o fuera de línea** | A.5.30 · buenas prácticas anti-ransomware | Verificar *object lock*, WORM o desconexión física | Todas las copias accesibles con credenciales de red |
| **C-11** | Los respaldos están cifrados | A.8.24 | Verificar el cifrado en reposo y la custodia de la clave | Sin cifrado, o clave almacenada junto al respaldo |
| **C-12** | La restauración se **verifica** periódicamente | ISO 22301:2019, 8.5 · A.8.13 | Solicitar las actas de verificación del periodo | Ninguna verificación en 12 meses |

**Demostración de inmutabilidad con MinIO** (prueba de concepto en laboratorio):

```bash
# Almacenamiento compatible S3 con object lock activado
docker run -d --name si084_minio -p 127.0.0.1:9000:9000 -p 127.0.0.1:9001:9001 \
  -e MINIO_ROOT_USER=labadmin -e MINIO_ROOT_PASSWORD=lab_si084 \
  quay.io/minio/minio server /data --console-address ":9001"

docker run --rm --network host -it --entrypoint sh minio/mc -c '
  mc alias set lab http://127.0.0.1:9000 labadmin lab_si084
  mc mb --with-lock lab/respaldos
  mc retention set --default GOVERNANCE 30d lab/respaldos
  mc retention info lab/respaldos
'
```

Se verifica que un objeto bajo retención **no puede eliminarse** antes del plazo, y se documenta como evidencia de qué significa «copia inmutable».

### Paso C — Prueba real de restauración

**El procedimiento de mayor fuerza probatoria de toda la auditoría.**

```bash
mkdir -p 20_evidencia/E15_bcp/prueba && cd 20_evidencia/E15_bcp/prueba

export RESTIC_REPOSITORY=$HOME/respaldo_si084
export RESTIC_PASSWORD='lab-si084'
R="docker run --rm -v $HOME/respaldo_si084:/repo -v $PWD:/datos \
   -e RESTIC_REPOSITORY=/repo -e RESTIC_PASSWORD=lab-si084 restic/restic"

# --- T0 · inicio del cronómetro (el RTO se mide desde la decisión de restaurar) ---
T0=$(date -u +%s); echo "T0 = $(date -u -Iseconds)" | tee acta_tiempos.txt

# 1. Identificar el punto de restauración disponible (determina el RPO REAL)
$R snapshots | tee snapshots.txt
ULTIMO=$($R snapshots --json | python3 -c "import json,sys;print(json.load(sys.stdin)[-1]['time'])")
echo "Último punto de restauración: $ULTIMO" | tee -a acta_tiempos.txt

# 2. Restaurar
$R restore latest --target /datos/restaurado
T1=$(date -u +%s); echo "T1 restauración de archivos = $(date -u -Iseconds)" | tee -a acta_tiempos.txt

# 3. Reconstruir el servicio en ambiente AISLADO
docker run -d --name si084_db_dr --network none \
  -e POSTGRES_USER=erp_app -e POSTGRES_PASSWORD=dr_test_2026 -e POSTGRES_DB=erp postgres:16
sleep 15
docker cp restaurado/datos/erp_*.sql si084_db_dr:/tmp/dump.sql
docker exec si084_db_dr psql -U erp_app -d erp -f /tmp/dump.sql > carga.log 2>&1
T2=$(date -u +%s); echo "T2 servicio operativo = $(date -u -Iseconds)" | tee -a acta_tiempos.txt

# 4. Verificar que el servicio es FUNCIONAL, no solo que arrancó
docker exec si084_db_dr psql -U erp_app -d erp -c "\dt" | tee verificacion_tablas.txt
docker exec si084_db_dr psql -U erp_app -d erp \
  -c "SELECT COUNT(*) AS registros FROM pagos;" | tee verificacion_datos.txt
T3=$(date -u +%s); echo "T3 verificación funcional = $(date -u -Iseconds)" | tee -a acta_tiempos.txt

# --- Resultados ---
{
 echo ""
 echo "RTO REAL MEDIDO"
 echo "  Restauración de archivos : $((T1-T0)) s"
 echo "  Servicio operativo       : $((T2-T0)) s"
 echo "  Verificación funcional   : $((T3-T0)) s  <-- este es el RTO real"
 echo "  Total en horas           : $(python3 -c "print(f'{($T3-$T0)/3600:.2f}')") h"
} | tee -a acta_tiempos.txt

# 5. Integridad del dato restaurado
sha256sum restaurado/datos/*.sql | tee hash_restaurado.txt

# 6. Limpieza obligatoria del ambiente de prueba
docker rm -f si084_db_dr
```

**Acta de prueba de restauración** (`30_papeles_trabajo/PT15-02_acta_restauracion.md`):

| Campo | Valor |
|---|---|
| Sistema restaurado | |
| Fecha y hora de inicio (UTC) | |
| Autorizado por (cargo) | |
| Ambiente utilizado | Aislado — `--network none` |
| Punto de restauración disponible | |
| **RPO real** (diferencia entre el punto disponible y el momento de la disrupción simulada) | |
| RPO declarado en el BIA | |
| **RTO real medido** (hasta verificación funcional) | |
| RTO declarado en el BIA | |
| **Desviación** | |
| Verificación de integridad (hash) | Coincide / No coincide |
| Verificación funcional | Tablas presentes: ___ · Registros verificados: ___ |
| Incidencias durante la prueba | |
| **Conclusión sobre la eficacia operativa del control** | |
| Ambiente de prueba eliminado | Sí — evidencia adjunta |

> **Distinción crítica.** El cronómetro se detiene en **T3, verificación funcional**, no en T1. Muchas organizaciones miden el RTO hasta que los archivos están copiados, lo que subestima el tiempo real en un factor de dos o tres. Un servicio que arrancó pero no responde consultas **no está recuperado**.

### Paso D — Gobierno de la crisis y programa de ejercicios

| Proc. | Objetivo | Criterio | Excepción |
|---|---|---|---|
| **C-13** | Existe autoridad definida para **activar** el plan | ISO 22301:2019, 5.3 y 8.4.2 | El plan no identifica quién declara la crisis, o depende de una sola persona sin suplente |
| **C-14** | Existe plan de comunicación de crisis con destinatarios y canales | ISO 22301:2019, 8.4.3 | Sin plan, o sin canal alternativo si falla el correo corporativo |
| **C-15** | El personal con rol en el plan lo conoce | ISO 22301:2019, 7.2 y 7.3 | Sin registros de capacitación en 12 meses |
| **C-16** | Existe **programa de ejercicios** planificado y ejecutado | ISO 22301:2019, 8.5 | Ningún ejercicio en 12 meses |
| **C-17** | Los ejercicios generan acciones correctivas con seguimiento | ISO 22301:2019, 8.5 y 10.1 | Actas de ejercicio sin acciones, o acciones sin cierre |
| **C-18** | Los **proveedores críticos** tienen requisitos de continuidad contractuales | ISO 22301:2019, 8.3.4 · A.5.22 | Proveedor crítico sin compromiso de continuidad en contrato |

**Hallazgo de continuidad** (`40_hallazgos/H-1xx.md`), sostenido en el acta de restauración, con la comparación RTO real vs. declarado, MTPD y el efecto de negocio cuantificado con el impacto del BIA.

```bash
cd ../../.. && sha256sum 20_evidencia/E15_bcp/prueba/* >> 20_evidencia/SHA256SUMS_E15.txt
git add . && git commit -m "E15: auditoria de continuidad, BIA, arquitectura de respaldo y prueba de restauracion"
```

---

### Paso E — Validar y corregir

El resultado no vale por estar hecho, sino por resistir una comprobación. Se ejecutan estas tres y **se corrige lo que falle antes de cerrar la sesión**.

1. Comprobar que los cuatro tiempos T0–T3 están registrados y que el RTO se midió **hasta la verificación funcional**, no hasta que el proceso terminó.
2. Verificar que el veredicto sobre copia inmutable o fuera de línea es explícito, con la demostración práctica que lo sostiene.
3. Revisar que el ambiente de prueba se eliminó y que hay evidencia de ello.

> Lo que no se pueda corregir hoy se anota en la sección **Problemas y mejoras** de la evidencia, con lo que faltó y por qué. Un resultado parcial documentado con honestidad vale más que uno declarado sin prueba.

### Paso F — Registrar la evidencia y cerrar

Se versiona lo producido, se anota la URL de cada resultado y se responde en dos frases la pregunta de transferencia — **qué riesgo correría una organización real si esto se hiciera mal**.

---

## 3. Resultados

> **Evidencia obligatoria en GitHub.** Todo resultado de este taller se versiona en el repositorio del equipo. El informe **no consigna capturas sueltas**. Consigna la **URL** del artefacto en GitHub. Una captura no permite verificar autoría, fecha ni contenido; un enlace sí.
>
> | Qué se entrega | Dónde vive | Qué se escribe en el informe |
> |---|---|---|
> | Código y archivos de configuración | Rama del taller, fusionada a `develop` vía Pull Request | URL del Pull Request |
> | Documentos y matrices | `docs/`, en formato de texto versionable | URL del archivo en la rama |
> | Capturas y videos que el taller exija | `docs/evidencias/S15/` | URL del archivo |
> | Salida de comandos | `docs/evidencias/S15/salidas/*.txt` | URL del archivo |
>
> **Etiqueta del taller.** Al cerrar el taller se crea la etiqueta `taller-15` sobre el commit entregado:
>
> ```bash
> git tag -a taller-15 -m "Taller 15 · SI084"
> git push origin taller-15
> ```
>
> La URL que se consigna en el informe apunta a esa etiqueta:
> `https://github.com/<organizacion>/<repositorio>/tree/taller-15`
>
> **El informe es lo que se califica; el repositorio es lo que lo prueba.** Cada resultado de la sección 3 del informe lleva la URL con la que se verifica, y **un resultado sin su URL se califica como no logrado**, por bien redactado que esté. Lo que no se puede abrir no se puede dar por hecho.

### 3.1. Los tres resultados que se califican

Son los que la rúbrica evalúa. El resto de la lista tiene que existir, pero no se califica fila por fila.

| Resultado | Qué demuestra | Dónde está |
|---|---|---|
| **El RTO real medido** | Los cuatro tiempos registrados y el contraste con el declarado | `acta_tiempos.txt` y acta de restauración |
| **El RPO real determinado** | El punto de restauración disponible, contrastado con el declarado | Acta de restauración |
| **El veredicto sobre inmutabilidad** | Explícito, con la demostración con *object lock* | Procedimiento C-10 y salida de `mc retention` |

### 3.2. Lista de comprobación del taller

Todo esto debe existir al cerrar la sesión.

| # | Resultado esperado | Verificación |
|---|---|---|
| 1 | Procedimientos C-01 a C-06 ejecutados sobre el BIA de la empresa, con veredicto | `PT15-01_bia.md` |
| 2 | Verificador de coherencia ejecutado, con las actividades cuyo **RTO ≥ MTPD** identificadas | Salida de `PT15_coherencia.py` |
| 3 | Auditoría de la arquitectura de respaldo C-07 a C-12 con inventario de copias por sistema crítico | Papel de trabajo |
| 4 | Veredicto explícito sobre la existencia de **copia inmutable o fuera de línea** | Procedimiento C-10 |
| 5 | Demostración práctica de inmutabilidad con MinIO *object lock* | Captura y salida de `mc retention` |
| 6 | **Prueba de restauración ejecutada** en ambiente aislado, con los cuatro tiempos T0–T3 registrados | `acta_tiempos.txt` |
| 7 | **RTO real medido hasta verificación funcional**, contrastado con el declarado | Acta de restauración |
| 8 | **RPO real** determinado por el punto de restauración disponible, contrastado con el declarado | Acta de restauración |
| 9 | Verificación de integridad por hash y verificación funcional del servicio restaurado | `hash_restaurado.txt`, `verificacion_datos.txt` |
| 10 | Ambiente de prueba eliminado, con evidencia | Salida del comando de limpieza |
| 11 | Procedimientos C-13 a C-18 con veredicto sobre gobierno de la crisis y ejercicios | Papel de trabajo |
| 12 | Hallazgo de continuidad con efecto cuantificado a partir del impacto del BIA | `40_hallazgos/` |
| 13 | Hashes y *commit* en Git | `SHA256SUMS_E15.txt` |

## Rúbrica procedimental (20 puntos)

Se aplica sobre el informe entregado y la evidencia enlazada en el repositorio. **Cada criterio se califica de forma independiente.**

| Criterio | 4 — Logrado | 2 — En proceso | 0 — Insuficiente |
|---|---|---|---|
| **Auditar el BIA** | Completo y correcto, con la evidencia que lo respalda | Completo con errores menores, o correcto pero sin toda la evidencia | Incompleto, o entregado sin ejecutar |
| **Prueba real de restauración** | Completo y correcto, con la evidencia que lo respalda | Completo con errores menores, o correcto pero sin toda la evidencia | Incompleto, o entregado sin ejecutar |
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

1. El RTO declarado en un plan de continuidad es una hipótesis hasta que se ejecuta una prueba de restauración y se mide el tiempo real; la brecha entre ambos es sistemáticamente mayor de lo que la organización supone.
2. Un BIA construido desde los sistemas produce requisitos técnicos sin justificación de negocio; construido desde la actividad, produce requisitos que la gerencia puede defender y financiar.
3. Frente al ransomware, la cantidad de copias es irrelevante si todas son alcanzables con credenciales de red. La copia inmutable o fuera de línea es la única que sobrevive al escenario más probable.

## 5. Referencias Bibliográficas

- ISO 22301:2019. *Security and resilience — Business continuity management systems — Requirements*. https://www.iso.org/standard/75106.html
- ISO 22313:2020. *Business continuity management systems — Guidance on the usa of ISO 22301*. https://www.iso.org/standard/75107.html
- ISO/IEC 27031. *Guidelines for ICT readiness for business continuity*. https://www.iso.org/standard/83507.html
- ISO/IEC 27001:2022, Anexo A, controles A.5.22, A.5.29, A.5.30, A.8.13, A.8.14, A.8.24. https://www.iso.org/standard/27001
- ISACA. (2018). *COBIT 2019*, objetivo **DSS04 Managed Continuity**. https://www.isaca.org/resources/cobit
- Resolución SBS N.º 504-2021 y modificatorias — gestión de la continuidad en entidades supervisadas. https://www.sbs.gob.pe/
- Business Continuity Institute. *Good Practice Guidelines*. https://www.thebci.org/
- restic. *restic Documentation*. https://restic.readthedocs.io/
- MinIO. *Object Locking and Retention*. https://min.io/docs/minio/linux/administration/object-management/object-retention.html
- Piattini Velthuis, M., Del Peso Navarro, E. y Del Peso Ruiz, M. (2009). *Auditoría de tecnologías y sistemas de información* (6.ª ed.). Alfaomega / Ra-Ma. Capítulo de continuidad.

## 6. Anexos

- `anexo_A_bia_auditado.xlsx` — BIA con la verificación de coherencia.
- `anexo_B_acta_restauracion.pdf` — acta firmada con los cuatro tiempos.
- `anexo_C_arquitectura_respaldo.png` — diagrama de las copias existentes contra la regla 3-2-1 extendida.
- `anexo_D_inmutabilidad_minio.pdf` — evidencia de la demostración de *object lock*.
- `anexo_E_autorizacion_prueba.pdf` — autorización escrita de la empresa o declaración de limitación de alcance.

---

---

[Semana 15](README.md) · [Teoría](1-TEORIA.md) · [Dinámica de aula](2-DINAMICA.md) · **Taller de laboratorio**

---

**Docente** · Dr. Oscar Juan Jimenez Flores
[oscarjimenezflores@upt.pe](mailto:oscarjimenezflores@upt.pe) · [LinkedIn](https://www.linkedin.com/in/oscar-jimenez-flores/) · [CTI Vitae — CONCYTEC](https://ctivitae.concytec.gob.pe/appDirectorioCTI/VerDatosInvestigador.do?id_investigador=33398)

Escuela Profesional de Ingeniería de Sistemas · Universidad Privada de Tacna · Tacna, Perú
