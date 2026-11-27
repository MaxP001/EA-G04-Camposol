# Glosario · Repository v0.3 (PC3)

- **Capability (CAP)**: habilidad estable de negocio enfocada en un resultado; no fija el cómo. Ej.: CAP-01 Trazabilidad del lote.
- **Business Function (BF)**: agrupación estable de trabajo y recursos que gestiona la empresa. Ej.: BF-03 Aseguramiento de calidad.
- **Business Process (BP)**: secuencia de actividades que ejecuta el trabajo. Ej.: BP-03 Inspeccionar y decidir conformidad.
- **Business Event (EV)**: hecho que dispara o resulta de un proceso. Ej.: EV-03 Lote retenido (HOLD).
- **Business Service (BSV)**: valor expuesto a un consumidor. Ej.: BSV-01 Historial auditable del lote.
- **Business Object (BO)**: concepto informacional de negocio. Ej.: BO-02 Genealogía del lote.
- **Value stream / etapa (VS-01 / VS-Sn)**: secuencia de etapas que entregan valor; cada etapa documenta Entra, Acción, Salida, Valor y Actor.
- **Handoff (HO)**: transferencia de unidad e información entre etapas, con aceptación u observación.
- **Genealogía**: relación física padre/hijo entre lotes, batches y pallets (división y mezcla). **Linaje** (Phase C): procedencia y transformación de los registros.
- **Liberación de Calidad (BO-03)**: decisión exclusiva del Aprobador de Calidad (PR-07). **Condición de despacho (BO-04)**: decisión de Despacho; no deriva de BO-03.
- **Gap (GAP-B)**: diferencia entre Baseline y Target sobre el mismo building block, con evidencia.
- **REQ / AR / RF**: requisito de negocio (B) / requisito de arquitectura (C) / requisito funcional de software (fuera de alcance).
- **CRC**: componente candidato de roadmap; no es proyecto aprobado.
- **Viewpoint / View**: regla de representación para un concern / diagrama concreto construido con esa regla.
- **ABB / SBB**: bloque lógico / realización concreta (ninguna seleccionada).
- **HP / IA / SV / DE / NV**: hecho público / supuesto o simulado / decisión académica / pendiente de validar. Desconocido no es cero.

## Términos de Phase C, D y gobierno (PC3)

- **ABB (Architecture Building Block)**: bloque requerido, definido por funcionalidad, interfaces, NFR y dependencias, sin producto. Ej.: T-ABB04 Transporte resiliente y réplica local.
- **SBB (Solution Building Block)**: realización concreta (producto, servicio o despliegue); en PC3 solo se comparan alternativas (SBB-T01…T04), la selección es de Phase E.
- **NFR-T**: requisito no funcional tecnológico con métrica, umbral, método de prueba y owner. Ej.: NFR-T01 autonomía ≥ 24 h.
- **Genealogía vs. linaje**: la genealogía relaciona unidades físicas (padre/hijo); el linaje (*data lineage*) muestra de qué fuentes y transformaciones proviene un dato.
- **Data Owner / Data Steward / custodio técnico**: responde por el significado y el riesgo / por la definición y la calidad / por la operación técnica del dato.
- **Zona y conducto (ISA/IEC 62443)**: grupo de activos con requisitos de seguridad comunes / canal controlado de comunicación entre zonas.
- **Plateau y Gap (ArchiMate)**: estado estable de la arquitectura (Baseline, Target) / diferencia entre dos plateaus.
- **HITL**: control humano obligatorio antes de que una sugerencia automática tenga efecto (PR-07).
- **Oportunidad diferida (OPP)**: idea de solución sin gap de negocio que la justifique; se registra para Phase E y no entra al Target (PR-05).
- **Clases de evidencia**: HP, IA, SV, DE, NV, NE (ver Reglas_de_evidencia.md).
