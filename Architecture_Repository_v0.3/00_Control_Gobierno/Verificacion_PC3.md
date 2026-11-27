# Verificación automática · Repository v0.3 (PC3)

Fecha: 2026-11-26 · Resultado: **28 OK / 0 fallas** · Script ejecutado sobre el ZIP final (rutas relativas a la raíz).

| ID | Comprobación | Resultado | Detalle |
|---|---|---|---|
| V-01 | Los 276 archivos abren (docx, xlsx, xml, csv) | OK |  |
| V-02 | MANIFEST cubre el 100 % de los archivos (sin huérfanos) | OK |  |
| V-03 | Toda ruta del MANIFEST existe (salvo el PPT de sustentación, registrado para que el grupo lo agregue con ese nombre) | OK | ; esperado y aún no agregado: 11_Sustentacion/SI605_PC3_Grupo04_Camposol_Sustentacion.pptx |
| V-04 | Todo archivo del MANIFEST tiene ID | OK |  |
| V-05 | Toda ruta citada en archivos vigentes (docx, xlsx, csv, md) existe | OK | RUTAS ROTAS 0 |
| V-06 | Modelo Open Exchange bien formado: 258 elementos, 554 relaciones, 34 vistas, sin referencias colgantes | OK |  |
| V-07 | Los 41 requisitos y restricciones (REQ, AR-D, AR-A, NFR-T, CNS) tienen prueba existente en Test_Catalog (3 restricciones se verifican por revisión documental) | OK |  |
| V-08 | Cada REQ-01…08 se deriva en al menos un AR-D/AR-A | OK |  |
| V-09 | Principios: 8 vigentes con Name/Statement/Rationale/Implications completos; PR-01 y PR-04 Superseded | OK | PR-02, PR-03, PR-05, PR-06, PR-07, PR-08, PR-09, PR-10 |
| V-10 | Gap Register unificado: 28 gaps ({'Negocio': 8, 'Datos': 6, 'Aplicaciones': 6, 'Tecnología': 8}); todos con origen, candidato y decisión | OK |  |
| V-11 | T-ABB08, TS-16, T-TAR13 y TD-RC08 solo aparecen como retirados/diferidos en archivos vigentes (incluido el modelo: ver V-17) | OK |  |
| V-12 | E2E-01_Historia: 33 IDs y 25 rutas comprobados | OK | IDs desconocidos: []; rutas: [] |
| V-13 | E2E-02_Liberacion: 34 IDs y 25 rutas comprobados | OK | IDs desconocidos: []; rutas: [] |
| V-14 | Todo CSV vigente tiene Ruta, Version, Estado y Fecha, y su Ruta coincide con su ubicación | OK |  |
| V-15 | Clases de evidencia en CSV dentro de HP/IA/SV/DE/NV/NE | OK |  |
| V-16 | README.md, MANIFEST.xlsx y CHANGELOG.md en la raíz; carpetas 00–11 presentes | OK |  |
| V-17 | Modelo tras M1–M14: sin IDs retirados ni AI-0x; 2 Composition componente→interfaz; 18 redes→conductos; cada gap con 2 plateaus; propiedades en todos los elementos; 34 vistas; todos los elementos documentados | OK | retirados=[]; asignaciones=0; sin doc=[] |
| V-18 | Figuras PNG/SVG de las 7 vistas nuevas de PC3 (AP-V01-B, D-V02-B, T-V11, AP-V02-B, D-V01-T, T-V01-B, X-V02) y XML de vista de T-V11, T-V01-B y X-V02 presentes | OK |  |
| V-19 | Ruta relativa máxima 74 caracteres (≤ 75). Con «Extraer todo» en C:\Users\<usuario>\Downloads la ruta total queda en ≈ 232 (límite 259) | OK |  |
| V-20 | Contenido de registros: HP con emisor/fechas/página/qué prueba; SV con plausibilidad/efecto/responsable/prueba; DEC con alternativas/impacto/firmante; 28 gaps con 22 campos llenos; CHANGELOG con fecha por fila; sin clases S/P/D/H en columnas «Clase» de xlsx y de tablas docx | OK |  |
| V-21 | El .archimate (guardado por Archi; ISS-03 cerrado) es XML válido, con las mismas vistas que el Open Exchange, IDs únicos y referencias resueltas | OK | 34 vistas; ids duplicados 0; referencias rotas 0 |
| V-22 | Las vistas mínimas de la guía §4.5 existen en el modelo y en View_Catalog con el ID de la guía (D-V01, D-V02, AP-V01, AP-V02, T-V01, T-V02 con -B y -T; X-V01 y X-V02) y las figuras usan esos nombres (DEC-PC3-11) | OK |  |
| V-24 | MANIFEST: 277 filas con ID único por archivo | OK |  |
| V-25 | Los enlaces Markdown `[texto](ruta)` de los archivos vigentes apuntan a archivos existentes | OK |  |
| V-26 | Cadenas E2E coherentes con los maestros: driver del requisito de negocio, origen de cada AR, gap de cada NFR y prueba de cada requisito citado | OK |  |
| V-27 | El método de verificación de cada NFR-T es idéntico en Requirements_Catalog, T1/04 y T2/02 (un solo conjunto de casos de aceptación por prueba) | OK |  |
| V-28 | Ninguna vista del .archimate tiene elementos hermanos superpuestos (geometría) | OK | 0 superposiciones entre elementos hermanos en 34 vistas |
| V-23 | Ningún ID de vista anterior al renombrado (D-V04, AP-V03B, T-V07, …) aparece en archivos vigentes, salvo como ID de la guía, en Historico, CHANGELOG y Equivalencias_ID (EQV-PC21…38) | OK |  |

**Qué NO comprueba este script:** que Archi abra el `.archimate` (lo comprobó el grupo en la interfaz de Archi: ISS-03 cerrado, capturas en 09_Evidencia_Fuentes); que la extracción funcione en un Windows real (solo mide longitudes); la corrección semántica de cada relación ArchiMate frente al Apéndice B (revisada a mano, no por validador); la exactitud de las fuentes HP (reconsultadas por web el 2026-11-26); la calidad de redacción. La completitud frente a la guía está en `00_Control_Gobierno/Matriz_Cumplimiento_PC3.xlsx`.

Pendiente del grupo: confirmar fechas de gates (ISS-02); agregar el PPT de sustentación como `11_Sustentacion/SI605_PC3_Grupo04_Camposol_Sustentacion.pptx` (ya está en el MANIFEST como SUS-02); exportar el informe a PDF para la entrega. ISS-03 cerrado (CHG-PC3-25).
