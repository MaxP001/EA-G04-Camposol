# **GUÍA PRÁCTICA SESIÓN 4**

TOGAF ADM fase Preliminary y fase A Architecture Vision

De la capacidad de arquitectura al encargo aprobado

Caso práctico Del Monte Fresh Division y piña de Costa Rica

Ruta de trabajo de la sesión práctica de 120 minutos · viernes 2 de octubre de 2026 · 20:00 a 22:00

| 1 Continuidad | 2 Capacidad EA | 3 Repositorio | 4 Continuum | 5 Preliminary | 6 Phase A | 7 Gate |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| AD Plan v0.1 | Roles y tailoring | Ocho clases | Reuso trazable | Solicitud | Visión y trabajo | Revisión |

Producto de la sesión: expediente inicial Preliminary y Phase A con repositorio navegable, clasificación en el Enterprise Continuum y vínculos al Architecture Description Plan de la sesión 3\. El expediente completo se consolida después del taller según el plazo que indique el docente.

| Dato | Definición |
| :---- | :---- |
| Curso | SI605 Arquitectura Empresarial |
| Horario | 20:00 a 22:00, inmediatamente después de la teoría de 18:00 a 20:00 |
| Duración | 120 minutos de trabajo guiado |
| Modalidad | Equipos sobre el mismo caso Del Monte de las prácticas anteriores; posterior transferencia a la empresa del Proyecto Integrador |
| Alcance | Un solo value stream estratégico: lotes de piña desde campo hasta despacho de exportación |
| Regla de evidencia | HP hecho público; DS dato simulado del caso; DE decisión del equipo; NV dato por validar |

# **1 Propósito y resultados esperados**

Al terminar, el equipo habrá preparado la capacidad mínima para gobernar un ciclo de arquitectura, clasificado activos reutilizables y definido una Architecture Vision suficiente para orientar las fases B, C y D. Preliminary establece el modo de trabajar; Phase A acuerda el problema, el valor, el alcance y el trabajo posterior. Los documentos y catálogos conservan identificadores, responsables, versión y evidencia.

| Resultado | Evidencia mínima |
| :---- | :---- |
| Continuidad | AD Plan v0.1 de la sesión 3 enlazado a concerns, viewpoints y decisión. |
| Nivel empresa | Modelo organizacional, principios, tailoring, gobierno y repositorio de ocho clases. |
| Enterprise Continuum | Clasificación de al menos cuatro activos de arquitectura y cuatro de soluciones, con origen, adaptación y ubicación. |
| Preliminary | PRE-01 a PRE-06 en versión inicial, con Request for Architecture Work. |
| Phase A | A-01 a A-06 en versión inicial; Vision, Communications Plan, Statement of Architecture Work y gate. |
| Trazabilidad | Driver → goal/outcome → concern → capability → principio → requirement → view → decisión → archivo. |

# **2 Empresa y caso de análisis**

## **2.1 Continuidad con las sesiones anteriores**

Use exactamente el sistema de interés y la decisión trabajados en la sesión 3: trazabilidad de los lotes de piña de la operación de Costa Rica de Del Monte Fresh Division. Recupere el driver, outcome, KPI, value stream, stakeholders, concerns, viewpoint card, views previstas y Architecture Decision Record. Si el equipo modificó la decisión, conserve su rationale y registre el cambio. No amplíe el alcance a toda Del Monte.

## **2.2 Base de evidencia y datos del ejercicio**

Conserve el dossier HP/DS/DE de la guía de la sesión 3\. A efectos del ejercicio, los datos DS proporcionados allí se aceptan como base del escenario, pero el expediente debe identificarlos como simulados. El caso T\&G de la teoría muestra el modo de producir un expediente; sus métricas y decisiones pertenecen a otro caso. Las afirmaciones adicionales sobre Del Monte real que no tengan fuente se registran como DS o NV.

| Indicador DS de sesión 3 | Base | Meta o referencia del caso |
| :---- | :---- | :---- |
| Lotes de exportación al año | 12 000 | Volumen de referencia |
| Conformidad en primera liberación | 89 % | ≥95 % |
| Trazabilidad digital completa campo–despacho | 68 % | ≥98 % |
| Tiempo para reconstruir historial de lote | 95 minutos | ≤30 minutos |
| Eventos completos de cadena de frío | 62 % | ≥95 % |
| Lotes en hold o retrabajo | 9 % | ≤4 % |

