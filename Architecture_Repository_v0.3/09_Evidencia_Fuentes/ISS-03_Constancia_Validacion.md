## Resultado de la revisión

| Comprobación | Resultado |
|---|---|
| XML originales encontrados e importados por Archi | 21 de 21 |
| Nativos correspondientes guardados por Archi | 21 de 21 |
| Vistas individuales importadas y guardadas por Archi | 34 de 34 |
| Reapertura y guardado del modelo principal | Correctos |
| Archivo nativo original suministrado por el equipo | También abrió y se pudo guardar |
| Validador de la interfaz de Archi para el modelo principal | 0 errores y 113 advertencias |
| Tipos de las 554 relaciones del modelo vigente | Compatibles con las reglas incluidas en Archi |
| Solapamientos rectangulares entre elementos hermanos después del ajuste | 0 |

Las **113 advertencias** son **8 elementos y 105 relaciones que no se utilizan en vistas**, comprobadas contra el archivo nativo y el resultado del validador. No impiden abrir, editar ni guardar el modelo. Se conservan porque pertenecen al modelo acumulativo; eliminarlas sin revisar su función podría romper referencias documentales. El detalle está en `05_Validacion/Advertencias_Archi.csv`.

## Qué se ajustó

En **T-V09 Availability & Continuity**, los bloques del nodo de borde y de la plataforma central se superponían. Se desplazaron la plataforma central y sus elementos internos, y se separaron los servicios de ejecución y observabilidad. Se mantienen los IDs, tipos, nombres, propiedades y relaciones del modelo. El ajuste se aplicó al modelo principal, al XML individual de T-V09 y a su nativo independiente. Las imágenes se volvieron a exportar mediante Archi.

No se cambiaron las decisiones de arquitectura del informe. Se mantuvo la nomenclatura de la entrega PC3 actualizada.

## Archivos actuales e históricos

- `01_Modelo_Principal`: modelo completo para trabajar y presentar.
- `02_XML_Convertidos`: 17 modelos vigentes convertidos desde los XML originales, respetando sus rutas relativas. Algunos contienen una sola vista; otros son extractos o el consolidado.
- `03_Vistas_Individuales`: las 34 vistas del consolidado, cada una en un modelo nativo con los elementos y relaciones correspondientes.
- `04_Historico`: 4 conversiones de XML archivados, separadas de los modelos vigentes.
- `04_Imagenes_Archi`: 34 PNG generados por el motor de Archi.
- `05_Validacion`: constancia, índices, advertencias, resultados y registros de ejecución.
- `06_Visor_HTML`: informe navegable generado por Archi.
- `07_XML_Validados`: intercambio actualizado del principal y de T-V09.

**Históricos:** los archivos `Modelo_16vistas_v3.0` y `Original_ABC_v3.0` contienen, cada uno, dos relaciones incompatibles de una versión anterior. Se importan, pero no son la versión a presentar. Sus relaciones se identifican en `05_Validacion/Relaciones_incompatibles_solo_historico.csv`. Los históricos se preservan sin corregir su contenido.

## Cómo incorporarlo al repositorio del grupo

Sustituir el archivo `08_ArchiMate_Modelos/Camposol_PC3_v0.3.archimate` del repositorio por el de `01_Modelo_Principal`. Sustituir el XML consolidado y el XML de T-V09 por sus archivos de `07_XML_Validados`. La tercera variante XML de esa carpeta se corresponde con el nativo individual de T-V09 y es opcional para el repositorio original.

Añadir la constancia de `05_Validacion` como evidencia técnica para atender **ISS-03**. La decisión formal de cierre en el Issue Log y los textos del informe corresponde al grupo. Si se incorporan archivos adicionales, actualizar su MANIFEST y CHANGELOG.

## Alcance de la constancia

La validación demuestra que Archi importa y guarda los modelos y que el principal se abre en su interfaz, ofrece vistas editables y pasa las reglas de tipos de relación. No constituye aprobación docente ni corporativa, ni verifica que los datos internos de Camposol sean reales. Los archivos y el informe original adjuntos no se sobrescribieron.

El modelo nativo generado por script que venía en el repositorio también abrió correctamente. Los entregados aquí se obtuvieron mediante el importador y guardado reales de Archi, sin limitarse a cambiar la extensión del XML.

Documentación de la herramienta: https://github.com/archimatetool/archi/wiki/Archi-Command-Line-Interface
