# GUÍA PRÁCTICA SESIÓN 5

**TOGAF ADM fase B — Business Architecture**

De Baseline y Target a gaps, requirements y Candidate Roadmap Components

Caso práctico Del Monte Fresh Division y piña de Costa Rica

Ruta de trabajo de la sesión práctica de 120 minutos · viernes 9 de octubre de 2026 · 20:00 a 22:00

| 1 Continuidad | 2 Baseline | 3 Target | 4 Gap Analysis | 5 Requirements | 6 Roadmap candidates | 7 Gate |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| Expediente S4 | AS-IS comparable | TO-BE negocio | Matriz \+ Register | Statements \+ prueba | Cambios candidatos | Review B→C |

Producto de la sesión: borrador verificable de Business Architecture Phase B para el mismo value stream de piña, con Baseline/Target comparables, Gap Register, requisitos verificables, Candidate Roadmap Components, views/catálogos y actualización del Repository. El expediente se consolida después del taller según el plazo del docente.

| Dato | Definición |
| :---- | :---- |
| Curso | SI605 Arquitectura Empresarial |
| Horario | 20:00 a 22:00, inmediatamente después de la teoría de 18:00 a 20:00 |
| Duración | 120 minutos de trabajo guiado |
| Modalidad | Equipos sobre el mismo caso Del Monte de las prácticas 1–4; posterior transferencia a la empresa del Proyecto Integrador |
| Alcance | Un solo value stream estratégico: lotes de piña desde campo hasta despacho de exportación |
| Regla de evidencia | HP hecho público; DS dato simulado del caso; DE decisión del equipo; NV dato por validar |

# 

# 

# 1 Propósito y resultados esperados

Al terminar, el equipo habrá convertido la Architecture Vision y el Statement de la sesión 4 en una Business Architecture inicial capaz de orientar Phase C. La práctica exige modelar el negocio con unidades comparables, identificar gaps mediante evidencia y criterios explícitos, derivar business requirements verificables y conservar Candidate Roadmap Components sin seleccionar tecnología o proveedor.

| Resultado | Evidencia mínima |
| :---- | :---- |
| Continuidad | A-02 Vision, A-04 Statement, principles, requirements y IDs recuperados sin romper trazabilidad. |
| Baseline | Actores/roles, capabilities, services/procesos/objetos y hand-offs suficientes para explicar la fricción. |
| Target | Mismos tipos de elementos, reglas de diseño y outcomes explícitos. |
| Gap Analysis | Matriz Baseline×Target y Gap Register con al menos cinco gaps defendibles. |
| Requirements | Gap → requirement → criterion of acceptance, owner y trazabilidad. |
| Roadmap candidates | Agrupación de gaps/requisitos en 3–4 cambios candidatos, sin convertirlos en proyectos. |
| Outputs B | ADD actualizada, requirements, gaps, roadmap candidates, views/catálogos y Repository. |

# 2 Empresa y caso de análisis

## 2.1 Continuidad con las sesiones anteriores

Use exactamente el mismo System of Interest trabajado en las sesiones 3 y 4: trazabilidad de lotes de piña de la operación de Costa Rica de Del Monte Fresh Division, desde campo hasta despacho de exportación. No amplíe el alcance a toda la corporación. Reutilice DRV, GOAL, OUT, CAP, STK, CON, PR, REQ, VP, VIEW y DEC. Si un identificador cambia, registre equivalencia y rationale.

## 2.2 Base de evidencia ya aceptada del caso

Se mantienen HP, DS01–DS22 y las decisiones de equipo de la sesión 4\. Para esta práctica los DS se usan como verdaderos dentro del escenario académico, pero siguen identificados como simulados y no deben atribuirse a la empresa real.