También se mantienen DS01–DS07: cinco soluciones separadas para eventos; cambios de identificador; conciliación manual diaria; autonomía local del packing ante desconexión; necesidad de reconstrucción rápida; prohibición de conexiones directas desde Internet a equipos industriales; y owner, versión y fuente para cada elemento arquitectónico. La iniciativa I1 de referencia tiene límite de US\$250 000 y 16 semanas; estimación DS: US\$220 000, 14 semanas, trazabilidad cercana a 90 % y consulta cercana a 35 minutos. El equipo debe explicar que I1 no alcanza todavía las metas finales de 98 % y 30 minutos.

## **2.3 Dossier complementario para Preliminary y Phase A**

Los datos DS08–DS22 siguientes se entregan como documentos internos simulados recibidos al inicio del taller. Se usan como verdaderos dentro del ejercicio y se citan por ID. La combinación de HP y DS no autoriza a atribuir roles, sistemas, cifras o decisiones a la compañía real.

| ID | Información simulada entregada al equipo | Implicación para la arquitectura |
| :---- | :---- | :---- |
| DS08 | La Dirección Fresh Costa Rica solicita reducir el tiempo de respuesta a reclamos por lote y proteger la conformidad de exportación. Designa un sponsor del programa. | Business directive y Request for Architecture Work. |
| DS09 | Un Comité de Transformación mensual incluye dirección de operaciones, calidad, exportación, TI, OT y finanzas. Ninguno tiene aún una función formal de Architecture Board. | Diseñar gobierno y RACI sin confundir el comité existente con la función nueva. |
| DS10 | Arquitectura empresarial tiene madurez 1/4: dos analistas producen diagramas por proyecto, sin principios comunes ni proceso de revisión. Meta inicial 3/4 en dos ciclos ADM. | Organizational Model, gaps, soporte y capability assessment. |
| DS11 | El sponsor autoriza para Phase A una bolsa de 80 horas de arquitectura durante cuatro semanas, con participación parcial de cinco responsables de dominio. No autoriza implementación. | Tailoring, calendario, recursos y alcance del Statement. |
| DS12 | Campo usa Registro A; packing, MES local B; calidad, sistema C; frío, plataforma D; exportación, sistema E. Los nombres son alias del caso. Hay archivos CSV diarios como interfaz temporal. | Landscape Baseline conceptual, data lineage, risks y requirements. |
| DS13 | El MES local B puede operar hasta 8 horas sin conexión corporativa; la sincronización de eventos se reintenta después. La regla actual de conciliación de conflictos no está documentada. | Principio de resiliencia, escenario de excepción y open issue. |
| DS14 | Un identificador de cosecha H, un ID de lote de packing P y un ID de pallet X no comparten una tabla de correspondencia gobernada. Calidad reconcilia muestras manualmente. | Principio de identidad, requisitos y posible ABB de linaje. |
| DS15 | Calidad define lote liberado; exportación define pedido despachable. Una discrepancia entre ambos estados bloquea el despacho hasta revisión. | Stakeholder concerns, correspondences y decisión de gobierno. |
| DS16 | El CIO propone reutilizar un patrón corporativo de identidad y eventos empleado en otra división. Documentación técnica disponible, aplicabilidad a piña aún no evaluada. | Common Systems Architecture; referencia candidata, no solución implantada. |
| DS17 | Un patrón sectorial de trazabilidad alimentaria describe lote padre, sublotes, eventos de calidad y transferencia de custodia. No contiene procesos específicos de Del Monte. | Industry Architecture y adaptación Organization-Specific. |
| DS18 | Un proveedor mostró un servicio de mensajería, pero no hay evaluación de seguridad, costo o integración OT ni decisión de adquisición. | Solutions Continuum como candidato; evitar selección prematura. |
| DS19 | Calidad es dueña de la definición de liberación; operaciones es dueña de eventos de packing; datos/TI custodia definiciones y linaje; OT custodia disponibilidad del control local. | Stewardship, RACI, communications y requirements. |
| DS20 | Riesgos priorizados: pérdida de enlace H–P–X, duplicación tras reconexión, acceso no autorizado a OT, atraso de inspección y resistencia al cambio de registro. | Risk Log, principios, escenario y readiness. |
| DS21 | El comité requiere una revisión de arquitectura en semanas 2 y 4 de Phase A. La autorización para B/C/D depende de Vision, Statement, riesgos y responsables. | Gates, criterios de aceptación y decision log. |
| DS22 | No se dispone de topología de red, inventario de interfaces completo ni datos observados de 2026 por mercado. | NV explícitos; trabajo de descubrimiento en B/C/D. |

## **2.4 Tarjeta de encargo entregada por el sponsor del caso**

