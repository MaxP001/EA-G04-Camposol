# Registro de cambios · v0.4 (Phase C)

2026-11-11 · Grupo 04 · Draft v0.4 · Decisión académica Grupo 04 · sin aprobación corporativa

## 1 Qué se agregó
- Phase C completa: C-00…C-06, C1/C2/C3, 7 vistas ArchiMate y modelo consolidado A+B+C.
- Dataset simulado DS-CS-13…30.
- Punteros Phase_C en el repositorio y carpeta 09 de guía.

## 2 Cambios inter-fases (C-00 Change_Log)
| ID | Elemento | Observación | Decisión | Documento |
|---|---|---|---|---|
| CHG-C01 | BO-01 Lote | Se precisa en DOBJ-01 Lot + DOBJ-02 SourceMapping + DOBJ-03 HarvestOrigin (DS-CS-19) | Refinamiento de diccionario; sin cambio de capacidad ni REQ | C1; C-02 |
| CHG-C02 | A-02 / A-04 | El alcance sigue siendo VS-01 en Chao; no cambia objetivo | Sin cambio | — |
| CHG-C03 | PR-03 | Owner se precisa como owner + steward + custodio | Refinado (propuesta) en C-00 | PRE-04 v0.4 si ROL-AB lo aprueba |
| CHG-C04 | VIEW-A04 | ASV-C01/C02 evolucionan a ASV-01/02; DO-C01 se detalla en DOBJ-12 LotHistory | Trazabilidad A → C | Equivalencias_ID |
| CHG-C05 | REQ-04 | La evidencia térmica exige zona horaria explícita (DS-CS-22) | Sin cambio de statement; precisión en AR-D03 | C-03 |
| CHG-C06 | Vistas ArchiMate A+B+C | Rediseño con la convención gráfica del ejemplo T&G: rejilla fija, tipo ArchiMate en cada tarjeta, color por capa y subgrafo completo de relaciones; B-V04 se reenfoca en servicios y consumidores y se agrega B-V05 (actor → rol → proceso) | Sin cambio de elementos ni relaciones del modelo (145 / 256); 16 vistas; las vistas detalladas previas se conservan como anexo | XML v0.4; Figuras; A-02, A-05, B-01, C-01, C-02 (DEC-C15) |

## 3 Principios revisados
| Principio | Dominio | Resultado | Efecto |
|---|---|---|---|
| PR-02 | Datos | Vigente | Fundamenta AR-D01 (lotId único y genealogía N:M) |
| PR-03 | Datos | Refinado (propuesta) | Se precisa 'owner' como Data Owner + Data Steward + custodio técnico (DS-CS-23) |
| PR-05 | Negocio | Vigente | Componentes Target como ABB lógicos sin producto (DEC-C14) |
| PR-06 | Tecnología | Vigente | Pasa a Phase D (PD-01…04) |
| PR-07 | Negocio | Vigente | Fundamenta AR-D04 y AR-A05: aplicaciones solo leen el estado QA |
| PR-08 | Aplicaciones | Vigente | Fundamenta AR-A01 (contratos IF-01…07) y AR-A04 (idempotencia) |

## 4 Pendientes para Phase D
| ID | Pendiente | AR |
|---|---|---|
| PD-01 | Buffer local en planta y autonomía ante caída del enlace externo (≥ 24 h a validar) | AR-A04;AR-D06 |
| PD-02 | RTO/RPO de ingesta y consulta | AR-A02;AR-A04 |
| PD-03 | Identidad técnica y gestión de accesos (IAM) | AR-A03 |
| PD-04 | Zonas y conductos IT/OT (ISA/IEC 62443) entre calibradoras, cámaras y red de planta | AR-A01;AR-A04 |
| PD-05 | Almacenamiento y retención de evidencias | AR-D05 |
| PD-06 | Sincronización de relojes y zona horaria | AR-D03 |
| PD-07 | Mecanismo de integración con SAP (sin presuponer API) | AR-A01;AR-A05 |

## 5 Verificación automática (2026-11-11)

- OK GAP-D01 → AR-D01 → D-RC01 → DEC-C01 → TEST-D01
- OK GAP-D02 → AR-D02 → D-RC02 → DEC-C02 → TEST-D02
- OK GAP-D03 → AR-D03 → D-RC03 → DEC-C03 → TEST-D03
- OK GAP-D04 → AR-D04 → D-RC03 → DEC-C04 → TEST-D04
- OK GAP-D05 → AR-D05 → D-RC03 → DEC-C05 → TEST-D05
- OK GAP-D06 → AR-D06 → D-RC04 → DEC-C06 → TEST-D06
- OK GAP-A01 → AR-A01 → A-RC01 → DEC-C07 → TEST-A01
- OK GAP-A02 → AR-A02 → A-RC02 → DEC-C08 → TEST-A02
- OK GAP-A03 → AR-A03 → A-RC03 → DEC-C09 → TEST-A03
- OK GAP-A04 → AR-A04 → A-RC04 → DEC-C10 → TEST-A04
- OK GAP-A05 → AR-A05 → A-RC02 → DEC-C11 → TEST-A05
- OK GAP-A06 → AR-A06 → A-RC04 → DEC-C12 → TEST-A06
- OK REQ-01…08 tienen al menos un AR
- OK 1 AR ↔ 1 TEST
- OK Todo GAP-D/A agrupado en un candidato y viceversa
- OK Dependencias de candidatos válidas
- OK C-00: 23 artefactos (9 + 14) con estado y justificación
- OK 12 objetos con Data Owner, Data Steward y custodio válidos
- OK IF-01…07 con productor y consumidor existentes
- OK Apps × Organización sin filas vacías
- OK Toda aplicación soporta al menos una capacidad (matriz derivada del portafolio)
- OK Cada componente Target (AP-08…AP-11) está restringido por al menos un AR
- OK XML A+B+C: 145 elementos y 256 relaciones con referencias válidas
- OK Todas las relaciones usan pares permitidos por ArchiMate 3.2
- OK 16 vistas en el modelo consolidado (VIEW-A01, VIEW-A02, VIEW-A03, VIEW-A04, B-V01, B-V02, B-V03, B-V04, B-V05, D-V01, D-V02, D-V03, AP-V01, AP-V02, AP-V03, X-V01)
- OK Vista D-V01: 14 nodos, 10 conexiones coherentes
- OK Vista D-V02: 11 nodos, 11 conexiones coherentes
- OK Vista D-V03: 15 nodos, 16 conexiones coherentes
- OK Vista AP-V01: 7 nodos, 6 conexiones coherentes
- OK Vista AP-V02: 15 nodos, 15 conexiones coherentes
- OK Vista AP-V03: 14 nodos, 14 conexiones coherentes
- OK Vista X-V01: 15 nodos, 18 conexiones coherentes
- OK C-00…C-06 y C1/C2/C3 presentes
- OK Todos los entregables de Phase C abren sin error
- OK Figuras PNG/SVG de las 7 vistas
- OK Inventario regenerado: 165 archivos

Límites: XML validado estructuralmente y por pares de relaciones; no se validó contra el XSD oficial ni se importó en Archi.
