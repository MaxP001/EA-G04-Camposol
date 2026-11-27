# Registro de cambios v3.0 · Phase D · 2026-11-11

Draft v3.0 · Decisión académica Grupo 04 · sin aprobación corporativa

| ID | Elemento | Cambio | Decisión | Documento |
|---|---|---|---|---|
| CHG-D01 | PR-06 | Se precisa con métrica: autonomía ≥ 24 h de captura y consulta local (NFR-T01) | Refinado (propuesta) | T1/03; Principles_Register |
| CHG-D02 | Principios | PR-09 Control OT local sin mando remoto y PR-10 Seguridad por zonas y conductos | Nuevo (propuesta) | T1/03; Principles_Register |
| CHG-D03 | TSV-C01 (Phase A) | Se detalla en TS-01 Captura y TS-02 Almacenamiento y reenvío (Aggregation) | Trazabilidad A → D | Equivalencias_ID |
| CHG-D04 | PD-01…PD-07 | Cerrados como DEC-D01…D08; lo no verificable pasa a NV-10…NV-13 | Cierre de pendientes C→D | T2/03; T-09 |
| CHG-D05 | AP-08 / AP-09 (Phase C) | Se despliegan en artefactos de borde y central sin cambiar su responsabilidad lógica ni sus contratos | Sin cambio de C2 | T-V03 |
| CHG-D06 | Modelo consolidado | XML v3.0: A+B+C+D con 27 vistas (16 + 11) | Integración | 12_Phase_D_Vistas_ArchiMate |
| CHG-D07 | SoI, VS-01, C1, C2, LOC-01 | Sin cambios | Confirmado en gate D→E | — |
| CHG-D08 | IDs de Phase D v0.5 | Renombrados según DEC-D15 (NFR-T, TD-RC, T-BASE/T-TAR, FAC/EQ, STD-T); NFR y principios ya no son elementos XML (como AR-D/AR-A en C) | Convención | Equivalencias_ID.csv; T2/07 |

## Verificación automática

- OK GAP-T01 → NFR-T01; NFR-T02; NFR-T03 → TD-RC03 → DEC-D01 → TEST-T01; TEST-T02; TEST-T03
- OK GAP-T02 → NFR-T05; NFR-T06 → TD-RC01; TD-RC02 → DEC-D02 → TEST-T05; TEST-T06
- OK GAP-T03 → NFR-T07; NFR-T09 → TD-RC04 → DEC-D03 → TEST-T07; TEST-T09
- OK GAP-T04 → NFR-T04; NFR-T13 → TD-RC06 → DEC-D04 → TEST-T04; TEST-T13
- OK GAP-T05 → NFR-T08 → TD-RC03 → DEC-D05 → TEST-T08
- OK GAP-T06 → NFR-T10 → TD-RC06 → DEC-D06 → TEST-T10
- OK GAP-T07 → NFR-T11 → TD-RC07 → DEC-D07 → TEST-T11
- OK GAP-T08 → NFR-T12 → TD-RC05 → DEC-D08 → TEST-T12
- OK GAP-T09 → NFR-T09 → TD-RC08 → DEC-D09 → TEST-T09
- OK 1 NFR-T ↔ 1 TEST-T (13/13)
- OK Todo NFR-T proviene de al menos un GAP-T
- OK Cada NFR-T cita su TEST-T
- OK Todo NFR-T es realizado por ≥ 1 servicio tecnológico (CP-09)
- OK Todo TD-RC agrupa al menos un GAP-T
- OK Dependencias de TD-RC válidas (TD-RC, D-RC, A-RC o NV)
- OK 8 T-ABB con servicios existentes en el modelo
- OK 8 artefactos Phase D registrados (T-01, T1/12)
- OK PD-01…PD-07 cerrados o reasignados a NV
- OK Dimensionamiento: 28 320 ev/día; 3 540 en E1; drenaje 9,4 min
- OK Sin servicio/flujo desde central o SAP hacia PLC/HMI (PR-09)
- OK AP-08…AP-11 con artefacto desplegado (CP-08)
- OK LOC-01 (Phase B) conservado como Location; áreas como Facility y máquinas como Equipment
- OK XML A+B+C+D bien formado: 258 elementos y 482 relaciones con referencias válidas
- OK Relaciones nuevas de Phase D en pares permitidos por ArchiMate 3.2 (subconjunto verificado)
- OK Los 145 elementos de Preliminary/A/B/C se conservan con el mismo ID
- OK 27 vistas en el modelo consolidado (16 heredadas + 11 de Phase D)
- OK Vista T-V01: 16 nodos, 10 conexiones; subgrafo completo
- OK Vista T-V01: XML individual y esquema SVG/PNG
- OK Vista T-V02: 19 nodos, 16 conexiones; subgrafo completo
- OK Vista T-V02: XML individual y esquema SVG/PNG
- OK Vista T-V03: 18 nodos, 14 conexiones; subgrafo completo
- OK Vista T-V03: XML individual y esquema SVG/PNG
- OK Vista T-V04: 15 nodos, 15 conexiones; subgrafo completo
- OK Vista T-V04: XML individual y esquema SVG/PNG
- OK Vista T-V05: 25 nodos, 3 conexiones; subgrafo completo
- OK Vista T-V05: XML individual y esquema SVG/PNG
- OK Vista T-V06: 23 nodos, 2 conexiones; subgrafo completo
- OK Vista T-V06: XML individual y esquema SVG/PNG
- OK Vista T-V07: 19 nodos, 18 conexiones; subgrafo completo
- OK Vista T-V07: XML individual y esquema SVG/PNG
- OK Vista T-V08: 16 nodos, 20 conexiones; subgrafo completo
- OK Vista T-V08: XML individual y esquema SVG/PNG
- OK Vista T-V09: 17 nodos, 8 conexiones; subgrafo completo
- OK Vista T-V09: XML individual y esquema SVG/PNG
- OK Vista T-V10: 17 nodos, 18 conexiones; subgrafo completo
- OK Vista T-V10: XML individual y esquema SVG/PNG
- OK Vista X-V02: 19 nodos, 18 conexiones; subgrafo completo
- OK Vista X-V02: XML individual y esquema SVG/PNG
- OK Todo elemento nuevo de Phase D aparece en al menos una vista
- OK 11 XML individuales bien formados
- OK T-00…T-09 presentes y abren sin error
- OK IDs citados en T-00…T-09 definidos (178 IDs)
- OK Sin IDs v0.5 residuales en los documentos
- OK Sin IDs v0.5 residuales en T1
- OK T1 con las 12 hojas del formato T&G (01…12)
- OK T2 con las 6 hojas del formato T&G + 07_Verificacion
- OK Resumen de gate en PDF de 5 páginas (guía: 4–6)

Resultado: 57 OK · 0 fallas.