| Campo | Dato DS que debe transformar el equipo en PRE-05 |
| :---- | :---- |
| Solicitante | Sponsor Fresh Costa Rica designado en DS08; nombre personal no especificado. |
| Pregunta | ¿Qué capacidades, definiciones de datos e interfaces se necesitan para elevar la trazabilidad de los lotes de piña, sostener calidad y operar durante desconexiones? |
| Value stream | Piña de campo a despacho de exportación; un único flujo. |
| Resultado esperado | Vision que vincule metas DS, requisitos y riesgos con un plan de arquitectura viable. |
| Límites | Phase A 4 semanas y 80 horas; piloto I1 de referencia sujeto a evaluación posterior. |
| Decisión solicitada | Autorizar Phase A; posteriormente decidir B/C/D según gate de DS21. |

| Código | Ejemplo de uso | Regla |
| :---- | :---- | :---- |
| HP | Fuentes corporativas de la actividad y cadena de suministro | Conservar URL, fecha y afirmación acotada. |
| DS | Indicadores y panorama interno dados en sesión 3 | Usar como hechos del escenario académico; no atribuirlos a la empresa real. |
| DE | Principio, alcance, alternativa o decisión del equipo | Registrar owner, justificación, impacto y versión. |
| NV | Inventario de aplicaciones o responsable real no disponible | Indicar acción de validación y efecto sobre Phase B/C/D. |

# **3 Resumen operativo de la sesión teórica**

| Concepto | Qué significa aquí | Comprobación |
| :---- | :---- | :---- |
| Preliminary | Establece Architecture Capability, principios, gobierno, método adaptado y repositorio. | ¿Quién decide, bajo qué reglas y dónde queda cada activo? |
| Architecture Repository | Estructura física y lógica para guardar, versionar y recuperar activos. | ¿Se puede localizar PRE-04, VIEW-01, REQ-02 y DEC-01? |
| Enterprise Continuum | Clasifica patrones desde genéricos hasta específicos en Architecture y Solutions Continuum. | ¿Qué se reutiliza, adapta o aún debe diseñarse? |
| Phase A | Construye la visión compartida y define el trabajo de arquitectura. | ¿Qué problema, valor, scope, stakeholders y gate se acuerdan? |
| Deliverable y artifact | Documento formal revisable frente a catálogo, matriz o vista que lo sustenta. | ¿Cuál es el documento y qué archivos fuente lo prueban? |

La clasificación del Continuum no reemplaza las carpetas del Repository. Un mismo activo tiene ubicación, versión y owner en el repositorio, y una clasificación de reuso en el continuum. Un ABB expresa una capacidad arquitectónica lógica; un SBB o producto concreto puede aparecer más adelante, si existe evidencia.

# **4 Plan de trabajo de 120 minutos**

| Hora | Min | Actividad | Acción principal | Salida del taller |
| :---- | :---- | :---- | :---- | :---- |
| 20:00–20:10 | 10 | A Continuidad | Recuperar AD Plan, distribuir roles y revisar DS08–DS22. | Ficha de alcance e IDs. |
| 20:10–20:30 | 20 | B Capacidad y tailoring | RACI, principios, método, gobierno y Request. | PRE-01 a PRE-05 inicial. |
| 20:30–20:53 | 23 | C Repository y Continuum | Crear clases, inventario, clasificación y ruta de un activo. | PRE-06 y Continuum. |
| 20:53–21:18 | 25 | D Phase A problema y visión | Escenario, capacidades, alcance y Target conceptual. | A-01, A-02 y A-06. |
| 21:18–21:40 | 22 | E Plan y encargo | Comunicaciones, definición inicial y Statement. | A-03, A-04, A-05. |
| 21:40–21:55 | 15 | F Gate y trazabilidad | Verificar cadenas, registrar decisión y condiciones. | Decision Log y gate. |
| 21:55–22:00 | 5 | G Cierre | Demostrar rutas y asignar pendientes. | Índice y responsables. |

La práctica de dos horas produce versiones iniciales verificables. El equipo consolida después los doce documentos, catálogos, matrices y vistas antes de la entrega formal que indique el docente. La sesión no pretende diseñar la arquitectura detallada de B, C o D.

# **5 Actividades de trabajo**

## **Actividad A Recuperar el caso y fijar el perímetro**

Tiempo: 10 minutos (20:00–20:10). Entrada: Architecture Description Plan v0.1 de la sesión 3 y dossier HP/DS. Salida: una ficha común para todas las piezas siguientes.

### **Paso A1 Confirmar la unidad de análisis**

Escriba empresa, unidad, producto, value stream único, trigger, inicio, fin, stakeholder receptor y outcome. Defina breadth, depth, período y dominios. Mantenga el foco de lote y packing/dispatch del caso.

### **Paso A2 Importar identificadores**

Reutilice DRV, GOAL, OUT, CAP, STK, CON, VP, VIEW, REQ y DEC de la sesión 3\. Si cambia un ID, registre equivalencia y razón; no rompa enlaces anteriores.

