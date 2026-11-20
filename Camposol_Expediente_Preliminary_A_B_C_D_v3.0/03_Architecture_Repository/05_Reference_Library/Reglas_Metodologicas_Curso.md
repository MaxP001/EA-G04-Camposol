# Reglas metodológicas SI605 · Sesiones 01–05

Este archivo separa reglas expresadas por las sesiones, condiciones particulares de sus ejemplos, restricciones de la solicitud actual y recomendaciones propias. No transforma ejemplos en obligaciones universales ni desarrolla entregables de Camposol.

## Fuentes

| Clave | Markdown |
|---|---|
| S1 | `SI605_Sesion01_2026-2 v1.0.md` |
| S2 | `SI605_Sesion02_2026-2 v1.3.md` |
| S3 | `SI605_Sesion03_2026-2 v1.1.md` |
| S4 | `SI605_Sesion04_v3.1.md` |
| S5 | `SI605_Sesion05_2026-2_v3.3.md` |

Las citas usan líneas físicas del Markdown, contadas desde 1 e incluidos los blancos; no corresponden necesariamente a páginas. Los títulos y rangos se pueden contrastar con el [Registro_Lectura.md](Registro_Lectura.md).

## A. Reglas explícitas del material

### A.1 Problema, valor, alcance y evidencia

| ID local de esta síntesis | Regla del material | Consecuencia para revisar un trabajo | Fuente |
|---|---|---|---|
| RC-01 | Identificar el problema correcto antes de proponer tecnología. | Cada propuesta puede explicarse desde driver, outcome y capability gap o requirement. | S1 L41–43, L197–211; S2 L71; S5 L27 |
| RC-02 | Mantener un solo value stream estratégico por grupo. | Nombre, stakeholder, trigger, resultado, límites, etapas, valor y KPI explícitos; evitar nombres de proyectos tecnológicos. | S1 L641; S2 L365–393 |
| RC-03 | No confundir capacidad con proceso, área, aplicación o proyecto. | El mapa expresa habilidades relativamente estables; las realizaciones se describen aparte. | S1 L295; S2 L395–419; S5 L411–423 |
| RC-04 | Distinguir cadena de valor, value stream y proceso. | No sustituir el value stream por un BPMN detallado. La plantilla S2 plantea 5–8 etapas de alto nivel. | S2 L325–393; S5 L489–501 |
| RC-05 | Separar evidencia pública, síntesis didáctica y decisión arquitectónica. Lo plausible no se vuelve hecho por aparecer en un diagrama. | Conservar origen y estatus de cada afirmación; no atribuir arquitectura interna real a una propuesta docente. | S1 L237–273, L337–339; S2 L487–571; S4 L1175–1191 |
| RC-06 | Los valores numéricos de requisitos se acuerdan con stakeholders. | No derivar una meta del simple potencial de una tecnología. La ficha de KPI requiere fuente, owner y frecuencia, además de Baseline, Target y horizonte. | S1 L427–443; S2 L233–249 |
| RC-07 | Delimitar el sistema antes de modelar. | Explicitar inclusiones, exclusiones y dependencias; revisar breadth, depth, time period y domains. | S3 L543–565; S4 L603–627, L915–943 |

Los IDs RC de este archivo son etiquetas editoriales para organizar reglas; no son identificadores oficiales del curso o de un expediente empresarial.

### A.2 Descripción, trazabilidad y cambios

