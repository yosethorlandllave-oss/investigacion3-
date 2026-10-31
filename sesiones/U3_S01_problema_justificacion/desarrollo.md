# Desarrollo — U3 Sesión 1: Identificación del problema y justificación

**Autor:** Yoseth Orlando Llave Huachaca

**Curso:** Investigación III — Universidad Peruana Unión

**Fecha:** 31 de octubre de 2026

**Estado:** avance para incorporación posterior al Perfil de Proyecto de Investigación (PPI).

**Alcance documental.** Este avance se redacta exclusivamente a partir de los dos borradores proporcionados. Las atribuciones a publicaciones científicas proceden del segundo borrador; sus textos originales no se han consultado en esta sesión. El primer borrador aporta antecedentes técnicos de análisis de sentimientos en reseñas. La matriz de trazabilidad y las copias de los documentos se encuentran en [evidencias](evidencias/README.md). Este avance no constituye una RSL concluida ni presenta resultados experimentales.

## E1. Tema de investigación

**Tema delimitado:** Comparación del desempeño de un clasificador TF-IDF + SVM y un modelo Transformer en español para clasificar sentimientos en comentarios ciudadanos sobre limpieza pública y recojo de residuos sólidos en Juliaca, Puno.

La investigación se ubica en el procesamiento del lenguaje natural y la clasificación supervisada de texto. Su unidad de análisis será el comentario textual individual relacionado con la limpieza de espacios públicos, acumulación de residuos o frecuencia del recojo, siempre que estos contenidos estén presentes en los datos disponibles.

Se propone comparar TF-IDF + SVM con un Transformer en español, cuya selección entre alternativas como BETO o RoBERTuito dependerá de su pertinencia y viabilidad computacional. El desempeño se analizará principalmente mediante macro-F1, acompañado de precisión, exhaustividad y matriz de confusión.

La fuente de comentarios, el periodo de observación, el tamaño del corpus y las categorías de sentimiento quedan pendientes de una comprobación de factibilidad. La población accesible estará constituida por los comentarios que cumplan los criterios establecidos; no se asumirá que representa a toda la ciudadanía de Juliaca.

## E2. Situación problemática

### Contexto

La gestión de residuos sólidos forma parte de los asuntos ambientales y municipales de Juliaca. El segundo borrador recoge la investigación de Cayra Uscamayta (2024), referida a contaminación ambiental y gestión de residuos en la Municipalidad Provincial de San Román. Este antecedente sitúa el tema en el contexto local, pero no demuestra por sí mismo la disponibilidad de comentarios digitales ni el desempeño de clasificadores automáticos.

Las plataformas digitales pueden contener valoraciones, quejas y preocupaciones acerca de servicios públicos. Los antecedentes de Jiang et al. (2021), Xue y Liu (2023) y Huang et al. (2025), según su descripción en el borrador, muestran aplicaciones del análisis de opiniones a conversaciones sobre segregación, reciclaje o clasificación de residuos. Esas aplicaciones respaldan la pertinencia del tema, aunque proceden de contextos distintos al de Juliaca.

### Situación problemática y problema computacional

El problema práctico consiste en la necesidad de organizar e interpretar opiniones ciudadanas relacionadas con estos servicios. Su manifestación y volumen en fuentes digitales locales todavía deben documentarse mediante un piloto de recopilación.

El problema computacional consiste en determinar qué diferencias de desempeño existen entre dos enfoques de clasificación de sentimientos aplicados al mismo corpus local. Las expresiones coloquiales, las diferencias entre dominios, la distribución de las categorías y la consistencia del etiquetado pueden afectar la evaluación. Los antecedentes disponibles no permiten anticipar el comportamiento de TF-IDF + SVM y un Transformer en estos datos.

La evidencia sobre restaurantes peruanos y lenguaje coloquial peruano justifica comparar los modelos en el corpus concreto, en lugar de trasladar directamente los resultados de otros estudios. Para que la comparación sea interpretable se necesitarán etiquetas de referencia, una partición de prueba común y control de duplicados entre subconjuntos.

## E3. Evidencia científica del problema

La siguiente evidencia se presenta conforme a las descripciones incluidas en el Documento 2. No se atribuyen resultados numéricos que no hayan sido comprobados en sus publicaciones originales.

