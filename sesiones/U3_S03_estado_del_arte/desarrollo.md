# Desarrollo — U3 Sesión 3: Estado del arte

**Título de la investigación:** Comparación de modelos de procesamiento del lenguaje natural para clasificar sentimientos en comentarios ciudadanos sobre la limpieza pública y el recojo de residuos sólidos en Juliaca, Puno

**Autor:** Yoseth Orlando Llave Huachaca

**Curso:** Investigación III — Universidad Peruana Unión

**Fecha de corte:** 31 de octubre de 2026

**Delimitación metodológica:** clasificación de sentimientos en comentarios sobre limpieza pública y recojo de residuos sólidos en Juliaca mediante TF-IDF + SVM y un Transformer en español.

**Estado del producto:** borrador académico con revisión bibliográfica estructurada de 11 publicaciones. La búsqueda externa amplía los dos documentos iniciales conforme a la actividad de esta sesión. No se declara una RSL exhaustiva concluida ni se presentan resultados experimentales propios. La cobertura y los accesos pendientes se documentan para su posterior ampliación.

## E1. Estrategia y registro de búsqueda

### Pregunta que orienta la revisión

¿Qué diferencias de desempeño, medidas principalmente mediante macro-F1, presentan un clasificador TF-IDF + SVM y un modelo Transformer en español al clasificar sentimientos en comentarios ciudadanos sobre limpieza pública y recojo de residuos sólidos en Juliaca?

Se conserva la pregunta de la [sesión 2](../U3_S02_objetivos_hipotesis_variables/desarrollo.md). Para fundamentarla se examinaron métodos, adaptación lingüística, aplicaciones a residuos y condiciones de evaluación. El propósito documental es establecer qué puede transferirse al proyecto y qué exige comprobación local.

La búsqueda combinó «sentiment analysis», «opinion mining», «SVM», «TF-IDF», «BERT», «Transformer», «Spanish», «Peruvian slang», «waste collection», «waste sorting», «Juliaca» y «Puno». Se consultaron fuentes primarias editoriales y repositorios académicos mediante búsquedas generales y por dominio. Se realizó rastreo hacia atrás desde P10 y P03, y hacia adelante desde P03, verificando las referencias de los trabajos recuperados.

El [registro de búsqueda](evidencias/busqueda/estrategia_registro.md) contiene cadenas, vías de acceso, candidatos y límites. Las [consultas literales](evidencias/busqueda/consultas_ejecutadas.json) permiten repetir las búsquedas. DBLP y Semantic Scholar no proporcionaron exportaciones por restricciones de acceso; no se atribuyen búsquedas nativas a bases no utilizadas ni se inventan recuentos de resultados.

## E2. Criterios de selección y evaluación de calidad

Se priorizaron artículos de revista, full papers y surveys publicados entre 2022 y 2026, pertinentes al método, idioma o dominio. Se admitieron dos antecedentes seminales anteriores. La síntesis incluye **11 publicaciones: 9 recientes (81,8 %) y 2 seminales**. Los rankings y recursos de consulta no entran en ese denominador.

Se verificaron venues mediante CORE, SJR u otros indicadores identificados explícitamente. Se evaluaron además claridad del corpus, métricas, referencia de anotación, transferibilidad y recursos de reproducción. Un venue reconocido no elimina limitaciones metodológicas. Los índices, categorías y años, así como las diferencias históricas de clasificación, constan en [criterios y calidad](evidencias/busqueda/criterios_calidad.md).

Las métricas de entrenamiento se distinguen de las de prueba; «no verificado» no se interpreta como «inexistente». Se mantuvieron fuera del corpus los candidatos sin extracción suficiente y se registraron sus motivos. La selección fue una revisión documental de esta sesión, sin doble cribado independiente.

## E3. Matriz de síntesis

La [matriz completa de once artículos](evidencias/matrices/matriz_sintesis.md) contiene autores, año, problema, método, dataset, métricas, resultados, limitaciones, disponibilidad de recursos y localizadores primarios. Cada trabajo tiene un identificador P01–P11 que se conserva en la bibliografía y la taxonomía.