| Campo | Respuesta del equipo |
| :---- | :---- |
| Value stream y límite IN/OUT |  |
| System of Interest y interfaces |  |
| Driver, outcome y KPI |  |
| Decisión vigente y concern crítico |  |
| Fuentes HP y datos DS reutilizados |  |

## **Actividad B Instalar la Architecture Capability y adaptar el ADM**

Tiempo: 20 minutos (20:10–20:30). Salida: PRE-01 a PRE-05 en borrador. Los roles son funcionales para el ejercicio y no representan un organigrama oficial de Del Monte.

### **Paso B1 Modelo organizacional PRE-01**

Asigne sponsor, Architecture Board, lead architect, responsables de negocio, datos, aplicaciones, tecnología/OT y custodio del repositorio. Para solicitar, elaborar, revisar, aprobar y custodiar, marque R, A, C o I; cada decisión debe tener un A inequívoco.

### **Paso B2 Tailoring PRE-02**

Justifique un solo value stream, Phase A completa, B/C/D iterativas, notaciones y productos mínimos. Declare checkpoints, versiones, principios, criterios de calidad y tratamiento de incertidumbre. No transforme una preferencia de herramienta en un requisito de negocio.

### **Paso B3 Contexto y principios PRE-03 y PRE-04**

Vincule business directive con DRV y GOAL. Redacte de 4 a 6 principios con Name, Statement, Rationale e Implications; al menos uno para identidad del lote, otro para datos gobernados y otro para continuidad operacional. Registre cómo se tramitan excepciones.

### **Paso B4 Request PRE-05**

El sponsor del escenario solicita arquitectura: problema, misión, valor esperado, alcance, restricciones, interesados, plazo preliminar, criterios de éxito y autoridad para iniciar Phase A. Señale que el Request activa Phase A; el Statement de A-04 define el ciclo posterior.

| Producto | Pregunta de control | Mínimo para el taller |
| :---- | :---- | :---- |
| PRE-01 | ¿Quién decide y produce? | Roles y RACI de cinco decisiones. |
| PRE-02 | ¿Cómo se adapta TOGAF? | Scope, ciclos, notaciones y gates. |
| PRE-03 | ¿Por qué actuar? | Drivers, metas, restricciones y fuentes. |
| PRE-04 | ¿Qué reglas guían decisiones? | Cuatro principios completos. |
| PRE-05 | ¿Qué trabajo se solicita? | Encargo, sponsor, misión y límites. |

## **Actividad C Construir el repositorio y asegurar el Continuum**

Tiempo: 23 minutos (20:30–20:53). Salida: PRE-06, estructura física, inventario, metadatos y catálogo del Enterprise Continuum. Esta actividad se realiza a nivel de empresa para que futuras iteraciones recuperen y reutilicen el trabajo.

### **Paso C1 Crear el árbol físico de ocho clases**

Cree 00\_Control, 01\_Preliminary, 02\_Phase\_A y 03\_Architecture\_Repository. Dentro de este último cree exactamente las ocho clases de la tabla siguiente; use subcarpetas Strategic/Segment donde corresponda. Añada 04\_Enterprise\_Continuum para la clasificación, sin confundirla con una novena clase del repository.

| Clase Repository | Contenido inicial exigido |
| :---- | :---- |
| 01 Architecture Metamodel | Convención de IDs, relaciones y Viewpoint Catalog. |
| 02 Architecture Capability | Charter, roles, RACI y tailoring. |
| 03 Architecture Landscape | Views estratégicas y de segmento; modelos fuente y scope. |
| 04 Standards Library | Principios, normas candidatas, aplicabilidad y estado. |
| 05 Reference Library | Patrones genéricos y sectoriales con fuente y condiciones de reutilización. |
| 06 Governance Repository | Decision Log, Risk Log, gates, aprobaciones y excepciones. |
| 07 Architecture Requirements Repository | Stakeholders, concerns, requisitos y matriz de trazabilidad. |
| 08 Solutions Landscape | Conceptos de solución y candidatos, sin atribuir implantación real. |

### **Paso C2 Inventario y control**

En 00\_Control cree README, Inventario\_artefactos.csv, Fuentes\_y\_Evidencias.csv y Glosario. Cada fila del inventario lleva ID, nombre, tipo deliverable/artifact, ruta, versión, owner, estado, fuente HP/DS/DE/NV, concern y fecha. Los DOCX canónicos viven en 01\_Preliminary y 02\_Phase\_A; el inventario los asigna a una clase sin duplicar archivos.

### **Paso C3 Clasificar el Enterprise Continuum**

