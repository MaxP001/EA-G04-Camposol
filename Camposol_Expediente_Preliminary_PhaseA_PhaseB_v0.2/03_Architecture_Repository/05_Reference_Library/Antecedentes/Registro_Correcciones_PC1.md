# Registro de correcciones de la PC1 de Camposol

Se editó una copia del mismo Word evaluado. Se conservan empresa, oportunidad, alcance, seis etapas y valor por etapa, mapa de capacidades, escenario declarado, stakeholders/concerns, viewpoints/views, Registro IA y alternativas A/B/C. No se ejecutaron ni generaron entregables de Preliminary, Phase A o Phase B.

## Documento de origen y alcance

- Original: `E:\UNI cursos\6to Ciclo\Arquitectura Empresarial\SI605_PC1_Grupo04_Camposol_AseguramientoPacking.docx`.
- Huella SHA-256 previa y posterior: `CD3BE3882DB3F2291D8311EF2ED6C6883A38A50F909F09D9E11CAB27477AE81A`. **Original sin cambios.** No se eligió una copia con sufijo.
- Resultado: `SI605_PC1_Grupo04_Camposol_AseguramientoPacking_CORREGIDO.docx`, en esta carpeta.
- Autoridad de requisitos: `SI605_Guia_Practica_Calificada_01_2026-2_v1.2.docx`, leída completa. Se contrastaron los 16 hallazgos con original y guía, además de releer íntegramente Feedback, Matriz y Continuidad de `00_Revision_PC1`. El feedback se trató como revisión, no como evidencia empresarial.
- Sin AGENTS.md aplicables encontrados. Sin commit ni push.

Las ubicaciones siguientes son secciones y nombres de artefactos del Word corregido. No se usan páginas porque no se pudo completar el renderizado. Se añadieron tres tablas para requisitos, equivalencias y dos recorridos; la numeración interna de tablas extraídas cambió después de §8.1.

**Interpretación de estados:** «Corregido» indica que la inconsistencia documental identificada se corrigió. No implica que se hayan validado con Camposol las premisas del escenario. «Parcialmente corregido» conserva una comprobación o decisión sustancial pendiente. «Pendiente de evidencia» se usa para la existencia/autoridad real de roles que no puede acreditarse desde las fuentes consultadas. Ningún hallazgo se da por resuelto por el mero cambio de etiqueta.

## Cambios por hallazgo

