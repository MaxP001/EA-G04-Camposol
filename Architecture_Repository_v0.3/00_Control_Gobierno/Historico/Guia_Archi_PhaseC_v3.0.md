# Guía de lectura, verificación y uso en Archi · v3.0

## Orden de lectura
1. `00_Control/README.md` y `Registro_Cambios_v3.0.md`.
2. `06_Phase_C_Entregables_TOGAF/C-00` (control) → `C-02 ADD` (arquitectura) → `C-03 ARS` (requisitos) → `C-04` (candidatos).
3. `08_Phase_C_Catalogos_Matrices/C1`, `C2` y `C3` para el detalle.
4. `07_Phase_C_Vistas_ArchiMate` para las vistas.

## Cómo abrir el modelo en Archi
1. Archi → File → Import → *Open Exchange XML Model*.
2. Seleccionar `Camposol_ADM_Preliminary_PhaseA_PhaseB_PhaseC_OpenExchange_v3.0.xml`.
3. El modelo trae 16 vistas: VIEW-A01…A04, B-V01…B-V05, D-V01…D-V03, AP-V01…AP-V03 y X-V01. Los IDs de elementos son los mismos de los catálogos.
4. En B-V01/B-V02 el rol dentro del actor y el proceso dentro del rol expresan Assignment por anidamiento.

## Verificación rápida (cadena de una brecha)
GAP-D01 (C1/Gaps_Datos) → AR-D01 (C1/Requisitos_AR_D) → D-RC01 (C1/Roadmap_D) → DEC-C01 (C3/ADR_C) → TEST-D01 → vista D-V02 → REQ-01 y GAP-B01 de Phase B (C3/REQ_BR_AR_Trace).

## Límites
Datos de Baseline simulados (DS-CS, clase IA) salvo SAP y calibradoras (HP). Componentes Target sin producto. XML validado estructuralmente; la importación en Archi debe confirmarla el equipo.
