# SI605 · PC3 · Grupo 04 · Camposol · Aseguramiento Packing · Architecture Repository v0.3

| Campo | Valor |
|---|---|
| Curso | SI605 Arquitectura Empresarial · FIIS-UNI · 2026-2 |
| Entrega | Práctica Calificada 3 (Phases C y D) · Repository v0.3 |
| Empresa | Camposol S.A. · Planta Packing Chao (La Libertad) · arándano fresco de exportación |
| Value stream | **VS-01 · Aseguramiento de fruta exportable**: desde la recepción de bins en packing hasta la entrega del FCL refrigerado al transportista en rampa |
| Propuesta de valor | Arándanos exportables con identidad, conformidad y frío demostrables |
| Fuera de alcance | Cosecha, transporte marítimo, puertos, otras plantas y el rediseño de SAP (sí está dentro su interfaz) |
| Marco | TOGAF Standard 10th Edition (ADM Preliminary → D) · ArchiMate 3.2 · ISO/IEC/IEEE 42010 |
| Integrantes | Gabriel Omar Chavez Mendoza · Eduardo Franco Gomez Acuña · Angel Sebastian Huamani Vargas · Diego Rodrigo Momediano Garcia · Max Joaquin Palomino Inza · Ballack Zidane Quintanilla Huamanraime |
| Versión y fecha | v0.3 (PC3) · 2026-11-26 · Draft · decisión académica del Grupo 04 (ROL-AB) · sin aprobación corporativa |

> **Aviso de evidencia.** Es un expediente académico. Los datos internos de la planta (volúmenes, códigos, sistemas, infraestructura Baseline) fueron **generados por IA** (dataset DS-CS-01…51, clase IA) y su valor real **no fue evaluado** (NE). Solo son hechos públicos (HP) la existencia de SAP corporativo, las calibradoras y la ampliación de Chao (fuentes F01–F04). El Target es una decisión del grupo (DE). Ver `00_Control_Gobierno/Reglas_de_evidencia.md`.

## 1. Cómo abrir el expediente

