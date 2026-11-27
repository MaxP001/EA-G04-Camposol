# Índice de evidencia para la sustentación PC3 · Grupo 04

La presentación de defensa la agrega el grupo en esta carpeta (`SI605_PC3_Grupo04_Camposol_Sustentacion.pptx`). Este índice dice dónde está la evidencia de cada pregunta probable, para responder abriendo el archivo y no de memoria.

| Pregunta probable | Respuesta corta | Evidencia (ruta) |
|---|---|---|
| ¿Qué parte del negocio cubren y por qué solo esa? | Un value stream: VS-01, de la recepción de bins a la entrega del FCL en rampa | `02_Phase_A_Architecture_Vision/A-02_Camposol_Architecture_Vision.docx` §2 (alcance 4D) |
| ¿Qué es real y qué es inventado? | HP solo SAP, calibradoras y ampliación de Chao; todo dato interno es IA y su valor real NE | `00_Control_Gobierno/Reglas_de_evidencia.md`; `09_Evidencia_Fuentes/Dataset_IA_DS-CS_Chao.csv`; `09_Evidencia_Fuentes/Registro_Uso_IA.csv` |
| Muestren la cadena de la motivación a la tecnología | E2E-01 (historia, CAP-01) y E2E-02 (liberación, CAP-07), con ruta por eslabón | `07_Entregables_Integrados/E2E_Cadenas_Trazabilidad_v0.3.xlsx` |
| ¿Por qué existe el borde de planta (T-ABB04)? | REQ-03 → AR-A04 → GAP-T01 → NFR-T01 (≥ 24 h sin WAN, 0 eventos perdidos) | `07_Entregables_Integrados/ARS_Consolidada_B_C_D_v0.3.docx` §2.5.1 y §2.11 |
| ¿Qué pasa si la WAN cae 6 horas? | La planta sigue capturando; ≈ 7 080 eventos en cola; reenvío ordenado sin duplicar | ADD-01 §2.5.4 (flujo PAL-55871); ARS-01 §2.5.2 (dimensionamiento) |
| ¿Puede la nube o el TI mandar al PLC? | No: conductos OT solo de lectura; mantenimiento remoto como excepción gobernada | `01_Preliminary/PRE-04_Principios_Arquitectura.docx` (PR-09); `06_Phase_D_Technology/T-07_IT_OT_Cybersecurity_Continuidad_v0.3.docx` |
| ¿Dónde está la IA? ¿Por qué no hay visión artificial? | La IA no es un dominio; la inspección visual se difirió (OPP-IA-01): sin gap ni KPI y la técnica simple ya cubre REQ-06 | `00_Control_Gobierno/Repo_Arq/08_Solutions/Oportunidades_Diferidas.csv`; DEC-D09 |
| ¿Quién libera un lote? | Solo ROL-B05 (Aprobador de Calidad); ningún sistema, SAP ni IA cambia QAResult | PR-07; AR-D04; NFR-T09; DEC-D12 |
| ¿Por qué target 3 y no 4 en CAP-01? | El nivel 4 exige KPI gobernados que dependen de CAP-05 y CAP-02 | `02_Phase_A_Architecture_Vision/A-01_Camposol_Capability_Assessment.docx`; DEC-PC3-02 |
| ¿Por qué no hay fechas ni olas en el roadmap? | En TOGAF el roadmap de B/C/D es insumo; Transition Architectures y calendario son de Phase E/F | DEC-PC3-06; `04_Phase_C_Data/C-04_Architecture_Roadmap_Candidates_PhaseC_v0.3.docx`; `06_Phase_D_Technology/T-04_Architecture_Roadmap_Candidatos_v0.3.docx` |
| ¿Qué SBB eligieron? | Ninguno: se compararon 4 alternativas; la selección es de Phase E | `06_Phase_D_Technology/T1_PhaseD_Catalogos_Matrices_v0.3.xlsx#13_Alternativas_SBB`; T-06 §5 |
| ¿Qué quedó abierto? | NV-01, 04, 05, 08, 09, 10, 11, 12 (condiciones del gate D→E); fechas de gates (ISS-02). ISS-03 cerrado: modelo validado en Archi (`09_Evidencia_Fuentes/ISS-03_*`) | `09_Evidencia_Fuentes/Validaciones_Pendientes.csv`; `00_Control_Gobierno/Repo_Arq/06_Governance/Issue_Log.csv` |
| ¿Qué cambiaron desde PC2? | 24 cambios (CHG-PC3-01…24) trazados a una revisión interna y a la guía; no hubo observaciones escritas del docente (OBS-PC2-00) | `CHANGELOG.md` |

| ¿Por qué las vistas se llaman D-V01-B, AP-V01-T…? | Usan los IDs de la guía PC3 §4.5 con sufijo Baseline/Target; en las Semanas 9 y 10 tenían otros IDs | `README.md` §3; `00_Control_Gobierno/Equivalencias_ID.csv` (EQV-PC21…38); DEC-PC3-11 |

Ensayo sugerido: cada integrante defiende una cadena (E2E-01, E2E-02), un principio (PR-07 o PR-09), un gap tecnológico y una decisión diferida (OPP-IA-01).
