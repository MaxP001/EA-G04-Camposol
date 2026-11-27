# Convenciones · Repository v0.3 (PC3)

- Cadena integrada: DRV → GOAL → OUT → KPI → STK/C (concern) → PR → VS-Sn/CAP → BSV/BP → BO/DOBJ → ASV/AP → TS/T-TAR/red → GAP → REQ/AR/NFR-T + TEST → ABB/SBB → vista/DEC → CRC/D-RC/A-RC/TD-RC → gate.
- Negocio: ACT, LOC, ROL-B, BF, BP, EV, BSV, BO; etapas VS-S1…S6; handoffs HO-01…06; principios de negocio PN-01…04.
- Datos y aplicaciones: DOBJ, AP, AF, ASV, AIF (interfaz de aplicación), IF (contrato lógico), ABB-C, D-RC, A-RC.
- Tecnología: T-BASE (Baseline), T-TAR (Target), TS, TPR, TEV, ART, FAC, EQ (Equipment), Z (zona), CD (conducto), T-ABB, TD-RC, SBB-T (alternativa comparada).
- Motivación y gobierno: PR (principio), RE (regla de evidencia), RST (Constraint), DEC, RSK, ISS, NV, OPP (oportunidad diferida), EQV (equivalencia de IDs).
- Un ID nunca cambia de significado ni se reutiliza; los sustituidos quedan como Superseded (PR-01, PR-04, DEC-B01…B03) o Diferido (GAP-T09 y relacionados).
- Los IDs del modelo ArchiMate son los mismos del catálogo (`Elementos.csv`).
- `Relaciones_Trazabilidad.csv` registra relaciones documentales de trazabilidad; no se confunden con las relaciones ArchiMate del modelo.
- Cada afirmación declara su clase HP, IA, SV, DE, NV o NE (`00_Control_Gobierno/Reglas_de_evidencia.md`).