| Fuente citada en el borrador | Evidencia bibliográfica reportada | Relación con el problema y límite de aplicación |
|---|---|---|
| Jiang et al. (2021) | Analizan participación y sentimientos en redes sociales relacionados con segregación y reciclaje de residuos domésticos. | Sustentan la pertinencia de estudiar conversaciones digitales sobre residuos; no evalúan el corpus de Juliaca. |
| Xue y Liu (2023) | Estudian la evolución de la opinión pública en línea sobre clasificación de residuos en Shanghái. | Aportan un antecedente temático; las diferencias de contexto e idioma limitan la transferencia de resultados. |
| Huang et al. (2025) | Abordan sentimiento y participación en redes sociales sobre separación de residuos; el borrador señala clasificación basada en BERT. | Vinculan modelos de lenguaje con el dominio de residuos; no demuestran superioridad sobre SVM en Juliaca. |
| Adrianzón Torres y Escobedo Cárdenas (2021) | Comparan métodos de aprendizaje automático para opiniones sobre restaurantes peruanos en Facebook. | Justifican evaluar clasificadores tradicionales en opiniones en español peruano; el dominio es diferente. |
| Calizaya-Milla et al. (2026) | Comparan modelos BERT monolingües para análisis de sentimientos en contextos de lenguaje coloquial peruano. | Respaldan considerar la adecuación lingüística y evaluar los modelos en datos pertinentes; no estudian el corpus local propuesto. |
| Cayra Uscamayta (2024) | Estudia contaminación ambiental y gestión de residuos sólidos en la Municipalidad Provincial de San Román. | Aporta contexto académico local; no constituye evidencia de clasificación de sentimientos en comentarios digitales. |

El Documento 1 describe modelos preentrenados e híbridos, conjuntos de reseñas y dificultades relacionadas con datos, lenguaje informal y eficiencia. Su utilidad es técnica. Los 29 estudios que declara incluir pertenecen a su revisión original y no se contabilizan como estudios sobre limpieza pública en Juliaca.

## E4. Brecha de investigación (research gap)

**¿Qué se conoce actualmente?** Los antecedentes recogidos describen análisis de opiniones digitales sobre residuos, comparaciones de clasificadores en opiniones peruanas y evaluación de modelos de lenguaje en expresiones coloquiales del español peruano. En conjunto, fundamentan la pertinencia de una comparación contextualizada.

**¿Qué aspecto permanece sin resolver?** La evidencia recopilada no permite establecer cómo difieren TF-IDF + SVM y un Transformer en español al clasificar el mismo conjunto de comentarios sobre limpieza pública y recojo de residuos en Juliaca. Los resultados de otros países, plataformas y dominios no resuelven esa comparación local.

**Brecha identificada:** falta de evidencia comparativa suficiente, dentro del material documental disponible, sobre el desempeño de ambos enfoques bajo un corpus local, etiquetas de referencia y condiciones de evaluación comunes.

Esta brecha es preliminar. No equivale a afirmar que no existen publicaciones sobre el tema. Para confirmarla será necesario ampliar y documentar la búsqueda bibliográfica. La disponibilidad del corpus constituye, además, una condición de factibilidad pendiente, distinta de la brecha científica.

## E5. Problema de investigación

### Formulación narrativa

Los antecedentes reunidos justifican el análisis de sentimientos en conversaciones sobre residuos y la comparación de clasificadores en español. Sin embargo, las diferencias entre sus datos y protocolos impiden determinar de antemano qué desempeño tendrán un clasificador tradicional y un Transformer sobre comentarios ciudadanos de Juliaca. Se requiere una comparación empírica que utilice datos pertinentes, etiquetas documentadas y una evaluación común, previa verificación de la factibilidad del corpus.

### Pregunta de investigación

¿Qué diferencias de desempeño, medidas principalmente mediante macro-F1, presentan un clasificador TF-IDF + SVM y un modelo Transformer en español al clasificar sentimientos en comentarios ciudadanos sobre limpieza pública y recojo de residuos sólidos en Juliaca?

## E6. Justificación de la investigación

### Justificación científica

