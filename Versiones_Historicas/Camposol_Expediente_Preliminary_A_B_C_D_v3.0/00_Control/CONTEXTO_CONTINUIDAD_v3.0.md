# CONTEXTO DE CONTINUIDAD · SI605 · Camposol S.A. (Planta Packing Chao, arándano) · Grupo 04
Fecha de corte: 2026-11-11 · Estado: expediente **v3.0 (Preliminary + A + B + C + D)** alineado al repositorio T&G v3.0; verificación automática 57 OK / 0 fallas; **listo para Phase E**. Adjuntar `Camposol_Expediente_Preliminary_A_B_C_D_v3.0.zip` (reemplaza a v0.5).

## Convención (DEC-D15)
- Prefijos de catálogo T&G: NFR-T, GAP-T, TD-RC, T-BASE/T-TAR, STD-T, T-ABB, CD, T-V, X-V02.
- Serie propia Camposol: DEC-D01…17, TEST-T01…13, principios PR (PR-06 refinado; PR-09 y PR-10 nuevos, en propuesta), igual que DEC-C/PR-07/08 en Phase C.
- LOC-01 (Phase B) intacto; instalaciones FAC-01 Sala de proceso, FAC-02 Pre-frío y cámaras, FAC-03 Sala técnica (Facility); EQ-01 Calibradoras, EQ-02 Túneles y cámaras (Equipment); entorno central T-TAR08 (Node, DC o nube NV-10).
- NFR-T y principios no son elementos XML (como AR-D/AR-A en C); se registran en T1/03–04. Equivalencias v0.5 → v3.0 en `00_Control/Equivalencias_ID.csv` y T2/07.

## Estructura Phase D (igual a T&G)
- 10: T-00…T-09 con las secciones T&G; T-01 sobre la plantilla oficial The Open Group Phases C/D (v2.0, julio 2024).
- 11: T1 con 12 hojas (01 Estándares … 12 Índice) y T2 con 6 hojas + 07_Verificacion.
- 12: XML consolidado A+B+C+D (258 elementos, 27 vistas = 16 + 11), 11 XML por vista y esquemas SVG/PNG en la raíz; Modelos_Fuente.
- 13_Phase_D_Soporte_Repositorio: manifiesto, ESTADISTICAS_VALIDACION.json, Resumen_Gate_D_E_v3.0.pdf (6 pág.) y guía. LEEME_FASE_D_v3.0.md en la raíz.
- Registros vivos de 00_Control y 03_Architecture_Repository actualizados como en Phase C; entregables 01–09 sin cambios.

## Contenido
- Portafolio: T-BASE01…09 (Included/Eliminated: T-BASE06 servidor, T-BASE08 LAN plana) y T-TAR01…23 (T-TAR13 cámara visual opcional).
- 13 NFR-T: 01 autonomía ≥ 24 h · 02 entrega sin duplicar · 03 latencia p95 ≤ 60 s · 04 ≥ 99,5 %, RTO ≤ 4 h, RPO ≤ 15 min · 05 control OT local con WAN caída · 06 zonas y conductos · 07 identidad nominal · 08 tiempo ≤ 1 s · 09 100 % decisiones QA auditadas · 10 persistencia y retención · 11 SAP acotado · 12 calidad de lectura térmica y vínculo con pallet · 13 mantenibilidad y versiones.
- 9 GAP-T (T08 vínculo térmico–pallet; T09 evidencia visual opcional); 8 TD-RC con horizonte relativo y prioridad P0–P3 (RC01 inventario, RC02 segmentación, RC03 borde y tiempo, RC04 identidad, RC05 vínculo térmico, RC06 plataforma central, RC07 SAP y retiro de AP-07, RC08 piloto visual).
- 8 T-ABB (01 captura, 02 control autónomo, 03 corredor IT/OT, 04 transporte y réplica, 05 persistencia, 06 ejecución/identidad/integración, 07 observabilidad y recuperación, 08 sensado visual opcional).
- Decisiones clave: DEC-D10 híbrido borde–central; DEC-D11 hosting central diferido a E; DEC-D12 ninguna tecnología/IA libera; DEC-D13 sin 2º WAN obligatorio; DEC-D14 ISA-95 ≠ despliegue; DEC-D17 gate D→E **propuesto** (NV-01/04/05/09/10/11/12).
- Riesgos RSK-D01…07; NV nuevos NV-10…13; dataset DS-CS-31…51 (28 320 eventos/día).

## Siguiente paso: Phase E
Evaluar SBB por categoría para T-ABB01…08 con costos (NV-06); consolidar D-RC/A-RC/TD-RC en paquetes y mesetas (patrón ArchiSurance), Project Context Diagram y Benefits diagram; cerrar NV-01/04/05/10.
