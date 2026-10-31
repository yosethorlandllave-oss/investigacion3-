# E5. Taxonomía y mapa de la literatura

**Elaboración propia a partir de P01–P11.** Los identificadores remiten a la [matriz de síntesis](../matrices/matriz_sintesis.md) y a [E9](../../desarrollo.md). La clasificación organiza funciones y métodos; no representa una jerarquía de calidad ni una red bibliométrica generada automáticamente.

## Taxonomía por pregunta que responde la literatura

| Categoría | Subcategoría / trabajos | Conocimiento aportado | Lo que queda por comprobar en Juliaca |
|---|---|---|---|
| A. Fundamentos de clasificación | Supervisados clásicos: P01. Preentrenamiento contextual: P02. | Dos familias que justifican la comparación. | Diferencia bajo iguales datos y etiquetas. |
| B. Adaptación de representaciones | Español web: P05. Español social: P03. Multilingüe social: P04. Variedad peruana: P10. | El idioma y el tipo de texto importan para seleccionar el modelo. | Transferencia al servicio de limpieza y sus formas de expresión. |
| C. Aplicación a residuos | Léxico + temas: P06. LSTM + coocurrencia: P08. Transformer + difusión: P09. SnowNLP + temas: P11. | Sentimientos como instrumento para estudiar opiniones y políticas. | Calidad de las predicciones antes de interpretar opiniones agregadas. |
| D. Síntesis del campo | Survey de métodos y retos: P07. | Organización de familias y problemas abiertos. | Protocolo específico y viable para el proyecto. |

Las categorías no son excluyentes: P09 usa un Transformer, pero se ubica en C por su finalidad social; P10 es un estudio comparativo y se ubica en B por su adaptación lingüística. LDA/BERTopic organizan temas, mientras que SVM, LSTM y BERT pueden producir etiquetas de sentimiento; no se comparan como si cumplieran la misma función.

## Mapa de proximidad al proyecto

| Eje | Evidencia más próxima en el corpus | Distancia que permanece |
|---|---|---|
| Método | P01–P05, P10 | No todos comparan TF-IDF + SVM con un Transformer bajo el protocolo propuesto. |
| Variedad lingüística | P10; P03–P05 como recursos de español | Español peruano general no equivale a discurso local sobre limpieza. |
| Dominio | P06, P08, P09, P11 | Separación de residuos en China no equivale a recojo y limpieza en Juliaca. |
| Intersección de los tres ejes | No cubierta por un experimento directamente equivalente dentro de los once trabajos seleccionados | Diseñar y evaluar un corpus local con controles comunes. |

La intersección es una **inferencia de esta revisión**, acotada al corpus y a su cobertura. No demuestra prioridad mundial ni ausencia de otros trabajos.

## Evolución temática observada

| Periodo | Cambio representado en el corpus |
|---|---|
| 2002 | Comparación de clasificadores supervisados con representaciones de palabras (P01). |
| 2019 | Preentrenamiento contextual y ajuste a tareas (P02). |
| 2022 | Especialización por idioma y plataforma (P03–P05). |
| 2023–2025 | Coexistencia de léxicos, redes recurrentes y Transformers en estudios de residuos (P06, P08, P09, P11); síntesis del campo (P07). |
| 2026 | Evaluación específica de una variedad peruana (P10). |

La coexistencia de métodos impide describir una sustitución total de técnicas clásicas por Transformers. Esta cronología es ilustrativa: no se calcularon frecuencias de publicación que permitan estimar tendencias globales.

## Relaciones de citación comprobadas

| Documento citante | Documento citado | Lugar de verificación |
|---|---|---|
| P03 | P02 | Antecedentes y referencias de RoBERTuito. |
| P10 | P02, P03, P05, P07 | Referencias del artículo peruano. |

Las relaciones anteriores sí representan citas verificadas. Las conexiones entre categorías y la propuesta representan razonamiento temático propio, no citas. No se calculan centralidad, cocitación ni impacto con esta pequeña red.