0. **Informe integrado PC3 v0.3**: `07_Entregables_Integrados/SI605_PC3_G04_Informe_v0.3.docx` (fuente editable, con nombre corto por el límite de rutas de Windows; el PDF se sube aparte, junto al ZIP, como `SI605_PC3_Grupo04_Camposol_AseguramientoPacking_Informe_v0.3.pdf`). **PPT de defensa**: `11_Sustentacion/SI605_PC3_Grupo04_Camposol_Sustentacion.pptx`.
1. **Empezar por** `07_Entregables_Integrados/ADD_Consolidado_B_C_D_v0.3.docx` (Architecture Definition Document único) y `07_Entregables_Integrados/ARS_Consolidada_B_C_D_v0.3.docx` (requisitos con prueba).
2. **Modelo ArchiMate**: `08_ArchiMate_Modelos/Camposol_PC3_v0.3.archimate` (formato nativo de Archi, *File → Open*) y `08_ArchiMate_Modelos/Camposol_PC3_Modelo_ArchiMate_OpenExchange_v0.3.xml` (Open Exchange, *File → Import → Open Exchange XML Model*). Las figuras de cada vista están en `08_ArchiMate_Modelos/Vistas/` (PNG y SVG). El `.archimate` fue importado y guardado por Archi y validado en su interfaz (0 errores; 113 advertencias por elementos y relaciones sin vista, aceptadas): ISS-03 cerrado, evidencia en `09_Evidencia_Fuentes/ISS-03_*` (DEC-PC3-13, CHG-PC3-25).
   **Extracción en Windows:** extraer en una carpeta corta y vacía (por ejemplo `C:\PC3\`) o con 7-Zip; no extraer encima de una versión anterior, porque quedan archivos con nombres viejos que no son parte de esta entrega. La ruta relativa más larga del ZIP tiene 74 caracteres, pero la carpeta raíz exigida por la guía (63) se duplica si se usa «Extraer todo» en Descargas.
3. **Trazabilidad extremo a extremo**: `07_Entregables_Integrados/E2E_Cadenas_Trazabilidad_v0.3.xlsx` (E2E-01 historia del lote; E2E-02 liberación de Calidad), con la ruta de cada eslabón.
4. **Inventario completo**: `MANIFEST.xlsx` (una fila por archivo, con ID, fase, tipo, Baseline/Target, owner, versión, estado, ruta y requisito o gap).
5. **Qué cambió desde PC2**: `CHANGELOG.md`.

Los `.docx` y `.xlsx` abren en Word/Excel o LibreOffice. Los `.csv` están en UTF-8 con BOM y coma como separador.

## 2. Índice de carpetas (estructura de la guía PC3 §4.1)

| Carpeta | Contenido |
|---|---|
| `00_Control_Gobierno/` | Reglas de evidencia, glosario, equivalencias de IDs, verificación PC3, auditoría archivo por archivo. **Repo_Arq/** con las 8 clases TOGAF (01 Metamodel … 08 Solutions Landscape): principios, estándares, decisiones, riesgos, issues, gates, RACI, requisitos, KPI, capacidades, stakeholders y trazabilidad. **Enterprise_Continuum/** (clasificación de reutilización). **Historico/** (versiones anteriores sin modificar: registros de cambios, modelos de PC2 y las versiones v3.0 de los incrementos de fase). |
| `01_Preliminary/` | PRE-01 Modelo organizacional y RACI · PRE-02 Marco adaptado · PRE-03 Contexto, metas y drivers · PRE-04 Principios (PR-02…PR-10, DEC-P01) · PRE-05 Request for Architecture Work · PRE-06 Architecture Repository |
| `02_Phase_A_Architecture_Vision/` | A-01 Capability Assessment · A-02 Architecture Vision · A-03 Communications Plan · A-04 Statement of Architecture Work · A-05 Draft Architecture Definition (salida de Phase A; lo desarrolla ADD-01) · A-06 Business Scenarios |
| `03_Phase_B_Business/` | B-01 Business Architecture · B-02 Heat map (escala 0–4) · B-03 VS × capacidades · B-04 Gap Register de negocio · B-05 Organización y servicios · B-06 vistas A y B en ArchiMate (extracto del modelo consolidado) · B-07 Requisitos · B-08 Candidatos de roadmap · B-09 Registro de vistas |
| `04_Phase_C_Data/` | Entregables de Phase C (Datos y Aplicaciones, como en la plantilla The Open Group): C-00 control y aplicabilidad · C-01 Architecture Deliverables · C-02 ADD de Phase C · C-03 ARS de Phase C · C-04 candidatos de roadmap · C-05 repositorio de Phase C · C-06 ABB candidatos. C1 catálogos y matrices de datos (incluye Data Entity × Business Function) |
| `05_Phase_C_Application/` | README de la carpeta · C2 catálogos y matrices de aplicaciones (portafolio, interfaces IF-01…07, App × Organización, App × Función, App × Dato). Las vistas de aplicación están en `08_ArchiMate_Modelos/Vistas/Phase_C` y la sección Application del ADD en C-02 y ADD-01 |
| `06_Phase_D_Technology/` | T-00 índice · T-01 plantilla The Open Group completada · T-02 ADD de Phase D · T-03 ARS de Phase D · T-04 candidatos de roadmap · T-05 artefactos · T-06 T-ABB y alternativas SBB · T-07 IT/OT, seguridad y continuidad · T-08 ejemplos Industria 4.0 · T-09 handoff y gate D→E · T1 catálogos (estándares, portafolio, NFR-T, gaps, ABB, SBB, ambientes) |
| `07_Entregables_Integrados/` | Informe integrado PC3 v0.3 (INF-01) · Estado vigente y consolidado: ADD-01 y ARS-01 (B/C/D) · Gap Register unificado B/C/D con oportunidades diferidas · E2E · C3 integración y viewpoints · T2 trazabilidad transversal · Resumen del gate D→E |
| `08_ArchiMate_Modelos/` | Modelo nativo `.archimate` (guardado y validado en Archi) · modelo consolidado Open Exchange · `Vistas/` PNG/SVG por fase · `XML_Vistas/` · `Anexo/` |
| `09_Evidencia_Fuentes/` | Fuentes y evidencias (F01…F14, IA-01…11) · Dataset IA DS-CS · Validaciones pendientes NV-01…13 · Supuestos SV (plausibilidad, efecto, responsable, prueba) · Registro de uso de IA · Evidencia de validación en Archi (ISS-03_*) |
| `10_Plantillas_TheOpenGroup/` | Mapa e índice de plantillas The Open Group usadas y dónde quedó cada sección |
| `11_Sustentacion/` | PPT de defensa `SI605_PC3_Grupo04_Camposol_Sustentacion.pptx` (SUS-02) · Índice de evidencia para la defensa (SUS-01) |

## 3. Vistas mínimas de la guía PC3 (§4.5)

Las vistas usan los IDs de la guía, con sufijo `-B` (Baseline) o `-T` (Target) cuando la guía pide ambos estados (DEC-PC3-11).

| Vista de la guía | Pregunta | Baseline (IA) | Target (DE) | Complementos |
|---|---|---|---|---|
| D-V01 | ¿Qué información usan los procesos y servicios? | D-V01-B | D-V01-T | D-V03 modelo conceptual Target |
| D-V02 | ¿Dónde se origina, transforma o distribuye un dato clave? | D-V02-B | D-V02-T | — |
| AP-V01 | ¿Cómo cooperan aplicaciones y servicios? | AP-V01-B | AP-V01-T | AP-V03 portafolio Baseline |
| AP-V02 | ¿Qué servicio de negocio habilita cada aplicación? | AP-V02-B | AP-V02-T | — |
| T-V01 | ¿Dónde se despliegan componentes y servicios? | T-V01-B | T-V01-T | T-V05 nodos, T-V06 servicios por ABB, T-V12 niveles ISA-95 |
| T-V02 | ¿Cómo se conectan sitios, redes y puntos de control? | T-V02-B | T-V02-T (redes y conductos) y T-V02-Z (zonas) | T-V09 continuidad |
| X-V01 | ¿Hay una relación consistente B → Datos → Apps → Tecnología? | — | X-V01 | X-V03 (cuatro capas con tecnología) |
| X-V02 | ¿Qué impacto explica el gap y cómo se materializa el ABB? | — | X-V02 | T-V10 gaps y candidatos, T-V11 plateaus |

Estas vistas tenían otros IDs en las guías de las Semanas 9 y 10 (por ejemplo, la cooperación de aplicaciones era AP-V03 y «Environments and Locations» era T-V01). La tabla antiguo → nuevo está en `00_Control_Gobierno/Equivalencias_ID.csv` (EQV-PC21…38).

El modelo tiene 34 vistas (258 elementos, 554 relaciones). Cada elemento lleva las propiedades Evidencia, Fase_ADM y Estado. Los cambios al modelo aprobados por el grupo el 2026-11-26 están en DEC-PC3-08, DEC-PC3-09, DEC-PC3-11, DEC-PC3-12 y DEC-PC3-13 y en el CHANGELOG (CHG-PC3-15, CHG-PC3-18, CHG-PC3-21, CHG-PC3-23 y CHG-PC3-25). Las figuras de `08_ArchiMate_Modelos/Vistas/` se generan desde las coordenadas del XML; al importar en Archi el estilo puede variar, no el contenido.

## 4. Convenciones

- **Clases de evidencia**: HP hecho público · IA generado por IA · SV supuesto por validar · DE decisión del equipo · NV no verificado · NE no evaluado.
- **IDs**: `Equivalencias_ID.csv` traduce los IDs antiguos (PC1, PC2, v0.5) a los vigentes; un ID retirado no se reutiliza.
- **Versión**: el expediente usó numeración interna v0.4 → v3.0 entre PC2 y PC3; la entrega PC3 es **Repository v0.3** (CHANGELOG §3).
- **Incrementos de fase y consolidado**: cada fase conserva su ADD/ARS (A-05, C-02, C-03, T-02, T-03), corregidos para no contradecir ADD-01 y ARS-01, que son el estado vigente (guía PC3 §4.3: un solo estado de verdad con referencia de versión).
- **ABB y SBB**: hasta Phase D solo hay building blocks lógicos (ABB). Las alternativas SBB se comparan sin aprobar compras; su selección es de Phase E.
