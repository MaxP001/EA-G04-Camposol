# Guía de lectura del modelo ArchiMate · Repository v0.3 (PC3)

Grupo 04 · Camposol Planta Chao · VS-01 Aseguramiento de fruta exportable · 2026-11-26 · Draft v0.3 (PC3), decisión académica Grupo 04, sin aprobación corporativa.

## 1. Archivos

| Archivo | Uso |
|---|---|
| `08_ArchiMate_Modelos/Camposol_PC3_Modelo_ArchiMate_OpenExchange_v0.3.xml` | Fuente de verdad del modelo (ArchiMate 3.2, Open Exchange). Archi: *File → Import → Open Exchange XML Model*. |
| `08_ArchiMate_Modelos/Camposol_PC3_v0.3.archimate` | Formato nativo de Archi, importado y guardado por Archi (mismos IDs, propiedades y coordenadas que el XML; Archi agrega conexiones ocultas de anidamiento). Validado en la interfaz de Archi: 0 errores, 113 advertencias aceptadas (ISS-03 cerrado; evidencia en `09_Evidencia_Fuentes/ISS-03_*`). |
| `08_ArchiMate_Modelos/XML_Vistas/` | Extracto Open Exchange por vista de Phase D, X-V02 y X-V03 (elementos de la vista y relaciones entre ellos). |
| `08_ArchiMate_Modelos/Vistas/Phase_A…D/` | Figura PNG y SVG de cada vista, dibujada desde las coordenadas del XML. |
| `08_ArchiMate_Modelos/Anexo/` | Vistas de detalle de A, B y C (modelo aparte, no consolidado). |

Modelo: 258 elementos, 554 relaciones, 34 vistas.

## 2. Convenciones

- **Nombre de elemento** = ID + nombre (por ejemplo `AP-09 Componente de trazabilidad`). Los IDs son los de los catálogos (`Elementos.csv`, C1, C2, T1).
- **Propiedades** de cada elemento: `Evidencia` (HP, IA, SV, DE), `Fase_ADM` y `Estado` (Baseline, Target, ambos o N/A). En Archi se ven en la pestaña *Properties*.
- **Documentación**: cada elemento y cada relación añadida en PC3 dice su clase de evidencia y su fuente.
- **Baseline** = clase IA (datos generados por IA, valor real NE). **Target** = decisión del grupo (DE). Los componentes Target son ABB lógicos, sin producto (PR-05; los SBB se comparan en T1/13 y se eligen en Phase E).
- **Pie de cada figura**: ID · viewpoint · concerns · autor · versión · estado y una lectura de la vista.
- **Leyenda de relaciones**: impresa al pie de cada figura (Assignment, Realization, Serving, Access con dirección, Triggering, Flow, Composition, Aggregation, Influence, Association). El anidamiento representa una relación estructural del modelo.

## 3. Vistas y pregunta que responde cada una

Las vistas mínimas de la guía PC3 §4.5 usan su ID con sufijo `-B` (Baseline) o `-T` (Target) (DEC-PC3-11). Columna «Vista de la guía»: fuente `View_Catalog.csv`.