El estudio aportaría evidencia contextualizada sobre dos enfoques de clasificación aplicados a comentarios locales. Su contribución consistiría en establecer la magnitud y las características de las diferencias observadas, así como los errores frecuentes, sin asumir previamente la superioridad del Transformer. La comparación permitiría examinar los límites de aplicación de antecedentes procedentes de otros dominios.

### Justificación tecnológica

La investigación permitiría documentar un procedimiento de preparación, etiquetado y clasificación de comentarios, junto con la configuración y evaluación de los modelos. Una partición de prueba común y el registro de parámetros, versiones y decisiones de preprocesamiento favorecerían la reproducibilidad. Los resultados aportarían criterios para seleccionar un enfoque según su desempeño y viabilidad en las condiciones del proyecto.

### Justificación práctica

Si el corpus y la clasificación resultan viables, el procedimiento podría apoyar la organización inicial de comentarios para revisión humana. Su aporte dependerá de la cobertura y calidad de los datos. La clasificación describirá las opiniones expresadas en los comentarios analizados; no medirá directamente el estado de limpieza de la ciudad ni sustituirá la inspección municipal o la participación de residentes.

## E7. Referencias científicas utilizadas

Referencias reproducidas a partir del Documento 2, pendientes de cotejo con las publicaciones originales. La lista de autores de Huang et al. se conserva abreviada porque el borrador no la proporciona completa.

1. Adrianzón Torres, M. J., & Escobedo Cárdenas, E. J. (2021). Análisis comparativo de métodos de machine learning para clasificar opiniones sobre el servicio de restaurantes peruanos en Facebook. En *Sociedad digital: retos y oportunidades de una nueva realidad. Actas del IV Congreso Internacional de Ingeniería de Sistemas* (pp. 67–81). Universidad de Lima. [DOI](https://doi.org/10.26439/ciis2021.5578).
2. Calizaya-Milla, S. E., Santos, J., & Huanca Torres, F. A. (2026). Fine-tuning monolingual pre-trained BERT models for sentiment analysis in Peruvian slang contexts. *Applied Artificial Intelligence, 40*(1), artículo 2641381. [DOI](https://doi.org/10.1080/08839514.2026.2641381).
3. Cayra Uscamayta, F. (2024). *La contaminación ambiental y la gestión de residuos sólidos en la Municipalidad Provincial de San Román Juliaca–2023* [Tesis, Universidad Privada San Carlos]. [Repositorio](http://repositorio.upsc.edu.pe/handle/UPSC/872).
4. Huang, H., Zeng, X., Ge, L., et al. (2025). Social media engagement in waste sorting: The role of sentiment in shaping public awareness. *Humanities and Social Sciences Communications, 12*, artículo 1763. [DOI](https://doi.org/10.1057/s41599-025-06041-x).
5. Jiang, P., Zhou, J., Fan, Y. V., Klemes, J. J., Zheng, M., & Varbanov, P. S. (2021). Data analysis of resident engagement and sentiments in social media enables better household waste segregation and recycling. *Journal of Cleaner Production, 319*, artículo 128809. [DOI](https://doi.org/10.1016/j.jclepro.2021.128809).
6. Xue, Y., & Liu, H. (2023). Exploration of the dynamic evolution of online public opinion towards waste classification in Shanghai. *International Journal of Environmental Research and Public Health, 20*(2), artículo 1471. [DOI](https://doi.org/10.3390/ijerph20021471).

## Lista de comprobación del avance

- [x] Tema delimitado, con decisiones de factibilidad pendientes explícitas.
- [x] Situación problemática formulada y vinculada con antecedentes descritos en los borradores.
- [x] Evidencia bibliográfica organizada con sus límites de aplicación.
- [x] Research gap preliminar explícito y derivado del material disponible.
- [x] Pregunta investigable y coherente con la comparación propuesta.
- [x] Justificación científica, tecnológica y práctica desarrollada.
- [x] Referencias identificadas y procedencia documentada.
- [ ] Consultar las publicaciones originales y completar los metadatos bibliográficos.
- [ ] Confirmar la brecha mediante una búsqueda bibliográfica ampliada y documentada.
- [ ] Confirmar fuente, periodo, volumen y condiciones de uso del corpus local.
