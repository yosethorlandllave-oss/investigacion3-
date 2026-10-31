# Desarrollo — U3 Sesión 2: Objetivos, hipótesis y variables

**Título de la investigación:** Comparación de modelos de procesamiento del lenguaje natural para clasificar sentimientos en comentarios ciudadanos sobre la limpieza pública y el recojo de residuos sólidos en Juliaca, Puno

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

## E4. Hipótesis de investigación

### Correspondencia con el enfoque y alcance

Se propone un enfoque cuantitativo y un alcance comparativo, con evaluación experimental computacional de dos procedimientos de clasificación sobre datos observacionales. No se manipulan servicios municipales ni opiniones ciudadanas. La comparación permite examinar el desempeño de los procedimientos en el corpus; no demostrar efectos sobre la limpieza de la ciudad.

Se formula una hipótesis porque el estudio busca contrastar una diferencia de desempeño. La revisión bibliográfica que fundamenta el proyecto no requiere por sí misma una hipótesis experimental; esta corresponde al estudio comparativo posterior.

### Hipótesis general (H1)

El desempeño esperado, medido mediante macro-F1, difiere entre TF-IDF + SVM y el Transformer en español al clasificar sentimientos en comentarios ciudadanos sobre limpieza pública y recojo de residuos sólidos en Juliaca, bajo las condiciones del protocolo establecido.

### Hipótesis nula (H0)

El desempeño esperado, medido mediante macro-F1, es igual para ambos enfoques bajo las condiciones del protocolo establecido.

Se define Δ = macro-F1 esperado del Transformer − macro-F1 esperado de TF-IDF + SVM. Así, H1: Δ ≠ 0; H0: Δ = 0. La diferencia calculada con el conjunto de prueba será una estimación de Δ, no una demostración automática de H1.

La hipótesis es bilateral. Los antecedentes descritos por Adrianzón Torres y Escobedo Cárdenas (2021) y Calizaya-Milla et al. (2026) sustentan la comparación de enfoques, pero no garantizan una ventaja del Transformer en este dominio.

### Alcance de la contrastación

Antes de examinar los resultados de prueba se fijarán el procedimiento de comparación, su tratamiento de la incertidumbre y el criterio de decisión. Debe respetarse que ambos modelos predicen sobre los mismos comentarios y considerarse la posible dependencia entre comentarios de una misma publicación. También se especificará si la inferencia queda condicionada a modelos entrenados concretos o incorpora variación entre ejecuciones. No se seleccionará el procedimiento estadístico después de observar cuál favorece a un modelo.

La precisión y la exhaustividad se usarán como resultados complementarios; el contraste principal corresponde a macro-F1. No rechazar H0 no demostrará equivalencia entre modelos. La interpretación quedará limitada por el muestreo y la cobertura del corpus.

### Hipótesis específicas

No se añaden hipótesis específicas: OE1 caracteriza los datos, OE2 produce las mediciones necesarias, OE3 contrasta la hipótesis general y OE4 analiza errores. No se plantean relaciones explicativas adicionales ni se convierte cada métrica complementaria en un contraste independiente.

## E5. Variables identificadas

| Tipo | Variable o condición | Función | Relación con la hipótesis |
|---|---|---|---|
| Independiente | Enfoque de clasificación de sentimientos | Factor comparado con dos niveles: TF-IDF + SVM y Transformer en español. | Define las dos condiciones entre las que se estima Δ. |
| Dependiente | Desempeño de clasificación | Correspondencia entre etiquetas de referencia y predicciones, resumida principalmente con macro-F1. | Su diferencia constituye el resultado principal. |
| Control | Corpus, etiquetas y particiones | Mantienen comunes los comentarios y la referencia de evaluación. | Reducen diferencias atribuibles a evaluar datos distintos. |
| Control o registro | Ajuste de modelos, semillas, versiones y presupuesto de búsqueda | Documentan condiciones que pueden afectar las predicciones. | Permiten interpretar el alcance de la comparación entre procedimientos concretos. |
| Intervinientes registradas | Desequilibrio de clases, ambigüedad, expresiones coloquiales y procedencia de los comentarios | Describen características que pueden influir en los errores. | Delimitan la aplicabilidad de la conclusión; no se tratarán como causas demostradas. |

