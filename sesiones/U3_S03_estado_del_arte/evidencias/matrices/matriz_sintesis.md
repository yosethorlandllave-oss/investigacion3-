# E3. Matriz de síntesis de publicaciones

**Corte:** 31/10/2026. **Corpus:** 11 artículos, 9 recientes (81,8 %). P01 y P02 son excepciones seminales; P07 es el survey. Las referencias completas están en [E9 del desarrollo](../../desarrollo.md).

**Convenciones:** NR = no reportado o no verificado en las secciones consultadas, según se precisa; NA = no aplicable. Los resultados pertenecen a los autores. Las implicaciones y cautelas de la última columna son evaluación crítica de esta revisión. Ningún modelo se entrenó ni se replicó en esta sesión. Los porcentajes se conservan en su escala original y no constituyen un ranking entre papers.

## Métodos, datos, evaluación y contribución

| ID / autores / año | Problema y método | Dataset y contexto | Métrica y resultado extraído | Limitación / implicación para el proyecto | Fuente primaria y localizador |
|---|---|---|---|---|---|
| P01. Pang, Lee y Vaithyanathan (2002) | Clasificación supervisada: Naive Bayes, máxima entropía y SVM. | 1 400 reseñas de cine IMDb en inglés; 700 por polaridad. | Validación cruzada de tres particiones: SVM con presencia de unigramas, accuracy 82,9 %. | Presencia binaria no equivale a TF-IDF. Dos clases y otro dominio; antecedente para la línea base, no meta de rendimiento local. | [ACL](https://aclanthology.org/W02-1011/), secciones 3–5 y figura 3. |
| P02. Devlin et al. (2019) | BERT: preentrenamiento bidireccional y fine-tuning. | Benchmarks de comprensión lingüística, entre ellos GLUE. | GLUE: puntuación agregada 80,5; no es macro-F1 de sentimientos municipales. | Fundamenta la familia Transformer, sin demostrar transferencia a Juliaca. | [ACL](https://aclanthology.org/N19-1423/), resumen y sección 4. |
| P03. Pérez et al. (2022) | RoBERTuito, modelo adaptado a texto social en español. | Preentrenamiento con 500 millones de tuits; sentimientos TASS 2020, tres clases. | Macro-F1 70,7 para la variante uncased; media de diez ejecuciones. | Ventaja en su benchmark, no garantía en servicios locales; conviene evaluar sensibilidad al dominio. | [ACL](https://aclanthology.org/2022.lrec-1.785/), secciones 4–5, tablas 1–2. |
| P04. Barbieri et al. (2022) | XLM-T: adaptación multilingüe a Twitter. | 198 millones de tuits; UMSAB en ocho idiomas, incluido español; evaluación adicional TweetEval. | TweetEval, sentimientos: macro-recall 72,3 frente a SVM 62,9. UMSAB se evalúa con macro-F1. | No confundir las métricas de los dos benchmarks ni atribuir el resultado de TweetEval al español. | [ACL](https://aclanthology.org/2022.lrec-1.27/), sección 3 y tabla 1. |
| P05. Gutiérrez-Fandiño et al. (2022) | MarIA: modelos RoBERTa/GPT-2 para español. | 570 GB de texto web depurado; tareas como MLDoc, NER y XNLI. | Rendimiento variable por tarea; BETO supera ligeramente a RoBERTa-large en MLDoc. Sin benchmark de sentimientos en el artículo. | El tamaño del preentrenamiento no asegura superioridad en la tarea propuesta. | [SEPLN](https://journal.sepln.org/sepln/ojs/ojs/index.php/pln/article/view/6405), sección de evaluación y tabla 4; PDF institucional UPC. |
| P06. Xue y Liu (2023) | Léxico de sentimientos y LDA para evolución de opinión sobre separación de residuos. | 46 056 publicaciones válidas de Weibo, Shanghái, julio 2019–diciembre 2020. | Distribuciones temporales de polaridad y temas; no se extrajo macro-F1 de un test anotado. | Evidencia temática, no comparación de clasificadores. La polaridad depende del contexto y del léxico. | [MDPI](https://doi.org/10.3390/ijerph20021471), métodos y resultados; [PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC9859488/). |
| P07. Mao, Liu y Zhang (2024) | RSL de métodos, aplicaciones y retos de sentimientos. | 132 estudios finales según sección 2.3. | Síntesis de familias léxicas, aprendizaje automático, profundo e híbrido; NA: no presenta clasificador propio. | Orienta categorías; no usar su diversidad de resultados como comparación experimental homogénea. | [Artículo](https://link.springer.com/article/10.1016/j.jksuci.2024.102048), sección 2 y taxonomía de métodos. |
| P08. Sui y Zhang (2024) | OCC-LSTM, redes de coocurrencia y análisis temático de residuos. | 367 856 publicaciones de Weibo; anotación de 2 000 ejemplos positivos y 2 000 negativos. | Accuracy 98,54 % explícitamente del conjunto de entrenamiento. Resultado de prueba: no verificado en la extracción. | No usar ese porcentaje como generalización ni compararlo con macro-F1 de prueba. Plataforma y selección limitan transferencia. | [PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC11471487/), sección 4.3 y limitaciones. |
| P09. Huang et al. (2025) | BERT chino con emojis; temas y regresión de difusión de mensajes. | 443 358 registros depurados de Weibo; 10 000 anotados; partición 6:2:2. | F1 85,70 %, precisión 85,85 %, recall 85,83 %. Promedio de F1 no precisado en el pasaje consultado. | Clasificación y difusión son resultados diferentes. No denominar macro-F1 a una agregación no comprobada. | [Editor](https://doi.org/10.1057/s41599-025-06041-x), apartado Sentiment y apéndice A referido por los autores. |
| P10. Calizaya-Milla, Santos y Huanca Torres (2026) | Comparación de Transformers monolingües en jerga peruana. | SMPS: 11 276 comentarios de Facebook; tres clases; ocho anotadores. | Macro-F1: RoBERTuito 0,750; BETO 0,661; BERTuit 0,700; RoBERTa-BNE 0,696. | Sin SVM en esa comparación; no calcularon índice de acuerdo entre anotadores. La evidencia peruana no valida automáticamente el dominio municipal. | [Editor](https://doi.org/10.1080/08839514.2026.2641381), métodos, tabla 6 y limitaciones; texto editorial indexado. |
| P11. Chen et al. (2025) | SnowNLP y LDA para comentarios sobre políticas de separación de residuos. | Weibo, 46 ciudades chinas; 56 841 comentarios iniciales, 35 021 procesados; 2019–2024. | Distribuciones de polaridad y temas; no se identificó evaluación de accuracy contra etiquetas humanas. | Se denomina análisis no supervisado, pero se describe un clasificador Naive Bayes preentrenado: requiere aclarar validación local. | [Frontiers](https://doi.org/10.3389/fenvs.2025.1546136), secciones 4.1–4.3 y 7. |

## Evaluación individual de calidad y reproducibilidad

«Declarado» significa que el artículo ofrece el recurso o enlace; no significa que su ejecución o acceso actual hayan sido auditados. NR no equivale a inexistencia. El ranking de cada venue se documenta por separado en [criterios_calidad.md](../busqueda/criterios_calidad.md).

| ID | Pertinencia | Datos / código / modelo | Juicio de uso en la revisión |
|---|---|---|---|
| P01 | Fundamento metodológico | SVMlight descrito; disponibilidad actual del dataset no auditada. | Conservar como seminal; extrapolación contextual limitada. |
| P02 | Fundamento metodológico | Implementación BERT declarada por los autores; no ejecutada aquí. | Conservar como seminal, sin convertir un benchmark general en evidencia local. |
| P03 | Alta para español social | Modelos públicos declarados; artefactos no ejecutados. | Candidato pertinente para elegir el Transformer antes de evaluar el test. |
| P04 | Alta para transferencia lingüística | [Repositorio declarado](https://github.com/cardiffnlp/xlm-t). | Aporta comparación multilingüe, con separación estricta de benchmarks. |
| P05 | Alta como alternativa en español | [Repositorio declarado](https://github.com/PlanTL-GOB-ES/lm-spanish). | Evidencia de recursos, no prueba de rendimiento sentimental. |
| P06 | Alta para dominio; baja proximidad lingüística | Datos bajo solicitud según declaración editorial. | Conservar para aplicación social; validación clasificatoria insuficiente para comparaciones numéricas. |
| P07 | Alta para organización del campo | No aplica entrenamiento propio; selección documental descrita. | Conservar como survey; distinguir corpus inicial y selección final. |
| P08 | Alta para dominio | Acceso a artefactos no verificado. | Conservar con cautela importante sobre la métrica de entrenamiento. |
| P09 | Alta para dominio | Disponibilidad ejecutable de datos/código no verificada. | Conservar; aclarar promedio de F1 y protocolo antes de una comparación cuantitativa externa. |
| P10 | Muy alta para variedad peruana | Dataset declarado en [Figshare](https://doi.org/10.6084/m9.figshare.26198315); no descargado ni auditado. | Conservar; acuerdo de anotación pendiente y acceso editorial parcial registrado. |
| P11 | Alta para dominio | Declaración remite al artículo/material complementario y contacto con autores. | Conservar para contraste crítico; no asumir que el clasificador se validó en estos comentarios. |

## Reglas para interpretar los resultados

- Accuracy, macro-recall y macro-F1 no miden lo mismo. Tampoco una proporción de mensajes negativos mide la precisión de un clasificador.
- Un número calculado en entrenamiento no estima por sí solo rendimiento en datos nuevos.
- Aun usando macro-F1, los valores de datasets diferentes no permiten ordenar modelos de forma causal: cambian etiquetas, particiones, dificultad y procedencia.
- La proximidad al español peruano y la proximidad al dominio de residuos son ejes independientes. La contribución propuesta consiste en evaluar su intersección bajo un protocolo común.
- No se calculó metaanálisis ni una media conjunta de métricas incompatibles. No se presentan resultados del futuro experimento de Juliaca.