En 04\_Enterprise\_Continuum cree Continuum\_Catalog.csv. Para Architecture Continuum clasifique Foundation, Common Systems, Industry y Organization-Specific; repita para Solutions Continuum. En cada fila escriba activo, fuente, adaptación al caso, ubicación física, estado y requisito/decisión beneficiada. Si no existe un activo verificado, declare candidato conceptual, nunca una solución implantada.

### **Paso C4 Probar recuperación y reuso**

Tome REQ-02 del caso o su equivalente: localice patrón genérico de identidad/eventos, indique adaptación agroalimentaria y modelo específico de lotes de piña. Siga los enlaces hasta VIEW y DEC y muestre la ruta física de cada archivo. Compruebe que otra persona pueda reconstruir esta cadena sin preguntar al autor.

| ID | Continuum / nivel | Activo y adaptación | Ruta Repository | Relación |
| :---- | :---- | :---- | :---- | :---- |
| EC-01 | Architecture / Foundation | Método ADM y viewpoint de referencia | 05\_Reference\_Library | PRE-02 / VP-01 |
| EC-02 | Architecture / Industry | Patrón sectorial de lote y evento por evaluar | 05\_Reference\_Library | REQ-02 |
| EC-03 | Architecture / Organization-Specific | View conceptual del caso Del Monte | 03\_Architecture\_Landscape | VIEW-01 / DEC-01 |
| EC-04 | Solutions / Organization-Specific | Candidato conceptual sin proveedor | 08\_Solutions\_Landscape | REQ-02 / SC-01 |

Complete al menos ocho filas: cuatro por continuum. Las filas anteriores son ejemplos de clasificación, no información publicada de Del Monte.

## **Actividad D Desarrollar el núcleo de Phase A**

Tiempo: 25 minutos (20:53–21:18). Salida: A-01, A-02 y A-06 iniciales.

### **Paso D1 Business Scenario A-06**

Escriba disparador, actores, secuencia normal, excepción, resultado y medida. Ejemplo DS: durante packing cambia o se divide un lote; calidad necesita reconstruir la identidad y evidencias hasta despacho. Formule al menos tres requisitos observables derivados del escenario.

### **Paso D2 Capability Assessment A-01**

Identifique tres o cuatro capacidades críticas, baseline DS, target del equipo, gap, readiness para el cambio, dependencia, riesgo y evidencia para validar fuera del escenario. La madurez debe usar escala definida; separe capacidad de negocio de aplicación y de proceso.

### **Paso D3 Architecture Vision A-02**

Defina problema, stakeholders/concerns, scope breadth-depth-time-domains, outcome/KPI, baseline y target conceptuales, beneficios, riesgos y restricciones. Dibuje una vista de motivación DRV → GOAL/OUT → REQ y otra de estrategia OUT → value stream → CAP. Indique viewpoint, destinatario y concern de cada view.

| Elemento Vision | Respuesta exigida |
| :---- | :---- |
| Valor y resultado | Outcome, KPI, baseline DS, target DE, horizonte y owner. |
| Alcance | Un value stream, interfaces, exclusiones y cuatro dominios a alto nivel. |
| Target conceptual | Capacidades e información necesarias; ABB, no selección de proveedor. |
| Views | ID, viewpoint, concern, elementos, relaciones y versión. |
| Riesgos y supuestos | Separar DS, DE y NV con plan de revisión. |

## **Actividad E Preparar comunicaciones y contrato de trabajo**

Tiempo: 22 minutos (21:18–21:40). Salida: A-03 a A-05 iniciales.

### **Paso E1 Communications Plan A-03**

Para sponsor, operaciones, calidad, growers/logística e IT/OT, indique concern, mensaje, canal, frecuencia, responsable, evidencia de recepción y decisión esperada. La comunicación al Board debe pedir un gate concreto; la revisión técnica debe permitir detectar inconsistencias.

### **Paso E2 Draft Architecture Definition A-05**

Resuma Baseline conocida, vacíos NV, Target conceptual por negocio, datos, aplicaciones y tecnología, principios, requirements, views y correspondences. Declare explícitamente qué se pospone a B/C/D. No dibuje una arquitectura detallada ni complete un inventario interno no disponible.

### **Paso E3 Statement of Architecture Work A-04**

Especifique alcance de B/C/D, productos, actividades, roles, calendario preliminar, recursos, dependencias, criterios de aceptación, control de cambios y gate de autorización. Diferencie Request PRE-05, Architecture Vision A-02 y Statement A-04: petición, dirección compartida y acuerdo de trabajo.

| Producto | Control |
| :---- | :---- |
| A-03 | Cada stakeholder recibe información que permite revisar su concern. |
| A-04 | El sponsor puede aceptar alcance, productos, responsabilidades, plazo y condiciones. |
| A-05 | La definición inicial no anticipa decisiones de diseño que requieren análisis posterior. |