La matriz separa evidencia de rendimiento y evidencia de aplicación social. No se obtiene un promedio de puntuaciones entre estudios porque los corpus, etiquetas y métricas no son homogéneos.

## E4. Papers seminales y survey

**P01 — Pang, Lee y Vaithyanathan (2002):** fundamenta la comparación supervisada de sentimientos y la inclusión de SVM como referencia. Su reconocimiento Test-of-Time aparece en la ficha oficial de ACL. El estudio utiliza representaciones que no deben identificarse automáticamente con TF-IDF. [Fuente primaria](https://aclanthology.org/W02-1011/).

**P02 — Devlin et al. (2019):** fundamenta el preentrenamiento bidireccional y el ajuste posterior que sustentan los modelos contextuales. Su relevancia para la línea revisada se observa también en las referencias de trabajos posteriores. [Fuente primaria](https://aclanthology.org/N19-1423/).

**P07 — Mao, Liu y Zhang (2024):** survey seleccionado para organizar familias metodológicas y desafíos. Su función es sintetizar el campo, no aportar un clasificador propio a la comparación. [Fuente primaria](https://doi.org/10.1016/j.jksuci.2024.102048).

La condición seminal se justifica por la contribución fundacional y continuidad metodológica, no únicamente por antigüedad o cantidad de citas.

## E5. Taxonomía o mapa de la literatura

La [taxonomía desarrollada](evidencias/mapas/taxonomia.md) organiza cuatro categorías:

| Categoría | Trabajos | Función en el argumento |
|---|---|---|
| Fundamentos de clasificación | P01, P02 | Explicar las familias comparadas. |
| Adaptación al idioma, plataforma y variedad | P03, P04, P05, P10 | Fundamentar la selección del Transformer y el problema de transferencia. |
| Opinión digital sobre residuos | P06, P08, P09, P11 | Establecer pertinencia temática y límites de interpretación. |
| Síntesis metodológica | P07 | Relacionar enfoques y retos. |

El mapa incluye evolución temporal, proximidad al proyecto y relaciones de citación verificadas. Es una elaboración conceptual propia, no un grafo de cocitación automatizado.

## E6. Categorías temáticas y análisis crítico

El desarrollo argumentado por categorías se presenta en E8. Su lectura transversal conduce a los siguientes criterios para el proyecto:

| Eje crítico | Evidencia del corpus | Consecuencia metodológica propuesta |
|---|---|---|
| Comparabilidad | P01–P04 y P08–P10 emplean distintos corpus, métricas o niveles de evaluación. | Usar etiquetas y prueba comunes; macro-F1 principal y resultados por clase. |
| Transferencia | La proximidad lingüística de P03–P05/P10 y la temática de P06/P08/P09/P11 no coinciden plenamente. | Verificar adecuación en comentarios del servicio de limpieza local. |
| Anotación | P10 explicita una limitación del acuerdo; las aplicaciones temáticas no siempre ofrecen validación clasificatoria suficiente. | Pilotar una guía de etiquetado y documentar consistencia antes de evaluar. |
| Interpretación | Los estudios de residuos analizan polaridad, temas o difusión, que son objetos diferentes. | Separar error del modelo, distribución de opiniones y calidad real del servicio. |
| Reproducción | Hay recursos declarados, pero no se ejecutaron artefactos en esta revisión. | Registrar versiones, particiones y configuraciones del futuro experimento. |

Estas decisiones son propuestas del equipo derivadas del contraste; no se atribuyen como recomendaciones textuales a todos los autores. La revisión no demuestra cuál es el mejor modelo disponible globalmente en 2026.

## E7. Brecha de investigación sustentada

**Brecha:** en el corpus seleccionado no se identificó una evaluación directamente equivalente que compare TF-IDF + SVM con un Transformer en español sobre el mismo conjunto de comentarios de limpieza pública y recojo de residuos de Juliaca, con referencia de anotación documentada y macro-F1 como resultado principal.

La brecha combina tres dimensiones. Los fundamentos justifican comparar familias distintas (P01–P02); los modelos de español y la evidencia peruana muestran antecedentes lingüísticos pertinentes (P03–P05, P10); las aplicaciones a residuos aportan evidencia temática en otros contextos (P06, P08, P09, P11). Ninguna de esas dimensiones, por sí sola, responde a la pregunta local. Esta conclusión es una inferencia acotada a la matriz, no una afirmación de inexistencia universal.

**Diferenciación de la propuesta:** producir evidencia comparativa contextual con un protocolo compartido, no proponer una arquitectura inédita. Se prevé caracterizar el corpus y su anotación (OE1), evaluar ambos procedimientos (OE2), estimar la diferencia de macro-F1 y su incertidumbre (OE3) y examinar errores por clase (OE4). Se conserva la hipótesis bilateral de la sesión 2: la literatura no autoriza a dar por ganadora una familia.

Quedan por confirmar la fuente, el periodo, el volumen viable del corpus y el Transformer concreto. La presencia de jerga, mezcla de idiomas o ironía deberá observarse y registrarse, no suponerse. Las conclusiones se limitarán a los comentarios analizados, sin equipararlos a una encuesta representativa de toda Juliaca.

## E8. Borrador de introducción y estado del arte para el PPI

### Introducción

Los comentarios digitales sobre servicios municipales constituyen una posible fuente de información acerca de las experiencias y valoraciones expresadas por sus usuarios. Su aprovechamiento exige distinguir la tarea de identificar sentimientos de la posterior interpretación de esas opiniones. En el ámbito de los residuos, la literatura reúne análisis de polaridad, organización temática y difusión de mensajes, con objetivos que no siempre incluyen comparar la capacidad predictiva de los clasificadores. Por ello, la existencia de aplicaciones en ese dominio no basta para seleccionar un procedimiento de clasificación adecuado para otro contexto lingüístico y territorial. [P06](https://doi.org/10.3390/ijerph20021471), [P09](https://doi.org/10.1057/s41599-025-06041-x).

En Juliaca, el proyecto propone comparar TF-IDF + SVM y un Transformer en español sobre comentarios relacionados con limpieza pública y recojo de residuos. Esta delimitación plantea un problema computacional verificable: determinar cómo difieren sus predicciones frente a una referencia común. No presupone que el volumen de comentarios represente la opinión de toda la ciudadanía ni que el sentimiento permita medir directamente la calidad objetiva del servicio.

La revisión se organiza alrededor de fundamentos de clasificación, adaptación lingüística y aplicaciones a residuos. Su finalidad es identificar aportes transferibles y limitaciones que orienten el protocolo experimental. La contribución prevista será una comparación contextual documentada, cuya viabilidad dependerá de la disponibilidad y calidad del corpus local.

### 1. Fundamentos: representaciones de palabras y modelos contextuales

El antecedente de Pang et al. sitúa la clasificación de sentimientos dentro de la comparación de procedimientos supervisados, mientras que BERT representa el uso de preentrenamiento contextual y ajuste a tareas. Ambos justifican familias de candidatos, pero no permiten deducir de antemano su desempeño en el mismo problema local. [P01](https://aclanthology.org/W02-1011/), [P02](https://aclanthology.org/N19-1423/).

La comparación propuesta deberá conservar una línea base definida con precisión. No bastará denominarla «SVM»: habrá que especificar su representación TF-IDF y sus parámetros, del mismo modo que se documentará el Transformer. La síntesis de Mao et al. ayuda a situar estas decisiones entre familias metodológicas diversas; esa diversidad exige evaluar la pertinencia de cada enfoque y evita presentar una secuencia tecnológica como una garantía de superioridad. [P07](https://doi.org/10.1016/j.jksuci.2024.102048).

### 2. Adaptación al español y al texto social

RoBERTuito y XLM-T orientan la revisión hacia modelos adaptados a redes sociales, mientras que MarIA aporta recursos construidos desde texto web en español. La distinción entre idioma y plataforma es relevante: compartir lengua no significa compartir distribución textual. Además, MarIA se evalúa en tareas que no incluyen directamente el sentimiento de este proyecto. [P03](https://aclanthology.org/2022.lrec-1.785/), [P04](https://aclanthology.org/2022.lrec-1.27/), [P05](https://doi.org/10.26342/2022-68-3).

El estudio de Calizaya-Milla et al. aporta un antecedente más cercano a la variedad peruana, pero mantiene abierta la comparación con una línea base clásica y la validación específica del servicio municipal. Su limitación de acuerdo entre anotadores también recuerda que evaluar modelos requiere examinar la calidad de la referencia humana. [P10](https://doi.org/10.1080/08839514.2026.2641381).

La selección del Transformer se realizará antes de observar el conjunto de prueba. Su elección debe responder a pertinencia y viabilidad; probar múltiples candidatos y conservar el que mejor funcione en test invalidaría la independencia de esa evaluación. La transferencia lingüística se tratará como una cuestión empírica y no como una propiedad asegurada por el nombre del modelo.

### 3. Sentimientos y opinión pública en gestión de residuos

En esta línea coexisten aproximaciones léxicas, redes recurrentes, Transformers y herramientas preentrenadas. Xue y Liu y Chen et al. combinan polaridad y temas; Sui y Zhang incorporan OCC-LSTM; Huang et al. vinculan clasificación con difusión de información. La variedad revela finalidades analíticas distintas, además de diferencias técnicas. [P06](https://doi.org/10.3390/ijerph20021471), [P11](https://doi.org/10.3389/fenvs.2025.1546136), [P08](https://doi.org/10.1016/j.heliyon.2024.e38510), [P09](https://doi.org/10.1057/s41599-025-06041-x).

El contraste exige atender al origen de cada indicador. Una distribución de mensajes positivos o negativos describe las etiquetas producidas; no verifica su corrección. Asimismo, la accuracy de entrenamiento destacada en P08 no constituye evidencia suficiente de generalización. Estas diferencias impiden construir una tabla de ganadores sumando o comparando directamente porcentajes de los artículos.

Para el proyecto, la utilidad temática de estas aplicaciones es distinta de su transferibilidad experimental. Las políticas de separación de residuos y los comentarios sobre recojo municipal pueden compartir vocabulario, pero no necesariamente el objeto de valoración. Será necesario definir en la guía si se etiqueta el servicio, una autoridad, una conducta ciudadana u otro objetivo expresado en el comentario; de lo contrario, una misma frase podría recibir etiquetas incompatibles.

### 4. Síntesis crítica y ubicación de la propuesta

La literatura seleccionada aproxima por separado los métodos, la variedad lingüística y el dominio. La pregunta del proyecto se sitúa en su intersección y requiere una comparación común que la revisión no encontró dentro del corpus analizado. El aporte esperado consiste en producir esa evidencia bajo condiciones explícitas, con análisis de errores y alcance contextual delimitado.

El protocolo deberá impedir contaminación entre entrenamiento y prueba, ajustar el vectorizador únicamente con entrenamiento y considerar la dependencia entre comentarios de una misma publicación. También deberá fijar el procedimiento de comparación y de incertidumbre antes de examinar los resultados finales. Estas son decisiones metodológicas propuestas para responder a las limitaciones observadas, no resultados de esta revisión.

La revisión permite justificar el estudio sin anticipar su conclusión. Una ventaja del Transformer, una diferencia pequeña o un resultado favorable a SVM serían hallazgos interpretables si proceden de un diseño consistente. La pertinencia del proyecto depende de esa calidad comparativa y de su información contextual, no de confirmar una superioridad previamente asumida.

## E9. Referencias científicas utilizadas

Los códigos sirven como enlaces entre las evidencias; el orden es metodológico-temático. Se utiliza el año de publicación formal.

**P01.** Pang, B., Lee, L., & Vaithyanathan, S. (2002). Thumbs up? Sentiment Classification using Machine Learning Techniques. *Proceedings of EMNLP*, 79–86. [DOI: 10.3115/1118693.1118704](https://doi.org/10.3115/1118693.1118704).

**P02.** Devlin, J., Chang, M.-W., Lee, K., & Toutanova, K. (2019). BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding. *Proceedings of NAACL-HLT, Volume 1*, 4171–4186. [DOI: 10.18653/v1/N19-1423](https://doi.org/10.18653/v1/N19-1423).

**P03.** Pérez, J. M., Furman, D. A., Alonso Alemany, L., & Luque, F. M. (2022). RoBERTuito: a pre-trained language model for social media text in Spanish. *Proceedings of LREC*, 7235–7243. [ACL Anthology](https://aclanthology.org/2022.lrec-1.785/).

**P04.** Barbieri, F., Espinosa Anke, L., & Camacho-Collados, J. (2022). XLM-T: Multilingual Language Models in Twitter for Sentiment Analysis and Beyond. *Proceedings of LREC*, 258–266. [ACL Anthology](https://aclanthology.org/2022.lrec-1.27/).

**P05.** Gutiérrez-Fandiño, A., Armengol-Estapé, J., Pàmies, M., Llop-Palao, J., Silveira-Ocampo, J., Carrino, C. P., Armentano-Oller, C., Rodríguez-Penagos, C., Gonzalez-Agirre, A., & Villegas, M. (2022). MarIA: Spanish Language Models. *Procesamiento del Lenguaje Natural, 68*, 39–60. [DOI: 10.26342/2022-68-3](https://doi.org/10.26342/2022-68-3).

**P06.** Xue, Y., & Liu, H. (2023). Exploration of the Dynamic Evolution of Online Public Opinion towards Waste Classification in Shanghai. *International Journal of Environmental Research and Public Health, 20*(2), 1471. [DOI: 10.3390/ijerph20021471](https://doi.org/10.3390/ijerph20021471).

**P07.** Mao, Y., Liu, Q., & Zhang, Y. (2024). Sentiment analysis methods, applications, and challenges: A systematic literature review. *Journal of King Saud University – Computer and Information Sciences, 36*(4), 102048. [DOI: 10.1016/j.jksuci.2024.102048](https://doi.org/10.1016/j.jksuci.2024.102048).

**P08.** Sui, F., & Zhang, H. (2024). How to go green? Exploring public attention and sentiment towards waste sorting behaviors on Weibo platform: A study based on text co-occurrence networks and deep learning. *Heliyon, 10*(19), e38510. [DOI: 10.1016/j.heliyon.2024.e38510](https://doi.org/10.1016/j.heliyon.2024.e38510).

**P09.** Huang, H., Zeng, X., Ge, L., & Sun, K. (2025). Social media engagement in waste sorting: the role of sentiment in shaping public awareness. *Humanities and Social Sciences Communications, 12*, 1763. [DOI: 10.1057/s41599-025-06041-x](https://doi.org/10.1057/s41599-025-06041-x).

**P10.** Calizaya-Milla, S. E., Santos, J., & Huanca Torres, F. A. (2026). Fine-Tuning Monolingual Pre-Trained BERT Models for Sentiment Analysis in Peruvian Slang Contexts. *Applied Artificial Intelligence, 40*(1), 2641381. [DOI: 10.1080/08839514.2026.2641381](https://doi.org/10.1080/08839514.2026.2641381).

**P11.** Chen, L., Huang, L., Ma, W., Ma, S., & Li, Y. (2025). The study on the dissemination of waste sorting policies on social media and the public’s feedback attitudes: a text analysis based on comment data of policies in 46 key cities in China. *Frontiers in Environmental Science, 13*, 1546136. [DOI: 10.3389/fenvs.2025.1546136](https://doi.org/10.3389/fenvs.2025.1546136).

Las fuentes bibliométricas están en [criterios_calidad.md](evidencias/busqueda/criterios_calidad.md). Los candidatos no incluidos están en el registro de búsqueda y no se contabilizan como estudios sintetizados. Las fuentes originales sustituyen la atribución indirecta a los borradores para los trabajos aquí verificados.