| ID | Nombre | Estado | Vista de la guía | Pregunta | Nodos/conexiones | Figura |
|---|---|---|---|---|---|---|
| VIEW-A01 | VIEW-A01 Motivación | Visión | — | ¿Por qué se cambia, qué se espera lograr y qué principios críticos lo restringen? | 25/26 | `08_ArchiMate_Modelos/Vistas/Phase_A/M-A01_Motivacion.png` |
| VIEW-A02 | VIEW-A02 Estrategia: curso de acción, value stream y capacidades | Visión | — | ¿Con qué curso de acción y capacidades se logran los outcomes? | 8/8 | `08_ArchiMate_Modelos/Vistas/Phase_A/M-A02_Estrategia.png` |
| VIEW-A03 | VIEW-A03 Contexto y alcance de Planta Chao | Visión | — | ¿Qué está dentro y fuera del alcance? | 9/7 | `08_ArchiMate_Modelos/Vistas/Phase_A/M-A03_Contexto.png` |
| VIEW-A04 | VIEW-A04 Concepto de solución (candidatos) | Visión | — | ¿Qué bloques lógicos y alternativas se evaluarán en Phase E? | 13/12 | `08_ArchiMate_Modelos/Vistas/Phase_A/M-A04_Concepto.png` |
| B-V01 | B-V01 Cooperación de negocio · Baseline (IA) | Baseline | B-V01 | ¿Cómo se transfiere hoy la evidencia y dónde se concilia a mano? | 15/18 | `08_ArchiMate_Modelos/Vistas/Phase_B/B-V01.png` |
| B-V02 | B-V02 Cooperación de negocio · Target (DE) | Target | B-V02 | ¿Qué procesos, objetos y eventos cambian frente a B-V01 (misma rejilla)? | 16/24 | `08_ArchiMate_Modelos/Vistas/Phase_B/B-V02.png` |
| B-V03 | B-V03 Value stream × capacidades | Target | — | ¿Qué capacidades habilitan cada etapa y dónde están los handoffs críticos? | 14/16 | `08_ArchiMate_Modelos/Vistas/Phase_B/B-V03.png` |
| B-V04 | B-V04 Servicios de negocio y consumidores · Target (DE) | Target | — | ¿Qué evento dispara cada proceso transversal y qué rol consume cada servicio? | 19/19 | `08_ArchiMate_Modelos/Vistas/Phase_B/B-V04.png` |
| B-V05 | B-V05 Actores, roles y procesos asignados · Target (DE) | Target | — | ¿Quién ejecuta cada proceso y a qué área pertenece? | 22/16 | `08_ArchiMate_Modelos/Vistas/Phase_B/B-V05.png` |
| D-V01-B | D-V01-B Estructura de datos Baseline (IA) | Baseline | D-V01 Baseline | ¿Dónde y con qué claves están hoy los datos? | 19/17 | `08_ArchiMate_Modelos/Vistas/Phase_C/D-V01-B.png` |
| D-V01-T | D-V01-T Información usada por procesos y servicios · Target (DE) | Target | D-V01 Target | ¿Qué información usan los procesos y qué componente la crea o la lee? | 24/20 | `08_ArchiMate_Modelos/Vistas/Phase_C/D-V01-T.png` |
| D-V02-B | D-V02-B Diseminación y linaje · Baseline (IA) | Baseline | D-V02 Baseline | ¿De dónde sale hoy cada dato de la historia y quién lo transforma? | 14/13 | `08_ArchiMate_Modelos/Vistas/Phase_C/D-V02-B.png` |
| D-V02-T | D-V02-T Diseminación y linaje · Target (DE) | Target | D-V02 Target | ¿Cómo viaja y se valida la evidencia hasta sus consumidores? | 15/16 | `08_ArchiMate_Modelos/Vistas/Phase_C/D-V02-T.png` |
| D-V03 | D-V03 Modelo conceptual de datos Target (DE) | Target | Complemento de D-V01 Target (modelo conceptual de datos) | ¿Cómo se preservan identidad, genealogía y evidencia? | 11/11 | `08_ArchiMate_Modelos/Vistas/Phase_C/D-V03.png` |
| AP-V01-B | AP-V01-B Cooperación de aplicaciones Baseline (IA) | Baseline | AP-V01 Baseline | ¿Cómo se transfieren hoy los datos entre aplicaciones y qué cambia en el Target? | 7/6 | `08_ArchiMate_Modelos/Vistas/Phase_C/AP-V01-B.png` |
| AP-V01-T | AP-V01-T Cooperación de aplicaciones Target (DE) | Target | AP-V01 Target | ¿Quién publica y quién consume, y bajo qué contrato? | 14/14 | `08_ArchiMate_Modelos/Vistas/Phase_C/AP-V01-T.png` |
| AP-V02-B | AP-V02-B Habilitación del negocio por aplicaciones · Baseline (IA) | Baseline | AP-V02 Baseline | ¿Qué proceso y servicio de negocio sostiene hoy cada aplicación? | 18/12 | `08_ArchiMate_Modelos/Vistas/Phase_C/AP-V02-B.png` |
| AP-V02-T | AP-V02-T Componentes y servicios de aplicación Target (DE) | Target | AP-V02 Target | ¿Qué componentes ofrecen qué servicios al negocio? | 18/18 | `08_ArchiMate_Modelos/Vistas/Phase_C/AP-V02-T.png` |
| AP-V03 | AP-V03 Portafolio de aplicaciones Baseline (IA) | Baseline | Complemento de AP-V01 Baseline (portafolio) | ¿Qué aplicaciones cooperan hoy y dónde hay traspasos manuales? | 7/6 | `08_ArchiMate_Modelos/Vistas/Phase_C/AP-V03.png` |
| X-V01 | X-V01 Alineación negocio – datos – aplicaciones | Target | X-V01 Target | ¿Cómo se conecta el valor de negocio con datos y software? | 15/18 | `08_ArchiMate_Modelos/Vistas/Phase_C/X-V01.png` |
| T-V01-B | T-V01-B · Despliegue de aplicaciones · Baseline | Baseline | T-V01 Baseline | ¿En qué nodos corren hoy las aplicaciones y con qué servicio técnico? | 13/10 | `08_ArchiMate_Modelos/Vistas/Phase_D/T-V01-B_Esquema_Visual_v0.3.png` |
| T-V01-T | T-V01-T · Platform Decomposition · Borde/Central | Target | T-V01 Target | ¿Dónde se ejecutan AP-08…AP-11 y dónde residen los datos? | 18/14 | `08_ArchiMate_Modelos/Vistas/Phase_D/T-V01-T_Esquema_Visual_v0.3.png` |
| T-V02-B | T-V02-B · Environments & Locations · Baseline | Baseline | T-V02 Baseline | ¿Dónde están hoy equipos, redes y servidores de la planta? | 16/10 | `08_ArchiMate_Modelos/Vistas/Phase_D/T-V02-B_Esquema_Visual_v0.3.png` |
| T-V02-T | T-V02-T · Network & Communications | Target | T-V02 Target | ¿Qué redes conectan cada nodo? | 19/18 | `08_ArchiMate_Modelos/Vistas/Phase_D/T-V02-T_Esquema_Visual_v0.3.png` |
| T-V02-Z | T-V02-Z · IT/OT Cybersecurity · zonas y conductos | Target | T-V02 Target (zonas, conductos y puntos de control) | ¿Cómo se limita el paso entre OT, DMZ, IT y central? | 16/20 | `08_ArchiMate_Modelos/Vistas/Phase_D/T-V02-Z_Esquema_Visual_v0.3.png` |
| T-V04 | T-V04 · Processing · Evento a historia de lote | Target | — | ¿Qué ocurre con un evento cuando cae y vuelve la WAN? | 15/15 | `08_ArchiMate_Modelos/Vistas/Phase_D/T-V04_Esquema_Visual_v0.3.png` |
| T-V05 | T-V05 · Networked Computing & Hardware | Target | Complemento de T-V01 Target (nodos e instalaciones) | ¿Qué instalaciones, equipos y nodos soportan el servicio? | 24/3 | `08_ArchiMate_Modelos/Vistas/Phase_D/T-V05_Esquema_Visual_v0.3.png` |
| T-V06 | T-V06 · Technology Services & ABB | Target | Complemento de T-V01 Target (servicios tecnológicos por ABB) | ¿Qué servicios tecnológicos componen cada ABB? | 21/2 | `08_ArchiMate_Modelos/Vistas/Phase_D/T-V06_Esquema_Visual_v0.3.png` |
| T-V09 | T-V09 · Availability & Continuity | Target | — | ¿Cómo se recupera el servicio de historia y qué no se pierde? | 17/8 | `08_ArchiMate_Modelos/Vistas/Phase_D/T-V09_Esquema_Visual_v0.3.png` |
| T-V10 | T-V10 · Gaps & Roadmap Candidates | Target | Complemento de X-V02 (gaps y candidatos) | ¿Qué brecha resuelve cada candidato y en qué orden? | 15/16 | `08_ArchiMate_Modelos/Vistas/Phase_D/T-V10_Esquema_Visual_v0.3.png` |
| T-V11 | T-V11 · Plateaus Baseline/Target y gaps tecnológicos | Baseline y Target | Complemento de X-V02 (gaps y plateaus) | ¿Qué estados compara cada gap tecnológico? | 10/17 | `08_ArchiMate_Modelos/Vistas/Phase_D/T-V11_Esquema_Visual_v0.3.png` |
| T-V12 | T-V12 · Environments & Locations · Target ISA-95 | Target | Complemento de T-V01 Target (niveles ISA-95) | ¿Qué función cumple cada equipo y aplicación según ISA-95? | 18/16 | `08_ArchiMate_Modelos/Vistas/Phase_D/T-V12_Esquema_Visual_v0.3.png` |
| X-V02 | X-V02 Impacto: motivación, gap y materialización del ABB · Target | Target | X-V02 Target / impacto | ¿Qué impacto explica el gap y cómo se materializa el ABB? | 34/32 | `08_ArchiMate_Modelos/Vistas/Phase_D/X-V02_Esquema_Visual_v0.3.png` |
| X-V03 | X-V03 · Vista integrada B–Data–Application–Technology | Target | Complemento de X-V01 Target (cuatro capas con tecnología) | ¿Cómo se sostiene BSV-01 y la autoridad de Calidad hasta la tecnología? | 19/18 | `08_ArchiMate_Modelos/Vistas/Phase_D/X-V03_Esquema_Visual_v0.3.png` |

## 4. Cómo recorrer las dos cadenas extremo a extremo

1. **E2E-01 historia del lote**: X-V02 (banda superior: DRV-02 → GOAL-01 → OUT-01 ← REQ-02) → B-V02 → D-V01-T / D-V03 → AP-V02-T → AP-V01-T → T-V01-T / T-V04 → X-V03. Eslabones y rutas en `07_Entregables_Integrados/E2E_Cadenas_Trazabilidad_v0.3.xlsx`.
2. **E2E-02 liberación de Calidad**: X-V02 (banda inferior: DRV-04 → GOAL-02 → OUT-02 ← REQ-06, restringido por CNS-02 y CNS-06) → B-V02 → D-V01-T → AP-V01-T → T-V02-Z → X-V03.

## 5. Límites

- Las figuras no se exportaron desde Archi: al importar, Archi aplica su propio estilo (colores, iconos), pero el contenido y las coordenadas son los mismos.
- Archi puede advertir relaciones que su validador considere no recomendadas; el modelo se revisó contra ArchiMate 3.2 (Apéndice B), no con el validador de Archi.
- Las figuras PNG/SVG se dibujan desde las coordenadas del XML con estilo propio; Archi muestra el mismo contenido con su estilo.
