# Anexo — Caso simulado de respaldo: **DISTRIBUIDORA ANDINA DEL SUR S.A.C.**

> **Cuándo se usa.** Este caso sustituye a la empresa real cuando el equipo no consigue acceso confirmado a una organización, o cuando el acceso se pierde durante el semestre. Permite ejecutar íntegramente las semanas 07 a 17 sin perder continuidad ni evidencia.
>
> **Advertencia.** La organización descrita es **ficticia**. Cualquier coincidencia con una empresa existente es casual. Los datos, cifras y documentos son sintéticos y se generan con los scripts del anexo. **No debe presentarse como un caso real ante terceros.**

---

## 1. Ficha de la organización

| Campo | Valor |
|---|---|
| Razón social | Distribuidora Andina del Sur S.A.C. |
| RUC (ficticio) | 20###### (asignado por el docente) |
| Sector | Comercio al por mayor de productos de consumo masivo |
| Ámbito | Tacna, Moquegua y Arequipa |
| Antigüedad | Más de diez años de operación |
| Personal | 64 trabajadores (8 en administración, 22 en almacén y despacho, 26 en fuerza de ventas, 5 en TI, 3 en gerencia) |
| Ventas anuales | S/ 38 millones |
| Clientes | 8 400 bodegas y minoristas registrados |
| Proveedores | 47 activos, 6 de ellos concentran el 78 % del volumen |
| **Régimen regulatorio** | **Empresa privada no supervisada**. Le aplican: Ley 29733 y su Reglamento D. S. 016-2024-JUS, D. Leg. 822, normativa de SUNAT sobre comprobantes y libros electrónicos, Ley 27269. **No** le aplican la Res. SBS 504-2021 ni la normativa de la Contraloría |

## 2. Estructura y gobierno

```
                    Junta de Accionistas
                            │
                    Gerencia General
        ┌───────────────┬───┴────────────┬──────────────────┐
  Gerencia de       Gerencia de      Gerencia de       Gerencia de
   Finanzas          Ventas          Operaciones       Administración
        │                                                    │
   Contabilidad                                     Jefatura de TI  ← 5 personas
   Tesorería                                        RR. HH.
```

**Hechos de gobierno relevantes para la auditoría.**

- **No existe comité de TI.** Las decisiones tecnológicas las toma el Gerente de Administración con el Jefe de TI.
- El **Jefe de TI reporta a la Gerencia de Administración**; su presupuesto compite con gasto corriente.
- El directorio **no ha tratado riesgo tecnológico** en ninguna de las 11 actas de los últimos 24 meses.
- El plan estratégico vigente, con horizonte de cuatro años, declara «digitalizar el canal de venta al detalle» como objetivo prioritario.
- **No existe declaración de apetito de riesgo.**

## 3. Sistemas de información

| Sistema | Función | Proveedor / origen | Criticidad | Ubicación | Observaciones |
|---|---|---|---|---|---|
| **ERP Comercial** (módulos: Compras, Ventas, Inventarios, Contabilidad) | Núcleo transaccional | Producto empaquetado de proveedor local, en uso desde hace más de una década | Muy alta | Servidor físico en oficina principal, Tacna | 87 usuarios; sin contrato de soporte vigente |
| **Sistema de Planilla** | Remuneraciones y datos de salud ocupacional | Proveedor externo, servicio en la nube | Alta | Nube, región no verificada | Contiene **datos sensibles** |
| **Portal de pedidos B2B** | Pedidos de bodegas | desarrollo propio | Alta | VPS contratado en el extranjero | Expuesto a internet; sin pruebas de seguridad desde su lanzamiento |
| **Correo y ofimática** | Comunicación y documentos | Suite ofimática en la nube | Alta | **Servidores en el extranjero** | **Flujo transfronterizo** |
| **Hojas de cálculo de Gerencia Comercial** | Márgenes por cliente, presupuesto de ventas, comisiones | Elaboración propia | **Muy alta** | Carpeta compartida en la nube | Mantenidas por una sola analista; sin control de versiones ni respaldo de fórmulas |
| **WMS de almacén** | Gestión de inventario físico | Módulo del ERP + escáneres | Alta | Servidor local | Integración por archivo plano nocturno |

## 4. Situación de TI — hechos verificables para el diagnóstico

