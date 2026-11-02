# Desarrollo — U3 Sesión 3: Estado del arte

**Título de la investigación:** Análisis de Sentimientos con Modelos de Lenguaje para Sistemas de Recomendación: Una Revisión Sistemática de la Literatura

**Autor:** Yoseth Orlando Llave Huachaca

**Curso:** Investigación III — Universidad Peruana Unión

**Fecha de corte:** 1 de noviembre de 2026

**Estado:** protocolo y síntesis bibliográfica documentados; borrador para integrar al Perfil de Proyecto de Investigación.

## Alcance del producto

Esta versión conserva el título original del Documento 1. Examina el análisis de sentimientos en reseñas con modelos de lenguaje y su relación con sistemas de recomendación. Distingue clasificación de polaridad, predicción de rating/ranking, recomendación explicable y resumen de opiniones. No se afirma que una mejora en clasificación produzca automáticamente mejores recomendaciones.

Se seleccionaron 12 trabajos científicos, incluidos dos antecedentes seminales, dos surveys y diez publicaciones recientes (2022–2026; 83,3 % del corpus). Se aplicaron criterios explícitos de búsqueda, elegibilidad y extracción. El resultado constituye una revisión sistemática de literatura en desarrollo: faltan exportaciones de bases nativas y una segunda persona para reproducir el cribado, por lo que no se declara cierre exhaustivo tipo PRISMA.

## E1. Estrategia y registro de búsqueda

### Pregunta de revisión

¿Cómo se han aplicado y evaluado los modelos de lenguaje y el análisis de sentimientos en reseñas para apoyar sistemas de recomendación, qué datos y métricas se utilizan, y qué limitaciones y brechas reporta la literatura?

Se empleó PICOC para cubrir reseñas, análisis sentimental/modelos de lenguaje, comparadores tradicionales e híbridos, métricas de sentimiento/recomendación/explicación y plataformas de productos o contenidos digitales. Se combinaron términos en inglés y español sobre sentiment analysis, opinion mining, online reviews, BERT/Transformer/LLM, recommender systems, recommendation, Steam, Amazon, Yelp, explainable recommendation y opinion summarization.

La [estrategia de búsqueda](evidencias/busqueda/estrategia_registro.md) conserva PICOC, cadenas por bloques, ventana, etapas, snowballing y candidatos pendientes. Las [consultas ejecutadas](evidencias/busqueda/consultas_ejecutadas.json) registran búsquedas por frase, DOI, dominio y fuente primaria. Se documenta lo efectivamente consultado; no se inventan exportaciones ni recuentos de bases que no se obtuvieron.

## E2. Criterios de selección y calidad

Se incluyeron trabajos con metadatos verificables y suficiente información sobre sentimiento en reseñas, integración textual en recomendación, explicación/síntesis basada en opiniones o surveys de esas tareas. La ventana fue 2022–2026. Pang et al. (2002) y Zheng et al. (2017) se admitieron por su papel fundacional en clasificación sentimental y recomendación con reseñas. Se conservaron publicaciones en inglés porque el campo y sus benchmarks son multilingües.

La evaluación considera pertinencia, método/datos, validez de etiquetas, partición y métrica, limitaciones, disponibilidad declarada y venue. No se sumaron puntos de calidad sin justificación. La categoría del venue, índice y año deben quedar identificados; cuando no se verificó una categoría de ranking, se dice así y se utiliza un juicio reservado. Véase [criterios de calidad](evidencias/busqueda/criterios_calidad.md).

El corpus final tiene **12 publicaciones: 10 de 2022–2026 (83,3 %) y dos seminales**. El denominador cuenta publicaciones únicas, no versiones espejo ni artículos encontrados en abstract. La tabla registra un candidato Steam 2026 pendiente y el estudio general de Tan et al. (2022) como adyacente, fuera del conteo principal.

## E3. Matriz de síntesis