| Indicador DS | Baseline | Meta / Target |
| :---- | :---- | :---- |
| Lotes de exportación/año | 12 000 | volumen de referencia |
| Conformidad en primera liberación | 89 % | ≥95 % |
| Trazabilidad digital campo–despacho | 68 % | ≥98 % |
| Reconstrucción de historial | 95 min | ≤30 min |
| Eventos completos de cadena de frío | 62 % | ≥95 % |
| Lotes en hold/retrabajo | 9 % | ≤4 % |

## 2.3 Dossier complementario para Phase B: DS23–DS45

Los siguientes datos se entregan como documentos internos simulados recibidos por el equipo al inicio de la sesión 5\. Para el ejercicio se tratan como hechos operativos. Deben citarse por ID en Baseline, Gap Register, Requirements y decisiones.

| ID | Información simulada entregada al equipo | Uso arquitectónico |
| :---- | :---- | :---- |
| DS23 | En un mes representativo se procesan 1 050 lotes; 310 sufren al menos un split y 74 un merge posterior. | Baseline de identidad y muestra para GAP-B01. |
| DS24 | En 18 % de los lotes con split/merge Calidad debe buscar manualmente una correspondencia H–P–X; en 3 % falta al menos un enlace en el primer intento. | Evidencia de continuidad de identidad. |
| DS25 | La historia de un lote se reconstruye desde cinco fuentes: Registro A, MES B, Calidad C, Frío D y Exportación E; no existe un servicio único de consulta. | Baseline para GAP-B02 y BSV-01. |
| DS26 | Muestra de 200 lotes: 76 % de eventos tiene timestamp y actor; 61 % conserva source; 54 % conserva procedencia completa. | Baseline de event history. |
| DS27 | Calidad y Exportación usan definiciones distintas de “lote listo”: Calidad usa liberación de inspección; Exportación usa documentación completa \+ booking confirmado. | Baseline para ownership/KPI y correspondencias. |
| DS28 | No existe un Data Steward formal. Datos/TI custodia definiciones; Calidad y Operaciones aprueban cambios por correo. | GAP-B03 governance. |
| DS29 | Excepciones de identidad, duplicado o conflicto se coordinan caso a caso; mediana 42 min y P90 135 min. | GAP-B04 y BSV-02. |
| DS30 | En una desconexión de 4 h, packing continúa localmente; 1,8 % de eventos sincronizados después genera duplicado o conflicto que requiere revisión. | Requirement de resiliencia/reconciliación. |
| DS31 | Definición de KPI de trazabilidad: Operaciones cuenta lotes con ID local; Calidad exige cadena H–P–X completa; Exportación exige además custodia y liberación. | GAP-B05: KPI no compartido. |
| DS32 | Capability baseline/target 0–4: trazabilidad 2→4; packing integrado 2→3; gobierno de información 1→3; calidad 2→3; excepciones 1→3; orquestación exportadora 2→3. | Heat Map de Phase B. |
| DS33 | Packhouse concentra packing, calidad, trazabilidad y excepción; campo/cosecha generan origen e ID; frío transfiere custodia; exportación consume evidencia. | Value Stream×Capabilities. |
| DS34 | Business objects mínimos: Lote, Evento de Lote, Historia de Lote, Liberación de Calidad, Custodia y Pedido de Exportación. | Target semántico y views. |
| DS35 | Target de identidad: cada lote hijo conserva parent\_id; merge conserva lista de parent\_ids; ningún ID se reutiliza. | Criterio Target de GAP-B01. |
| DS36 | Target de evento: event\_id, lot\_id, event\_type, timestamp, actor/role, source, location, reason y parent/child cuando aplique. | REQ-02 y criterio de aceptación. |
| DS37 | Target de servicio BSV-01: Calidad/Exportación pueden obtener historia auditable de un lote en ≤30 min sin conciliación manual recurrente. | Target de GAP-B02. |
| DS38 | Target de servicio BSV-02: excepción identificada, owner asignado, estado visible, evidencia de resolución y cierre. | Target de GAP-B04. |
| DS39 | Target BSV-03: “Liberación conforme” exige regla común que combine calidad y condiciones de exportación; diferencias se registran como excepción. | Organization & Services. |
| DS40 | Target de stewardship: Data Steward es accountable por definiciones, reglas de calidad y correspondencias; owners de proceso conservan responsabilidad operacional. | REQ-05. |
| DS41 | Criterios de prioridad: Crítica si afecta inocuidad/trazabilidad o bloquea despacho; Alta si afecta eficiencia, gobierno o medición; Media si no bloquea outcomes del scope. | Gap priority. |
| DS42 | Decisión preliminar del sponsor: GAP-B01..B04 deben resolverse; B05 se resuelve si el esfuerzo es compatible con Phase B/C; ninguna brecha se acepta sin rationale. | Treatment del Gap Register. |
| DS43 | Candidate roadmap grouping propuesto como punto de partida: CRC-01 trazabilidad end-to-end; CRC-02 stewardship; CRC-03 resiliencia/excepciones; CRC-04 KPI compartido. | Salida Phase B, no proyectos. |
| DS44 | Dependencias conocidas: CRC-01 necesita Data \+ Application; CRC-03 necesita Application \+ Technology/OT; CRC-02/04 requieren Business \+ Data. | Preparación para Phase C/D/E. |
| DS45 | Gate B→C exige: Baseline/Target comparables, ≥5 gaps con evidencia, requirements con criterio, 3–4 CRC, dos views ArchiMate, inventario actualizado y dos cadenas trazables. | Criterio de cierre de la práctica. |

