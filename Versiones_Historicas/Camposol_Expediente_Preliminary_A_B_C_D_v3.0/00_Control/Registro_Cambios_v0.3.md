# Registro de cambios y verificación · v0.3

2026-11-11 · Grupo 04 · Draft v0.3 · Decisión académica Grupo 04 · sin aprobación corporativa

## 1 Cambios frente a v0.2
| ID | Elemento | Cambio | Causa (auditoría) | Dónde |
|---|---|---|---|---|
| CHG-01 | Todos los documentos | Autoría: se reemplaza 'propuesta del asistente; sin aprobación del equipo' por decisión académica del Grupo 04. | Dueño de decisiones ausente | RE-03; gates |
| CHG-02 | IDs transversales | Unificación a la cadena DRV→GOAL→OUT→KPI→CAP→GAP→REQ→CRC→DEC→TEST. | Seis esquemas paralelos y colisión C3/C03 | Equivalencias_ID.csv |
| CHG-03 | PRE-04 | Formato TOGAF de 4 campos; PR-01/PR-04 → RE-01/RE-02; nuevos PR-07 y PR-08. | Principios metodológicos y faltantes | PRE-04; Principles_Register |
| CHG-04 | VS-01 / B-03 | Value stream con 5 campos por etapa y nueva etapa VS-S3 Verificar conformidad. | Sin campos ni etapa de Calidad | B-01; B-03 |
| CHG-05 | Requisitos | Nuevo REQ-08 y GAP-B08 (excepciones); KPI-04…07 nuevos; MED-A02 → KPI-04. | OUT-02/OUT-03 sin KPI; excepciones sin requisito | Requirements_Catalog; KPI_Catalog |
| CHG-06 | Escala de madurez | Escala 1–4 con rúbrica; los niveles 1–3 de PC1 conservan su significado. | Target uniforme 3 sin discriminación | A-01; B-02 |
| CHG-07 | KPI-03 | Baseline 0 % (SV sin sustento) reemplazado por 40 % (DS-CS-11), coherente con calibradoras públicas F04. | Supuesto implausible | KPI_Catalog |
| CHG-08 | CAP-02 | 'Operational Data Integration' renombrada 'Gestión de evidencia operativa' (capacidad de negocio). | Sesgo de aplicación | Capability_Catalog |
| CHG-09 | CAP-07 | Nueva capacidad 'Control de conformidad y liberación'. | La etapa de Calidad no tenía capacidad | B-02; B-03 |
| CHG-10 | Gap Analysis | Matriz sobre building blocks (procesos, servicios, roles y objetos) con Included/New/Eliminated. | Matriz diagonal degenerada | B-04 |
| CHG-11 | B-06 XML y vistas | B-V01 ≠ B-V02 con carriles por área (anidamiento) y layout por etapa; B-V04 complementaria (eventos y consumidores); nuevas B-V03, VIEW-A01 y VIEW-A02 en ArchiMate. | Baseline = Target; vistas A no formales | B-06; figuras |
| CHG-12 | MODEL-01 | Genealogía N:M (admite mezclas), origen de cosecha y resultado de inspección con HOLD. | Convención '1 padre' impedía merge | MODEL-01 |
| CHG-13 | PRE-03 / A-02 | Inversiones I1…I5 salen de las decisiones de Preliminary/A y pasan a hipótesis de solución para Phase E. | Value Before Technology | Solution_Concept_Candidates |
| CHG-14 | A-02 alcance 4D | Breadth organizacional, Depth por dominio y Time con horizonte. | Breadth repetía el VS | A-02; PRE-02 |
| CHG-15 | A-06 | Se añaden BS-02 (recepción y mezcla) y BS-03 (inspección y HOLD) con eventos de negocio. | Un solo escenario | A-06 |
| CHG-17 | Vistas de Phase A | VIEW-A01 reducida a la cadena del por qué; VIEW-A02 con Course of Action CoA-01 y VS como bloque; VIEW-A03 y VIEW-A04 pasan a ArchiMate (alineado con el ejemplo T&G). | Vistas A cargadas o fuera de notación | B-06; A-02; A-05 |
| CHG-16 | Trazabilidad | Matriz con 8 filas (una por REQ) y cadena completa; DEC por gap. | 5/7 REQ huérfanos | Matriz_Trazabilidad |

