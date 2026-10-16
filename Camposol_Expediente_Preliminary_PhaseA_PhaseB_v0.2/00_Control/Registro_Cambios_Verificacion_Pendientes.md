# Registro único de cambios, verificación y pendientes

## Corte vigente v0.2 · Preliminary + A + B

2026-10-15 · ROL-EA propuesto · elaboración DE del asistente, sin aceptación del equipo. El historial v0.1 al final describe exclusivamente la entrega S4; sus límites temporales no sustituyen este corte.

### Cambios de formato

Se inspeccionaron los seis A: cuatro usan Normal Times New Roman 11 pt y dos 10,5. Se adoptó A-02 como representante del patrón dominante: título 16 pt, Heading 2 negro/negrita 12 pt, Normal 11 pt, interlineado 259/240 (1,079), después 6 pt, márgenes superior/inferior 2,159 cm y laterales 2,286 cm. Cabeceras E7E6E6, bordes D9D9D9 de 0,5 pt, padding 90 twips; sin encabezados/pies/campos de página. PRE-01…06 v0.2 heredan estilos/jerarquía y tablas dentro de caja 16,428 cm, cabecera repetida, títulos junto al párrafo siguiente. Se preservaron todas las tablas, textos e IDs excepto cambios explícitos siguientes. B-01/B-05 y resumen S5 DOCX/PDF aplican el patrón. XLSX adaptan fuente/negro/gris; color del heatmap se limita al score IA y marca NE.

### Cambios de contenido

- PRE: controles v0.2 y base de edición actualizada; cierre sustituye “B no desarrollado” por B condicionado y mantiene pruebas pendientes. PRE-02 distingue mapas A de XML B y añade ubicación de productos; PRE-06 identifica rama v0.2. No cambian decisiones ni cifras por estética. Propósito, ID, estado, owner, inputs y outputs conservados.
- A-05 v0.2 añade ampliación de negocio y fuentes actuales sin borrar historia v0.1. A-01/02/03/04/06 quedan v0.1 sin cambios. Nueve productos B, seis capacidades originales, siete unidades a igual granularidad, dos brechas IA y cinco candidatos, cuatro CRC y siete REQ refinados con aceptación prevista. No se inventan cinco gaps confirmados.
- Ocho clases Repository conservadas; maestro Requirements_Catalog.csv v0.2, B-07 exportación por ID con SHA y mecanismo de regeneración. Assessment actual B-02; CSV de capacidades identifica snapshot A y puntero, sin otra evaluación vigente. Catálogos de concerns/VP/views/correspondences y roles incorporan B con autoridad de registro explícita. Inventario, elementos, relaciones, DEC-B01…03, RSK-B01/02 y gates actualizados. TR-01/02 A preservadas; TR-B01/02 incorporan gap→AC→CRC y son verificables en ambos sentidos con IDs/rutas/secciones.
- Resumen S4 preservado byte por byte y rotulado por nombre/alcance. Resumen S5 PDF en cinco páginas y fuente editable DOCX. Respaldo v0.1 creado y contrastado archivo por archivo fuera de la raíz final. Originales E: y PC1 no modificados.

### Checklist completo S5 §7

| Criterio | Resultado y evidencia concreta |
|---|---|
| 1 Scope y SoI consistentes | VS01, un Packing Chao hasta entrega FCL en rampa; B-01 §1, B-03 Stages; pre-frío según ruta NV-08. |
| 2 Evidencia y procedencia | B-01 §1–2, B-04 Criterios; IA/NE/SV/DE explícitos y fuentes heredadas; ningún DS transferido. |
| 3 Baseline/Target comparables | Siete unidades U-B01…07 en B-04 Criterios/Matriz; mismas unidades, real NE conservada. |
| 4 Gaps completos y defendibles | Campos B-04 Registro/Criterios, siete registros. Dos brechas de escenario IA y cinco candidatos; mínimo cinco gaps sustentados pendiente, no cumplimiento ficticio. |
| 5 Pain distinto de gap | Impacto potencial separado de diferencia/evidencia; NE no prueba defecto. B-01 §2 y B-04. |
| 6 Resolve con requisito | GAP-B01…06 → REQ-01/02/04/03/06/07; tratamiento propuesto con rationale. GAP-B07 Defer detalle C/D conserva REQ-05. |
| 7 Aceptación verificable | AC-B01…07 en maestro y B-07; población/fuente/protocolo NV explícitos; pruebas previstas, no ejecutadas. |
| 8 CRC candidatos, no proyectos | Cuatro CRC con propósito/gaps/REQ/outcomes/dependencias/dominios, B-08 CRC; sin proveedor/costo/plazo. |
| 9 Views y modelos editables | B-06 XML; B-V01/B-V02 SVG/PNG embebidos B-01 §5; B-09 Vistas/Semantica. Hipótesis baseline visible. |
| 10 Definition integra salidas | A-05 addendum v0.2 y B-01 §§2–8, mapping de nueve salidas y rationale/impactos. |
| 11 Repository y logs actualizados | Inventario/Elementos/Relaciones; Req maestro; DEC/riesgos/VP/views/concerns/CP; ocho clases intactas. |
| 12 Gate condicionado | Gates G-B-C y B-01 §7; ROL-EA integra, ROL-AB revisa, STK-01 decide con mandato; cierre y devolución explícitos; sin acta/firma. |