## 2.4 Tarjeta de trabajo de Phase B

| Campo | Dato del caso |
| :---- | :---- |
| Pregunta | ¿Qué debe cambiar en la arquitectura de negocio para escalar la trazabilidad de piña sin perder identidad, evidencia, calidad ni continuidad operacional? |
| Value stream | Campo → cosecha → packing → frío → exportación; único flujo. |
| Foco de profundidad | Packing/Quality y hand-offs de identidad/evidencia. |
| Outcome | Trazabilidad digital ≥98 %, historia ≤30 min, conformidad ≥95 %, hold/retrabajo ≤4 %. |
| Restricción | No seleccionar proveedor, API, base de datos, cloud/edge ni producto. |
| Decisión solicitada | Proponer Business Architecture suficiente para gate B→C. |

# 3 Resumen operativo de la sesión teórica

| Concepto | Qué significa aquí | Comprobación |
| :---- | :---- | :---- |
| Baseline | Descripción suficiente del negocio actual para comparar. | ¿Hay evidencia y mismas unidades que Target? |
| Target | Condición de negocio deseada, independiente de implementación. | ¿Responde principles/outcomes/requirements? |
| Gap | Diferencia relevante Baseline–Target. | ¿Tiene unidad, criterio, impacto y decisión? |
| Gap Register | Registro gobernable de brechas. | ¿Tiene owner, priority, requirement y status? |
| Business Requirement | Condición verificable que la solución deberá satisfacer. | ¿Tiene acceptance criterion? |
| Candidate Roadmap Component | Cambio arquitectónico candidato agrupando gaps/requirements. | ¿Evita aún proyecto/vendor/presupuesto? |
| Architecture Definition | Contenedor cualitativo que integra/referencia Business Architecture. | ¿Incluye Baseline, Target, rationale, views, gaps? |
| Views/Catalogs | Artifacts seleccionados por concerns. | ¿Cada artifact soporta una decisión? |

# 4 Plan de trabajo de 120 minutos

