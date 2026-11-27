# Resumen ejecutivo de Camposol

v0.1 · Draft académico; propuesta del asistente DE; sin aprobación del equipo ni corporativa · 2026-10-15

## Página 1 Contexto alcance y gobierno

Expediente académico v0.1 · Grupo 04 · SI605 · 15/10/2026. Draft: propuesta del asistente, pendiente de revisión del equipo. Basado en PC1 corregida, los doce borradores y guía S4.

Oportunidad: evaluar si el aumento de escala de Packing Chao conserva identidad, evidencia y coordinación. Las fuentes públicas F01/F03/F04/F05 ofrecen contexto; no demuestran fallas locales. IA/SV y datos NV mantienen su procedencia.

| Frontera | Definición vigente |
| --- | --- |
| Inicio y recorrido | Recepción de bins → calibrado → empaque → pre-frío según ruta → cámara → carga y entrega del FCL refrigerado en rampa. |
| Receptor y variantes | Transportista inmediato; cliente internacional beneficiario. Validar recepción refrigerada, ruta y documentos NV-08. |
| Fuera del diseño | Campo, puertos, transporte marítimo, distribución internacional y ERP corporativo. |
| Dirección | OBJ01/OUT01: evidencia íntegra y reconstrucción oportuna; complementos de handoffs/picos conservados. |

### Organización propuesta para hacer arquitectura

Sponsor funcional STK-01 Operaciones; Board académico ROL-AB; arquitecto ROL-EA; responsables de negocio, Calidad, Frío, Despacho e IT/OT; Mejora Continua y custodio. Son funciones propuestas, no cargos confirmados. RACI tiene A único por actividad. Architecture Capability es distinta de habilidades operativas.

### Límites para decidir

KPI/score reales NE. No se realizaron entrevistas, reuniones ni pruebas operativas. NV-01…08 conservan acción y owner propuesto. La propuesta B de nodo local sigue exploratoria/reabrible; no hay tecnología elegida o autorización de implementación. Fuentes y correcciones previas se reutilizan sin nueva investigación web.


## Página 2 Repository y reutilización

Doce DOCX canónicos en 01_Preliminary/02_Phase_A; controles en 00_Control. El inventario clasifica y enlaza, sin duplicar esos documentos en las ocho clases.

| Clase Repository | Activos recuperables |
| --- | --- |
| 01 Metamodel | Convenciones, Elementos, Relaciones, Viewpoint Catalog |
| 02 Capability | Roles funcionales y Capability Charter EA |
| 03 Landscape | Strategic/Segment: cuatro fuentes A, ER PC1 y planes |
| 04 Standards | Principios y estándares con estado/aplicabilidad |
| 05 Reference | PC1/registro/guía y patrones candidatos |
| 06 Governance | RACI, decisiones, riesgos, comunicaciones, gates/excepciones |
| 07 Requirements | STK, concerns, CAP, KPI, REQ, correspondences y cadenas |
| 08 Solutions | Conceptos/alternativas y diagrama lógico sin SBB seleccionado |

### Dos continuos y cuatro niveles

| Nivel | Architecture / Solutions |
| --- | --- |
| Foundation | Método/AD del curso / funciones genéricas de captura e intercambio |
| Common Systems | Eventos y responsables / servicio lógico de evidencia |
| Industry | Identidad alimentaria / series térmicas y custodia candidatas |
| Organization-Specific | Vision/Target Chao / alternativas A-B-C y ABB propios |

Continuum_Catalog contiene 8 registros con origen, adaptación, archivo real y REQ/DEC beneficiada. Los patrones sectoriales y soluciones son candidatos sin validación de implantación. Ejemplo: evento genérico → identidad/custodia alimentaria → genealogía/pallet/ruta de Chao → REQ-01/02/04 y alternativas revisables.


## Página 3 Principios solicitud capacidades y visión