## **Actividad F Gate de Phase A y trazabilidad bidireccional**

Tiempo: 15 minutos (21:40–21:55). Salida: registro de decisión de gate y matriz de trazabilidad actualizada.

### **Paso F1 Evaluar el gate**

Simule el Architecture Board: ¿la visión expresa valor?, ¿scope es manejable?, ¿se cubren concerns fundamentales?, ¿hay owners, recursos y riesgos?, ¿el Statement describe B/C/D? Registre decisión Aprobar, Aprobar con condiciones o Rehacer, con responsables y fecha. Es una decisión del ejercicio DE, no autorización corporativa.

### **Paso F2 Demostrar dos cadenas completas**

Para dos requisitos, recorra HP/DS → DRV → OUT/KPI → CAP → CON/STK → PR → REQ → VP/VIEW → DEC y haga el recorrido inverso. La matriz debe contener IDs y rutas del repository. Una relación sin evidencia o modelo es un open issue.

| ID cadena | Origen | Resultado y concern | Requisito y view | Decisión y archivo |
| :---- | :---- | :---- | :---- | :---- |
| TR-01 |  |  |  |  |
| TR-02 |  |  |  |  |

## **Actividad G Integrar y cerrar**

Tiempo: 5 minutos (21:55–22:00). Un integrante abre el README y localiza PRE-04, A-02, REQ-02, VIEW-01 y DEC-01. Otro explica la ubicación física, clasificación Continuum, fuente y estado. El equipo entrega el índice y asigna los pendientes por owner.

# **6 Productos y estructura de entrega**

El expediente completo conserva doce deliverables editables, sus catálogos y modelos fuente. La entrega académica puede incluir un PDF ejecutivo para lectura, pero el ZIP contiene los DOCX, CSV y diagramas editables. Nombre sugerido: SI605\_S4\_GrupoXX\_Preliminary\_PhaseA\_DelMonte\_v0.1.zip. El docente determinará el plazo de consolidación.

| Ruta | Entregable o artifact | Contenido mínimo |
| :---- | :---- | :---- |
| 01\_Preliminary/PRE-01.docx | Modelo organizacional | Roles, RACI, gobierno y brechas. |
| 01\_Preliminary/PRE-02.docx | Marco adaptado | Tailoring ADM, metamodelo, notación y gates. |
| 01\_Preliminary/PRE-03.docx | Contexto | Business directive, drivers, metas y fuentes. |
| 01\_Preliminary/PRE-04.docx | Principios | Name, Statement, Rationale, Implications y excepciones. |
| 01\_Preliminary/PRE-05.docx | Request for Architecture Work | Sponsor, misión, alcance, valor y restricciones. |
| 01\_Preliminary/PRE-06.docx | Architecture Repository | Ocho clases, inventario, control de versión y acceso. |
| 02\_Phase\_A/A-01.docx | Capability Assessment | Baseline, target, readiness, gaps y riesgos. |
| 02\_Phase\_A/A-02.docx | Architecture Vision | Problema, scope, outcomes, stakeholders, views y Target conceptual. |
| 02\_Phase\_A/A-03.docx | Communications Plan | Audiencias, mensajes, mecanismos, cadencia y evidencia. |
| 02\_Phase\_A/A-04.docx | Statement of Architecture Work | Contrato de trabajo B/C/D, productos, roles y aceptación. |
| 02\_Phase\_A/A-05.docx | Draft Architecture Definition | Baseline conocida, Target alto nivel, requirements y vacíos. |
| 02\_Phase\_A/A-06.docx | Business Scenario | Actores, flujo, excepciones, resultados y requisitos. |
| 03\_Architecture\_Repository/ | Catálogos y modelos | Viewpoint, stakeholders, requirements, RACI, logs, views y trazabilidad. |
| 04\_Enterprise\_Continuum/ | Continuum Catalog | Dos continuos, cuatro niveles, fuente, adaptación y ubicación. |

## **6.1 Contenido del resumen ejecutivo**

| Página o lámina | Contenido |
| :---- | :---- |
| 1 | Contexto, value stream, problema, drivers, scope y organización de arquitectura. |
| 2 | Mapa del repositorio y clasificación Continuum con un ejemplo de reuso. |
| 3 | Principios, solicitud PRE-05, capacidades, escenario y visión A-02. |
| 4 | Views conceptuales, Statement A-04, gate, riesgos y cadena de trazabilidad. |

## **6.2 Paquete mínimo que se muestra a las 22:00**

