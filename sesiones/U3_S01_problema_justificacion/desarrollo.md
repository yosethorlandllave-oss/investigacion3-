# Desarrollo — U3 Sesión 1: Identificación del problema y justificación

**Título de la investigación:** Análisis de Sentimientos con Modelos de Lenguaje para Sistemas de Recomendación: Una Revisión Sistemática de la Literatura

**Autor:** Yoseth Orlando Llave Huachaca

**Curso:** Investigación III — Universidad Peruana Unión

**Fecha:** 1 de noviembre de 2026

**Estado:** formulación del problema de revisión, para integrar al PPI.

## E1. Tema de investigación

La revisión estudia métodos de análisis de sentimientos basados en modelos de lenguaje para interpretar reseñas y usar su información en sistemas de recomendación. Incluye tanto clasificación de polaridad como uso de reseñas para estimar ratings, personalizar recomendaciones, producir explicaciones o resumir opiniones. Distingue análisis de sentimiento, predicción de preferencias y recomendación como tareas relacionadas, pero con resultados de evaluación diferentes.

## E2. Contexto y situación problemática

Las reseñas en línea contienen expresiones valorativas sobre productos, servicios y contenidos. Los modelos de lenguaje permiten representar aspectos semánticos y contextualizar expresiones; los recomendadores, a su vez, pueden combinar texto con ratings e interacciones para predecir preferencias o explicar resultados. Sin embargo, un buen clasificador sentimental no demuestra por sí solo que las recomendaciones mejoren: para establecerlo se debe medir el resultado downstream del sistema.

El Documento 1 plantea una RSL sobre sentimientos en reseñas con modelos de lenguaje, con énfasis declarado en sistemas de recomendación de videojuegos. Su introducción discute Steam/Epic, sentimiento por aspectos, modelos híbridos, interpretabilidad y eficiencia. Luego la estrategia PICOC amplía el contexto a reseñas en línea y comercio electrónico. El texto informa 29 estudios, pero su bibliografía contiene registros incompletos y trabajos de relevancia heterogénea. Por ello, sus cifras y conclusiones no pueden asumirse como resultados reproducibles de la presente revisión.

La literatura localizada también usa distintas unidades y métricas: F1 o accuracy para clasificar polaridad; MSE/RMSE para predicción de ratings; ranking para calidad de recomendación; y medidas automáticas o evaluación humana para explicaciones. Compararlas como si midieran el mismo fenómeno puede llevar a conclusiones erróneas. La situación problemática es la falta de una síntesis trazable que conecte qué se extrae de las reseñas, cómo se incorpora a modelos de lenguaje y si ello aporta a la recomendación, explicación o experiencia de usuario.

## E3. Evidencia de la existencia del problema

| Evidencia primaria | Hallazgo útil para delimitar el problema | Límite |
|---|---|---|
| Pang et al. (2002), reseñas cinematográficas | Compara clasificadores supervisados de polaridad, incluido SVM. | Clasificación de sentimiento no implica integración en recomendación. |
| Zheng et al. (2017), DeepCoNN | Integra reseñas de usuarios e ítems para predecir ratings. | Usa redes convolucionales; no es un Transformer ni mide polaridad directamente. |
| Fadhlurrahman et al. (2023), reseñas de Steam | Contrasta BERT y BiLSTM-CRF en reseñas de videojuegos. | La clasificación no mide una recomendación personalizada posterior. |
| Li et al. (2023), PEPLER; Xie et al. (2023), PRAG | Usan modelos preentrenados, reseñas y generación de explicaciones dentro de recomendación. | Evalúan rating y explicación con métricas distintas de clasificación sentimental. |
| Ma et al. (2024), XRec | Combina señales colaborativas y LLM para explicar comportamiento usuario–ítem. | Explicabilidad no equivale a precisión de polaridad. |
| Roumeliotis et al. (2026) | Compara LLM individuales, agregación y ensambles para sentimiento de reseñas de compra dentro de recomendación; reporta desempeño y costos. | La referencia de polaridad se deriva de ratings y el modelo depende de servicios cerrados. |