La [matriz de R01–R12](evidencias/matrices/matriz_sintesis.md) incluye propósito, modelo, dataset, tipo de etiqueta, tarea, métrica, resultados extraídos, limitaciones y fuente primaria. `NR` significa no reportado o no verificado en el pasaje consultado. No se descargaron o ejecutaron códigos/datasets de terceros; las disponibilidades se califican como declaraciones del artículo.

### E4. Antecedentes seminales y surveys

- **R01 — Pang, Lee y Vaithyanathan (2002):** antecedente fundacional para clasificación supervisada de polaridad en reseñas. Establece la línea histórica de clasificación, pero no integra sentimientos en recomendación.
- **R02 — Zheng, Noroozi y Yu (2017):** DeepCoNN es antecedente fundacional de usar reseñas textuales para representar usuario e ítem en predicción recomendadora. No se describe como Transformer ni como clasificador de polaridad.
- **R08 — Zhang et al. (2023):** survey de análisis sentimental por aspecto, que permite distinguir sentimiento general de opiniones asociadas a características.
- **R11 — Wu et al. (2024):** survey más directo sobre LLM y recomendación, con familias discriminativas/generativas y retos del campo.

Los dos surveys complementan funciones distintas: tareas de sentimiento por aspecto y arquitectura de recomendación. Ninguno presenta un resultado experimental único que pueda compararse con los clasificadores.

## E5. Taxonomía o mapa de literatura

La [taxonomía](evidencias/mapas/taxonomia.md) ordena la secuencia conceptual desde la reseña hasta la recomendación:

| Categoría | Trabajos | Objeto principal |
|---|---|---|
| Clasificación sentimental de reseñas | R01, R03–R05, R12 | Predecir polaridad; en algunos estudios la etiqueta se deriva del rating. |
| Texto de reseñas dentro del recomendador | R02, R06–R07, R10, R12 | Estimar rating/preferencia y combinar texto con señales de usuario e ítem. |
| Explicaciones y resúmenes de opinión | R06–R10 | Comunicar motivos o sintetizar evidencia textual. |
| Síntesis del campo | R08, R11 | Organizar tareas, arquitecturas y desafíos. |

Las categorías se pueden cruzar, pero sus salidas y métricas no son intercambiables. El mapa describe el corpus seleccionado, no una clasificación exhaustiva del campo entero.

## E6. Análisis crítico por categorías

### 1. Clasificación del sentimiento en reseñas

R01 introduce una comparación supervisada clásica. R03 explora ensambles de RoBERTa y recurrentes sobre varios datasets; R04 compara SVM y BERT en reseñas Yelp etiquetadas mediante extremos del rating; R05 estudia reseñas de Steam con BERT y variantes recurrentes; R12 evalúa ensambles de LLM en sentimiento vinculado a compras. Estos trabajos muestran que hay más de una estrategia y que los resultados cambian con dominio, etiqueta, configuración y protocolo.

Las métricas F1 y accuracy de distintos conjuntos no ordenan modelos de manera válida. Si los ratings se convierten a polaridad, la etiqueta es un proxy de la valoración y puede ocultar ironía, opiniones mixtas o diferencias entre aspectos. El estudio de Steam da proximidad a juegos, pero no compara directamente SVM ni prueba que sus etiquetas eleven la utilidad de una recomendación. R12 añade costo, aunque evalúa modelos propietarios y los resultados se ligan al precio y versiones disponibles al momento del experimento.

### 2. Incorporación de reseñas en recomendaciones

DeepCoNN modela reseñas de usuario e ítem y predice ratings. PEPLER adapta modelos preentrenados con prompts para recomendación explicable, y PRAG recupera reseñas para producir justificaciones y estimar rating. XRec combina señales colaborativas y capacidad lingüística para explicar perfiles. R12 acerca sentimiento y recomendación mediante reseñas y etiquetas derivadas de estrellas.

Los artículos orientados a rating informan RMSE/MSE; los de clasificación informan accuracy/F1. Una disminución del error de rating no indica necesariamente mejor clasificación sentimental, y al revés. Para sostener que el análisis de sentimientos contribuye al sistema, el estudio debe evaluar también el resultado recomendador con comparadores pertinentes y describir la señal textual utilizada.

