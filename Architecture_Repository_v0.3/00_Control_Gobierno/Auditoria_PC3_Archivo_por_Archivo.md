> **Antecedente (no vigente).** Auditoría de entrada del ZIP v3.0, hecha antes de la reorganización PC3. Sus rutas e IDs (por ejemplo `13_Phase_C/…`, `AP-V03`, `T-V01`) son los de esa versión; no son enlaces de este repositorio. Equivalencias: `Equivalencias_ID.csv` y MANIFEST (hoja Mapa_rutas).

# PC3 · Auditoría archivo por archivo del ZIP Camposol v3.0

> **Estado (2026-11-26):** auditoría de entrada sobre el expediente v3.0 (rutas antiguas). Los hallazgos fueron atendidos en el Repository v0.3 según `CHANGELOG.md` §2; los que dependen del grupo o del modelo ArchiMate quedan en `Issue_Log.csv` (ISS-02, ISS-03, ISS-04). Las rutas citadas aquí son las del ZIP v3.0; su equivalencia está en `MANIFEST.xlsx`, hoja Mapa_rutas.


Grupo 04 · SI605 · 26-11-2026. Complementa `PC3_Lista_Ajustes_ZIP_Camposol.md`: los códigos A1…G11 y C1…C13 remiten a esa lista.

**Criterios de comparación**

- Guía PC3 v1.0 (rúbrica, §2 actividades, §4 repositorio).
- Contenido típico de cada entregable según TOGAF (Architecture Content / Deliverables).
- Técnicas ADM (principios, gap analysis, business scenarios, building blocks).
- ArchiMate 3.2.
- Fuentes de expertos ya revisadas (Google Rules of ML, CMMI, DAMA/SAP para clases de datos).

**Veredictos**

- ✅ Bien (solo actualizar versión o etiquetas).
- 🔧 Mejorar (completar o corregir dentro del mismo archivo).
- 🔁 Reestructurar (cambiar organización o fusionar en otro entregable).
- ♻️ Rehacer.
- 📦 Pasar a `/Historico`.
- ➕ Crear (no existe).

**Ajustes que aplican a casi todos los archivos** (no se repiten fila por fila):

- **T1.** Clases de evidencia: P/S/D/NV → HP/IA/SV/DE/NV(/NE). Todo DS-CS es IA (B4).
- **T2.** Nombre del VS: "VS-01 · Aseguramiento de fruta exportable" (B2). Aparece en unos 25 archivos.
- **T3.** Encabezados "Semana 10", "v3.0" y "Draft v0.3" → "PC3 · Repository v0.3" con su fecha.
- **T4.** Rutas que apuntan a `B-06_ArchiMate_Exchange.xml` o a carpetas viejas → rutas del modelo consolidado y de la nueva estructura (A6).
- **T5.** Baseline con valores IA → agregar "Baseline real = NE" y el NV que lo valida (B6).
- **T6.** Referencias a GAP-T09, T-TAR13, TS-16, T-ABB08 y TD-RC08 → "diferido (OPP-IA-01)" (F7).
- **T7.** Targets de CAP-01 y CAP-07: 4 → 3, y escala 0–4 (C7).

---

## 0. Raíz y `00_Control`