La polaridad del sentimiento es la etiqueta objetivo que los modelos predicen. No es una variable independiente adicional. Sus categorías definitivas se fijarán en la guía de anotación después del piloto y antes de la evaluación final.

## E6. Matriz de operacionalización de variables

### Variable independiente: enfoque de clasificación

**Definición conceptual:** procedimiento computacional que transforma un texto en una predicción de sentimiento. Se consideran un enfoque de representación TF-IDF con SVM y otro basado en representaciones contextuales de un Transformer en español. La distinción se fundamenta en el Documento 2, especialmente E1, E5 y E6, y en los antecedentes de comparación allí citados. No se atribuye esta definición a una cita textual de una publicación primaria.

**Definición operacional:** aplicar los dos procedimientos al mismo problema de clasificación, con datos comunes y ajustes propios documentados. El modelo Transformer concreto, su versión y su configuración se elegirán por pertinencia y factibilidad, antes de la evaluación de prueba. No se tomarán decisiones de selección usando resultados del conjunto de prueba.

| Dimensión | Indicador | Forma de medición o registro | Escala o unidad | Instrumento o fuente |
|---|---|---|---|---|
| Familia del procedimiento | TF-IDF + SVM / Transformer en español | Identificación del procedimiento que genera cada predicción. | Nominal; dos categorías sin orden. | Registro de configuración y archivo de predicciones. |
| Especificación técnica | Modelo, versión, vectorizador o tokenizador y parámetros | Registro de la configuración utilizada en cada ejecución. | Metadatos nominales y valores numéricos según el parámetro. | Ficha de ejecución y archivos de configuración previstos. |

### Variable dependiente: desempeño de clasificación

**Definición conceptual:** grado de correspondencia entre las predicciones y las etiquetas de referencia en los comentarios evaluados. El Documento 2 propone macro-F1 como criterio principal y precisión, exhaustividad y matriz de confusión como complementos. El Documento 1 describe el uso de métricas de clasificación en la literatura revisada. Estos borradores fundamentan la elección general; las convenciones de cálculo siguientes se explicitan como propuesta operacional del proyecto.

**Definición operacional:** comparar cada predicción con su etiqueta de referencia en el conjunto de prueba común; calcular métricas para el conjunto completo y por clase. La unidad textual es el comentario, mientras que macro-F1 es un resultado agregado sobre el conjunto evaluado para cada modelo y ejecución.

| Dimensión | Indicador | Forma de medición | Escala o unidad | Instrumento o fuente |
|---|---|---|---|---|
| Desempeño global equilibrado entre clases | Macro-F1, principal | Media aritmética de F1 de las K clases definidas. | Índice cuantitativo adimensional entre 0 y 1. | Etiquetas de referencia, predicciones y script de evaluación previsto. |
| Precisión por categoría | Precisión de cada clase y macroprecisión | TP / (TP + FP); promedio no ponderado entre clases para macroprecisión. | Proporción entre 0 y 1, cuando el denominador es distinto de cero. | Mismas etiquetas y predicciones. |
| Recuperación por categoría | Exhaustividad de cada clase y macroexhaustividad | TP / (TP + FN); promedio no ponderado entre clases. | Proporción entre 0 y 1, cuando el denominador es distinto de cero. | Mismas etiquetas y predicciones. |
| Distribución de errores | Matriz de confusión | Recuento de comentarios por etiqueta real y predicha. | Frecuencia absoluta, escala de razón. | Tabla cruzada derivada de las predicciones. |
| Diferencia entre enfoques | Δ estimado | Macro-F1 observado del Transformer menos macro-F1 observado de SVM. | Diferencia adimensional entre −1 y 1; multiplicar por 100 permite reportar puntos porcentuales. | Resultados agregados y procedimiento de comparación previsto. |