| Ámbito | Hecho |
|---|---|
| **Personal** | 5 personas: 1 jefe, 2 soporte, 1 desarrollador, 1 administrador de base de datos. El desarrollador es el único que conoce el portal B2B |
| **Documentación** | Política de Seguridad de la Información v1.2, aprobada hace más de cuatro años, sin revisión posterior. No existe procedimiento documentado de gestión de cambios |
| **Accesos** | 87 usuarios activos en el ERP; la nómina vigente es de 64 personas. Las bajas se ejecutan «cuando alguien avisa» |
| **Cambios** | 41 despliegues a producción en el último trimestre; 34 con aprobación registrada por correo. El desarrollador despliega su propio código |
| **Respaldo** | Copia diaria del ERP a un disco USB conectado permanentemente al servidor, más una copia semanal a la nube. **Ninguna copia inmutable o fuera de línea.** Última prueba de restauración documentada: hace más de dos años |
| **Continuidad** | **No existe BCP ni BIA.** El Jefe de TI declara un RTO de 4 horas «porque es lo que aguanta el almacén» |
| **Monitoreo** | Sin SIEM. Los registros del ERP se conservan 30 días y son editables por el DBA |
| **Vulnerabilidades** | Sin proceso de gestión de vulnerabilidades. El sistema operativo del servidor del ERP salió de soporte del fabricante |
| **Datos personales** | No existe inventario de bancos de datos ni registro de actividades de tratamiento. El aviso de privacidad del portal B2B es un texto genérico copiado de otra empresa |
| **Licenciamiento** | 71 instalaciones de una suite ofimática; 40 licencias adquiridas |
| **Incidentes (24 meses)** | (1) Caída del ERP de 9 horas por falla del disco, <mes/año>; (2) correo de un vendedor comprometido usado para solicitar cambio de cuenta bancaria a tres clientes, <mes/año>; (3) borrado accidental de la tabla de precios, recuperado desde respaldo en 6 horas, <mes/año> |

## 5. Presupuesto de TI (para la Semana 14)

| Categoría | Año anterior (S/) | Año en curso (S/) | Tipo |
|---|---|---|---|
| Licencias y suscripciones | 180 000 | 210 000 | Operar |
| Infraestructura y nube | 120 000 | 145 000 | Operar |
| Soporte y personal operativo | 240 000 | 250 000 | Operar |
| Mantenimiento correctivo | 60 000 | 72 000 | Operar |
| Seguridad de la información | 25 000 | 18 000 | Operar |
| Nuevos módulos del ERP | 90 000 | 40 000 | Crecer |
| Canal digital | 45 000 | 20 000 | Crecer |
| Analítica de datos | 30 000 | 0 | Transformar |
| **Total** | **790 000** | **755 000** | |

> **Contraste para el hallazgo de gobierno.** El plan estratégico declara la digitalización del canal como prioridad y el presupuesto del año en curso **reduce** «Canal digital» en 56 % y elimina «Transformar».

## 6. Inversiones cerradas (para la prueba de Val IT, Semana 14)

| Inversión | Año | Monto | Caso de negocio | Beneficio proyectado | Beneficio medido |
|---|---|---|---|---|---|
| Portal de pedidos B2B | Año -4 | S/ 180 000 | Sí, dos páginas | «Aumentar 20 % los pedidos del canal detalle» | **No se midió** |
| Renovación de servidores de almacén | Año -2 | S/ 95 000 | No | — | **No se midió** |
| Módulo de comisiones del ERP | Año -1 | S/ 40 000 | Correo del Gerente de Ventas | «Reducir el tiempo de cálculo de comisiones» | **No se midió** |

## 7. Datos sintéticos para los laboratorios

Los scripts generan los conjuntos de datos que consumen las guías. Se ejecutan una sola vez al inicio del semestre.