| Hora | Min | Actividad | Acción principal | Salida del taller |
| :---- | :---- | :---- | :---- | :---- |
| 20:00–20:10 | 10 | A Continuidad | Recuperar A-02/A-04/PR/REQ y revisar DS23–DS45. | Scope \+ IDs \+ fuentes. |
| 20:10–20:30 | 20 | B Baseline | Modelar unidades comparables y evidencias. | B-01 Baseline \+ B-V01 borrador. |
| 20:30–20:48 | 18 | C Target | Definir Target, services, ownership y objetos. | B-01 Target \+ B-V02 borrador. |
| 20:48–21:15 | 27 | D Gap Analysis | Matriz \+ cinco pasos \+ prioridad/decisión. | Gap Matrix \+ Gap Register. |
| 21:15–21:35 | 20 | E Requirements | Derivar statements y criterios de aceptación. | Requirements Catalog actualizado. |
| 21:35–21:50 | 15 | F CRC \+ outputs | Agrupar cambios y mapear ADD/views/catalogs. | CRC Register \+ Output Map. |
| 21:50–22:00 | 10 | G Gate y cierre | Revisar trazabilidad, Repository y gate B→C. | Decision Log \+ pendientes. |

La práctica de dos horas produce versiones iniciales verificables. El expediente completo se consolida después. No se requiere elegir tecnología: se evalúa la calidad de la lógica arquitectónica y la trazabilidad.

# 5 Actividades de trabajo

## Actividad A Recuperar el expediente y fijar criterios de comparación

Tiempo: 10 minutos. Entrada: A-02 Architecture Vision, A-04 Statement, PRE-04 Principles, Requirements Catalog y dossier DS. Salida: ficha de comparación Phase B.

### Paso A1 Reutilizar IDs y alcance

Anote System of Interest, value stream, scope breadth/depth, stakeholders/concerns, outcomes/KPI, principles y requirements existentes. No cree nuevos IDs si ya existe un concepto equivalente.

### Paso A2 Declarar unidades comparables

Seleccione al menos cinco unidades del mismo tipo en Baseline y Target: identidad, evidencia/historia, service, ownership, excepción, KPI o capability. Para cada una declare el criterio: concern, principle, outcome o requirement que permitirá juzgar la diferencia.

## Actividad B Construir Business Architecture Baseline

Tiempo: 20 minutos. Salida: B-01 Baseline y una view B-V01. Modelar solo lo necesario para explicar las fricciones del scope.

### Paso B1 Capabilities y value stream

Use DS32 y DS33. Registre Baseline/Target de las seis capabilities y marque hotspots. Dibuje el value stream de seis stages y una matriz Stage×Capability simplificada.

### Paso B2 Organization, services y objects Baseline

Identifique actores/roles, comportamiento, business objects y hand-offs. Use DS25–DS31. Diferencie quién ejecuta, quién responde y quién consume evidencia.

### Paso B3 View Baseline

Elabore una view ArchiMate o diagrama equivalente que responda CON-02: por qué la historia del lote no se recupera end-to-end sin conciliación. Debe mostrar al menos Actor/Role, Process, Business Object y hand-offs relevantes.

## Actividad C Diseñar Business Architecture Target

Tiempo: 18 minutos. Salida: Target comparable y view B-V02.

### Paso C1 Reglas de diseño

Transforme PR-01…PR-04, outcomes y REQ existentes en reglas del Target. Use DS35–DS40. No describa productos ni protocolos técnicos.

### Paso C2 Services y ownership

Incluya BSV-01 Historial auditable, BSV-02 Resolución de excepción y BSV-03 Liberación conforme. Asigne consumidores y owner. Formalice Data Steward como role de gobierno.

### Paso C3 Objetos y eventos

Use DS34 y DS36. Defina Lote, Evento de Lote e Historia de Lote con semántica suficiente para Phase C. Para split/merge declare genealogía parent/child.

## Actividad D Ejecutar Gap Analysis

Tiempo: 27 minutos. Salida: matriz Baseline×Target y Gap Register con al menos cinco gaps.

### Paso D1 Matriz formal

Coloque elementos Baseline en filas y Target en columnas o, si usa tabla comparativa, mantenga una unidad por fila. Clasifique Included, New, Eliminated o Modify. Si detecta una eliminación accidental, corrija Target antes de continuar.

### Paso D2 Aplicar los cinco pasos