| Archivo | Qué debería contener (guía / TOGAF) | Estado actual | Veredicto | Acción |
|---|---|---|---|---|
| `LEEME_FASE_D_v3.0.md` (raíz) | README raíz: empresa, VS, alcance, equipo, versión, cómo abrir, índice de carpetas (§4.2) | Solo describe la Fase D; datos ya cambiados (9 GAP-T, gate "propuesto") | 🔁 | Sustituir por `README.md` raíz (A3) |
| `00_Control/README.md` | Igual | **Contradicción interna:** la sección "Límites" dice "Phase D no desarrollada (PD-01…07)" y abajo hay un apéndice de Phase D. Solo cifras de C | 🔁 | Fusionar en el README raíz y eliminar |
| `CONTEXTO_CONTINUIDAD_v3.0.md` | No es un entregable TOGAF | Nota de continuidad de las sesiones de IA ("Adjuntar…zip") | 📦 | Sacarlo del entregable. Registrar su existencia en el registro de uso de IA |
| `Dataset_Simulado_Chao.csv` | Evidencia clasificada con plan de validación | 51 filas DS-CS en clase S | 🔧 | Clase → IA; columnas `Baseline_real` (NE) y `NV_validacion`; mover a `09_Evidencia_Fuentes` |
| `Equivalencias_ID.csv` | Continuidad de IDs entre versiones | Buena (v0.2→v0.3, C, D) | 🔧 | Agregar IDs de la PC2 corregida (B3); renombrar EQ-xx → EQV-xx (G10); agregar VS, GAP-T09→OPP-IA-01 y ABB-01..04→ABB-C→T-ABB |
| `Fuentes_y_Evidencias.csv` | Dossier HP con URL, fecha y alcance; registro de IA con modelo, objetivo, entrada, salida, validación y límites (§4.2) | F01–F08 bien acotadas ✅. IA-07 sin los campos exigidos | 🔧 | Columna `Clase_PC3`; completar los campos de IA (B5); agregar como fuentes el informe PC2 y la guía PC3 |
| `Glosario.md` | Términos del expediente | Solo términos de B (v0.3) | 🔧 | Agregar ABB/SBB, NFR, Plateau/Gap, zona/conducto, linaje vs genealogía, SoR, HITL |
| `Inventario_artefactos.csv` | MANIFEST.xlsx con los campos de §4.2 | Completo (225/225) pero sin dominio, fase, tipo, Baseline/Target, owner, concern ni REQ/GAP | 🔁 | Convertir en `MANIFEST.xlsx` raíz (A4) |
| `Procedencia_Originales.csv` | Origen de plantillas y archivos base | Correcto | ✅ | Mover a `10_Plantillas_TheOpenGroup` |
| `Registro_Cambios_v0.3/v0.4/v3.0.md` | CHANGELOG PC1→PC2→PC3 con observación, acción, fecha, responsable y fundamento | Tres archivos sueltos; buenos verificadores automáticos | 🔁 | Unificar en `CHANGELOG.md` raíz (A5); originales a `/Historico` |
| `Reglas_de_evidencia.md` | Reglas de evidencia de la guía (HP/IA/SV/DE/NV) | Usa P/S/D/NV con rangos vencidos (DS-CS-01…12, NV-01…08) | ♻️ | Reescribir con la nomenclatura de la guía y rangos vigentes |
| `Resumen_Ejecutivo_v0.3.docx/.pdf` | Resumen ejecutivo PC3 (≤ 1 página, §3) | Solo Preliminary/A/B; VS nuevo; targets 4 | ♻️ / 📦 | Pasar a `/Historico`; el resumen nuevo va en el informe PDF |

## 1. Preliminary (`01_Preliminary`)