Para cada clase k, TP_k representa verdaderos positivos; FP_k, falsos positivos; y FN_k, falsos negativos, considerando esa clase frente a las demás. Se calculará F1_k = 2TP_k / (2TP_k + FP_k + FN_k), y macro-F1 = (1/K) × suma de F1_k.

**Convención propuesta:** cuando el denominador de una métrica sea cero, se registrará el caso y se asignará cero para calcular el resumen agregado. Se mantendrá fijo el conjunto de K etiquetas; no se omitirán clases para mejorar el promedio. También se reportará el soporte de cada clase. La ausencia de una clase en prueba se señalará como una limitación, pues la convención numérica no aporta evidencia sobre su desempeño.

### Condiciones de control e intervinientes

| Condición | Posible efecto | Estrategia de control o registro | Evidencia prevista |
|---|---|---|---|
| Fuente y periodo | Cambios de lenguaje, temática o cobertura. | Definir criterios de inclusión y registrar procedencia y fechas. | Ficha del corpus. |
| Etiquetas y ambigüedad | Inconsistencia en la referencia de evaluación. | Elaborar guía; revisar una parte del corpus de forma independiente, si es viable, y documentar desacuerdos y su resolución. | Guía y registro de anotación. |
| Partición y duplicados | Contaminación entre entrenamiento y prueba. | Usar los mismos subconjuntos para ambos modelos y mantener duplicados o casi duplicados en un mismo subconjunto; valorar agrupación por publicación. | Manifiesto de partición y registro de deduplicación. |
| Representación y preprocesamiento | Pérdida de señales o acceso indebido a información de prueba. | Ajustar TF-IDF solo con entrenamiento; respetar el tokenizador del Transformer y documentar las transformaciones de cada enfoque. | Configuraciones reproducibles. |
| Desbalance de clases | Concentración del rendimiento en categorías frecuentes. | Reportar soporte por clase; cualquier ponderación o remuestreo se decidirá con entrenamiento/validación. | Recuentos y decisiones de ajuste. |
| Hiperparámetros y presupuesto | Ventajas debidas a una búsqueda desigual o al uso de prueba para ajustar. | Establecer y registrar reglas y presupuesto de búsqueda; seleccionar con validación. | Registro de experimentos. |
| Aleatoriedad | Variación entre ejecuciones. | Fijar y registrar semillas; decidir antes de evaluar si se realizarán repeticiones y cómo se resumirán. | Ficha de ejecución. |
| Recursos y versiones | Restricciones en la configuración o reproducibilidad. | Registrar hardware y versiones. No se plantea eficiencia computacional como resultado principal adicional. | Ficha técnica. |

### Definiciones e indicadores de las condiciones de control

Las siguientes definiciones son propuestas operacionales del proyecto que desarrollan las condiciones descritas en el Documento 2. Su función es documentar el contexto de la comparación; no introducen hipótesis causales adicionales.

