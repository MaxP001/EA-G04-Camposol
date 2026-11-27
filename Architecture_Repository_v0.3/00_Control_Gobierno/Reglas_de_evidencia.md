# Reglas de evidencia · Repository v0.3 (PC3)

Grupo 04 · SI605 · 2026-11-26 · Aprobadas por ROL-AB académico (DEC-PC3-03)

## Reglas

| ID | Regla | Enunciado | Origen |
|---|---|---|---|
| RE-01 | Evidencia y escenario explícitos | Toda afirmación declara su clase (HP, IA, SV, DE, NV, NE) y su fuente. Un dato IA o SV nunca se presenta como hecho de Camposol. | Ex PR-01 |
| RE-02 | Medición comparable | Baseline y Target se comparan con la misma unidad, población y fórmula; "desconocido" es NE, nunca cero. | Ex PR-04 |
| RE-03 | Separación de autoría | Las decisiones (DE) son del Grupo 04 y las ratifica ROL-AB. La IA redacta, genera escenarios y verifica, sin autoridad de decisión; cada uso queda en `09_Evidencia_Fuentes/Registro_Uso_IA.csv`. | v0.3 |
| RE-04 | Baseline real separada | Junto a cada valor IA de Baseline se declara "Baseline real = NE" y el NV que lo valida. | PC3 |

## Clases (guía PC3 §1.3)

| Clase | Nombre | Tratamiento obligatorio | Rango en el expediente |
|---|---|---|---|
| HP | Hecho público | URL, fecha, emisor y alcance de lo que prueba | F01–F14 |
| IA | Generado por IA | Modelo/herramienta, objetivo, entrada, salida, validación y límites | DS-CS-01…51; IA-01…07; IAU-01…05 |
| SV | Supuesto por validar | Plausibilidad, efecto, responsable y prueba de validación | Cargos tipo (STK), PN-04 |
| DE | Decisión del equipo | Alternativas, rationale, impacto y firmante (DEC) | DEC-01…DEC-PC3-07 |
| NV | No verificado | Owner, prioridad, fecha límite y cómo conseguir la evidencia | NV-01…13 |
| NE | No evaluado | Valor no medido; nunca cuenta como cero | Baseline real de KPI y capacidades |

Equivalencia con la nomenclatura interna anterior (v0.3–v3.0): P → HP; S → IA (dataset y escenarios) o SV (supuestos humanos); D → DE; NV → NV/NE (EQV-PC09).