| Archivo | Contenido típico TOGAF | Estado actual | Veredicto | Acción |
|---|---|---|---|---|
| **PRE-01** Organizational Model + RACI | Organizaciones en alcance; madurez, gaps y resolución; roles y responsabilidades; **restricciones del trabajo de arquitectura; presupuesto**; gobierno y soporte | Alcance, 7 stakeholders, gobierno, madurez EA (EA-01…04), RACI con A único ✅, gates | 🔧 | (1) Agregar "Restricciones y presupuesto" (académico: sin presupuesto, horas del equipo, acceso a datos = NV). (2) Precisar "ERP corporativo fuera": **SAP fuera de rediseño, su interfaz IF-05/06 dentro** (hoy contradice el Target C/D). (3) Agregar G-C-D y G-D-E. (4) Confirmar con el grupo que las fechas 30-10 y 04-11 de los gates son reales; si no, poner "fecha de registro" y no "aprobado el…". |
| **PRE-02** Tailored Architecture Framework | Método adaptado; contenido adaptado (entregables y artefactos); **herramientas configuradas**; interfaces con otros marcos de gobierno | §2 desactualizado: C figura como "Siguiente" y D como "Restricciones IT/OT…"; no hay sección de herramientas | 🔁 | Reescribir §2 con el tailoring real de C (23 artefactos, C-00) y de D (8 artefactos + vistas suplementarias); IA como preocupación transversal (no quinto dominio); equivalencias de vistas guía→grupo (G5). Agregar §"Herramientas" (Archi versión x, Open Exchange 3.x, verificación automática, asistente de IA con su registro) y §"Interfaces con gobierno" (gates del curso, Architecture Board académico). §5 Clases → T1 |
| **PRE-03** Business Principles, Goals & Drivers | Principios de negocio, metas y drivers (contenido variable) | Contexto, 4 drivers, goals, outcomes, 7 KPI, escenario de exposición, restricciones ✅ | 🔧 | **Faltan los principios de negocio** que exige el nombre del entregable. Agregar 3–4 (por ejemplo, inocuidad y cumplimiento sanitario primero; decisiones basadas en evidencia medida; segregación de funciones) apoyados en HP (F05 certificaciones, F08 SENASA). El escenario de exposición (US$ 2,78 M) → etiqueta IA |
| **PRE-04** Architecture Principles | Name / Statement / Rationale / Implications; precedencia; recursos y costos; los 5 criterios | Formato correcto; PR-01/PR-04 bien retirados | 🔁 | Aplicar C1–C13 (lista): una sola versión; PR-09 sin contradicción; justificaciones sin datos IA presentados como hechos; regla de precedencia; implicaciones de recursos; PR-09/PR-10 dentro del documento; justificaciones por drivers, no por gaps ni DEC; aprobación por ROL-AB |
| **PRE-05** Request for Architecture Work | Patrocinador; misión, metas y cambios; **plazos**; restricciones de organización, **presupuesto** y externas; **descripción del sistema de negocio y TI actual**; recursos disponibles | Patrocinador, problema, objetivos, alcance, restricciones, entregables | 🔧 | (1) El campo "Solicitante académico" **está vacío**. (2) Agregar plazos (hitos PC2/PC3/PC4) y recursos. (3) Descripción breve del entorno actual solo con HP (SAP corporativo F01/F02, calibradoras F04). (4) El problema hoy cita DS-CS como hecho conocido al momento de la solicitud: redactarlo como hipótesis a validar. (5) Entregables esperados: agregar C y D (hoy solo A, B y repositorio) |
| **PRE-06** Architecture Repository | 8 clases de repositorio + Enterprise Continuum; metadatos; control | 8 clases ✅, estados, prueba de recuperación ✅ | 🔁 | Actualizar la estructura a 00–11 de la guía (A6) e incluir las carpetas de C/D; la prueba de recuperación debe apuntar al modelo consolidado y a objetos de C/D |

## 2. Phase A (`02_Phase_A`)

| Archivo | Contenido típico TOGAF | Estado actual | Veredicto | Acción |
|---|---|---|---|---|
| **A-01** Capability Assessment | Capacidad de negocio (baseline/target); **capacidad de TI**; **madurez de arquitectura**; preparación para la transformación | Capacidades de negocio con rúbrica ✅, readiness ✅, validaciones | 🔧 | T7 (targets 3, escala 0–4, justificación por dependencias). Agregar §"Capacidad de TI/OT" (baseline IA, target) y §"Madurez de la arquitectura" (referir PRE-01 §4). El texto "DS-CS-01…12" está vencido |
| **A-02** Architecture Vision | Descripción del problema (stakeholders, concerns, issues); **objetivo del SoAW**; vistas resumen (cadena de valor, **concepto de solución**, requisitos mapeados); referencia al ADD | Visión, 4D ✅, stakeholders/concerns ✅, valor KPI, vistas A01–A03, riesgos | 🔧 | Agregar VIEW-A04 (concepto de solución) en §5, el "objetivo del SoAW" y la tabla concern → REQ. Rutas → modelo consolidado. KPI con "real = NE" |
| **A-03** Communications Plan | Stakeholders agrupados; necesidades y mensajes; **riesgos y factores críticos de éxito**; mecanismos; **calendario** | Plan por audiencia ✅, registro honesto (sin reuniones simuladas) ✅ | 🔧 | Agregar calendario PC3 (gates C→D, D→E, sustentación), riesgos y FCE. Actualizar mensajes que dicen "Gate B→C" o "Antes de Phase C/D" |
| **A-04** Statement of Architecture Work | Título y antecedentes; alcance y resumen de la visión; procedimiento de cambio de alcance; roles; entregables; aceptación; plan y calendario; aprobaciones | Estructura completa ✅ | 🔁 | §2 desactualizado (C lista C-00…C-05 sin C-06; D dice "Restricciones IT/OT…"); faltan los entregables PC3 (informe, ZIP, MANIFEST, PPT). §3 calendario sin fechas. **§5 firmas con placeholders "[Nombre] [AAAA-MM-DD]"**: completar o poner "pendiente de firma docente" |
| **A-05** Draft ADD (A) | Borrador de ADD de la Fase A | Baseline/Target por dominio, ABB-01…04, REQ | 📦 | Marcar "Superseded por ADD consolidado v0.3"; mapear ABB-01…04 → ABB-C → T-ABB en Equivalencias |
| **A-06** Business Scenario | Problema (rankeado); entorno de negocio y técnico; **objetivos SMART**; actores humanos y **computacionales**; roles, responsabilidades y **medidas de éxito** | 3 escenarios (BS-01/02/03) con disparador, actores, pasos, excepciones, eventos y TEST ✅ | 🔧 | Agregar por escenario: problema y prioridad; objetivo SMART (enlazado a KPI); actores computacionales (AP-xx de C); medida de éxito por actor |

