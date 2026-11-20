# Reglas de evidencia

| ID | Regla | Enunciado | Origen |
|---|---|---|---|
| RE-01 | Evidencia y escenario explícitos | Toda afirmación declara su clase (P, S, D, NV) y su fuente; un dato S nunca se presenta como hecho de Camposol. | Ex PR-01 |
| RE-02 | Medición comparable | Baseline y target se comparan con la misma unidad, población y fórmula; desconocido no es cero. | Ex PR-04 |
| RE-03 | Separación de autoría | Las decisiones son del Grupo 04; las herramientas de asistencia (IA-07) solo redactan y verifican, sin autoridad de decisión. | Nuevo v0.3 |

## Clases

| Clase | Nombre | Regla | Equivalencia v0.2 |
|---|---|---|---|
| P | Hecho público verificable | Fuente pública F01–F08 con URL, fecha y alcance. Contextualiza; no prueba un problema interno de Chao. | HP |
| S | Supuesto o dato simulado | Escenario académico declarado: dataset DS-CS-01…12 y valores sintéticos heredados de PC1 (IA-01…06). No representa información de Camposol. | IA, SV |
| D | Decisión arquitectónica | Decisión académica del Grupo 04 registrada con rationale (DEC). No es aprobación corporativa. | DE |
| NV | Pendiente de validación | Dato que solo la empresa puede confirmar (NV-01…08). Se mantiene visible; no bloquea el avance académico. | NV, NE |