### 3. Explicación y síntesis de opiniones

PEPLER, PRAG y XRec generan explicaciones en contexto recomendador. HIRO selecciona grupos de reseñas y produce resúmenes fundamentados; no estima por sí solo qué ítem recomendar. Zhang et al. sitúan la extracción de aspectos y polaridad como una tarea más fina. Las explicaciones requieren medir fidelidad a reseñas, cobertura y utilidad legible; fluidez lingüística por sí sola no confirma que la explicación sea verdadera.

### 4. Síntesis de surveys

Zhang et al. organiza elementos de sentimiento por aspecto, mientras Wu et al. clasifica paradigmas de LLM para recomendación. Sus ámbitos complementarios ayudan a explicar por qué el corpus es heterogéneo. La síntesis de esta revisión, por lo tanto, conserva la tarea exacta de cada resultado y no calcula una puntuación promedio entre estudios.

## E7. Brecha de investigación sustentada

**Brecha del estado del arte:** los estudios se distribuyen entre (a) clasificar el sentimiento de reseñas, (b) incorporar texto para estimar ratings/recomendaciones y (c) explicar o resumir opiniones. La relación empírica entre esos eslabones aún requiere una síntesis comparativa y trazable que identifique cuándo la señal sentimental aporta al resultado downstream y cómo se ponderan calidad, fidelidad, dominio, costo y eficiencia.

La brecha se acota con evidencia concreta: R01 y R03–R05 miden clasificación; R02 y R06–R07 evalúan recomendación y explicaciones; R09 resume opiniones; R10 usa señales colaborativas para explicar; R12 examina ensambles de sentimiento, métricas recomendadoras/costo y deriva etiqueta desde rating. R12 aproxima los objetivos, por lo que el vacío no es “ausencia de estudios”: falta organizar las diferencias de supervisión y tarea, identificar qué mejoras son comparables y precisar los límites que impiden generalizar. Es una inferencia limitada al corpus de 12 trabajos y a la estrategia documentada.

**Diferenciación del proyecto:** auditar y sintetizar la relación entre sentimiento y recomendación en una revisión sistemática, distinguiendo polaridad, predicción recomendadora, explicación y resumen. No se propone una arquitectura ni se presupone que Transformers o LLM superen a métodos clásicos.

## E8. Borrador de introducción y estado del arte

### Introducción

Las reseñas digitales reúnen valoraciones sobre productos y servicios en forma de texto libre y, con frecuencia, ratings numéricos. Los sistemas de recomendación pueden utilizar la interacción usuario–ítem y la información expresada en reseñas para predecir preferencias, ordenar opciones o presentar explicaciones. Los modelos de lenguaje aportan representaciones contextuales y capacidad para generar explicaciones, mientras que el análisis de sentimientos transforma expresiones valorativas en etiquetas o señales que pueden integrarse en esos sistemas.

Estas actividades están relacionadas, pero responden a preguntas distintas. Un clasificador puede predecir polaridad con buen F1 y, aun así, no mejorar el orden de recomendaciones. Un sistema puede obtener menor RMSE sin identificar correctamente los aspectos que sustentan la opinión. Una explicación puede ser fluida y no estar apoyada por las reseñas. Por ello, la literatura debe compararse según la tarea, las etiquetas, el conjunto de datos y la métrica que realmente se evalúan.

Esta revisión analiza estudios sobre análisis de sentimiento y modelos de lenguaje aplicados a reseñas en el contexto de recomendación. Organiza la evidencia en clasificación, integración recomendadora, explicabilidad y síntesis de opiniones. La revisión busca determinar qué aportes pueden transferirse, cómo se ha demostrado su utilidad y qué limitaciones impiden comparar o reproducir resultados.

### Modelos para clasificar sentimientos en reseñas

