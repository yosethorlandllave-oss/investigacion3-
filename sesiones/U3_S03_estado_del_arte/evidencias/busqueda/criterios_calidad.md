# E2. Criterios de selección y evaluación de calidad

**Corte:** 31/10/2026. Evaluación documental realizada para esta sesión; no constituye una certificación externa de calidad.

## Reglas de elegibilidad

1. Incluir full papers de conferencias, artículos de revista y surveys formalmente publicados, pertinentes a métodos de sentimientos, adaptación al español/Perú o residuos y opinión digital.
2. Priorizar 2022–2026 y alcanzar al menos 80 % de actualidad; admitir antecedentes anteriores si su función seminal está justificada.
3. Exigir fuente primaria con información suficiente para la contribución que se le atribuye. Un resumen aislado permite detectar candidatos, no completar resultados experimentales.
4. Priorizar CORE A*, A o B, o revistas Q1/Q2 indicando índice, categoría y año. El ranking orienta; no sustituye la lectura crítica del artículo.
5. Excluir duplicados, materiales comerciales, referencias sin identificación suficiente y trabajos cuyo foco no aporte al alcance delimitado. Los preprints solo pueden ser complementarios y se distinguen de la publicación formal.
6. Mantener separados los candidatos pendientes por acceso o verificación; no confundir falta de acceso con baja calidad científica.

## Dimensiones de evaluación

| Dimensión | Pregunta aplicada | Consecuencia para la síntesis |
|---|---|---|
| Pertinencia | ¿Aporta al método, idioma, contexto o problema? | Clasificación por función; no exigir que todos estudien Juliaca. |
| Validez de evaluación | ¿Se conocen datos, partición y métrica? ¿Es entrenamiento o prueba? | Comparar solo resultados compatibles; marcar NR donde no se verificó. |
| Etiquetado | ¿Se explica la referencia humana y su consistencia? | Registrar incertidumbre y no asumir que «manual» equivale a fiable. |
| Transferibilidad | ¿Coinciden lengua, plataforma, población y tema? | Limitar inferencias al corpus correspondiente. |
| Reproducibilidad | ¿Se declaran modelos, datos o código? | Distinguir disponibilidad declarada de artefactos efectivamente ejecutados. |
| Transparencia | ¿Se pueden localizar las afirmaciones y limitaciones? | Registrar sección/tabla y enlace primario. |

No se fabrica una puntuación numérica agregada: las carencias tienen consecuencias distintas para un survey, un modelo base y una aplicación social. La matriz documenta decisiones por trabajo.

## Verificación de venues

Todos los enlaces se consultaron el 31/10/2026. La clasificación de una edición reciente no se atribuye retroactivamente al año de publicación. AIS, CiteScore y SJR son indicadores distintos; sus cuartiles no son intercambiables.

| Trabajos | Venue | Indicador verificado | Fuente / alcance |
|---|---|---|---|
| P01 | EMNLP | ICORE 2026 A* | [Portal CORE](https://portal.core.edu.au/conf-ranks/?search=EMNLP&by=all&source=all&sort=atitle&page=1). Referencia de prestigio actual, no ranking histórico de 2002. |
| P02 | NAACL | CORE 2023 A; ICORE 2026 A | [Ficha CORE](https://portal.core.edu.au/conf-ranks/1648/). |
| P03–P04 | LREC | CORE 2023 B; ICORE 2026 B | [Ficha CORE](https://portal.core.edu.au/conf-ranks/2092/). En CORE 2021 figuraba C; se explicita esta diferencia temporal. |
| P05 | Procesamiento del Lenguaje Natural | SJR 2024 Q2 Computer Science Applications; Q1 Linguistics and Language | [Calidad de la revista, SEPLN](https://www.sepln.org/index.php/la-revista/calidad). En 2022: Q3 en Computer Science Applications y Q1 en lingüística. |
| P06 | International Journal of Environmental Research and Public Health | CiteScore 2023: Q1 Public Health, Environmental and Occupational Health; Q2 Pollution | [Anuncio editorial de 12/06/2024](https://www.mdpi.com/journal/ijerph%C2%A0/news-and-conferences/news/8589). No se afirma cuartil JCR actual. |
| P07 | Journal of King Saud University – Computer and Information Sciences | AIS 2024 Q2, Computer Science, Information Systems | [Clasificación UEFISCDI, edición junio 2025](https://uefiscdi.gov.ro/resource-860007-clasament.ais.jcr.2024.pdf), página física 99. No confundir con la revista del mismo nombre terminada en Science. |
| P08 | Heliyon | SJR 2024 Q1 Multidisciplinary | [CroRIS, sistema institucional croata](https://www.croris.hr/casopisi/casopis/22186). Reproducción institucional del indicador; no consulta directa a Scimago. |
| P09 | Humanities and Social Sciences Communications | SJR 2024 Q1 Social Sciences (miscellaneous) | [CroRIS](https://www.croris.hr/casopisi/casopis/30001). Otras categorías pueden tener otro cuartil. |
| P10 | Applied Artificial Intelligence | AIS 2024 Q2, Computer Science, Artificial Intelligence | [UEFISCDI](https://uefiscdi.gov.ro/resource-860007-clasament.ais.jcr.2024.pdf), página física 85. |
| P11 | Frontiers in Environmental Science | AIS 2024 Q2, Environmental Sciences | [UEFISCDI](https://uefiscdi.gov.ro/resource-860007-clasament.ais.jcr.2024.pdf), entrada del journal. |

Scimago directo devolvió 403 durante la consulta. Se recurrió a fuentes editoriales, institucionales y a la agencia pública UEFISCDI, identificando el indicador exacto. Los rankings anteriores son evidencias bibliométricas complementarias, no parte de las 11 referencias científicas ni del cálculo de actualidad. No se utilizan recuentos de citas dinámicos para decidir qué modelo es mejor.

## Dos seminales y un survey

- **P01, Pang et al. (2002):** antecedente temprano de comparación supervisada de sentimientos y del uso de SVM. La [ficha oficial ACL](https://aclanthology.org/W02-1011/) registra el reconocimiento Test-of-Time de NAACL 2018. Su función es fundamentar la línea base; no demostrar el rendimiento de TF-IDF en español.
- **P02, Devlin et al. (2019):** fundamento del preentrenamiento bidireccional y ajuste posterior que sustenta los Transformers considerados. La [ficha oficial ACL](https://aclanthology.org/N19-1423/) registra Best Long Paper; P03 y P10 permiten verificar su continuidad en esta línea. No es un estudio municipal.
- **P07, Mao et al. (2024):** survey sistemático que organiza métodos y retos. Su sección de selección identifica 132 estudios finales; las menciones introductorias a un conjunto más amplio no se usan como tamaño final. Aporta clasificación del campo, no un experimento propio que pueda competir en la matriz de métricas.