## 3. Architecture Repository (`03_…`, `04_…`)

| Archivo | Estado actual | Veredicto | Acción |
|---|---|---|---|
| `01_Metamodel/Elementos.csv` (420) | Coincide con el XML (0 faltantes) ✅ | 🔧 | T1 en `Clase_evidencia`; agregar los elementos nuevos (Plateau, Constraint RST-xx, Deliverable, OPP-IA-01 fuera del Target) |
| `Relaciones.csv` (123) | Son relaciones **documentales** de trazabilidad, no las 482 del modelo | 🔧 | Renombrar `Relaciones_Trazabilidad.csv` o aclarar en el encabezado; agregar las cadenas E2E-01/02 (G4) |
| `Viewpoint_Catalog.csv` (27) | Viewpoints A–D | 🔧 | Agregar los campos de la Actividad B (decisión que soporta, preguntas, calidad requerida) — G11 |
| `Convenciones.md` | Cadena antigua (solo B) | 🔧 | Agregar cadena C/D y convención RST, OPP, EQV |
| `02_Capability/*` | Correcto | ✅ | T3 |
| `03_Landscape/View_Catalog.csv` (28) | Fuente editable apunta a B-06; no hay pares Baseline/Target ni equivalencias | 🔁 | G5. Declararlo **registro canónico de vistas**; B-09/Vistas y C3/Viewpoint_Catalog solo lo referencian |
| Figuras B-V01…05, M-A01…04, MODEL-01 | Dibujos propios | 🔧 | Reexportar desde Archi (A7); B-V03 con el nombre del VS |
| `…/Anexo/*` | Vistas previas a v0.4 | 📦 | `/Historico` |
| `Plan_Modelos_PC1.md` | Estado de MODEL-02/03/04 | ✅ | Actualizar: MODEL-03 → T-V03/T-V05 entregados |
| `04_Standards/Principles_Register.csv` | Doble versión de PR-06; columna "Estado" duplicada | 🔁 | C1–C13 |
| `Standards_Register.csv` (16) | Duplica T1/01 | 🔧 | Unificar con T1/01 (STD + STD-T) con versión y estado (F2) |
| `05_Reference/Reference_Assets.csv` | 4 activos | 🔧 | Agregar el informe PC2, la guía PC3, TOGAF 10, ArchiMate 3.2 e ISO 42010 |
| `SI605_Guia_S4/S5.md`, `Reglas_Metodologicas_Curso.md` | Referencias del curso | ✅ | Agregar la guía PC3 |
| `Antecedentes/PC1_Corregida.docx`, `Historico_v0.2/*` | Antecedentes | ✅ | **Agregar el PDF del informe PC2 entregado** (está en el proyecto): es la evidencia de continuidad |
| `Patrones_Candidatos.md` | Patrones etiquetados como no verificados ✅ | ✅ | T1 |
| `06_Governance/Communication_Plan.csv` | Honesto: "Planificado, no enviada" ✅ | ✅ | Agregar fila de sustentación PC3 |
| `Decision_Log.csv` (49) | Completo | 🔧 | DEC-01 ("Diferida a E") → "Resuelta a nivel ABB por DEC-D10; SBB en E". DEC-D09 → Defer. DEC-D17 final. DEC nuevos: nombre del VS, targets CAP, aprobación de principios, tailoring de vistas, diferimiento de GAP-T09 |
| `Exception_Log.csv` | Sin excepciones (honesto) | ✅ | — |
| `Gates_y_Aprobaciones.md` | G-D-E "propuesta, pendiente docente" | 🔧 | Decisión final (F9); confirmar que las fechas de los gates anteriores son reales |
| `RACI.csv` | Sincronizado con PRE-01 | ✅ | — |
| `Risk_Log.csv` (20) | Bien (owner, prioridad) | 🔧 | Cerrar RSK-D07; agregar el riesgo "contenido IA no validado" con su control |
| — | **Issue Log** (exigido en §4.3 de la guía) | ➕ | Crear `Issue_Log.csv` (G8) |
| `07_…/Capability_Catalog.csv` | Targets 4 (CAP-01/07) | 🔧 | T7 |
| `Concern_Catalog.csv`, `Stakeholder_Catalog.csv`, `Estrategia_Catalog.csv`, `Medidas_Complementarias.csv` | Correctos | ✅ | T1/T2 |
| `Correspondences.csv` (10) | Solo B | 🔧 | Agregar correspondencias C/D (BO↔DOBJ, AP↔ART/nodo, NFR↔TS) |
| `KPI_Catalog.csv` | Baseline S | 🔧 | T5 |
| `Matriz_Trazabilidad.csv` (8) | Solo cadena B | 🔁 | Extender a C/D o enlazar las E2E-01/02 (G4) |
| `Requirements_Catalog.csv` (8) | **Solo REQ-B**; faltan 12 AR y 13 NFR-T | 🔁 | G2: repositorio de requisitos completo |
| `Test_Catalog.csv` (21) | **Faltan TEST-D01…06 y TEST-A01…06** (están solo en C1/C2) | 🔧 | Agregarlos (33 pruebas en total) |
| `Validaciones_Pendientes.csv` (13) | NV-01/04/05/08 con "fase de cierre: Phase C", ya vencida | 🔧 | Reprogramar a "condición del gate D→E / Phase E"; agregar prioridad y fecha límite (G9) |
| `08_Solutions/Solution_Concept_Candidates.csv` | SC-01…03 "alternativa conceptual"; I1…I5 con US$ 265k | 🔧 | Actualizar el estado de SC-01…03 tras DEC-D10 (el patrón borde–central coincide con la alternativa B a nivel ABB; el SBB sigue en E); I1…I5 → IA |
| `04_Enterprise_Continuum/Continuum_Catalog.csv` (8) | Los 4 niveles × 2 continuos, conforme a TOGAF ✅ | ✅ | Opcional: ISA-95/62443 como Industry Architecture de referencia |
| `*/Phase_C/README.md`, `*/Phase_D/README.md` | Punteros a ubicaciones canónicas (buena práctica) | ✅ | Actualizar rutas tras A6 |