| Evidencia | Condición para aceptarla en el taller |
| :---- | :---- |
| Carpeta y README | Árbol de ocho clases, inventario con rutas reales y cinco archivos localizables. |
| Preliminary | RACI con A único; tres principios completos; tailoring y PRE-05 que usa DS08, DS11 y DS21. |
| Continuum | Ocho registros, cuatro por continuum, con origen, adaptación, ubicación y estado. |
| Phase A | Escenario con excepción; visión de una página, capacidades, tres concerns y al menos dos views conceptuales. |
| Contrato y gate | A-04 con alcance B/C/D y un gate con decisión, condiciones y responsables. |
| Trazabilidad | Una cadena completa bidireccional demostrada con IDs; segunda cadena asignada para consolidación. |

La versión inicial no se penaliza por carecer de nombres de productos tecnológicos, topología OT o datos reales no entregados. Sí debe identificar NV y su acción de obtención. El expediente completo se revisa con el checklist de la sección 7\.

# **Anexo A Hojas de trabajo editables para la sesión**

Copie estas tablas a los DOCX/CSV indicados. Los ejemplos DS facilitan empezar, pero el equipo decide y justifica los valores DE. Cada hoja debe llevar ID, versión v0.1, owner, estado Draft y fuente.

## **A1 Modelo organizacional y gobierno PRE-01**

| Decisión o actividad | Sponsor | Board | Lead EA | Calidad | Operaciones | Datos TI | OT |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| Aprobar principios | A | C | R | C | C | C | C |
| Aprobar Vision y Statement |  |  |  |  |  |  |  |
| Mantener repositorio |  |  |  |  |  |  |  |
| Resolver conflicto de identidad H–P–X |  |  |  |  |  |  |  |

Regla: R realiza, A responde por la decisión, C consulta, I recibe información. Ajuste la fila de ejemplo y complete las tres restantes. Use DS09, DS19 y DS21.

## **A2 Tailoring y principios PRE-02 a PRE-04**

| Decisión de tailoring | Opción del equipo | Rationale y efecto |
| :---- | :---- | :---- |
| Alcance del ADM | Un value stream; Preliminary y Phase A; B/C/D posteriores |  |
| Nivel de detalle de Phase A | Target conceptual; sin diseño de interfaces |  |
| Notaciones y view kinds | ArchiMate / matriz / escenario; otras según concern |  |
| Gate y control de cambios | Semanas 2 y 4 del escenario |  |

| ID principio | Name / Statement | Rationale con DS | Implications verificables |
| :---- | :---- | :---- | :---- |
| PR-01 | Identidad de lote conservada |  |  |
| PR-02 | Operación local resiliente |  |  |
| PR-03 | Datos con owner y procedencia |  |  |
| PR-04 | Separación IT/OT segura |  |  |

## **A3 Request for Architecture Work PRE-05**

| Campo | Respuesta del equipo |
| :---- | :---- |
| Sponsor y business directive |  |
| Problema, driver y evidencia DS/HP |  |
| Outcome, KPI y valor esperado |  |
| Scope, exclusiones y horizonte |  |
| Recursos/constraints DS11 |  |
| Decisión solicitada y gate |  |

## **A4 Repositorio y Continuum PRE-06**

| ID activo | Tipo | Ruta física | Continuum y nivel | Fuente | Owner y versión | Usado por |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| REF-01 | Patrón identidad/eventos | 03\_Architecture\_Repository/05\_Reference\_Library/ | Architecture / Common Systems | DS16 |  | REQ-02 |
| VIEW-01 | View motivación | 03\_Architecture\_Repository/03\_Architecture\_Landscape/Strategic/ | Architecture / Organization-Specific | DE |  | CON-02 |
| SC-01 | Candidato mensajería | 03\_Architecture\_Repository/08\_Solutions\_Landscape/ | Solutions / Common Systems | DS18 |  | REQ-02 |

Añada Foundation e Industry en ambos continuos. Un patrón de DS16 es reutilizable tras evaluar su aplicabilidad; el servicio de DS18 sigue siendo candidato sin compra aprobada.

## **A5 Capability Assessment y escenario A-01 y A-06**

| CAP | Capacidad | Base 0–4 DS/DE | Target 0–4 DE | Gap y consecuencia | Owner | Validación NV |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| CAP-01 | Trazabilidad de lote |  |  |  | Calidad |  |
| CAP-02 | Conciliación de eventos |  |  |  | Datos/TI |  |
| CAP-03 | Continuidad packing |  |  |  | OT |  |

| Escenario BS-01 | Contenido esperado |
| :---- | :---- |
| Disparador | Cambio o división de lote durante packing. |
| Secuencia normal | Evento H–P–X, liberación de calidad, vinculación a pallet y despacho. |
| Excepción | Caída de red DS13, reintento, conflicto o duplicado, revisión de DS15. |
| Resultado y métrica | Historia recuperable en ≤30 minutos; integridad de eventos. |
| Requisitos | REQ-01 identidad; REQ-02 procedencia; REQ-03 reconciliación; REQ-04 seguridad IT/OT. |

