# Material Suplementario — Revisión Sistemática de Literatura (SLR) en LLM-MAS

**Título del estudio:** *Evaluación sistemática de técnicas de observabilidad y atribución causal para la detección de fallos colectivos en sistemas multiagente basados en modelos de lenguaje de gran escala (LLM-MAS)*  
**Conferencia:** XVII Conferencia Internacional INFONOR-CHILE 2026

Este repositorio contiene el material suplementario que respalda la trazabilidad metodológica del proceso de búsqueda, selección y extracción de datos conforme a la guía **PRISMA 2020**.

---

## Estructura del Repositorio

* **[`protocolo/Protocolo_revision.md`](protocolo/Protocolo_revision.md):** Documento de protocolo definido previo a la ejecución de las búsquedas (formulación de preguntas de investigación PI1–PI3, selección de fuentes, cadena booleana de búsqueda, criterios de inclusión CI1–CI4 y exclusión CE1–CE4, diseño del formulario de extracción y procedimiento de resolución de discrepancias).
* **[`matrices/matrix_papers.xlsx`](matrices/matrix_papers.xlsx):** Planilla estructurada con los registros identificados y la aplicación secuencial de los filtros de elegibilidad:
  * `Hoja original`: $n = 8.692$ registros identificados inicialmente.
  * `Filtrado titulo`: $n = 5.470$ registros tras deduplicación inicial por coincidencia de título y autores ($-3.222$).
  * `Filtrado citas`: $n = 2.227$ registros tras aplicar el umbral mínimo de citaciones CI3 ($-3.243$).
  * `Filtrado años`: $n = 1.746$ registros dentro de la ventana temporal 2021–2026 CI1 ($-481$).
  * `Rellenado DOI`: $n = 1.662$ registros tras verificación de presencia y deduplicación por DOI ($-84$).
  * `Rellenado ISSN`: $n = 378$ registros tras aplicar el filtro de presencia de ISSN ($-1.284$).
  * `Indexados` y `Priorizados`: $n = 347$ registros confirmados con indexación en Web of Science o Scopus ($-31$), previos a la lectura crítica de pertinencia temática ($N = 30$ estudios incluidos).
* **[`fichas_extraccion/`](fichas_extraccion/):** Las **30 Fichas de Extracción de Información estandarizadas** (`D-01.pdf` a `D-15.pdf` y `V-01.pdf` a `V-15.pdf`) correspondientes al corpus final incluido ($N = 30$), donde se detallan los metadatos, evidencia objetiva, topología de comunicación, métricas reportadas, tipos de fallo colectivo, análisis crítico y valoración en escala de 1 a 5.