## 4. Phase B (`05_Phase_B`)

| Archivo | Contenido típico (sección B del ADD/ARS; TOGAF Business Architecture) | Estado actual | Veredicto | Acción |
|---|---|---|---|---|
| **B-01** Business Architecture Definition | Baseline/Target, VS, capacidades, organización, gap, REQ, CRC, impactos | Completo, con gate B→C ✅ | 🔧 | T2, T5, T7; pasa a ser la sección B del ADD consolidado (G1) |
| **B-02** Capability Heat Map | Escala 0–4, criterio, evidencia, owner, baseline, target, delta, prioridad | Delta vacío en el Excel (sí existe en A-01 y en el CSV); targets 4 | 🔧 | T7; llenar Delta; "Baseline real NE" |
| **B-03** Value Stream × Capability | Etapas con entrada/salida/valor; matriz etapa × capacidad | 5 campos por etapa ✅, handoffs ✅ | ✅ | T2 |
| **B-04** Gap Register | Included/New/Modify/Eliminated + Resolve/Accept/Defer/Revise | Clases de building block ✅; columna "Tratamiento" | 🔧 | Normalizar "Tratamiento" a Resolve/Accept/Defer/Revise; T5; alimenta G3 |
| **B-05** Organization & Services | Organización, roles, funciones, procesos, eventos, servicios, objetos, autoridades | Completo ✅ | ✅ | T1 |
| **B-06** ArchiMate XML (A+B) | — | Sustituido por el modelo consolidado | 📦 | `/Historico` (A8) |
| **B-07** Requirements | REQ con statement, criterio, owner y TEST | ✅ | 🔁 | Fusionar en la ARS consolidada (G2) |
| **B-08** CRC | Componentes candidatos con dependencias | ✅ La hoja "Secuencia" es prioridad, no cronograma (válido en B) | ✅ | Etiquetar como "prioridad lógica, insumo para E" |
| **B-09** Views/Catalogs Register | Registro de vistas y semántica | Duplica View_Catalog; fuente B-06 | 🔧 | Dejar la semántica y referenciar View_Catalog como canónico |

## 5. Phase C (`06`–`09`)