Para cada gap: 1\) unidad/criterio; 2\) evidencia Baseline y condición Target; 3\) clasificación; 4\) impacto/prioridad; 5\) decisión Resolve/Accept/Defer/Revise Target. Use DS41–DS42.

### Paso D3 Gap Register

Registre Gap ID, elemento, Baseline, Target/criterio, tipo, evidencia, impact, priority, owner, decision, requirement, criterion of acceptance, dependency, CRC y status.

## Actividad E Derivar Business Requirements y aceptación

Tiempo: 20 minutos. Salida: Requirements Catalog actualizado.

### Paso E1 Gap → Requirement

Cada gap a resolver genera o refina un requirement. Debe ser un statement verificable, no una solución. Ejemplo: “Todo lote hijo conservará vínculo inequívoco con el/los lote(s) padre” es válido; “usar blockchain” no lo es.

### Paso E2 Acceptance Criteria

Defina una prueba por requirement. REQ-01: muestra split/merge sin huérfanos. REQ-02: historia con timestamp, actor, source y provenance. REQ-04: recuperación sin pérdida tras desconexión. REQ-05: owner/steward aprobado. REQ-06: definición y medición común de KPI.

## Actividad F Construir Candidate Roadmap Components y mapa de salidas

Tiempo: 15 minutos. Salida: CRC Register y Output Map.

### Paso F1 Agrupar cambios

Use DS43–DS44. Agrupe gaps y requirements relacionados en CRC-01…CRC-04. Para cada CRC indique propósito, gaps, requirements, dependencies y dominios que deben completar el diseño. No asigne vendor, proyecto, presupuesto ni cronograma.

### Paso F2 Actualizar Architecture Definition y artifacts

Liste qué contenidos se incorporan a B-01 Architecture Definition: Baseline, Target, capabilities, value stream, services/organization, gaps, views y Repository mapping. Mapee qué archivos editables prueban cada sección.

## Actividad G Gate B→C, trazabilidad e integración

Tiempo: 10 minutos. Salida: gate y pendientes.

### Paso G1 Demostrar dos cadenas completas

Cadena 1 sugerida: DS24 → CON-02 → PR-01/PR equivalente → CAP-01 → GAP-B01 → REQ-01 → CRC-01 → TEST → VIEW. Cadena 2: DS26/DS25 → OUT de historia → GAP-B02 → REQ-02 → CRC-01. Use los IDs reales del expediente del grupo.

### Paso G2 Evaluar gate

Simule Architecture Board con DS45. Decisión: Aprobar Phase C, Aprobar con condiciones o Refinar. Toda condición lleva owner, fecha y criterio de cierre.

# 6 Productos y estructura de entrega

El expediente de la sesión 5 amplía el ZIP de la sesión 4\. Nombre sugerido: SI605\_S5\_GrupoXX\_PhaseB\_DelMonte\_v0.1.zip. Los archivos de trabajo tabulares se entregan en XLSX, no CSV, para conservar formato, validaciones y trazabilidad.

| Ruta | Entregable / artifact | Contenido mínimo |
| :---- | :---- | :---- |
| 05\_Phase\_B/B-01.docx | Business Architecture Definition | Baseline, Target, capabilities, value stream, services, rationale y mapping. |
| 05\_Phase\_B/B-02.xlsx | Capability Heat Map | 6 capabilities, baseline/target, owner, evidence, priority. |
| 05\_Phase\_B/B-03.xlsx | ValueStream×Capability | Stages y capabilities. |
| 05\_Phase\_B/B-04.xlsx | Gap Register | ≥5 gaps con todos los campos de gobierno. |
| 05\_Phase\_B/B-05.docx/xlsx | Organization & Services | Actors/roles/services/consumers/ownership. |
| 05\_Phase\_B/B-06.xml | ArchiMate Exchange | Views Baseline/Target y trazabilidad. |
| 05\_Phase\_B/B-07.xlsx | Requirements | Requirement \+ criterion \+ owner \+ gap. |
| 05\_Phase\_B/B-08.xlsx | Candidate Roadmap Components | CRC \+ gaps \+ requirements \+ dependencies. |
| 05\_Phase\_B/B-09.xlsx | Views & Catalogs Register | Concern → artifact → route → version. |
| Repository transversal | Inventario/Traceability/Decision/Risk | Rutas, IDs, status y cambios. |