### Comprobaciones y pendientes materiales

- Verificación estructural automatizada de integridad ZIP/DOCX/XML/XLSX, metadatos PRE, preservación de contenido/tablas, cinco A sin cambios y antecedente PC1 intacto; rutas y extremos reales. Fórmulas de B-02: 2/2/1/NE/NE/NE; blanco da NE y cero numérico se trata aritméticamente, restaurando NE al final. No cero inventado. Deltas son del escenario IA, nunca madurez observada.
- Se renderizaron las diez hojas de los seis XLSX; se corrigieron bandas de tabla ajenas al patrón y se verificó el resultado. Filtros/tablas, paneles A/filas1–6, validaciones y caches de fórmula presentes. Impresión A3 horizontal a100%, área/cabeceras repetidas; no se reduce un registro ancho a una página minúscula. El API de impresión no expuso operación en consulta acotada: solo esa configuración se completó en OOXML, conservando la autoría con artifact-tool. No se afirma impresión física ni apertura nativa en Excel.
- XML parseado y validado con los cinco XSD públicos 3.0 de The Open Group distribuidos por el repositorio del importador Archi; 28 elementos, 36 relaciones, dos vistas. Se comprobaron referencias y pares de tipos de Assignment/Realization/Serving/Access/Triggering. SVG/PNG comparten geometría y se revisaron, corrigiendo números/lectura de Access. Fuente técnica F-XSD. El esquema comprueba estructura, no verdad operativa ni toda regla semántica posible. Importación en Archi no realizada.
- PDF S5: cinco páginas renderizadas e inspeccionadas. DOCX: render no disponible (soffice ausente y Word COM E_ACCESSDENIED comprobados previamente); se reutiliza ese bloqueo, sin repetir intentos. Revisión visual de paginación, saltos, tablas y figuras de los diez DOCX creados/modificados permanece pendiente. QA estructural y figura independiente no sustituyen render de Word.
- Gate A pendiente; aceptación académica/corporativa no acreditada. Obtener evidencia o ratificar límites académicos, cinco gaps defendibles o adaptación, autoridad/roles y recursos; resolver NV-01…08 según dominios. 265k/250k, secuencia20/16, fuente térmica NV-05 e incertidumbre de beneficio siguen abiertos. Pruebas AC pendientes; no revalidación web de hechos empresariales; solo se consultó fuente técnica para el XML.

Siguiente paso: revisión del equipo del expediente v0.2 y cierre/ratificación de las condiciones G-B-C; no desarrollar C hasta recibir encargo. No se desarrolló Phase C ni se hizo commit/push.

Resultado de comprobación v0.2: 81 archivos, 540 IDs recuperables, diez hojas en seis XLSX y dos cadenas B de once enlaces verificadas en ambos sentidos; 29 originales de entrada conservan SHA-256. PDF S5 cinco páginas. Integridad documental comprobada; las limitaciones de operación, gate, importación y render DOCX permanecen.

## Historial cerrado v0.1 · alcance S4

# Registro de cambios verificaciones y pendientes

v0.1 · elaboración2026-10-15 · ROL-EA propuesto · DE/IA-07. Este es el único registro de esta elaboración; no acredita reuniones o decisiones del equipo.

## Cambios y conciliaciones