| ID | Regla del material | Consecuencia para revisar un trabajo | Fuente |
|---|---|---|---|
| RC-08 | Elegir instrumentos por propósito y decisión. | TOGAF desarrolla/gobierna; ISO 42010 organiza calidad y trazabilidad de la descripción; ArchiMate integra EA; BPMN/UML aportan detalle especializado. | S3 L155–185, L235–335 |
| RC-09 | Los concerns preceden a las views. | Identificar stakeholder y pregunta; especificar viewpoint antes de construir la representación concreta. | S3 L387–463, L685–711 |
| RC-10 | Comprobar cobertura y coherencia de la AD. | Concern con viewpoint; viewpoint con view; model conforme a model kind; correspondences explícitas; inconsistencias registradas y rationale de decisiones clave. | S3 L483–497 |
| RC-11 | Mantener identificadores y referencias entre documentos del mismo expediente. | Drivers, goals, capacidades, stakeholders, concerns, principios, requisitos, vistas y decisiones deben poder seguirse entre fases. | S4 L1047–1071, L1919–1963 |
| RC-12 | ADM es iterativo y los cambios se controlan. | Iterar dentro de fase, entre fases o entre ciclos dejando traza en requirements, decisions y Repository. | S4 L149–173 |
| RC-13 | Tailoring explícito, justificado y repetible. | Definir método, contenido, herramientas, gobierno y cadencia; justificar omisiones/simplificaciones sin romper trazabilidad. | S4 L175–201, L401–435 |
| RC-14 | Repositorio acumulativo con evidencia recuperable. | Reutilizar canvas, AD Plan, matrices, principios, Vision, decisiones y modelos; guardar el editable e integrarlo/referenciarlo desde ADD. | S4 L437–491; S5 L1175–1193 |
| RC-15 | Cada artifact responde una pregunta arquitectónica y apoya una decisión. | Evitar documentos sin uso decisorio o sin relación con concerns y evidencia. | S5 L183, L735–753 |
| RC-16 | Las relaciones ArchiMate tienen significado. | Distinguir Assignment, Realization, Serving, Access y Triggering según tipos y propósito; un enlace de trazabilidad no prescribe una flecha única. | S5 L665–691; distinción final como síntesis de S3 L497 y estas relaciones |

### A.3 Preparación y límites por fase

| Fase/contenido | Exigencia del material | Límite y revisión | Fuente |
|---|---|---|---|
| Preliminary | Definir organización/gobierno, adaptar framework, herramientas, principios y Repository; disponer de Request. | Preparar Architecture Capability, sin confundirla con las capacidades del negocio que luego se analizarán. | S4 L243–363 |
| Organizational Model | Scope organizacional, madurez, gaps/resolución, roles/RACI, restricciones, presupuesto, gobierno y soporte. | La plantilla requiere más que organigrama; versión mínima incluye sponsor, Board, arquitecto líder, leads, reviewers y cadencia. | S4 L365–399 |
| Architecture Principles | Name, Statement, Rationale e Implications. | La regla y sus consecuencias deben orientar decisiones; los ejemplos no son automáticamente el catálogo del proyecto. | S4 L513–537, L629–649 |
| Request | Explicar necesidad, decisión que se espera habilitar y límites iniciales. | No prescribe solución técnica ni equivale al Statement of Work. | S4 L539–571 |
| Phase A | Alinear valor, stakeholders, concerns, resultados, scope, riesgos y preparación; acordar trabajo posterior. | Target conceptual. Vision es parte del paquete junto a assessment, comunicaciones, Work y artefactos/registros enlazados. | S4 L675–811, L997–1045 |
| Scope | Breadth, depth, time period, domains; in/out y dependencias. | Una dependencia externa se coordina aunque no se diseñe dentro del alcance. | S4 L603–627, L915–943 |
| Capability Assessment y readiness | Examinar capacidades de negocio, TI/arquitectura, desempeño, impactos, madurez, preparación, riesgos y acciones. | No reducirlo a un mapa o puntuaciones sin respaldo. | S4 L853–887 |
| Business Scenario | Problema/oportunidad, actores, outcomes y requisitos. | Usarlo para hacer verificables los concerns, sin presentar el escenario como hecho externo. | S4 L889–913 |
| Statement of Work | Trabajo, responsables, entregables, plan, cambios, métricas, criterios/procedimiento de aceptación y approvals. | Acordar cómo se autoriza y acepta el trabajo, no solo describir una visión. | S4 L963–995 |
| ArchiMate en A | Motivación, estrategia, contexto, capacidades/value stream y concepto de alto nivel. | Evitar detalle prematuro, vendor lock-in y sustituir método por notación. La sesión recomienda vistas y formatos PPT/XML/MMD para su entrega. | S4 L1073–1137, L1965–1981 |
| Phase B | Baseline/Target, capabilities, valor, organización/servicios, gaps, business requirements, vistas y candidatos. | No seleccionar producto/proveedor, modelo físico, API concreta, base de datos, cloud/edge específico ni topología final. | S5 L87–123 |
| Arquitectura acumulativa | B incrementa ADD y refina Requirements; cada salida se guarda y reutiliza. | Requirements Management y Repository acompañan todas las decisiones. | S5 L133–219, L693–715 |

### A.4 Comparación, gaps, requisitos y candidatos