| Hallazgo | Cambios realizados y contraste con el original | Ubicación corregida | Estado | Pendientes |
|---|---|---|---|---|
| F-01 | Fecha de IT/USERS corregida a 24/06/2016; se retira la atribución de «integración pendiente» a esa entrevista. SAP corporativo se distingue de despliegue/API/comportamiento Chao. | Resumen, §§1.1–1.4, 2.3–2.4, 3.1, ADR y Referencias F01/F02 | Parcialmente corregido | NV-01/NV-04 y SV-01: comprobar interfaces y flujo local. La fuente histórica no se convierte en prueba de actualidad. |
| F-02 | Oportunidad, D1/D3, gaps, mapa y conclusiones conservan IA/SV/DE. El 19/20 se mantiene como juicio exploratorio heredado; su columna se explicita como soporte del escenario, no evidencia pública de reclamos. | §§1.3, 3.1–3.2, 4.4, 9–10; figura 2 | Corregido | Repriorización real depende de NV-03/SV-01. No se revalida una pérdida ni se autoriza inversión por puntaje. |
| F-03 | Se preservan importes independientes 185k/55k/25k y se suman 265k: excedente de 15k frente a techo DE de US$250.000. Se elimina la inclusión ficticia de adopción como contingencia. Costos por frente se distinguen del paquete; la matriz histórica no prueba su encaje. Duraciones 14/6/6 permanecen estimaciones; nodo+captura secuenciales serían 20 semanas. | Canvas, §§5.1–5.2, 5.4–5.5, C05, CP-03, ADR, conclusiones | Parcialmente corregido | NV-06: cotizaciones, inclusiones, recursos, techo aceptado y secuencia. No se asignaron importes nuevos ni paralelismo para encajar en 16 semanas. |
| F-04 | I2 sigue fuera del alcance inicial. KPI-02 depende de registros térmicos existentes con timestamps, fuente y relación pallet/ubicación/custodia; el nodo y la app no se presentan como fuente suficiente de series. Si no se comprueba disponibilidad/protocolo, no se declara éxito. | Ficha KPI, Gap2, iniciativa, piloto, REQ-04, NV-05/NV-07 | Parcialmente corregido | Comprobar registradores y frecuencia/continuidad de datos. No se añadió IoT automáticamente ni se afirmó cierre del gap por I1. |
| F-05 | NV-03 conserva mediciones, duplicados, incidencias y costos. El protocolo de calibradoras se denomina NV-04. Se elimina SV-03 como referencia activa; se conserva solo en la tabla histórica para explicar su retiro. | §§1.4, 8.3, 8.3.1, 9; referencias cruzadas | Corregido | Ocho pendientes NV definidos con un significado cada uno. Repetirlos en inventario y open issues referencia la misma incertidumbre, no nuevos elementos. |
| F-06 | El bosquejo se acota a identidad conceptual; se explicitan dos asociativas. Se retiran garantías basadas en FK/JOIN y se proponen pruebas de completitud, cronología, procedencia, custodia y consulta. Las series térmicas se reconocen como evidencia complementaria necesaria. | §§7.2–7.4, 8.1.1, 8.2; figura 1 | Parcialmente corregido | NV-03/NV-05/NV-07/NV-08 y casos de prueba. No se creó un modelo físico de datos ni una arquitectura de negocio completa. |
| F-07 | Se mantienen A/B/C y B seleccionada como hipótesis. Se explicitan comportamientos supuestos; A no implica necesariamente paro y B no garantiza continuidad/latencia. Reapertura incluye SAP, protocolos, red, herramientas existentes, costo, integridad, seguridad y desempeño. | Cadena vertical, REQ, correspondences y DEC-01/RAT-01 | Parcialmente corregido | Ejecutar observaciones y ensayos acordados; autorización empresarial pendiente. No se reemplazó B por otra topología. |
| F-08 | TTCT se desagrega: KPI-01 por solicitud/lote operativo, KPI-02 por pallet despachado y KPI-03 por evento. Se definen denominadores, t0/t1, fuente, faltantes, unidad y éxito; sin población conocida no se registra cero. 65 % queda normalizado explícitamente como premisa sintética por pallet, sin derivarlo de lecturas en papel. | §§3.3, 4.4, 5.5, REQ-01…04 y Registro IA | Parcialmente corregido | Acordar muestras/carga, frecuencia térmica y aceptación NV-07; baseline real NV-03/NV-05. La normalización no equivale a una medición validada. |
| F-09 | Registro IA ampliado: volumen, unidad financiera, tasas, costos, duraciones, scores, metas y pruebas. IA-06 identifica la corrección actual. Se mantienen resúmenes históricos existentes y se declara que no hay prompt literal o detalle histórico de ciertos parámetros. | Anexo Registro IA-01…06; usos en texto/tablas/figuras | Parcialmente corregido | Plausibilidad y magnitud empresarial no comprobadas; validar parámetros y revisión del equipo. No se inventaron prompts históricos ni valores RTO/RPO. |
| F-10 | Se usa política sin redondeos intermedios; cálculo exacto con 2.812,5 unidades financieras equivalentes. Ahorro bruto 1.252.968,75, presentado 1.252.969 USD/año. Se separan expectativa, beneficio neto y ROI; se retira garantía de certificación y comparación financiera interanual no conciliada. | Ficha, cadena estratégica, Canvas, §5.3, riesgos, conclusiones | Corregido | Incidencia, costos, volumen, causalidad y retorno real siguen sin validar. Unidad financiera de 16 TM no es lote operativo ni denominador térmico. |
| F-11 | Receptor inmediato es el transportista en rampa; cliente internacional es beneficiario final. Se mantiene el límite de planta. No se exige BL emitido o carga a bordo como prueba local. Variantes de recepción refrigerada y documentos efectivos se registran NV-08. | §§2.1–2.3, Operating Model, etapas, STK-06, modelo | Parcialmente corregido | Validar handoff, rutas, reglas y documentos con operación. No se amplió diseño a mar/puertos/reclamos. |
| F-12 | Figura, tabla y editable concilian multiplicidades. Posicion_Camara es historial de ocupaciones, con intervalos sin solapamiento y un máximo abierto; Pallet_FCL conserva historial y una asignación activa máxima. Identidad es lógica, no PK/FK físico. | Figura 1; §7.4 y reglas de integridad | Corregido | Convenciones DE/IA-06 propuestas, no descripción real de Chao. Bin puede tener 0..N vínculos durante flujo; batch exige al menos un origen; liberación exige completar genealogía. |
| F-13 | Se retira HP de cargos y autoridad no comprobados. Catálogo, owners y pruebas se declaran propuestos; se distribuyen preparación/validación de medidas como propuesta de análisis. | Catálogo STK, KPI, comunicaciones implícitas, open issues, ADR | Pendiente de evidencia | NV-08: confirmar cargos, responsables y facultad para aceptar/financiar. La reetiquetación evita una atribución falsa, pero no acredita existencia o designación. |
| F-14 | Card incorpora rationale y fuentes. Las cuatro correspondences CP-01…04 indican extremos, regla, método y evidencia esperada; seguridad exige acceso autorizado, rechazo de intentos no permitidos y trazas. Firewall/VLAN son mecanismos candidatos. | §§7.2, 8.1.1, 8.2; C03/C04 | Corregido | Pruebas planificadas, no ejecutadas. Tolerancias, roles y RTO/RPO se acordarán en NV-07; las flechas del mapa son documentales. |
| F-15 | Se concilian semana 8 para KPI-03 y cierre deseado de 16 para KPI-01/KPI-02 condicional. Se separan validación inicial, autorización del trabajo arquitectónico y autorización de implementación. Las iniciativas posteriores no equivalen a Phase B. | §§5.2, 5.5, 9–10 | Corregido | El plazo no está demostrado; recursos/calendario NV-06. No se declara preparación de empresa, piloto aprobado ni beneficios alcanzables con certeza. |
| F-16 | Ocho fuentes recuperables con hyperlinks, fechas/periodos, tipos y alcance. F05 reemplaza referencia imprecisa por comunicado corporativo; F08 por programa SENASA exacto. Se retira mezcla de destinos sectoriales y composición histórica como presente. Carátula conserva nombres/código suministrados, sin inventar datos personales. | Carátula, §§1.1–1.2, Referencias | Parcialmente corregido | Faltan apellidos completos/códigos de integrantes; confirmar formato de entrega. Render/paginación pendientes. No se afirma que DOCX incumpla formato permitido en aula. |

