# Expediente Camposol · Preliminary, Phase A y Phase B

v0.2 · 2026-10-15 · Borrador académico condicionado; propuestas DE del asistente, sin aprobación corporativa.

Esta carpeta es el expediente vigente ampliado. Preliminary v0.2 normaliza el formato y corrige referencias de estado; A-05 v0.2 amplía la definición. A-01/02/03/04/06 v0.1 se conservan como documentos de la fase A: sus afirmaciones sobre “B no desarrollado” describen ese corte histórico. El estado actual está en A-05, B-01 y Gates. El gate A→B/C/D sigue pendiente.

La versión anterior está preservada fuera de esta raíz y verificada por contenido en `work/phase_b/respaldo_v0.1.zip`, además de su carpeta v0.1 de outputs. No hay copias activas de reemplazo dentro de esta entrega. No se desarrolló Phase C ni se hizo commit/push.

Comience por el [resumen S5 de cinco páginas](Resumen_Ejecutivo_S5.pdf) ([DOCX editable](Resumen_Ejecutivo_S5.docx)), [inventario](Inventario_artefactos.csv) y [registro único de cambios, checklist y límites](Registro_Cambios_Verificacion_Pendientes.md). El [resumen S4](Resumen_Ejecutivo_S4.pdf) y su [fuente](Resumen_Ejecutivo_S4.md) se preservan íntegros como antecedente histórico de cuatro páginas; sus menciones a la antigua entrega y cifras de trazas no describen v0.2.

Base vigente: [PC1 corregida](../03_Architecture_Repository/05_Reference_Library/Antecedentes/PC1_Corregida.docx) y [registro de correcciones](../03_Architecture_Repository/05_Reference_Library/Antecedentes/Registro_Correcciones_PC1.md). Originales sin modificar. La guía [S5 completa](../03_Architecture_Repository/05_Reference_Library/SI605_Guia_S5.md) controla el producto consolidado; los datos Del Monte no son de Camposol.

## Documentos y productos canónicos

- [PRE-01 · Modelo organizacional y RACI](../01_Preliminary/PRE-01_Modelo_Organizacional_RACI.docx)
- [PRE-02 · Marco de arquitectura adaptado](../01_Preliminary/PRE-02_Marco_Adaptado_TOGAF.docx)
- [PRE-03 · Contexto metas y drivers](../01_Preliminary/PRE-03_Contexto_Metas_Drivers.docx)
- [PRE-04 · Principios de arquitectura](../01_Preliminary/PRE-04_Principios_Arquitectura.docx)
- [PRE-05 · Solicitud de trabajo de arquitectura](../01_Preliminary/PRE-05_Request_for_Architecture_Work.docx)
- [PRE-06 · Architecture Repository](../01_Preliminary/PRE-06_Architecture_Repository.docx)
- [A-01 · Evaluación de capacidades y preparación para el cambio](../02_Phase_A/A-01_Camposol_Capability_Assessment.docx)
- [A-02 · Visión de arquitectura](../02_Phase_A/A-02_Camposol_Architecture_Vision.docx)
- [A-03 · Plan de comunicaciones de arquitectura](../02_Phase_A/A-03_Camposol_Communications_Plan.docx)
- [A-04 · Declaración del trabajo de arquitectura](../02_Phase_A/A-04_Camposol_Statement_of_Architecture_Work.docx)
- [A-05 · Definición inicial de arquitectura](../02_Phase_A/A-05_Camposol_Draft_Architecture_Definition.docx)
- [A-06 · Escenario de negocio de cámara a despacho](../02_Phase_A/A-06_Camposol_Business_Scenario_BS-01.docx)