## 2 Decisiones nuevas o sustituidas
| ID | Decisión | Estado |
|---|---|---|
| DEC-01 | Explorar nodo local asíncrono (alternativa B) frente a A y C | Diferida a Phase E |
| DEC-02 | Diagnosticar y evaluar alternativas antes de implementar | Vigente |
| DEC-B01 | Describir B solo con IA/NE y Target sin gaps confirmados | Superseded por DEC-B04 |
| DEC-B02 | Resolve GAP-B01…06 en bloque | Superseded por DEC-B11…B18 |
| DEC-B03 | Revisión condicionada sin abrir C | Superseded por DEC-B05 |
| DEC-B04 | Sustentar Baseline con dataset simulado DS-CS-01…12 (clase S) y Target como decisión D | Vigente |
| DEC-B05 | Gate B→C: aprobar con condiciones el inicio de Phase C | Vigente (pendiente de ratificar fecha) |
| DEC-B06 | Mantener la frontera del VS-01 en la recepción de bins | Vigente |
| DEC-B11 | Resolver GAP-B01 con identidad de planta vinculada al origen y genealogía N:M | Vigente |
| DEC-B12 | Resolver GAP-B02 con BSV-01 ejecutado por ROL-B01 y revisado por Calidad | Vigente |
| DEC-B13 | Resolver GAP-B03 vinculando serie térmica y posición a cada pallet | Vigente |
| DEC-B14 | Resolver GAP-B04 con registro en contingencia y reconciliación formal | Vigente |
| DEC-B15 | Resolver GAP-B05 con acta de handoff y estados Calidad/Despacho separados | Vigente |
| DEC-B16 | Resolver GAP-B06 con ROL-B02 y fichas de los 7 KPI | Vigente |
| DEC-B17 | Resolver GAP-B07 fijando el criterio de acceso en B y difiriendo controles técnicos a C/D | Vigente |
| DEC-B18 | Resolver GAP-B08 con proceso formal de excepción BP-08 | Vigente |

## 3 Verificación automática
Ver sección generada al final de este archivo por `verificacion`.

## 4 Pendientes que pasan a Phase C/D
| ID | Dato | Owner | Fase |
|---|---|---|---|
| NV-01 | Aplicaciones e interfaces locales (SAP y otras) | STK-04 | Phase C (AP-V01) |
| NV-02 | Red por tramo y enlace externo | STK-04 | Phase D |
| NV-03 | Mediciones reales | STK-02 | Cualquier fase |
| NV-04 | Exportación de eventos de calibradoras | STK-04 | Phase C |
| NV-05 | Fuente térmica por pallet | STK-03 | Inicio de Phase C |
| NV-06 | Costos y autoridad financiera | STK-07 | Phase E |
| NV-07 | Protocolo de pruebas | STK-04 | Phase C/D |
| NV-08 | Roles reales y secuencia física | STK-01 | Phase C |

## 5 Resultado de la verificación automática (2026-11-11)