**Balance:** 6 hallazgos corregidos en su formulación documental; 9 parcialmente corregidos; 1 pendiente de evidencia. Cero hallazgos se presentan como validaciones operativas de Camposol. La incompatibilidad financiera sigue abierta y visible.

## Fuentes y verificación reutilizada

Se reutilizaron comprobaciones documentadas en el Feedback cuando bastaban. En esta etapa se reabrió Gestión para precisar título/fecha 05/02/2025 y su alcance sectorial. No se volvió a investigar todo el dossier. Las referencias no localizadas inequívocamente se sustituyen de forma explícita, sin simular que eran las originales:

| ID nuevo | Origen / cambio | Fuente recuperable | Soporte limitado utilizado |
|---|---|---|---|
| F01 | Antigua1 | [Reporte 2024](https://www.camposol.com/wp-content/uploads/2025/09/RSCAMP2024ING-1.pdf) | Gestión/SAP y estándares corporativos en §7.1; no interfaces de Chao. |
| F02 | Antigua2, fecha corregida | [Entrevista IT/USERS](https://itusers.today/peru-camposol-innova-con-sap-s4hana/) | Testimonio histórico corporativo de 2016; no brecha actual. |
| F03 | Antigua3 identificada | [Ampliación Chao](https://redagricola.com/camposol-duplica-su-capacidad-de-despacho-de-arandanos-en-chao/) | Capacidad publicada y declaraciones de la compañía; no producción efectiva/pérdidas. |
| F04 | Antigua4; variante textual precisa | [Recorrido de packing](https://redagricola.com/la-ruta-del-arandano-camposol-desde-dentro-2/) | Equipos/capacidad/TOPSY publicados; no reproducción de video ni validación de todo VS01. |
| F05 | **Sustituye antigua5** no identificada con precisión | [Comunicado corporativo1S 2025](https://investors.camposol.com/node/8111/pdf) | Certificaciones Chao declaradas, p.1; no pérdida de certificación ni tasa de incidencia. |
| F06 | Antigua6; fecha/título precisados | [Ranking de Gestión](https://gestion.pe/economia/empresas/estas-son-las-15-principales-exportadoras-de-arandanos-quien-llega-por-primera-vez-agroexportacion-peru-oro-azul-camposol-hortifrut-agrovision-noticia/) | Ranking atribuido a Fluctuante/SUNAT; prensa, no base aduanera directa. |
| F07 | Antigua7 | [Reporte 2023](https://www.camposol.com/wp-content/uploads/2024/07/CAMP_RSCAMP2023ESP.pdf) | Contexto histórico y SAP; no crecimiento por mezclar bases. |
| F08 | **Sustituye antigua8** genérica | [Programa SENASA 08/04/2025](https://www.senasa.gob.pe/senasa/descargasarchivos/2025/04/CTD-VIRU-08.04.25.pdf) | Programación y capacitación de trazabilidad para Camposol; no auditoría integral ejecutada. |

Se mantienen ocho fuentes útiles. F01/F05/F07 son corporativas oficiales y F08 institucional: cuatro cumplen ese tipo de origen, superando el mínimo de tres. La utilidad se limita a contexto y preguntas concretas; ninguna soporta tasas, costos, scores o fallas internas sintéticas. Los modelos/hipótesis siguen teniendo su registro IA y plan de validación.

## Equivalencias e identificadores

- NV-03 conserva la medición de baseline; NV-04 identifica protocolos. NV-05…08 consolidan evidencias térmicas, viabilidad, protocolos de prueba y roles/reglas/documentos.
- SV-03 no tiene una definición recuperable: se eliminó como supuesto activo. Su única mención histórica está en §8.3.1; no es una referencia pendiente de resolver.
- REQ-03 conserva la necesidad de continuidad con redacción verificable. REQ-01/02/04/05 son propuestas nuevas para enlaces ya existentes, declaradas DE/IA-06. No se presume que existieran REQ-01/02 en el original por la numeración de REQ-03.
- MODEL-01…04 son alias explícitos de los cuatro nombres originales de modelo; MODEL-03 no cambia de significado. OBJ01/OUT01/VS01 se vinculan con sus definiciones; C1…C6 capacidades y C01…C06 concerns se mantienen separados.
- El registro de incertidumbres y el de open issues repiten los mismos IDs para rastrear una misma incertidumbre. No hay dos significados vigentes para un ID.

## Comprobaciones realizadas

| Control | Resultado |
|---|---|
| Original correcto y huella intacta | Coincide con el evaluado; SHA-256 sin cambios. |
| DOCX válido | ZIP sin errores CRC; todos los XML parseables; reapertura con python-docx correcta. |
| Diseño heredado | Un mismo sectPr: tamaño, márgenes y orientación conservados. Estilos, numeración, tema y pie semánticamente idénticos en XML canónico; diferencias de serialización no cambian sus propiedades. |
| Organización | Se conservan diez secciones, carátula y anexo; las 35 tablas originales se editan in situ y se añaden 3 de apoyo. Dos saltos de página manuales originales, sin nuevos saltos por sección. |
| Tablas | Encabezados repetidos; filas sin altura fija; se permite crecimiento/fraccionamiento. No se certifica disposición visual final por esos controles. |
| Figuras | Dos imágenes sustituidas en sus mismas relaciones; comparación binaria confirma que el DOCX contiene los PNG nuevos. SVG/MMD editables separados; PNG originales preservados. Se inspeccionaron las dos figuras nuevas a resolución legible. |
| Fuentes | Ocho hyperlinks externos distintos, correspondientes a F01…F08 y a sus entradas. Cuatro fuentes corporativas/institucionales. |
| IDs | NV-01…08 definidos, REQ-01…05 definidos, IA-01…06 registrados, cuatro modelos con alias; SV-03 solo en equivalencia histórica. Referencias/coberturas contrastadas. |
| Aritmética | 185.000+55.000+25.000=265.000; excedente 15.000. 45.000/16=2.812,5; pérdida hipotética 2.784.375; unidades evitadas 75,9375; ahorro 1.252.968,75, redondeado 1.252.969. |
| Unidades | Solicitud/lote operativo, pallet, evento y unidad financiera separados; no se interpreta desconocido como cero. |
| Dos cadenas | §9.1 recorre fuente/contexto+hipótesis hasta DEC-01 y vuelve por los mismos elementos. La continuidad se prueba con REQ-03 además de KPI-03; el KPI de captura no sustituye RTO/RPO. |
| Etiquetas | Se contrastaron resumen, tablas, mapa, ADR, conclusiones y Registro IA. Los datos sintéticos siguen IA; propuestas/convenciones DE; hechos locales no comprobados NV/SV. |
| Renderizado | Se intentó con `render_docx.py`; falló por ausencia de `soffice.exe`. No se halló LibreOffice empaquetado. **Revisión visual de páginas pendiente**, incluida paginación, tamaño efectivo de texto/figuras y títulos aislados. No se inventó un PDF ni una comprobación visual. |

## Entrega y pendientes finales

- Word corregido y matriz actualizada en esta carpeta.
- `figuras_editables` contiene dos SVG y dos Mermaid; `figuras_originales` conserva ambos PNG originales. El paquete `Figuras_PC1_Editables.zip` reúne estas fuentes y sus instrucciones.
- Permanecen pendientes de evidencia NV-01…08, validación de parámetros IA, aceptación de propuestas y conciliación financiera/temporal. No se eligen nuevos importes o alcance para ocultar el déficit.
- Para completar la carátula se requieren los apellidos completos y códigos no suministrados de los integrantes. Los datos existentes se conservaron; no se inventaron identificadores personales.
- No se asigna una nueva nota al informe ni nota oral/final. Corregir redacción y trazabilidad no constituye por sí solo evidencia operativa ni aprobación.