| Principio propuesto | Regla de decisión |
| --- | --- |
| PR-01 Evidencia y escenario explícitos | La descripción del proceso real usa evidencia autorizada; las hipótesis, escenarios IA y propuestas DE conservan su procedencia. |
| PR-02 Claridad de identidad y custodia | Cada handoff identifica unidad/genealogía, emisor, receptor, información mínima, aceptación y excepción. |
| PR-03 Trazabilidad con responsable y evidencia | Cada evento/estado tiene fuente y responsable; liberación de Calidad y condición de despacho se registran por separado con acceso gobernado. |
| PR-04 Medición comparable antes y después | Las metas se pueden proponer en el escenario, pero el desempeño real y su mejora requieren baseline y protocolo medidos con poblaciones comparables. |
| PR-05 Tecnología como habilitador revisable | Se comparan reutilización y alternativas técnicas conforme a necesidad y evidencia; no se selecciona proveedor ni se impone nodo local. |
| PR-06 Continuidad con acceso seguro | Las interfaces del alcance deben conservar evidencia, reconciliar interrupciones y aplicar acceso autorizado sin atribuir capacidades no verificadas. |

PRE-05 solicita Phase A: misión de evaluar capacidades, coordinación, información y soporte. Propone seis semanas A-S1…A-S6, con recursos/acceso por acordar. No autoriza B/C/D, piloto ni gasto.

### Capacidades y escenario

C4 Traceability/H1 Integration y C3 Cold Chain conservan los focos IA de PC1 en escala 1–3; situación real NE y target 3 propuesto. CAP-A01 handoffs, CAP-A02 medición y CAP-A03 excepciones se conservan de los borradores con IDs conciliados. Readiness depende de mandato, acceso, adopción, evidencia y recursos.

BS-01 IA: transferencia cámara→despacho y solicitud de historia. Validar identidad, custodia y dos estados distintos: liberación de Calidad y condición de despacho. Ante faltantes o interrupción, conservar evidencia y escalar/reconciliar según protocolo por acordar; no es incidente observado.

### AV-01 y valor propuesto

Sostener el flujo con evidencia consultable, custodia verificable, handoffs claros y excepciones controladas. KPI-01: 120 min IA→≤30min DE por solicitud/lote. KPI-02: 65% IA→≥95% DE por pallet, condicionado NV-05/07. KPI-03: 0% SV→≥90% DE por evento esperado. Semanas 8/16 pertenecen al eventual piloto, no a las semanas de arquitectura.


## Página 4 Trabajo gates y trazabilidad

A-04 propone seis semanas BC-S1…BC-S6 posteriores a otra autorización para Baseline/Target y gaps B/C/D, Requirements Specification y dependencias/roadmap preliminar. No se desarrolló B. Horas, acceso y recursos siguen por acordar. A-05 solo define cuatro dominios y ABB conceptuales.

Modelo fuente: 03_Architecture_Repository/03_Architecture_Landscape/Strategic/M-A02_Estrategia.png

Vistas A: motivación, estrategia, contexto y concepto; SVG editables y PNG embebidos en A-02. Mapas documentales, no ArchiMate formal. MODEL-02/03/04 de PC1 siguen planificados.

TR-01: F01/F03/F04+IA-01/SV-01 → D1/D3 → OBJ01/OUT01/KPI-01 → C4/H1 → STK-02/C01 → PR-01/03/04 y REQ-02 → VP01/VIEW-01/MODEL-01 y vistas A → DEC-01. TR-02: contexto+IA → D1/D2 → OBJ01/OUT01/KPI-02 → C3/C4 → STK-03/02 y C06 → PR-03/04 y REQ-04 → VP01/VIEW-01/MODEL-01 y vistas A → DEC-01. Ambas vuelven por Relaciones.csv con rutas; no validan las premisas.

Gates: asistente recomienda continuación conceptual/revisión con condiciones; aprobación del equipo y corporativa pendientes. Riesgos abiertos: US$265k > US$250k por 15k; secuencia 14 + 6 > 16 sin solape demostrado; fuente térmica NV-05; interfaces/red y autoridad pendientes. Ahorro bruto IA US$1.252.969/año no es ROI. Paginación DOCX pendiente de revisión; PDF ejecutivo comprobado aparte.