## **A6 Architecture Vision y Communications Plan A-02 y A-03**

| Elemento de Vision | Respuesta del equipo |
| :---- | :---- |
| Problema y valor del cambio |  |
| Scope breadth, depth, time y domains |  |
| Stakeholders y tres concerns fundamentales |  |
| Outcome y KPI DS con Target |  |
| Target conceptual / ABB |  |
| VIEW-01 Motivation y VIEW-02 Strategy |  |
| Riesgos, dependencias y decisiones abiertas |  |

| Stakeholder | Concern | Mensaje para revisión | Canal y cadencia | Owner | Evidencia de acuerdo |
| :---- | :---- | :---- | :---- | :---- | :---- |
| Sponsor |  |  |  |  |  |
| Calidad |  |  |  |  |  |
| Operaciones/OT |  |  |  |  |  |
| Datos/TI |  |  |  |  |  |

## **A7 Statement, definición inicial y gate A-04 y A-05**

| Campo de A-04 | Respuesta del equipo |
| :---- | :---- |
| Trabajo autorizado tras Phase A |  |
| Productos B, C y D previstos |  |
| Exclusiones y recursos |  |
| Calendario, revisiones y responsables |  |
| Criterios de aceptación |  |
| Riesgos y control de cambios |  |

| Dominio A-05 | Baseline conocida DS | Target conceptual | NV para B/C/D |
| :---- | :---- | :---- | :---- |
| Negocio |  |  |  |
| Datos |  |  |  |
| Aplicaciones |  |  |  |
| Tecnología y OT |  |  |  |

| Gate | Decisión y fundamento | Condición | Responsable | Fecha |
| :---- | :---- | :---- | :---- | :---- |
| PRE → A |  |  |  |  |
| A → B/C/D |  |  |  |  |

## **A8 Matriz de trazabilidad y prueba oral**

| Fuente | Driver / outcome / KPI | Capability / concern | Principio / requisito | View / decisión | Ruta de archivo |
| :---- | :---- | :---- | :---- | :---- | :---- |
| DS14 |  |  |  |  |  |
| DS13 |  |  |  |  |  |

Prueba oral de un minuto: una persona explica la cadena DS14 → CAP-01 → CON-02 → PR-01 → REQ-01 → VIEW-01 → DEC-01 y otra recorre el camino inverso. Cada salto debe poder localizarse en un documento o catálogo.

# **7 Checklist de calidad antes de entregar**

* ☐  Un solo value stream estratégico y mismo System of Interest que la sesión 3 o cambio justificado.  
* ☐  HP, DS, DE y NV están identificados; ninguna cifra simulada se atribuye a la empresa.  
* ☐  PRE-01 a PRE-06 y A-01 a A-06 contienen propósito, owner, estado, versión, inputs y outputs.  
* ☐  Cada una de las ocho clases del Repository existe y el inventario permite localizar sus activos.  
* ☐  El Continuum tiene Architecture y Solutions, cuatro niveles cada uno, y enlaces al repositorio.  
* ☐  Principios y requisitos guían decisiones; el Request y el Statement cumplen funciones distintas.  
* ☐  Cada concern fundamental tiene viewpoint y view, con model kind y correspondences.  
* ☐  La Vision relaciona outcome, capability, escenario, riesgo, scope y target conceptual.  
* ☐  El gate consigna decisión académica, condiciones, responsable y siguiente paso.  
* ☐  Dos cadenas bidireccionales se pueden recorrer con IDs y rutas sin saltos.

# **8 Referencias y material de apoyo**

* SI605. Sesión 4\. TOGAF ADM Preliminary y Phase A, versión T\&G de 74 láminas, especialmente secciones de Transferencia y Anexo H.  
* SI605. Guía práctica sesión 3\. Caso Del Monte, Architecture Description Plan v0.1 y dossier HP/DS.  
* Expediente académico T\&G Global Preliminary y Phase A v1.1: modelo de doce deliverables, repositorio y Continuum. Los datos H pertenecen solo a ese escenario.  
* The Open Group. The TOGAF Standard, 10th Edition. Introduction and Core Concepts, secciones ADM, Architecture Repository y Enterprise Continuum.  
* ISO/IEC/IEEE 42010:2011. Architecture description, stakeholders, concerns, viewpoints, views, correspondences y rationale.

Cierre: Preliminary configura la capacidad que permite repetir la práctica de arquitectura; Phase A obtiene una visión y un mandato de trabajo trazables. El Repository conserva el conocimiento y el Continuum permite volver a utilizarlo con una adaptación explícita.