| Condición y dimensión | Definición conceptual | Definición operacional e indicador | Escala o unidad | Fuente o instrumento previsto |
|---|---|---|---|---|
| Corpus: cobertura | Conjunto de comentarios que cumplen la delimitación temática y de procedencia. | Registrar fuente, fechas inicial y final y número de comentarios incluidos tras depuración. | Fuente: nominal; fechas: calendario; cantidad: razón, comentarios. | Ficha del corpus y registro de inclusión. |
| Etiquetado: consistencia | Grado de coincidencia en la asignación de categorías conforme a la guía. | En el subconjunto revisado independientemente, contar coincidencias y desacuerdos antes de resolverlos; registrar número revisado y proporción de coincidencias. Si no hay revisión independiente, consignar que no se estimó concordancia. | Etiquetas: nominal; recuentos: razón; coincidencia: proporción entre 0 y 1. | Guía de anotación y registro de decisiones de los revisores. |
| Ambigüedad: interpretación | Presencia de comentarios cuya categoría no se determina de forma unívoca mediante la guía. | Marcar los casos que requieren revisión y documentar su resolución; contar casos marcados sin equipararlos automáticamente a errores del modelo. | Marca: nominal; cantidad: razón. | Registro de anotación y revisión de casos. |
| Partición: asignación | Distribución de los comentarios entre entrenamiento, validación y prueba. | Registrar subconjunto por identificador y número de comentarios en cada uno; conservar la misma asignación para ambos enfoques. | Subconjunto: nominal; cantidad: razón. | Manifiesto de partición. |
| Duplicación: repetición textual | Presencia de textos idénticos o casi idénticos según el criterio de depuración definido. | Registrar grupos detectados y comprobar su asignación a un único subconjunto. Documentar criterio y método de detección. | Identificador de grupo: nominal; recuento de cruces entre subconjuntos: razón. | Registro de deduplicación y manifiesto de partición. |
| Clases: distribución | Frecuencia relativa de las categorías de sentimiento en el corpus. | Calcular n_k y n_k/N por clase y subconjunto. | Clase: nominal; soporte: razón, comentarios; proporción: 0 a 1. | Etiquetas de referencia y tabla de distribución. |
| Lenguaje: expresiones coloquiales | Uso de expresiones locales o informales que pueden requerir interpretación contextual. | Durante el análisis de errores, registrar casos identificados con criterios explícitos y fragmentos desidentificados. No estimar prevalencia general a partir de una selección de errores. | Categoría descriptiva: nominal; recuento en la selección revisada: razón. | Ficha de análisis de errores. |
| Preprocesamiento: transformación | Operaciones que convierten el texto en la entrada de cada modelo. | Registrar reglas de limpieza, vectorizador o tokenizador y subconjunto usado para ajustar componentes aprendidos. | Reglas, componente y subconjunto: nominal. | Configuración del procedimiento. |
| Ajuste: presupuesto | Recursos y oportunidades de búsqueda asignados a la selección de configuraciones. | Registrar número de configuraciones evaluadas y criterio de selección; documentar parámetros propios de cada enfoque. | Número de configuraciones: razón; criterio: nominal; parámetros: escala según su definición. | Registro de experimentos y validación. |
| Aleatoriedad: ejecuciones | Variación inducida por procesos aleatorios del procedimiento. | Registrar semilla por ejecución y número de repeticiones; la semilla actúa como identificador, no como magnitud de desempeño. | Semilla: identificador nominal; repeticiones: razón. | Ficha de ejecución. |
| Entorno: reproducibilidad | Condiciones de software y hardware bajo las que se ejecuta cada modelo. | Registrar versiones, CPU/GPU y memoria disponible. | Versiones y modelos de equipo: nominal; memoria: razón, GB. | Ficha técnica del entorno. |

La proporción de coincidencias entre anotadores es descriptiva y no corrige el acuerdo por azar. No se interpretará como una validación completa de las etiquetas. Las condiciones descritas se registrarán antes o durante la ejecución según corresponda; en esta sesión se especifican los instrumentos, no sus valores.

## E7. Matriz de consistencia

**Pregunta común:** ¿qué diferencias de desempeño, medidas principalmente mediante macro-F1, presentan TF-IDF + SVM y un Transformer en español en comentarios ciudadanos sobre limpieza pública y recojo de residuos en Juliaca?

**Objetivo general común:** comparar ese desempeño bajo un protocolo de evaluación común. La matriz descompone cómo cada objetivo específico contribuye a responder la misma pregunta.