| Archivo | Contenido típico TOGAF | Estado actual | Veredicto | Acción |
|---|---|---|---|---|
| **C-00** Control y aplicabilidad (xlsx) | Aplicable / No aplicable / Diferido con rationale (§2.1 de la guía) | 23 artefactos con justificación ✅; gate C→D ✅ | 🔧 | D-ART02 y AP-ART05 → rehacer contra BF (D1, E1); AP-ART03 → ACT (E2); **AP-ART14 Software Distribution sigue "Pendiente Phase D"**: cerrarlo (cubierto por T-V03 con artefactos y nodos) |
| **C-01** Architecture Deliverables (plantilla C/D) | Plantilla oficial con artefactos | Muy bien estructurado ✅ | ✅ | Actualizar filas de D-ART02 y AP-ART03/05 y las equivalencias de vistas |
| **C-02** ADD Phase C | Plantilla ADD: alcance; metas; principios; baseline; modelos; rationale; mapeo al repositorio; gap; impacto; transición | Sigue la plantilla TOGAF ✅ | 🔁 | **Base del ADD consolidado** (G1). §2.5.4 Tecnología vencido; §7 "Transition Architecture" con olas T0–T3 → "insumo propuesto para Fase E" (las transiciones son de E) |
| **C-03** ARS Phase C | Medidas de éxito; contratos de servicio; guías, especificaciones y estándares; interoperabilidad; ITSM; restricciones; supuestos | Sigue la plantilla TOGAF ✅ | 🔁 | **Base de la ARS consolidada** (G2) + NFR-T de T-03 |
| **C-04** Roadmap candidates C | Candidatos de roadmap de la fase | §2 ✅. **§3 "Initial Complete Version" contiene contenido de la Fase E** (portafolio de WP, matriz consolidada de gaps/soluciones/dependencias, transiciones) | 🔧 | Dejar §3 como "Reservado para Phase E (paso 9.3.3)" con solo las dependencias; no presentar portafolio ni transiciones |
| **C-05** Repository C | Actualización del repositorio | Vencido tras D | 📦 | Lo sustituye PRE-06 actualizado + MANIFEST |
| **C-06** ABB candidatos C | Especificación ABB: funcionalidad y atributos (incl. seguridad y gestionabilidad); interfaces; interoperabilidad; ABB dependientes; mapeo a entidades y políticas | Responsabilidad, datos/interfaz, AR, negocio, RC ✅; contratos entre bloques ✅ | 🔧 | Agregar atributos/NFR, ABB dependientes y principios o políticas; mapa ABB-01…04 (A) → ABB-C → T-ABB |
| **C1** Data catalogs (xlsx) | Data Entity/Component; **Data Entity/Business Function**; Application/Data; conceptual/lógico; diseminación; seguridad; ciclo de vida | Muy completo (owner/steward/custodio, linaje, calidad con meta) ✅ | 🔧 | D1 (matriz contra BF-01…06, CRUD); D2 (definición de Lot); D3 (owner = ROL); D4 (confidencialidad y retención); Gaps_Datos: decisión R/A/D/RT |
| **C2** Application catalogs (xlsx) | Portfolio; Interface; App/Org (unidad org.); Role/App; **App/Function (función de negocio)**; Interaction; Process/App | Muy completo ✅ | 🔧 | E1, E2, E3; Transicion_Apps (olas) → "insumo para E" (F8) |
| **C3** Integración (xlsx) | Trazabilidad, viewpoints, ADR, riesgos | ✅ | 🔧 | Viewpoint_Catalog → referencia al canónico; Pendientes_PhaseD → cerrados por D; Candidatos_ABB → mapa único |
| `07_Phase_C_Vistas_ArchiMate/*.xml` | — | 3 XML (A+B+C, anexo, original) superados por el consolidado | 📦 | `/Historico` (A8) |
| `07_…/Figuras` D-V0x, AP-V0x, X-V01 | Vistas exportadas | Dibujos propios | 🔧 | Reexportar desde Archi |
| `07_…/Figuras` C01…C04 | Diagramas TOGAF complementarios | C03 y C04 ilegibles (2282×185 px, 2143×248 px) | 🔧 | Renombrar DD-01…04 (G10); reacomodar en dos filas (D6) |
| `09_Phase_C_Guia_Repositorio/*` | Guía de lectura | Útil, pero apunta al XML de 16 vistas | 🔁 | Fusionar en el README raíz; el mapa de plantillas va a `10_Plantillas_TheOpenGroup` (A11) |