1. **Fijar comparabilidad:** misma unidad y granularidad en Baseline y Target; criterio desde principle, outcome, requirement o KPI. [S5, L237–323].
2. **Registrar evidencia antes de prioridad:** Baseline respaldada, Target explícito y delta describible. [S5, L325–337].
3. **Clasificar:** Included/Retain, New y Eliminated; MODIFY se marca como ayuda pedagógica del curso. Las celdas New y Eliminated no son proyectos. [S5, L289–355].
4. **Evaluar impacto:** valor, riesgo, criticidad, dependencias, esfuerzo y urgencia. El delta mayor no siempre merece prioridad mayor. Owner, prioridad y rationale quedan documentados; el heatmap resume. [S5, L357–373].
5. **Decidir tratamiento:** Resolve crea/refina requirement y candidato; Accept conserva rationale/riesgo; Defer fija trigger o revisión; Revise Target provoca iteración. [S5, L375–389].
6. **Gobernar el gap:** ID, unidad, Baseline/evidencia, Target/criterio, decisión, owner, prioridad, dependencias, requisito, aceptación, candidato y estado. [S5, L391–409].
7. **Respaldar el score:** escala, criterio, evidencia, owner, Baseline, Target y prioridad. La escala 0–4 de S5 distingue inexistente, ad hoc, repetible parcial, gestionada e integrada/medida. [S5, L441–467].
8. **Escribir requisitos verificables:** statement, owner, trazabilidad y criterio de aceptación. El ejemplo split/merge permite observar procedencia y ausencia de identidades huérfanas. [S5, L859–875, L1079–1097].
9. **Mantener CRC como candidatos:** agrupar por outcome/dependencia, conservar Gap IDs/REQ y consolidar posteriormente con C/D en E; no atribuirles solución final, presupuesto, cronograma o aprobación de proyecto. [S5, L717–733, L1099–1133].

## B. Criterios explícitos de revisión y continuidad

| Revisión | Condiciones que se comprueban | Resultado o alcance | Fuente |
|---|---|---|---|
| Preliminary→A | Roles y governance, Repository accesible, herramientas/notaciones, principios iniciales aprobables, drivers, tailoring y Request con sponsor/necesidad/límites. | Preparación mínima para iniciar trabajo gobernable. | S4 L655–673 |
| Cierre de A | Vision, Work, comunicaciones, assessment; catálogos/matrices, vistas, requisitos iniciales, riesgos/decisiones, Repository y approvals. | No basta mostrar el documento Vision. | S4 L997–1045 |
| Gate A, ejemplo T&G | Sponsor acepta problema/visión/resultados; Board revisa cuatro dimensiones de scope; concerns cubiertos; evidencia pendiente explícita; contrato, calendario, cambios y pruebas acordados. | Aprobar, pedir ajustes o detener; el ejemplo permanece Draft y no acredita aprobación corporativa. | S4 L1847–1875 |
| Sustentación | Explicar por qué cada decisión responde a drivers, concerns, principles y requirements. | Una colección de diagramas no demuestra por sí sola comprensión. | S4 L1919–1963 |
| Gate B→C | Baseline/Target comparables; mapa/heatmap de capacidades; value stream objetivo; services/organization; gaps→requirements; vistas, Repository y rationale; suficiencia/consistencia/trazabilidad. | Aprobar Phase C, aprobar con condiciones o devolver a refinamiento. | S5 L1217–1265 |

Las condiciones del gate A se presentan en la sesión dentro del ejemplo T&G. Pueden orientar la comprensión del método, pero sus roles nominales, códigos y calendarios no se imponen a otra empresa.

## C. Actividades y productos expresamente anunciados

| Sesión | Actividad o producto solicitado | Referencia |
|---|---|---|
| 1 | Empresa agroexportadora, un value stream, problema/oportunidad, alcance preliminar y dossier inicial. | S1 L629–643 |
| 2 | Práctica de dos horas: Strategic Alignment Canvas de caso global resumido; aplicación posterior a empresa real con evidencia y mayor detalle. | S2 L697–741 |
| 3 | Architecture Description Plan v0.1 como producto de la práctica posterior. | S3 L719–759 |
| 4 | Preliminary packet, Phase A packet y modelos de visión; completar el caso del grupo y dejar expediente PC1 listo. Formatos docentes: PPT, XML de intercambio y fuentes MMD. | S4 L27–29, L1135, L1977–2011 |
| 5 | Paquete de cierre de B: ADD incrementada, business requirements, Gap Register, CRC, vistas/catálogos y Repository para revisión B→C. | S5 L1217–1265 |