## 6.1 Contenido del resumen ejecutivo

| Página/lámina | Contenido |
| :---- | :---- |
| 1 | Contexto, scope, outcomes y principles heredados de A. |
| 2 | Baseline \+ Target comparables. |
| 3 | Capability Heat Map \+ Value Stream×Capabilities. |
| 4 | Gap Matrix/Gap Register y requirements. |
| 5 | CRC, views/catálogos, Repository y gate B→C. |

## 6.2 Paquete mínimo que se muestra a las 22:00

| Evidencia | Condición |
| :---- | :---- |
| Baseline/Target | Cinco unidades comparables con evidencia/criterio. |
| Gap Register | Cinco gaps con decision y priority. |
| Requirements | Cinco statements con criterion of acceptance. |
| CRC | Al menos tres cambios candidatos, sin tecnología. |
| Views | B-V01 y B-V02 o equivalentes. |
| Repository | Inventario y trazabilidad actualizados. |
| Gate | Decisión y condiciones. |

# Anexo A Hojas de trabajo editables para la sesión

Copie estas tablas a los DOCX/XLSX del expediente. Cada hoja debe llevar ID, versión v0.1, owner, estado Draft y fuente HP/DS/DE/NV.

## A1 Ficha de unidades comparables

| Unidad | Baseline DS | Target / criterio | Fuente del criterio | View / artifact |
| :---- | :---- | :---- | :---- | :---- |
| Identidad |  |  |  |  |
| Evidencia/historia |  |  |  |  |
| Service |  |  |  |  |
| Ownership |  |  |  |  |
| Excepción |  |  |  |  |
| KPI |  |  |  |  |

## A2 Capability Assessment y Heat Map

| CAP | Capability | Base 0–4 | Target 0–4 | Δ | Evidence | Owner | Priority |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| CAP-01 | Trazabilidad de lote |  |  |  |  |  |  |
| CAP-02 | Packing integrado |  |  |  |  |  |  |
| CAP-03 | Gobierno de información |  |  |  |  |  |  |
| CAP-04 | Aseguramiento calidad |  |  |  |  |  |  |
| CAP-05 | Gestión excepciones |  |  |  |  |  |  |
| CAP-06 | Orquestación exportadora |  |  |  |  |  |  |

## A3 Matriz Baseline × Target

| Baseline \\ Target | T1 Identidad | T2 Historia | T3 Ownership | T4 Excepción | T5 KPI | Eliminated |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| B1 Identidad |  |  |  |  |  |  |
| B2 Registros dispersos |  |  |  |  |  |  |
| B3 Ownership fragmentado |  |  |  |  |  |  |
| B4 Excepción ad hoc |  |  |  |  |  |  |
| B5 KPI divergente |  |  |  |  |  |  |
| NEW |  |  |  |  |  |  |

## A4 Gap Register

| Gap ID | Elemento | Baseline | Target/criterio | Tipo | Impacto/Priority | Owner | Decision | REQ | Acceptance | Dependency | CRC | Status |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| GAP-B01 |  |  |  |  |  |  |  |  |  |  |  |  |
| GAP-B02 |  |  |  |  |  |  |  |  |  |  |  |  |
| GAP-B03 |  |  |  |  |  |  |  |  |  |  |  |  |
| GAP-B04 |  |  |  |  |  |  |  |  |  |  |  |  |
| GAP-B05 |  |  |  |  |  |  |  |  |  |  |  |  |

## A5 Business Requirements

