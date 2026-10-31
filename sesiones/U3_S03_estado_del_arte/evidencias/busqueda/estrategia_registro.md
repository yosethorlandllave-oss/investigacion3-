# E1. Estrategia y registro de búsqueda

**Fecha de consulta y corte:** 31 de octubre de 2026. **Tema:** comparación de TF-IDF + SVM y un Transformer en español para sentimientos sobre limpieza pública y recojo de residuos en Juliaca. **Tipo de producto:** revisión bibliográfica estructurada para el PPI; no se declara una RSL exhaustiva concluida.

## Alcance y conceptos

Se buscaron tres líneas complementarias: fundamentos de clasificación; adaptación lingüística al español y al Perú; aplicaciones a residuos y opinión ciudadana. Exigir simultáneamente «Juliaca», «SVM» y «Transformer» habría ocultado antecedentes transferibles. Se amplió primero por dominio y método, y después se comprobó la proximidad contextual.

| Bloque | Español | Inglés / identificadores |
|---|---|---|
| Tarea | análisis de sentimientos, minería de opiniones, polaridad | sentiment analysis, opinion mining, sentiment classification |
| Método | máquina de soporte vectorial, modelos de lenguaje | SVM, TF-IDF, BERT, Transformer, RoBERTuito, XLM-T, MarIA |
| Dominio | limpieza pública, recojo de residuos, segregación de residuos | waste collection, waste sorting, municipal solid waste, public services |
| Contexto | español peruano, jerga peruana, Juliaca, Puno | Spanish, Peruvian Spanish, Peruvian slang |

## Cadenas reutilizables

Estas cadenas constituyen el protocolo para replicación en título/resumen/palabras clave; no se afirma que todas hayan sido ejecutadas en interfaces nativas. Las consultas efectivamente enviadas están en el JSON adjunto.

```text
S1: ("sentiment analysis" OR "opinion mining") AND (SVM OR "TF-IDF" OR BERT OR Transformer) AND (Spanish OR Peruvian)
S2: ("sentiment analysis" OR "opinion mining") AND ("waste collection" OR "waste sorting" OR "municipal solid waste")
S3: ("Juliaca" OR "Puno") AND ("sentiment analysis" OR "análisis de sentimientos") AND (limpieza OR residuos)
S4: ("sentiment analysis") AND (survey OR "systematic literature review") AND (methods OR challenges)
```

Ventana: publicaciones de 2022 a 2026 inclusive, anteriores al corte; excepción razonada para dos seminales. No se impuso idioma español al artículo: se incluyeron textos en inglés con pertinencia metodológica o temática. El año corresponde a la publicación formal, no al primer preprint.

## Ejecución comprobable

El archivo [consultas_ejecutadas.json](consultas_ejecutadas.json) conserva las consultas literales B01–B11 y sus filtros de dominio. Los años incluidos en una consulta fueron términos de búsqueda, no filtros nativos garantizados. B01–B03 localizaron modelos, survey y seminales; B04–B07 contrastaron índices y venues; B08–B10 verificaron detalles metodológicos; B11 amplió dominio, ubicación y citación hacia adelante.

| Recurso / vía | Uso realizado | Resultado y límite |
|---|---|---|
| Buscador web con consultas generales y por dominio | Descubrimiento y recuperación de páginas académicas | Registro de consultas; sin total global fiable ni exportación exhaustiva. |
| ACL Anthology | Metadatos y PDF de P01–P04 | Fuentes primarias consultadas. |
| SEPLN y repositorio UPC | P05 | PDF leído desde el repositorio institucional; descarga editorial directa fallida. |
| MDPI / Europe PMC | P06 | Texto completo editorial y XML del repositorio. |
| Springer / página editorial | P07 | Texto del survey y referencias. |
| PMC / ScienceDirect | P08 | Texto primario consultado; algunos accesos posteriores mostraron controles de acceso. |
| Nature / editor | P09 | Texto editorial e indexación; reapertura posterior redirigió a autenticación. |
| Taylor & Francis | P10 | Texto editorial indexado; apertura directa devolvió 403. No se descargó PDF. |
| Frontiers | P11 | Texto completo, métodos y limitaciones. |
| IEEE Xplore | Candidato C01 | Metadatos/resumen; sin extracción completa suficiente. |
| DBLP | Consulta por dominio y API de RoBERTuito | API bloqueada por comprobación anti-bot; no se obtuvo exportación. |
| Semantic Scholar | Consulta por dominio y API sobre waste sorting sentiment | API devolvió 429; no se obtuvo exportación ni red de citas. |
| CORE y fuentes de indicadores de revistas | Verificación de venues | Detalles y años en criterios_calidad.md. |