S5 no desarrolla en su texto leído una actividad temporizada adicional equivalente al canvas de S2. Sus referencias a guía detallada y expediente no permiten inventar instrucciones de evaluación no incluidas.

## D. Reglas particulares de ejemplos y estatus de evidencia

- **T&G S2/S3:** la evidencia pública se distingue de síntesis y decisiones. Sus matrices de concerns, viewpoints y heatmap son didácticas y requieren validación para representar una empresa real. [S2, L487–671; S3, L569–637].
- **T&G S4 Anexo H:** los H se usan como datos establecidos del ejercicio, sin condicionales dentro de ese escenario; su origen hipotético se conserva y no representan resultados oficiales de T&G. H no equivale a supuesto libre añadido por un equipo. [S4, L2025–2057].
- **T&G S5:** H-01…H-22 son sintéticos y operativos dentro del escenario docente. El anexo completo no está incorporado al Markdown S5; no se reconstruye su contenido faltante. [S5, L1265].
- **AgroGlobal Apples S2:** nombres y cifras creados con fines educativos. [S2, L697–737].
- **Danper S1:** propuesta de arquitectura de aprendizaje a partir de afirmaciones públicas; integración e inventario interno no observables no se presentan como hechos. [S1, L237–273, L337–339].
- Las contradicciones entre cuerpo y anexo de S4 permanecen abiertas: no se mezclan metas ni se impone una precedencia editorial no declarada. Véase Registro. Este último tratamiento es una decisión de lectura exigida por el usuario, no una nueva regla textual del curso.

## E. Restricciones expresas del usuario para esta etapa

Estas reglas proceden de la solicitud pegada, no se atribuyen a los cinco Markdown:

1. Leer completos y en orden los cinco archivos, incluidos anexos, tablas, actividades y revisión; recuperar cualquier truncamiento y registrar cobertura.
2. Revisar AGENTS.md aplicables antes de comenzar; informar faltantes o versiones distintas sin selección silenciosa.
3. Producir únicamente los cuatro Markdown de la carpeta de apoyo `00_Contexto_Curso`, con referencias verificables.
4. No modificar originales ni entregables del proyecto; no desarrollar Phase A/B de Camposol; no hacer commit/push.
5. No transferir problemas, cifras, puntuaciones o identificadores de T&G/Del Monte a Camposol ni mezclar catálogos de distintos casos.
6. Diferenciar dato simulado aceptado, supuesto de equipo, escenario generado por IA y hecho comprobado. No atribuir origen IA si el material no lo establece.
7. Desconocido no significa cero ni deficiencia. No calcular gaps numéricos sin Baseline evaluada; un score H permite análisis del escenario, no diagnóstico de la empresa real.
8. Marcar interpretaciones/conocimiento externo y no completar contenidos ausentes como si se hubieran leído. La etapa no requiere investigación web.

## F. Recomendaciones propias de organización y control

Son recomendaciones de esta síntesis, no reglas oficiales nuevas ni requisitos ya aprobados para Camposol:

- Identificar cada elemento por caso, ID y versión; compartir códigos entre documentos de un mismo expediente y evitar cruces accidentales entre expedientes.
- Mantener ficha de evidencia con origen, fecha/versión, alcance, estatus P/H/supuesto/IA, responsable de validación y enlace al elemento que respalda.
- Registrar «no evaluado» cuando falte evidencia. Separar explícitamente esa condición de nivel 0 de la escala y de un gap confirmado.
- Documentar cambios de granularidad entre sesiones: por ejemplo siete etapas de S2 frente a seis stages de S4/S5, sin asumir equivalencia exacta.
- Antes de aceptar un requisito de prueba, concretar población/muestra, procedimiento, evidencia y responsable de aceptación cuando el material solo enuncia el resultado esperado.
- Registrar contradicciones con ambas referencias, impacto y pregunta pendiente; no resolverlas promediando valores o favoreciendo silenciosamente el anexo.
- Antes de modelar un enlace documental en ArchiMate, identificar qué significa, los tipos de sus extremos y la relación admisible. Para validar diagramas, consultar después el XML y las fuentes visuales de la versión correcta.
- Mantener un inventario de ADD, Requirements, modelos y registros con estado y referencias cruzadas; una aprobación debe dejar decisión, condiciones y owner reconocibles.