## 6. Phase D (`10`–`13`)

| Archivo | Contenido típico TOGAF | Estado actual | Veredicto | Acción |
|---|---|---|---|---|
| **T-00** Índice y control D | Entradas, salidas, criterios | ✅ | 🔧 | T3, T6 |
| **T-01** Plantilla oficial Phases C & D completada | Plantilla The Open Group | **Fortaleza** para el criterio "plantillas TOGAF completas" ✅ | 🔧 | Historial de versiones contradictorio ("0.5 Primera versión" frente a v3.0; portada "AGOSTO 2026") → corregirlo |
| **T-02** ADD Phase D | Plantilla ADD (ver C-02) | Muy buen contenido (baseline, target, flujo E2E PAL-55871, ABB, seguridad, gaps) pero **sin las secciones "Mapping to Repository" ni "Impact Assessment"** | 🔁 | Se convierte en §2.5.4 y §5–6 del ADD consolidado (G1); T6 |
| **T-03** ARS Phase D | Ver C-03 | Registro NFR y dimensionamiento excelentes ✅; §3 reescribe principios ❌ | 🔁 | Se fusiona en la ARS consolidada; eliminar §3 (C2); NFR-T09/TEST-T09 sin el caso visual |
| **T-04** Roadmap candidatos D | Roadmap de D como insumo para E (paso 8.3.5) | Columna "Cuándo" con meses y "Ola" | 🔧 | F8; quitar TD-RC08 (T6) |
| **T-05** Artefactos y vistas | Artefactos recomendados y su pregunta | ✅ | 🔧 | Equivalencias con las vistas de la guía (G5) |
| **T-06** ABB tecnológicos | Especificación ABB (ver C-06) | Capacidad, tipo, soportes, contrato, servicios, NFR, consumidor, conformidad, categorías SBB ✅ | 🔧 | Agregar ABB dependientes y principios o políticas; quitar T-ABB08; **agregar la tabla de alternativas SBB** (F4) |
| **T-07** IT/OT, ciberseguridad y continuidad | Zonas y conductos, controles, escenarios, pruebas | **Fortaleza** (SL-T sin afirmar cumplimiento, E1–E5) ✅ | 🔧 | Redactar CD-06 en línea con el nuevo PR-09 (mantenimiento como excepción gobernada); quitar T-TAR13 de Z-01 |
| **T-08** Ejemplos integradores I4.0 | (Didáctico, no es un artefacto TOGAF) | Ejemplo C = piloto IA diferido; **Ejemplo D Digital Twin**: no está en el Target | 🔧 | C → "Oportunidad diferida OPP-IA-01 (por qué no)". D → quitarlo o pasarlo a anexo "exploratorio, fuera del Target", porque da impresión de "primero la tecnología" |
| **T-09** Handoff D→E | Checklist, pendientes, decisiones | ✅ | 🔧 | Decisión final del gate (F9); DEC-D09 Defer |
| **T1** Catálogos D (12 hojas) | Standards; Portfolio; App/Tech; NFR; gaps; candidatos; ABB… | Completo ✅ | 🔧 | 01 (F2); 02 (F1, F3); 03 (C2); 04 (NFR-T09); 05 (GAP-T09 fuera; owner y decisión R/A/D/RT); 06 (F8); 07 (DEC-D09); 10 (CD-06); 11 (ABB); 12 |
| **T2** Trazabilidad y verificación | Trazabilidad B→C→D | 01_Trazabilidad con 6 filas sin driver/concern/principio/rutas | 🔧 | G4 (E2E-01/02 completas con ruta por eslabón); 03 y 04 sin GAP-T09; **volver a correr 07_Verificacion** tras los cambios |
| `12_…/` XML consolidado + 11 XML por vista + SVG/PNG | Modelo nativo + XML + exportaciones (§4.2) | Sin `.archimate`; nunca importado en Archi | 🔧 | Ver sección 7; A7 |
| `13_…/MANIFIESTO_ENTREGABLES_FASE_D.csv` | — | Manifiesto parcial | 🔁 | Se absorbe en MANIFEST.xlsx |
| `ESTADISTICAS_VALIDACION.json` | — | `archi_import_tested: false` | 🔧 | Regenerar tras los cambios y la importación en Archi |
| `Resumen_Gate_D_E_v3.0.pdf` | Resumen del gate | Decisión "propuesta" | ♻️ | Regenerar con la decisión final |
| `Guia_lectura…PhaseD.md` | Guía | Útil | 🔁 | Fusionar en el README raíz |