La línea de clasificación va desde la comparación supervisada de Pang et al. hasta ensambles neuronales y Transformers. Los estudios contemporáneos abarcan Yelp, Steam y reseñas asociadas a ratings. Aunque sus puntuaciones de F1 o accuracy ilustran el desempeño en cada caso, difieren en idioma, balance, fuente de etiquetas, configuración y partición. En particular, la derivación de positivo/negativo a partir de ratings no equivale a la anotación directa de cada expresión. Los resultados sirven como evidencia de clasificación contextualizada; por sí solos no prueban impacto en recomendación.

La reseña de videojuegos es especialmente pertinente al enfoque original del título. El estudio de Steam contrasta BERT con variantes recurrentes en juegos populares, pero no evalúa cómo las predicciones modificarían decisiones de recomendación. A su vez, estudios de datasets generales ofrecen conjuntos comparativos más amplios, aunque la transferencia a jerga, ironía y comunidades de videojuegos no debe suponerse.

### Integración del texto en recomendadores

DeepCoNN establece una vía temprana: aprender representaciones de usuarios y productos a partir de las reseñas y utilizarlas en predicción de rating. Los modelos posteriores como PEPLER y PRAG integran modelos de lenguaje y estructuras personalizadas para estimar ratings y producir explicaciones. XRec incorpora una señal colaborativa a LLM para describir perfiles y explicar interacciones. Estos estudios se evalúan por tareas recomendadoras y de generación; su resultado no puede resumirse como si fuera precisión de polaridad.

El estudio reciente de Roumeliotis et al. conecta más explícitamente sentimiento y recomendación al comparar LLM, agregadores y ensambles sobre reseñas con rating. Aporta un análisis de exactitud y costos. Sin embargo, el rating de estrellas funciona como etiqueta indirecta y los servicios cerrados vuelven sensibles al tiempo la identidad del modelo y su costo. Esta evidencia ilustra la necesidad de registrar la procedencia de etiquetas, el modelo exacto y la fecha de evaluación.

### Explicaciones y resúmenes fundamentados en reseñas

En recomendación explicable, PEPLER, PRAG y XRec buscan comunicar por qué una opción corresponde a un perfil. HIRO aborda una tarea cercana: condensar opiniones de muchas reseñas mediante selección jerárquica de evidencia y generación. El survey de Zhang et al. aporta granularidad por aspecto. En conjunto, estos trabajos muestran que personalizar una recomendación y resumir opiniones no son sinónimos. La evaluación de una explicación debe considerar que sus afirmaciones sean rastreables a reseñas, además de legibles y específicas.

### Síntesis crítica

Wu et al. organiza el uso de LLM para recomendación en paradigmas distintos y ayuda a situar estos estudios dentro de un área amplia. El survey de ABSA complementa esa taxonomía al enfocarse en elementos de opinión. La matriz de esta revisión muestra que los resultados provienen de tareas, supervisiones y objetivos heterogéneos; no corresponde comparar métricas agregadas sin armonizar datos y protocolo.

La contribución esperada de la revisión es clarificar la cadena entre reseña, señal sentimental y recomendación. Su brecha consiste en la integración insuficientemente sintetizada de desempeño sentimental, resultado downstream, fidelidad de explicación y costo. El estudio de 2026 ya aborda parte de esa intersección; por ello, la agenda debe identificar qué componentes quedan separados y qué evidencia es todavía incomparable, en vez de afirmar que no hay investigaciones relacionadas.

## E9. Referencias del corpus