- Base: PC1 corregida y RC prevalecen ante contradicciones; guía S4 rige contenido. Se leyeron los doce Markdown nuevos y se inspeccionaron estructura/estilos/figuras de DOCX homónimos. No se releyó completa la teoría, la guía o PC1 ya analizadas. Sin AGENTS.md aplicables encontrado.
- Se editaron copias de los doce DOCX: estilos, geometría, numeración y partes no afectadas preservadas; cuerpo/tablas/controles/figuras conciliados. Procedencia_Originales.csv identifica originales y hashes. No se creó una segunda serie de Markdown PRE/A.
- Equivalencias_ID.csv conserva el detalle: KPI-01…03, STK/concerns/VP/VIEW/REQ PC1 mantienen significado; medidas de borradores pasan a MED-A; vistas A nuevas a VIEW-A; handoff/estados y evidencia se integran en REQ-06/07. DEC-01 sigue B reabrible; diagnóstico de borradores es DEC-02 propuesto.
- Se retira condición H aceptada de Template5: alcance/gobierno/calendario son propuestas DE; presión SV; datos internos NV. IA-01…06 conserva procedencia; IA-07 identifica esta elaboración. No se importaron cifras/problemas/significados de T&G/Del Monte.
- Seis principios completos, ocho clases materializadas, catálogos con metadatos, cuatro vistas A editables/PNG y ER PC1 conservado. MODEL-02/03/04 siguen planificados, sin desarrollar B/C/D.
- Dos ventanas DE: seis semanas de A y seis posteriores B/C/D; horas efectivas/acceso por acordar. No se altera calendario del eventual piloto ni se inventa encaje265k/250k.

## Checklist completo S4 y evidencia

| Criterio S4 §7 | Resultado de esta elaboración |
|---|---|
| Un value stream/SoI y fronteras | PRE-02/A-02; VS01 hasta transportista; variantes NV-08 |
| Evidencia sin cifras atribuidas falsamente | Fuentes_y_Evidencias, IA/SV/DE/NV y PC1/RC preservados |
| Doce documentos con propósito/owner/estado/versión/inputs/outputs | Controles de PRE-01…06 y A-01…06 |
| Ocho clases e inventario real | Ocho carpetas exactas y todas sus rutas indexadas |
| Dos continuos/cuatro niveles | Ocho filas EC-01…08 con origen/adaptación/ruta/beneficio |
| Principios/REQ y Request≠Statement | PRE-04/05 y A-04, seis principios completos |
| Concern→VP/view/model kind/correspondence | Catálogos de concern/VP/view y Correspondences.csv; planes PC1 distinguidos |
| Vision relaciona valor/CAP/escenario/scope/Target | A-02/05/06, KPI vigentes y mapas conceptuales |
| Gate con decisión/condiciones/owner/siguiente paso | Recomendación DE del asistente en Gates; decisión del equipo pendiente, no fabricada |
| Dos cadenas ida/vuelta con IDs/rutas | TR-01/02 y Relaciones.csv; documental, premisas operativas pendientes |

## Verificaciones

Estado final cuantitativo y resultados se completan por la auditoría del paquete. Se verifican hashes de originales, rutas/IDs/extremos, metadatos, relaciones de imágenes DOCX, geometría/partes preservadas, cifras y cuatro páginas PDF. El ZIP incluye la misma raíz y archivos que la carpeta. La auditoría no demuestra desempeño operativo ni autoridad empresarial.

## Pendientes y límites

- NV-01…08 conserva acciones y owners en Validaciones_Pendientes.csv: SAP local, red, mediciones/costos, protocolos, registros térmicos, viabilidad/recursos, aceptación/RTO/RPO y autoridad/rutas/documentos.
- US$185k+55k+25k=265k>250k por15k. Secuencia14+6=20>16 sin solape demostrado; I2/I4 siguen postergadas. Ahorro bruto IA US$1.252.968,75→1.252.969/año, no ROI/beneficio comprobado.
- Revisión del equipo, horas/acceso, acuerdos de calendario y gates reales pendientes. No entrevistas, mediciones, actas, firmas, reuniones ni pruebas inventadas.
- Render DOCX pendiente: render_docx.py no dispone de soffice.exe; Word COM devuelve E_ACCESSDENIED. Se conserva geometría/estilos y se revisa XML; no se afirma paginación limpia ni ausencia visual de páginas vacías. SVG/PNG y PDF se inspeccionan aparte.
- Normas/ediciones: se usa ISO42010:2011 de la guía; Template2 citaba2022. Aplicabilidad/edición externa no verificada aquí. URLs de PC1 reutilizadas con alcance y fecha previos, sin nueva comprobación web. No se entrega XML ArchiMate ni se afirma importación.

Siguiente paso: revisión académica del equipo sobre este paquete, ratificar/revisar propuestas y resolver condiciones antes de autorizar B/C/D. No se desarrolló Phase B, no se modificó original y no hubo commit ni push.

## Resultado final de comprobación

Comprobación del asistente: 65 archivos, 12 DOCX canónicos, 377 IDs recuperables, 85 relaciones documentales; TR-01/TR-02 verificadas en ida y vuelta, nueve filas RACI con A único, ocho registros Continuum y PDF de cuatro páginas. Rutas/relaciones internas, geometría y partes preservadas de Word comprobadas; 28 originales de entrada conservan hash. Sin errores de integridad documental detectados. Figuras y cuatro páginas PDF inspeccionadas visualmente; paginación DOCX y aceptación del equipo pendientes.