## 7. Modelo ArchiMate consolidado (27 vistas, 258 elementos, 482 relaciones)

Verificado: XML bien formado, IDs únicos, 0 referencias rotas, todos los elementos en Elementos.csv. Hallazgos:

| # | Hallazgo | Norma | Acción |
|---|---|---|---|
| M1 | No hay Plateau, Deliverable, Constraint ni Assessment | ArchiMate cap. 12: un Gap se asocia a dos Plateaus | G7, C5. Opcional: Assessment entre Driver y Goal con el hallazgo IA |
| M2 | Solo los GAP-T son elementos; los GAP-B/D/A no | Consistencia | Modelarlos o justificarlo en el tailoring (G7) |
| M3 | AP→AI con *Assignment* | ArchiMate: la interfaz es parte del componente (Composition) | E5 |
| M4 | Path (conductos) sin *Realization* desde CommunicationNetwork; asociado a Grouping | Patrón técnico de la especificación | F6 |
| M5 | Work Packages encadenados con *Triggering* | Secuencia = planificación de E/F | F8 |
| M6 | Faltan vistas Baseline: diseminación, procesos-aplicaciones, despliegue, red | Guía §4.5 | D5, E4, F5 |
| M7 | X-V02 sin motivación, gap ni WP | Guía §4.5 | G6 |
| M8 | Elementos de GAP-T09 dentro del Target | Requirements-Based Change | F7 |
| M9 | Sin `propertyDefinitions` (clase de evidencia, fase, estado por elemento) | Guía §1.3 "evidencia por elemento" | Agregar las propiedades `Evidencia`, `Fase_ADM`, `Estado` (se ven en Archi) |
| M10 | 23 elementos sin documentación | Calidad | Completar |
| M11 | Sin `organizations` (carpetas) | Usabilidad en Archi | Opcional: carpetas por capa o fase |
| M12 | Nombre del VS-01 | Continuidad | T2 |

## 8. Archivos nuevos que hay que crear (➕)

`README.md`, `MANIFEST.xlsx`, `CHANGELOG.md` (raíz) · ADD consolidado B/C/D · ARS consolidada · Gap Register unificado B/C/D (insumo para E) · Matriz E2E-01/02 con rutas · `Issue_Log.csv` · `Oportunidades_Diferidas.csv` (OPP-IA-01) · Registro de uso de IA completo · Tabla de alternativas SBB · `Camposol_PC3_v0.3.archimate` · Índice de plantillas I094 · Sección "Revisión interna PC2→PC3" (OBS-PC2-00) · Vistas Baseline nuevas (D-V03B, AP-V02B, T-V11, red Baseline) y X-V02 de impacto · PPT de sustentación · Informe PDF v0.3.

## 9. Balance

| Veredicto | Cantidad aproximada de archivos o grupos |
|---|---|
| ✅ Bien (solo T1–T7) | 25 |
| 🔧 Mejorar | 48 |
| 🔁 Reestructurar o fusionar | 17 |
| ♻️ Rehacer | 4 (Reglas de evidencia, Resumen ejecutivo, Resumen del gate, y PRE-04 en lo textual) |
| 📦 A histórico | 8 grupos (XML viejos, anexos de vistas, registros de cambio, C-05, A-05, B-06, CONTEXTO) |
| ➕ Crear | 16 |

**Fortalezas que conviene destacar en la sustentación:**
- verificación automática y trazabilidad por ID;
- linaje frente a genealogía;
- owner, steward y custodio;
- T-07 (zonas, conductos y SL-T sin afirmar cumplimiento);
- NFR con dimensionamiento y prueba;
- plantilla oficial C/D completada;
- registro de comunicaciones honesto;
- Enterprise Continuum en sus 8 niveles.

**Riesgos que más restan si no se corrigen:**
1. falta el `.archimate`;
2. no hay MANIFEST, CHANGELOG ni README en la raíz;
3. PR-09 se contradice a sí mismo;
4. las matrices TOGAF cruzan contra lo que no corresponde;
5. GAP-T09;
6. hay contenido de la Fase E dentro de C y D;
7. ADD y ARS fragmentados;
8. faltan las vistas Baseline;
9. hay datos IA presentados como hechos en las justificaciones.
