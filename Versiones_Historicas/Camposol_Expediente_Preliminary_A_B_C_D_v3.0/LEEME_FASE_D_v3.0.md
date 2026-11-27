# Expediente Camposol Chao — ADM Preliminary, A, B, C, D · v3.0

Grupo 04 | UNI · SI605 Arquitectura Empresarial | 2026-11-11 | Draft v3.0 · Decisión académica Grupo 04 · sin aprobación corporativa

## Estructura acumulativa (patrón del repositorio T&G v3.0)
- `00_Control` a `09_Phase_C_Guia_Repositorio`: entregables v0.3 (Preliminary, A, B) y v3.0 (Phase C, antes v0.4) **preservados** en contenido; solo se agregan filas a los registros vivos (dataset, fuentes, equivalencias, Elementos, Decision_Log, Risk_Log, NV, Test_Catalog, estándares, principios, vistas), como se hizo en Phase C.
- `10_Phase_D_Entregables_TOGAF`: T-00…T-09 (incluye la plantilla oficial The Open Group Phases C/D completada).
- `11_Phase_D_Catalogos_Matrices`: T1 (12 hojas) y T2 (6 + 1 hojas).
- `12_Phase_D_Vistas_ArchiMate`: XML combinado A+B+C+D con 27 vistas, 11 XML individuales y 11 esquemas SVG/PNG. *El esquema es figura de apoyo; el XML es editable en Archi.*
- `13_Phase_D_Soporte_Repositorio`: manifiesto, estadísticas, resumen de gate en PDF (5 páginas) y guía.

## Artefactos Phase D recomendados (plantilla The Open Group 10, julio 2024)
1. Technology Standards Catalog — T1/01. 2. Technology Portfolio Catalog — T1/02. 3. Application/Technology Matrix — T1/08.
4. Environments and Locations — T-V01, T-V02. 5. Platform Decomposition — T-V03, T-V06. 6. Processing — T-V04.
7. Networked Computing/Hardware — T-V05. 8. Network and Communications — T-V07 (y T-V08).

**Además**: principios refinados T1/03; NFR T1/04; gaps T1/05; candidatos de roadmap T1/06; decisiones T1/07; conduits T1/10; ABB T1/11; gate y pendientes en T-09.

## Decisión central
DEC-D10 híbrido borde–central: en planta, captura, cola persistente (≥ 24 h) y réplica de lectura del estado QA; en el entorno central, historia única, portal, excepciones y respaldo. Control OT local sin mando remoto (PR-09). Solo ROL-B05 libera (PR-07, NFR-T09).

## Verificación
57 controles OK · 0 fallas (T2/07_Verificacion). Importación validada a nivel XML/referencias; no se declara haber abierto en Archi. Gate D→E **propuesto** (DEC-D17), pendiente de revisión docente.

Todos los datos tecnológicos de Camposol en este expediente son simulados (DS-CS-31…51) salvo los hechos públicos F01–F08; validar en la empresa antes de cualquier ejecución.