| Problema o componente de la pregunta | Objetivo general | Objetivo específico | Hipótesis relacionada | Variables o condiciones | Indicadores y evidencia |
|---|---|---|---|---|---|
| Delimitación del corpus local que permite responder la pregunta. | Comparar el desempeño de ambos enfoques en el contexto definido. | OE1. Caracterizar disponibilidad y propiedades del corpus. | Condición de factibilidad; sin hipótesis específica. | Corpus, procedencia, etiquetas y ambigüedad. | Número de comentarios, soporte por clase, periodo y registro de anotación. |
| Desempeño de cada procedimiento sobre datos comunes. | Comparar el desempeño de ambos enfoques en el contexto definido. | OE2. Evaluar ambos modelos. | Produce las mediciones para H1/H0. | Enfoque de clasificación y desempeño. | Macro-F1, precisión, exhaustividad y predicciones por comentario. |
| Magnitud e incertidumbre de la diferencia. | Comparar el desempeño de ambos enfoques en el contexto definido. | OE3. Determinar la diferencia y su incertidumbre. | H1: Δ ≠ 0; H0: Δ = 0. | Enfoque y macro-F1 esperado bajo el protocolo. | Δ estimado y análisis de incertidumbre previamente definido. |
| Alcance y limitaciones de los resultados. | Comparar el desempeño de ambos enfoques en el contexto definido. | OE4. Analizar errores y límites de aplicación. | Interpretación complementaria de H1/H0; sin contraste adicional. | Desempeño por categoría y características registradas del corpus. | Matrices de confusión, soporte y análisis de errores. |

La pregunta, el objetivo general y H1/H0 se refieren a los mismos enfoques y al mismo resultado principal. Los instrumentos previstos producen los datos necesarios, pero aún deben implementarse. La validez externa estará condicionada por la fuente y el periodo del corpus; las métricas no representan automáticamente a todos los comentarios ni a todos los habitantes de Juliaca.

## E8. Referencias y fundamento documental

La distinción entre enfoques y la pertinencia de evaluar datos en español peruano se apoyan en los antecedentes descritos en el Documento 2. Las referencias siguientes se reproducen desde ese borrador y no se presentan como publicaciones consultadas directamente:

1. Adrianzón Torres, M. J., & Escobedo Cárdenas, E. J. (2021). Análisis comparativo de métodos de machine learning para clasificar opiniones sobre el servicio de restaurantes peruanos en Facebook. En *Sociedad digital: retos y oportunidades de una nueva realidad. Actas del IV Congreso Internacional de Ingeniería de Sistemas* (pp. 67–81). Universidad de Lima. [DOI](https://doi.org/10.26439/ciis2021.5578).
2. Calizaya-Milla, S. E., Santos, J., & Huanca Torres, F. A. (2026). Fine-tuning monolingual pre-trained BERT models for sentiment analysis in Peruvian slang contexts. *Applied Artificial Intelligence, 40*(1), artículo 2641381. [DOI](https://doi.org/10.1080/08839514.2026.2641381).

**Documentos efectivamente consultados:**

- [Documento 1: revisión de análisis de sentimientos](../U3_S01_problema_justificacion/evidencias/documento_1_revision_sentimientos.pdf): antecedente de familias de modelos y métricas de clasificación.
- [Documento 2: perfil de investigación sobre Juliaca](../U3_S01_problema_justificacion/evidencias/documento_2_perfil_juliaca.pdf): E1, E5 y E6 fundamentan la comparación, las variables y la selección de macro-F1.

Las fórmulas, convenciones y controles se formulan aquí como definiciones operacionales propuestas. Su exposición no acredita que los artículos citados hayan usado exactamente este protocolo. La consulta directa y el respaldo bibliográfico específico del procedimiento inferencial quedan pendientes de la ampliación bibliográfica.

## Lista de comprobación final

- [x] Pregunta revisada y alineada con la sesión 1.
- [x] Objetivo general y cuatro objetivos específicos verificables.
- [x] Enfoque y alcance definidos; uso de hipótesis justificado.
- [x] H1 y H0 bilaterales; ausencia de hipótesis específicas justificada.
- [x] Variables y condiciones de control identificadas.
- [x] Definiciones conceptuales y operacionales formuladas con procedencia explícita.
- [x] Dimensiones, indicadores, escalas e instrumentos previstos descritos.
- [x] Matriz de consistencia elaborada.
- [x] Referencias y límites de consulta identificados.
- [ ] Confirmar corpus, fuente, periodo, categorías y modelo Transformer concreto.
- [ ] Consultar fuentes primarias y completar el respaldo del procedimiento de comparación.
- [ ] Fijar partición, presupuesto, repeticiones y procedimiento inferencial antes de evaluar prueba.