```python
# generar_datos_caso.py  —  requiere: pip install pandas numpy faker
import numpy as np, pandas as pd
from faker import Faker
from datetime import date

SEMILLA = 20240101                      # semilla fija: los datos son reproducibles
rng = np.random.default_rng(SEMILLA)
fk = Faker("es_ES"); Faker.seed(SEMILLA)

# El periodo se calcula respecto de hoy para que el caso no envejezca.
INICIO_PERIODO = pd.Timestamp(date.today().replace(month=1, day=1)) - pd.DateOffset(years=1)

# ---------- 1. Población de pagos (Semana 06) ----------
N = 180_000
prov = [f"Proveedor {i:03d} SAC" for i in range(1, 48)]
usuarios = [f"u{n:03d}" for n in range(1, 65)]
fechas = INICIO_PERIODO + pd.to_timedelta(rng.integers(0, 365*24*60, N), unit="m")

# Distribución log-normal: cumple las condiciones de la Ley de Benford
montos = np.round(rng.lognormal(mean=7.2, sigma=1.4, size=N), 2)

pagos = pd.DataFrame({
    "id_pago": [f"PG{i:07d}" for i in range(1, N+1)],
    "fecha": fechas,
    "proveedor": rng.choice(prov, N, p=np.r_[np.repeat(.13, 6), np.repeat(.0053, 41)][:47]/
                            np.r_[np.repeat(.13, 6), np.repeat(.0053, 41)][:47].sum()),
    "monto": montos,
    "usuario_solicitante": rng.choice(usuarios, N),
    "usuario_aprobador": rng.choice(usuarios, N),
    "nro_comprobante": np.arange(100000, 100000+N),
})

# --- Anomalías INTENCIONALES que los CAAT deben detectar ---
# a) Fraccionamiento bajo el umbral de S/ 5000
idx = rng.choice(N, 900, replace=False)
pagos.loc[idx, "monto"] = np.round(rng.uniform(4750, 4999, 900), 2)
pagos.loc[idx, "proveedor"] = "Proveedor 019 SAC"

# b) Autoaprobación
idx = rng.choice(N, 240, replace=False)
pagos.loc[idx, "usuario_aprobador"] = pagos.loc[idx, "usuario_solicitante"]

# c) Duplicados exactos
dup = pagos.sample(140, random_state=7).copy()
dup["id_pago"] = [f"PG9{i:06d}" for i in range(140)]
pagos = pd.concat([pagos, dup], ignore_index=True)

# d) Saltos en la secuencia de comprobantes
pagos = pagos.drop(pagos.sample(60, random_state=11).index)

# e) Montos redondos elevados (importes fabricados)
idx = rng.choice(len(pagos), 80, replace=False)
pagos.iloc[idx, pagos.columns.get_loc("monto")] = rng.choice([10000, 15000, 20000, 25000], 80)

pagos.to_csv("poblacion_pagos.csv", index=False)

# ---------- 2. Empleados y proveedores (cruce de la Semana 06) ----------
emp = pd.DataFrame({
    "id": usuarios,
    "nombre": [fk.name() for _ in usuarios],
    "area": rng.choice(["Ventas","Almacén","Contabilidad","Tesorería","TI","RR.HH.","Gerencia"], 64),
    "cuenta_bancaria": [f"00119{rng.integers(10**9,10**10)}" for _ in usuarios],
    "direccion": [fk.address().replace("\n", ", ") for _ in usuarios],
    "telefono": [fk.phone_number() for _ in usuarios],
    "correo": [fk.email() for _ in usuarios],
})
prv = pd.DataFrame({
    "razon_social": prov,
    "ruc": [f"20{rng.integers(10**8,10**9)}" for _ in prov],
    "cuenta_bancaria": [f"00119{rng.integers(10**9,10**10)}" for _ in prov],
    "direccion": [fk.address().replace("\n", ", ") for _ in prov],
    "telefono": [fk.phone_number() for _ in prov],
    "correo": [fk.email() for _ in prov],
})
# --- Coincidencias INTENCIONALES ---
prv.loc[18, "cuenta_bancaria"] = emp.loc[emp.area == "Tesorería", "cuenta_bancaria"].iloc[0]
prv.loc[31, "direccion"]       = emp.loc[emp.area == "Compras" if (emp.area=="Compras").any()
                                          else emp.area == "Almacén", "direccion"].iloc[0]
prv.loc[5,  "telefono"]        = emp.loc[emp.area == "Ventas", "telefono"].iloc[0]

emp.to_csv("empleados.csv", index=False)
prv.to_csv("proveedores.csv", index=False)

# ---------- 3. Usuarios del ERP vs. nómina (Semana 13) ----------
cesados = pd.DataFrame({
    "id": [f"x{n:03d}" for n in range(1, 24)],
    "nombre": [fk.name() for _ in range(23)],
    "fecha_cese": INICIO_PERIODO + pd.to_timedelta(rng.integers(180, 580, 23), unit="D"),
    "rol_erp": rng.choice(["consulta","ventas","compras","admin_compras"], 23, p=[.5,.25,.16,.09]),
})
usuarios_erp = pd.concat([
    emp[["id","nombre"]].assign(estado="activo", vinculo="vigente"),
    cesados[["id","nombre"]].assign(estado="activo", vinculo="cesado"),
], ignore_index=True)
usuarios_erp.to_csv("usuarios_erp.csv", index=False)
cesados.to_csv("personal_cesado.csv", index=False)
emp[["id","nombre","area"]].to_csv("personal_vigente.csv", index=False)

# ---------- 4. BIA con incoherencias intencionales (Semana 15) ----------
bia = pd.DataFrame([
 # actividad, mtpd_h, rto_h, rpo_h, mbco, frecuencia_respaldo_h, estrategia_actual
 ("Facturación y emisión de comprobantes", 8,  12, 1,  "50 % del volumen diario", 24, "Respaldo diario a USB"),
 ("Despacho de pedidos",                   12, 8,  4,  "Pedidos urgentes",        24, "Respaldo diario a USB"),
 ("Cobranza",                              48, 24, 24, "",                        24, "Respaldo semanal a nube"),
 ("Pago a proveedores",                    72, 24, 24, "Pagos críticos",          24, "Respaldo semanal a nube"),
 ("Pago de planilla",                      24, 48, 24, "",                        168,"Responsabilidad del proveedor"),
 ("Portal de pedidos B2B",                 24, 72, 24, "",                        168,"Sin estrategia definida"),
], columns=["actividad","mtpd_h","rto_h","rpo_h","mbco","frecuencia_respaldo_h","estrategia_actual"])
bia["rto_real_h"] = [None]*len(bia)     # se completa con la prueba de restauración
bia.to_csv("bia_empresa.csv", index=False)

print("Datos del caso simulado generados:")
for f in ["poblacion_pagos.csv","empleados.csv","proveedores.csv","usuarios_erp.csv",
          "personal_cesado.csv","personal_vigente.csv","bia_empresa.csv"]:
    print("  ·", f)
```