- OK REQ-01 cadena completa DRV→…→TEST sin referencias inexistentes
- OK REQ-02 cadena completa DRV→…→TEST sin referencias inexistentes
- OK REQ-03 cadena completa DRV→…→TEST sin referencias inexistentes
- OK REQ-04 cadena completa DRV→…→TEST sin referencias inexistentes
- OK REQ-05 cadena completa DRV→…→TEST sin referencias inexistentes
- OK REQ-06 cadena completa DRV→…→TEST sin referencias inexistentes
- OK REQ-07 cadena completa DRV→…→TEST sin referencias inexistentes
- OK REQ-08 cadena completa DRV→…→TEST sin referencias inexistentes
- OK GAP-B01 → REQ-01 / CRC-B01 / DEC-B11
- OK GAP-B02 → REQ-02 / CRC-B01 / DEC-B12
- OK GAP-B03 → REQ-04 / CRC-B02 / DEC-B13
- OK GAP-B04 → REQ-03 / CRC-B03 / DEC-B14
- OK GAP-B05 → REQ-06 / CRC-B02 / DEC-B15
- OK GAP-B06 → REQ-07 / CRC-B04 / DEC-B16
- OK GAP-B07 → REQ-05 / CRC-B03 / DEC-B17
- OK GAP-B08 → REQ-08 / CRC-B02 / DEC-B18
- OK CRC-B01 agrupa gaps y REQ existentes
- OK CRC-B02 agrupa gaps y REQ existentes
- OK CRC-B03 agrupa gaps y REQ existentes
- OK CRC-B04 agrupa gaps y REQ existentes
- OK Todos los DRV participan en al menos una cadena
- OK Todos los GOAL participan en al menos una cadena
- OK Todos los OUT participan en al menos una cadena
- OK Todos los KPI participan en al menos una cadena
- OK Todos los CAP participan en al menos una cadena
- OK Cada principio vigente es realizado por al menos un REQ
- OK 1 REQ ↔ 1 TEST
- OK Cada etapa VS-S1…S6 documenta Entra, Acción, Salida, Valor y Actor
- OK Existe la etapa de Calidad (VS-S3)
- OK Cada capacidad (salvo transversales CAP-05/06) es primaria en alguna etapa
- OK Matriz_Trazabilidad: 8 filas, sin columnas vacías
- OK XML: 105 elementos y 175 relaciones con referencias válidas
- OK XML usa los mismos IDs del catálogo
- OK Todas las relaciones usan pares origen/destino permitidos por ArchiMate 3.2
- OK Vista V-VIEW-A01: 14 nodos y 14 conexiones coherentes con el modelo; sin elementos aislados
- OK Vista V-VIEW-A02: 8 nodos y 8 conexiones coherentes con el modelo; sin elementos aislados
- OK Vista V-VIEW-A03: 9 nodos y 7 conexiones coherentes con el modelo; sin elementos aislados
- OK Vista V-VIEW-A04: 13 nodos y 12 conexiones coherentes con el modelo; sin elementos aislados
- OK Vista V-B-V01: 15 nodos y 18 conexiones coherentes con el modelo; sin elementos aislados
- OK Vista V-B-V02: 16 nodos y 24 conexiones coherentes con el modelo; sin elementos aislados
- OK Vista V-B-V03: 12 nodos y 14 conexiones coherentes con el modelo; sin elementos aislados
- OK Vista V-B-V04: 19 nodos y 19 conexiones coherentes con el modelo; sin elementos aislados
- OK Vista V-B-V05: 22 nodos y 16 conexiones coherentes con el modelo; sin elementos aislados
- OK B-V01 ≠ B-V02: 4 elementos solo Target, 3 solo Baseline
- OK Todo building block New de B-04 (8) aparece en las vistas Target y no en B-V01
- OK Todo building block Eliminated de B-04 (3) aparece solo en B-V01
- OK CP-06: B-V02 ∪ B-V04 ∪ B-V05 contienen los 35 procesos, servicios, objetos, eventos y roles Target
- OK CP-02: B-V01 y B-V02 comparten rejilla (12 elementos comunes en la misma celda)
- OK Ningún archivo vigente usa IDs de v0.2
- OK 32 DOCX/XLSX vigentes abren sin error
- OK Inventario regenerado: 165 archivos

Límites: el XML se validó estructuralmente y por pares de relaciones; no se validó contra el XSD oficial en esta versión ni se importó en Archi.