- [B-01 · B-01_Business_Architecture_Definition.docx](../05_Phase_B/B-01_Business_Architecture_Definition.docx)
- [B-02 · B-02_Capability_Heat_Map.xlsx](../05_Phase_B/B-02_Capability_Heat_Map.xlsx)
- [B-03 · B-03_ValueStream_Capability.xlsx](../05_Phase_B/B-03_ValueStream_Capability.xlsx)
- [B-04 · B-04_Gap_Register.xlsx](../05_Phase_B/B-04_Gap_Register.xlsx)
- [B-05 · B-05_Organization_Services.docx](../05_Phase_B/B-05_Organization_Services.docx)
- [B-06 · B-06_ArchiMate_Exchange.xml](../05_Phase_B/B-06_ArchiMate_Exchange.xml)
- [B-07 · B-07_Requirements.xlsx](../05_Phase_B/B-07_Requirements.xlsx)
- [B-08 · B-08_Candidate_Roadmap_Components.xlsx](../05_Phase_B/B-08_Candidate_Roadmap_Components.xlsx)
- [B-09 · B-09_Views_Catalogs_Register.xlsx](../05_Phase_B/B-09_Views_Catalogs_Register.xlsx)

## Fuentes únicas y trazabilidad

B-02 gobierna el assessment vigente; el Capability_Catalog transversal conserva identidad/antecedente A y puntero. B-03 gobierna stages×capacidades; B-04 gaps/unidades/matriz; B-05 organización/servicios/objetos; B-08 CRC; B-09 selección de vistas y convenciones. B-06 es el modelo XML editable; SVG/PNG son proyecciones legibles. Los catálogos transversales de VP/view permiten navegación y remiten a B-09.

El [maestro de requisitos](../03_Architecture_Repository/07_Architecture_Requirements_Repository/Requirements_Catalog.csv) v0.2 es la única fuente de REQ-01…07 y AC-B01…07. B-07 es exportación controlada: editar maestro, validar IDs/versiones y regenerar por ID, cotejando su SHA-256 en la hoja. No editar B-07 como catálogo independiente. No se crean nuevos requisitos para completar cantidades.

[Matriz de trazabilidad](../03_Architecture_Repository/07_Architecture_Requirements_Repository/Matriz_Trazabilidad.csv) y [relaciones con secciones/rutas](../03_Architecture_Repository/01_Architecture_Metamodel/Relaciones.csv): TR-01/02 se conservan como cadenas A; TR-B01/02 incorporan gap, aceptación y CRC. Para lectura inversa buscar Destino y recuperar Origen. PR/REQ son vínculos documentales y no relaciones ArchiMate indistintas.

[Principios](../03_Architecture_Repository/04_Standards_Library/Principles_Register.csv), [decisiones](../03_Architecture_Repository/06_Governance_Repository/Decision_Log.csv), [riesgos](../03_Architecture_Repository/06_Governance_Repository/Risk_Log.csv), [gates](../03_Architecture_Repository/06_Governance_Repository/Gates_y_Aprobaciones.md), [pendientes NV](../03_Architecture_Repository/07_Architecture_Requirements_Repository/Validaciones_Pendientes.csv), [fuentes](Fuentes_y_Evidencias.csv) y [ocho clases/elementos](../03_Architecture_Repository/01_Architecture_Metamodel/Elementos.csv) mantienen rutas reales. [Continuum](../04_Enterprise_Continuum/Classification/Continuum_Catalog.csv) conserva sus ocho registros; no se declara solución implementada.

## Límites de aceptación

Dos brechas de escenario IA y cinco candidatos, cero brechas empresariales confirmadas. Mínimo de cinco gaps sustentados pendiente de evidencia o adaptación académica ratificada. Baseline real NE; metas DE. Gate B→C es propuesta condicionada, sin reunión/acta/firma. No hay pruebas operativas ejecutadas, proveedor, presupuesto o calendario de implementación de CRC.

XML: parseo, XSD exchange 3.0 y pares de tipos/referencias comprobados; importación en Archi no ejecutada. XLSX recalculados y renderizados; impresión A3 horizontal 100%, varias páginas cuando corresponde y cabeceras repetidas. Se revisaron figuras y PDF S5 de cinco páginas. DOCX: QA estructural; revisión visual de paginación, páginas vacías y recortes pendiente por falta de LibreOffice y bloqueo E_ACCESSDENIED de Word COM.