> **Incoherencias del BIA que los equipos deben detectar en la Semana 15.** En «Facturación» el RTO (12 h) supera el MTPD (8 h); en «Pago de planilla» y «Portal B2B» ocurre lo mismo; varios RPO declarados (1 h, 4 h) son menores que la frecuencia real de respaldo (24 h, 168 h); y tres actividades carecen de MBCO.

## 8. Documentos del caso que el docente entrega por semana

| Semana | Documento |
|---|---|
| 02 | Organigrama y matriz de accesos con roles del ERP (para la dinámica «El organigrama tóxico») |
| 03 | Relato del incidente de compromiso del correo del vendedor, <mes/año> |
| 04 | Narrativa del proceso de compras y pagos, dos páginas |
| 07 | Plan Estratégico Institucional vigente, extracto; actas de directorio (11, resumidas) |
| 08 | Seis condiciones de auditoría para «El criterio exacto» |
| 10 | Cuestionario de diagnóstico defectuoso de 12 preguntas |
| 11 | Contratos con el proveedor de planilla y con el proveedor de nube |
| 13 | Extracciones de usuarios, registro de cambios y registro de respaldos |
| 14 | Presupuesto de TI y expedientes de las tres inversiones cerradas |
| 15 | Política de respaldo y el BIA incompleto |
| 16 | Guion del auditado para la reunión de validación simulada |

## 9. Declaración obligatoria en el informe

Todo equipo que use este caso incorpora en la sección 2.1 del informe final:

> *«El presente informe se elaboró sobre un caso de estudio simulado con fines académicos, denominado Distribuidora Andina del Sur S.A.C. La organización, sus datos, sistemas y documentos son ficticios y fueron construidos por el docente del curso SI-084 de la Escuela Profesional de Ingeniería de Sistemas de la Universidad Privada de Tacna. Los procedimientos, criterios y metodología aplicados son los mismos que se emplearían en un encargo real.»*
