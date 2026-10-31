# Desarrollo — U3 Sesión 2: Objetivos, hipótesis y variables

**Autor:** Yoseth Orlando Llave Huachaca

**Curso:** Investigación III — Universidad Peruana Unión

**Fecha:** 31 de octubre de 2026

**Estado:** propuesta metodológica para incorporación posterior al PPI; sin ejecución experimental.

Este avance continúa el [problema de la sesión 1](../U3_S01_problema_justificacion/desarrollo.md). La base documental se mantiene limitada a los dos borradores proporcionados. Las decisiones de operacionalización que se formulan aquí son propuestas para el estudio, no resultados extraídos de los artículos. Las fuentes primarias citadas en los borradores siguen pendientes de consulta.

## E1. Pregunta de investigación revisada

### Brecha identificada

La evidencia reunida no permite establecer qué diferencias de desempeño existen entre TF-IDF + SVM y un Transformer en español al clasificar sentimientos en el mismo corpus de comentarios ciudadanos sobre limpieza pública y recojo de residuos en Juliaca. La brecha es comparativa y contextual, y conserva su carácter preliminar hasta ampliar y documentar la búsqueda bibliográfica.

### Pregunta

¿Qué diferencias de desempeño, medidas principalmente mediante macro-F1, presentan un clasificador TF-IDF + SVM y un modelo Transformer en español al clasificar sentimientos en comentarios ciudadanos sobre limpieza pública y recojo de residuos sólidos en Juliaca?

### Revisión de la delimitación

La pregunta identifica el factor comparado, el resultado, el contexto y la unidad textual de análisis. Puede responderse mediante predicciones contrastadas con etiquetas de referencia sobre una misma partición de prueba. Su viabilidad depende de confirmar la fuente, el periodo, el volumen de datos y la posibilidad de etiquetarlos consistentemente. No implica representar a toda la ciudadanía ni evaluar directamente la calidad del servicio municipal.

## E2. Objetivo general

Comparar el desempeño de un clasificador TF-IDF + SVM y un modelo Transformer en español para clasificar sentimientos en comentarios ciudadanos sobre limpieza pública y recojo de residuos sólidos en Juliaca, mediante macro-F1 como indicador principal y métricas complementarias bajo un protocolo de evaluación común.

El objetivo responde directamente a la pregunta y será verificable mediante resultados experimentales documentados, una vez comprobada la factibilidad del corpus.

## E3. Objetivos específicos

| Código | Objetivo específico | Resultado verificable | Relación con el objetivo general |
|---|---|---|---|
| OE1 | Caracterizar la disponibilidad y las propiedades de un corpus de comentarios pertinentes al contexto de Juliaca, considerando procedencia, periodo, distribución de etiquetas y consistencia de la anotación. | Ficha del corpus, guía de etiquetado, recuentos por clase y registro de desacuerdos revisados. | Delimita los datos y las condiciones bajo las que tendrá sentido comparar los modelos. |
| OE2 | Evaluar el desempeño de TF-IDF + SVM y de un Transformer en español sobre una partición de prueba común y con configuraciones documentadas. | Predicciones por comentario, configuraciones y métricas de cada modelo. | Produce resultados comparables para los dos enfoques. |
| OE3 | Determinar la magnitud y la incertidumbre de la diferencia de macro-F1 entre ambos enfoques conforme a un procedimiento de comparación definido antes de evaluar el conjunto de prueba. | Diferencia de macro-F1 y análisis de incertidumbre según el protocolo adoptado. | Responde a la pregunta y permite contrastar la hipótesis. |
| OE4 | Analizar los errores de clasificación por categoría de sentimiento y describir las limitaciones de aplicación de los modelos al corpus estudiado. | Matrices de confusión y análisis documentado de errores. | Explica el alcance de las diferencias observadas y sus límites. |

Los objetivos siguen una secuencia de caracterización, evaluación, comparación y análisis. La recopilación, el entrenamiento y el registro de parámetros serán actividades necesarias para alcanzar estos resultados; no se presentan como resultados ya obtenidos.