No se ejecutaron búsquedas nativas en ACM Digital Library ni Google Scholar. No se utilizaron Connected Papers, Litmaps, ResearchRabbit o VOSviewer. Sus nombres no se presentan como fuentes consultadas. No se generaron recuentos PRISMA a partir de estimaciones del buscador.

## Snowballing verificado

| Dirección | Semilla | Trabajo localizado / relación comprobada | Evidencia |
|---|---|---|---|
| Hacia atrás | P10, Calizaya-Milla et al. (2026) | P03, P05, P07 y P02 aparecen en sus referencias. | Bibliografía del [texto editorial](https://doi.org/10.1080/08839514.2026.2641381). |
| Hacia atrás | P03, Pérez et al. (2022) | P02 como fundamento del preentrenamiento. | Sección 2 y bibliografía del [PDF](https://aclanthology.org/2022.lrec-1.785.pdf). |
| Hacia adelante | P03 | B11 buscó RoBERTuito + Peruvian + 2026 y recuperó P10; se comprobó la cita en el artículo posterior. | Consulta literal B11 y referencias de P10. |

Es un rastreo dirigido y comprobado de relaciones, no una exportación de todos los trabajos citantes. P01 se incorporó por su papel fundacional y reconocimiento académico, no porque se hubiera probado una relación de cita con cada trabajo posterior.

## Selección y trazabilidad

Se seleccionaron **11 publicaciones** P01–P11; **9/11 = 81,8 %** son de 2022–2026 y dos son seminales. Los identificadores son estables en matriz, taxonomía y bibliografía. La deduplicación de candidatos se realizó por DOI o, cuando no existe, título y autores; los espejos de un mismo artículo no cuentan como estudios distintos. Esta cifra es el tamaño del corpus de síntesis, no el número de resultados recuperados por todos los motores.

| Candidato adicional | Decisión en este corte | Motivo y localizador |
|---|---|---|
| C01: Regional Sentimental Flows and Hierarchical Drivers of Urban Waste Sorting (2025) | Pendiente de elegibilidad; fuera de las 11 síntesis | [IEEE, DOI 10.1109/ACCESS.2025.3547766](https://doi.org/10.1109/ACCESS.2025.3547766). Se localizó resumen; faltó verificar el texto necesario para extracción. No se juzga negativamente su calidad. |
| C02: Public Discourse on Waste Sorting Policy (2026) | Pendiente; fuera del corpus | [DOI 10.62159/dawuh.v7i2.2845](https://doi.org/10.62159/dawuh.v7i2.2845). Venue y evaluación metodológica aún no comprobados. |
| C03: Sentiment Analysis of Spanish Political Party Communications on Twitter Using Pre-trained Language Models (2024) | No incluido en corpus principal | [arXiv 2411.04862](https://arxiv.org/abs/2411.04862). Versión localizada como preprint; se priorizó publicación formal. |
| C04: Detection of Polarizing Narratives in Social Media through Machine Learning during Peruvian Political Unrest (2025) | Antecedente contextual fuera de la comparación central | [DOI 10.51847/ePYLFVct7c](https://doi.org/10.51847/ePYLFVct7c). Tema político, no servicio de limpieza. Su localización impide afirmar que no existe investigación de opiniones en Puno. |
| C05: Evaluation of transformer models for financial targeted sentiment analysis in Spanish (2023) | Excluido por foco secundario | [PMC10280559](https://pmc.ncbi.nlm.nih.gov/articles/PMC10280559/). Sentimiento dirigido financiero, fuera del dominio y granularidad definidos. |

El registro conserva candidatos revisados individualmente; no equivale a un censo de todas las coincidencias de búsqueda. Los documentos borradores de las sesiones previas orientaron las semillas, pero sus referencias incompletas no se dieron por verificadas automáticamente.

## Reproducción y ampliación

Para repetir el trabajo: ejecutar las consultas literales; registrar fecha, interfaz y filtros; exportar los registros cuando la base lo permita; deduplicar por DOI/título; aplicar los criterios; comprobar fuentes y localizar cada resultado; actualizar la matriz y el denominador de actualidad. Para una RSL final faltan las exportaciones nativas, resolver los candidatos pendientes, una segunda revisión independiente y repetir el rastreo de citas hasta documentar un criterio de cierre. La búsqueda de esta sesión fundamenta el borrador y acota la brecha; no demuestra ausencia universal de estudios.
