# Estrategia y registro de búsqueda

**Título revisado:** *Análisis de Sentimientos con Modelos de Lenguaje para Sistemas de Recomendación: Una Revisión Sistemática de la Literatura*. **Fecha de búsqueda y corte:** 1 de noviembre de 2026. **Propósito:** identificar cómo se aplican modelos de lenguaje y análisis de sentimiento a reseñas en tareas de recomendación y explicación, y comparar corpus, métodos, métricas, resultados y límites.

## Preguntas guía / PICOC

| Componente | Delimitación |
|---|---|
| Población | Reseñas, opiniones y texto generado por usuarios sobre productos, servicios, películas, videojuegos y otras entidades recomendadas. |
| Intervención | Análisis de sentimiento y modelos de lenguaje, incluidos Transformers, para representar, clasificar o generar información basada en reseñas. |
| Comparación | Métodos tradicionales, enfoques híbridos, modelos preentrenados, LLM y sistemas sin análisis de sentimiento explícito. |
| Resultados | Clasificación sentimental; precisión de rating/ranking; utilidad, fidelidad y diversidad de explicaciones; costo y eficiencia cuando se reporten. |
| Contexto | Sistemas de recomendación, reseñas en línea y generación/síntesis de explicaciones. |

## Términos y cadenas

Se agruparon variantes y sinónimos para recuperar evidencia de tres etapas relacionadas: entender polaridad, incorporar texto en recomendación y comunicar la recomendación mediante explicaciones o resúmenes.

| Concepto | Palabras clave |
|---|---|
| Opinión | sentiment analysis, opinion mining, sentiment classification, aspect-based sentiment, polaridad, análisis de sentimientos |
| Texto | review, user-generated content, online review, reseña, comentario |
| Modelos | language model, pretrained language model, Transformer, BERT, LLM, SVM, TF-IDF, hybrid, ensemble |
| Recomendación | recommender system, recommendation, review-based recommendation, explainable recommendation, rating prediction |
| Aplicación | game review, Steam, Amazon, Yelp, movie review, e-commerce |

```text
Q1: ("sentiment analysis" OR "opinion mining" OR "aspect-based sentiment")
    AND ("recommender system" OR recommendation OR "rating prediction")
    AND (review OR "user-generated content")
Q2: ("pretrained language model" OR Transformer OR BERT OR LLM)
    AND (sentiment OR review OR opinion)
    AND (recommender OR recommendation OR explanation)
Q3: ("game review" OR Steam OR "online product review")
    AND (sentiment OR BERT OR Transformer OR "language model")
Q4: ("explainable recommendation" OR "opinion summarization")
    AND (review OR sentiment OR "language model")
Q5: (survey OR "systematic literature review")
    AND ("sentiment analysis" OR "recommender systems" OR "language models")
```

Las expresiones anteriores son una estrategia reproducible por bloques. Las consultas efectivamente enviadas y las búsquedas de verificación quedan en [consultas_ejecutadas.json](consultas_ejecutadas.json). Se buscó por título, DOI, venue y frases en páginas académicas/editoriales accesibles. Se priorizaron ACL Anthology, IEEE, ACM, AAAI, Springer, MDPI, ACM author copies, arXiv complementario y repositorios institucionales. El registro no finge consultas nativas a Scopus, Web of Science, ScienceDirect o Semantic Scholar cuando no se exportaron desde esas plataformas.

## Fechas, criterios y selección

Fecha límite inclusiva: 1/11/2026. Ventana reciente: 2022–2026. Los dos trabajos anteriores se admiten por su papel fundacional: Pang et al. para polaridad supervisada en reseñas, y Zheng et al. para integración profunda de reseñas en recomendación. El corpus principal contiene 12 trabajos: diez recientes (83,3 %) y dos seminales. El survey se identifica dentro de la ventana y no se añade dos veces al denominador.

Se incluyeron publicaciones formales o artículos científicos con texto suficiente para identificar método, datos/tarea y resultados o alcance de síntesis; estudios de análisis sentimental de reseñas, integración de reseñas en recomendación, explicaciones/resúmenes que procesan opiniones y surveys pertinentes. Se excluyeron duplicados, documentos sin metadatos verificables y estudios de recomendación que no usaran reseñas, texto u opinión en su objeto analítico. Un candidato encontrado solo mediante resumen se conserva como pendiente, no se eleva al corpus de lectura.

| Etapa | Criterio de registro | Resultado de esta sesión |
|---|---|---|
| Detección | Título, autores, año, DOI/URL y propósito | Registro de consultas y candidatos. No se calcula un número global de hits de motores heterogéneos. |
| Deduplicación | DOI; título + autores para duplicados/versiones | R01–R12 son trabajos distintos; preprints/versiones espejo no cuentan aparte. |
| Selección | Pertinencia, tipo de fuente y datos suficientes para extracción | Matriz de 12. Se excluye del conteo el candidato sin evaluación completa que solo fue encontrado por abstract. |
| Calidad | Diseño, etiqueta de sentimiento, partición, métricas, limitaciones, venue y recursos | Evaluación cualitativa por dominio; véase [criterios_calidad.md](criterios_calidad.md). |

La estrategia de descubrimiento se apoyó en búsquedas web por frases y dominios, acceso a textos primarios y referencias consultadas. Se usó snowballing dirigido desde DeepCoNN, PEPLER, Wu et al. y el artículo de Steam, revisando citas y trabajos relacionados disponibles en páginas editoriales e índices. No se interpreta ese rastreo como grafo completo de citación.

## Candidatos y pendientes

El artículo de Tan et al. (2022) estudia ensambles sentimentales en IMDb/Twitter, sin conexión directa con recomendación: se conserva como candidato metodológico, no como parte de R01–R12. *Forecasting User Perception of Steam Game Reviews across Multiple Genres* (2026; DOI 10.59562/jessi.v7i3.13290) apareció durante el cribado y se deja como candidato: falta evaluar de forma suficiente el venue y el texto completo para incorporarlo. El ámbito de juegos está representado por R05; los sistemas de recomendación abarcan más que videojuegos, como ya planteaba PICOC en el borrador.

El Documento 1 reporta 29 estudios y un protocolo anterior, pero contiene referencias incompletas, temas mezclados y detalles bibliográficos no verificables. Ese número no se toma como resultado de la presente búsqueda ni se presentan sus registros como auditados. La revisión de esta sesión es una nueva síntesis documentada con fuentes primarias localizadas. Para denominarla RSL exhaustiva final aún hacen falta exportaciones nativas de bases bibliográficas, cribado por una segunda persona y un criterio de cierre de búsqueda previamente fijado.

## Registro de consultas

Las búsquedas ejecutadas se registraron por lotes Q01–Q08, más verificación de metadatos, venues y referencias en textos primarios. Se guardan consultas literales en JSON, con la fecha de ejecución. El buscador no proporciona en todos los casos un conteo reproducible ni los mismos filtros; por eso no se presenta un diagrama PRISMA ficticio. Se documenta el corpus efectivamente leído y los candidatos pendientes para que el equipo continúe la búsqueda formal.