**R01.** Pang, B., Lee, L., & Vaithyanathan, S. (2002). Thumbs up? Sentiment Classification using Machine Learning Techniques. *Proceedings of EMNLP*, 79–86. [DOI: 10.3115/1118693.1118704](https://doi.org/10.3115/1118693.1118704).

**R02.** Zheng, L., Noroozi, V., & Yu, P. S. (2017). Joint Deep Modeling of Users and Items Using Reviews for Recommendation. *Proceedings of WSDM*, 425–434. [DOI: 10.1145/3018661.3018665](https://doi.org/10.1145/3018661.3018665).

**R03.** Tan, K. L., Lee, C. P., Lim, K. M., & Anbananthen, K. S. M. (2022). Sentiment Analysis With Ensemble Hybrid Deep Learning Model. *IEEE Access, 10*, 103694–103704. [DOI: 10.1109/ACCESS.2022.3210182](https://doi.org/10.1109/ACCESS.2022.3210182).

**R04.** Areshey, A., & Mathkour, H. (2023). Transfer Learning for Sentiment Classification Using Bidirectional Encoder Representations from Transformers (BERT) Model. *Sensors, 23*(11), 5232. [DOI: 10.3390/s23115232](https://doi.org/10.3390/s23115232).

**R05.** Fadhlurrahman, J. A. M., Herawati, N. A., Aulya, H. R. W., Puspasari, I., & Utama, N. P. (2023). Sentiment Analysis of Game Reviews on STEAM using BERT, BiLSTM, and CRF. *2023 International Conference on Electrical Engineering and Informatics (ICEEI)*, 1–6. [DOI: 10.1109/ICEEI59426.2023.10346219](https://doi.org/10.1109/ICEEI59426.2023.10346219).

**R06.** Li, L., Zhang, Y., & Chen, L. (2023). Personalized Prompt Learning for Explainable Recommendation. *ACM Transactions on Information Systems, 41*(4), Article 111. [DOI: 10.1145/3580488](https://doi.org/10.1145/3580488).

**R07.** Xie, Z., Singh, S., McAuley, J., & Majumder, B. P. (2023). Factual and Informative Review Generation for Explainable Recommendation. *Proceedings of AAAI, 37*(11), 13816–13824. [DOI: 10.1609/aaai.v37i11.26618](https://doi.org/10.1609/aaai.v37i11.26618).

**R08.** Zhang, W., Li, X., Deng, Y., Bing, L., & Lam, W. (2023). A Survey on Aspect-Based Sentiment Analysis: Tasks, Methods, and Challenges. *IEEE Transactions on Knowledge and Data Engineering, 35*(11), 11019–11038. [DOI: 10.1109/TKDE.2022.3230975](https://doi.org/10.1109/TKDE.2022.3230975).

**R09.** Hosking, T., Tang, H., & Lapata, M. (2024). Hierarchical Indexing for Retrieval-Augmented Opinion Summarization. *Transactions of the Association for Computational Linguistics, 12*, 1533–1555. [DOI: 10.1162/tacl_a_00703](https://doi.org/10.1162/tacl_a_00703).

**R10.** Ma, Q., Ren, X., & Huang, C. (2024). XRec: Large Language Models for Explainable Recommendation. *Findings of the Association for Computational Linguistics: EMNLP 2024*, 391–402. [DOI: 10.18653/v1/2024.findings-emnlp.22](https://doi.org/10.18653/v1/2024.findings-emnlp.22).

**R11.** Wu, L., Zheng, Z., Qiu, Z., Wang, H., Gu, H., Shen, T., Qin, C., Zhu, C., Zhu, H., Liu, Q., Xiong, H., & Chen, E. (2024). A Survey on Large Language Models for Recommendation. *World Wide Web, 27*, Article 60. [DOI: 10.1007/s11280-024-01291-2](https://doi.org/10.1007/s11280-024-01291-2).

**R12.** Roumeliotis, K. I., Margaris, D., Spiliotopoulos, D., & Vassilakis, C. (2026). A Large-Scale Empirical Study of LLM Orchestration and Ensemble Strategies for Sentiment Analysis in Recommender Systems. *Future Internet, 18*(2), 112. [DOI: 10.3390/fi18020112](https://doi.org/10.3390/fi18020112).

## Control de versiones y uso en el PPI

La matriz, taxonomía y criterios respaldan E8 y E9. El título, problema, objetivos y categorías deben conservar una misma delimitación al incorporarse al PPI. El corpus puede ampliarse si un cribado formal posterior identifica publicaciones elegibles adicionales.