La matriz de la sesión 3 consigna datasets, protocolos, métricas y resultados extraídos. También muestra que las conclusiones no son directamente comparables sin atender a las etiquetas y a la tarea evaluada.

## E4. Brecha de investigación (research gap)

**Brecha preliminar:** la evidencia se distribuye entre clasificación de sentimientos en reseñas, integración del texto en predicción de preferencias y generación de explicaciones/resúmenes. Hace falta una síntesis crítica y trazable que compare cómo se conectan esas etapas, qué señales de opinión usan los modelos de lenguaje y qué evidencia demuestra mejoras en la recomendación, junto con los costos, limitaciones y riesgos de fidelidad.

La brecha no afirma que no existan trabajos; la revisión incluye estudios directamente relacionados y uno de 2026 que evalúa sentimiento y ensambles en recomendación. La pregunta pendiente es cómo organizar y comparar esa evidencia con criterios metodológicos comunes, incluidos los artículos del borrador original que puedan verificarse. La conclusión se limita al corpus y estrategia documentados en la sesión 3.

## E5. Problema y pregunta de investigación

**Problema:** la evidencia sobre sentimientos, modelos de lenguaje y sistemas de recomendación se evalúa con tareas, datos y métricas diferentes, lo que dificulta reconocer cuándo el análisis sentimental mejora una predicción o explicación recomendadora y qué costos o limitaciones conlleva.

**Pregunta de investigación:** ¿Cómo se han aplicado y evaluado los modelos de lenguaje y el análisis de sentimientos en reseñas para apoyar sistemas de recomendación, qué datos y métricas se utilizan, y qué limitaciones y brechas reporta la literatura?

La pregunta es apropiada para una revisión, no para un experimento causal. Su población documental y criterios de búsqueda se delimitan en la sesión 3.

## E6. Justificación

**Científica.** La revisión organiza la relación entre clasificación sentimental y recomendación, separa evidencia sobre predicción, personalización, explicación y resumen, e identifica las condiciones bajo las cuales los resultados pueden compararse. Esto permite ubicar con precisión qué aporta cada familia de modelos y evita deducir valor recomendador a partir de F1 aislado.

**Metodológica.** El trabajo documenta la estrategia de búsqueda, selección y extracción de datos, registra las diferencias de métrica y formula una síntesis temática. La matriz facilita replicación y actualización; las limitaciones de los borradores se hacen explícitas en vez de convertir referencias incompletas en evidencia verificada.

**Práctica y tecnológica.** La síntesis puede orientar a equipos que desarrollan recomendadores basados en reseñas a elegir datos, señales, métricas y procedimientos de explicación apropiados. La revisión también organiza aspectos de costo y eficiencia cuando los estudios los reportan. Sus resultados no garantizan un aumento de satisfacción o calidad comercial; esa conclusión requeriría evaluación con usuarios y sistemas desplegados.

## E7. Referencias científicas utilizadas

La lista completa y trazable de 12 trabajos se presenta en E9 de la sesión 3. Entre las fuentes centrales se encuentran Pang et al. (2002), Zheng et al. (2017), Li et al. (2023), Xie et al. (2023), Ma et al. (2024), Wu et al. (2024) y Roumeliotis et al. (2026). Se emplean las fichas de origen y DOI registradas en la matriz; los antecedentes incompletos del Documento 1 se mantienen pendientes hasta su verificación.

## Control de avance

- [x] Tema y contexto delimitados al título original.
- [x] Situación problemática formulada en términos de la síntesis de evidencia.
- [x] Evidencia primaria localizada y límites explicitados.
- [x] Brecha y pregunta de revisión formuladas sin declarar ausencia universal de trabajos.
- [x] Justificaciones científica, metodológica y práctica.
- [x] Referencias trazables a la sesión 3.