| REQ | Statement | Origin Gap | Owner | Priority | Acceptance Criterion | Traceability |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| REQ-01 |  |  |  |  |  |  |
| REQ-02 |  |  |  |  |  |  |
| REQ-04 |  |  |  |  |  |  |
| REQ-05 |  |  |  |  |  |  |
| REQ-06 |  |  |  |  |  |  |

## A6 Candidate Roadmap Components

| CRC | Nombre | Gaps | Requirements | Outcome | Dependencies | Domains futuros | No decidir todavía |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| CRC-01 | Trazabilidad end-to-end |  |  |  |  |  |  |
| CRC-02 | Stewardship / ownership |  |  |  |  |  |  |
| CRC-03 | Resiliencia / excepciones |  |  |  |  |  |  |
| CRC-04 | KPI compartido |  |  |  |  |  |  |

## A7 Views y catálogos

| Concern / decisión | Viewpoint / artifact | Tipo | Elementos | Ruta Repository | Owner | Version |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| Historia recuperable | B-V01 Baseline | ArchiMate View |  |  |  |  |
| Target trazable | B-V02 Target | ArchiMate View |  |  |  |  |
| Hotspots | Capability Heat Map | Matrix |  |  |  |  |
| Qué cambia | Gap Register | Catalog |  |  |  |  |
| Accountability | Organization & Services | Catalog/Matrix |  |  |  |  |

## A8 Gate B→C y prueba oral

| Criterio | Cumple S/N | Evidencia / ruta | Condición / owner |
| :---- | :---- | :---- | :---- |
| Baseline/Target comparables |  |  |  |
| Gaps defendibles |  |  |  |
| Requirements verificables |  |  |  |
| CRC trazables |  |  |  |
| Views/catálogos suficientes |  |  |  |
| Repository actualizado |  |  |  |

Prueba oral de 90 segundos: un integrante recorre una cadena desde DS hasta CRC/test; otro la recorre en sentido inverso. Cada salto debe localizarse en un artifact o registro.

# 7 Checklist de calidad antes de entregar

* ☐ Un solo value stream y mismo System of Interest; cambios justificados.  
* ☐ HP, DS, DE y NV identificados; los DS no se atribuyen a la empresa real.  
* ☐ Baseline y Target utilizan las mismas unidades y granularidad.  
* ☐ Cada gap tiene evidencia, Target/criterio, impacto, owner y decisión.  
* ☐ Pain point ≠ gap: no se registra una brecha sin comparación.  
* ☐ Cada gap Resolve deriva/refina un requirement verificable.  
* ☐ Cada requirement tiene criterion of acceptance y trazabilidad.  
* ☐ Los CRC agrupan cambios pero no son proyectos/work packages definitivos.  
* ☐ Views y catálogos responden concerns y tienen fuente editable/versionada.  
* ☐ Architecture Definition integra o referencia artifacts sin duplicarlos sin control.  
* ☐ Repository, Requirements, Decision Log y Matriz de Trazabilidad quedan actualizados.  
* ☐ El gate B→C registra decisión, condiciones, owner y siguiente paso.

# 8 Referencias y material de apoyo

* SI605. Sesión 5\. TOGAF Phase B – Business Architecture, versión de 70 láminas con Gap Analysis y salidas detalladas.  
* SI605. Guía práctica sesión 4\. Preliminary \+ Phase A, caso Del Monte Fresh Division.  
* The Open Group. TOGAF Standard, 10th Edition: ADM Phase B, Architecture Content, Requirements Management y Gap Analysis.  
* ISO/IEC/IEEE 42010:2011: stakeholders, concerns, viewpoints, views y correspondences.  
* ArchiMate Specification: Motivation, Strategy, Business e Implementation & Migration elements.

Cierre: Phase B convierte la visión en una Business Architecture explícita y defendible. La clave no es producir muchos diagramas, sino demostrar una cadena consistente Baseline → Target → Gap → Requirement → Candidate Roadmap Component → View/Decision/Repository que permita a Phase C continuar con suficiente claridad.