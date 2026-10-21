# Protocolo de Revisión Sistemática de Literatura

**Título:** Evaluación sistemática de técnicas de observabilidad y atribución causal para la detección de fallos colectivos en sistemas multiagente basados en modelos de lenguaje de gran escala (LLM-MAS)

---

## 1. Question Formularization

### 1.1. Question Focus

El enfoque de la revisión sistemática corresponde a identificar y evaluar las técnicas actuales de observabilidad del proceso colaborativo, los métodos de atribución causal del aporte individual de agentes, y los mecanismos de detección de fallos colectivos en sistemas multiagente basados en modelos de lenguaje de gran escala (LLM-MAS). Se busca determinar en qué medida estas técnicas permiten auditar el flujo de información entre agentes y distinguir fallos perjudiciales de fenómenos de inteligencia colectiva beneficiosa.

### 1.2. Question Quality and Amplitude

* **Problem:** Los sistemas multiagente basados en modelos de lenguaje de gran escala (LLM-MAS) han emergido como paradigma para abordar tareas complejas mediante la colaboración entre múltiples agentes autónomos. No obstante, la comunidad ha desarrollado estos sistemas a un ritmo mucho mayor que las metodologías para evaluarlos: las prácticas actuales se apoyan casi exclusivamente en el *output* final, sin abordar el proceso colaborativo intermedio que da origen a ese resultado. Como consecuencia, los fallos que emergen de la interacción entre agentes resultan difíciles de identificar y la auditabilidad de los LLM-MAS en contextos de despliegue real se ve seriamente limitada.
* **Question:**
  * **PI1:** ¿Qué técnicas de observabilidad y métricas de proceso colaborativo se han propuesto en sistemas LLM-MAS para hacer visible el proceso interno entre agentes más allá del *output* final?
  * **PI2:** ¿Qué métodos de atribución causal se han propuesto para identificar el aporte individual de agentes, mensajes, memorias o *prompts* al resultado colectivo en sistemas LLM-MAS, y cómo varía su aplicabilidad según la topología de comunicación empleada?
  * **PI3:** ¿Cómo se aplican las técnicas de observabilidad y atribución causal para detectar fallos colectivos en sistemas LLM-MAS (como cascadas de alucinación, colusión emergente, deriva epistémica o engaño sistémico), y en qué medida permiten distinguir entre fallo perjudicial e inteligencia colectiva beneficiosa?
* **Keywords:** LLM-based multi-agent systems, LLM-MAS, multi-agent LLM, large language model agents, observability, process tracing, logging, provenance, process evaluation, process-level metrics, causal attribution, influence tracing, ablation analysis, message attribution, agent attribution, communication topology, collective failure, failure detection, error propagation, hallucination cascade, emergent collusion, epistemic drift, systemic deception.
* **Intervention:** Identificación y comparación de técnicas de observabilidad, métodos de atribución causal y mecanismos de detección de fallos colectivos en sistemas multiagente basados en LLM, analizando su comportamiento bajo distintas topologías de comunicación y unidades de atribución, así como su capacidad para identificar distintas categorías de fallo colectivo.
* **Control:** Establecimiento de una línea base de comparación utilizando métricas convencionales de evaluación orientadas al *output* final (*task success rate*, *accuracy*, *exact match*), así como sistemas LLM-MAS que operan como cajas negras sin instrumentación del proceso colaborativo interno.
* **Effect:** Incremento medible en la observabilidad del proceso colaborativo interno, mejora en la atribución causal del aporte individual de componentes al resultado colectivo, y aumento en la sensibilidad de detección de fallos colectivos respecto a las evaluaciones basadas exclusivamente en el *output* final.
* **Outcome Measure:** Análisis cuantitativo mediante métricas de proceso colaborativo, atribución causal y detección de fallos colectivos reportadas en los estudios primarios, tales como *coordination efficiency*, *attribution accuracy*, *detection rate*, *false positive rate* y *consistency score*, contrastadas con métricas de *output* final (*task success rate*, *accuracy*).
* **Population:** Sistemas multiagente basados en modelos de lenguaje de gran escala (LLM-MAS) compuestos por dos o más agentes generativos que interactúan mediante comunicación estructurada para lograr una resolución colaborativa, simulación de entornos o evaluación de agentes.
* **Application:** Investigadores y desarrolladores de sistemas multiagente basados en LLM, equipos de ingeniería que despliegan sistemas colaborativos en producción, y auditores de sistemas de inteligencia artificial responsables de evaluar la confiabilidad y trazabilidad de procesos colaborativos automatizados.
* **Experimental Design:** Implementación de análisis estadísticos descriptivos detallados sobre frecuencias y distribuciones porcentuales de las técnicas de observabilidad, métodos de atribución causal y mecanismos de detección de fallos colectivos reportados en los estudios primarios.

---

## 2. Sources Selection

### 2.1. Studies Selection Criteria Definition

Con el objetivo de mantener estándares rigurosos de calidad en los estudios primarios incluidos, las fuentes bibliográficas deberán ajustarse a los criterios mencionados a continuación:

* **Disponibilidad y Accesibilidad:** Los repositorios seleccionados deben formar parte de la red de acceso institucional disponible para el investigador o estar publicados bajo licencias de acceso abierto (*Open Access*), asegurando la descarga completa de los manuscritos sin restricciones de suscripción.
* **Funcionalidad de Consulta:** Las plataformas bibliográficas deben admitir la construcción de consultas con operadores booleanos (`AND`, `OR`, `NOT`), filtrado por metadatos (año, autor, tipo de publicación, indexación) y exportación estructurada de resultados, condiciones necesarias para ejecutar la *Search String* definida en este protocolo sin limitaciones técnicas.
* **Lenguaje de estudios:** La revisión se restringe al idioma inglés, dado que constituye la lengua predominante en la publicación de investigación sobre sistemas multiagente basados en modelos de lenguaje de gran escala y en el desarrollo de sus sistemas de referencia (MetaGPT, AutoGen, CAMEL, entre otros), lo que asegura la cobertura exhaustiva de los estudios más relevantes del campo.

### 2.2. Sources Identification

| Repositorio / Herramienta | Metodología de Uso | Justificación de su Selección Científica |
| :--- | :--- | :--- |
| **Web of Science (WoS)** | Búsqueda Especializada Principal | Constituye una de las bases de datos de referencia obligatoria para investigación científica indexada, ofreciendo cobertura en ciencias de la computación, inteligencia artificial y sistemas multiagente con estándares rigurosos de revisión por pares. |
| **Scopus** | Búsqueda Multidisciplinar Principal | Provee amplia cobertura y filtrado avanzado por citaciones, indexación y áreas temáticas, permitiendo identificar estudios relevantes publicados en conferencias y revistas de alto impacto del campo LLM-MAS. |
| **IEEE Xplore** | Búsqueda Técnica | Provee acceso a la literatura más rigurosa sobre arquitecturas distribuidas, sistemas multiagente e ingeniería de software aplicada a inteligencia artificial. |
| **Google Scholar** | Exploración General | Actúa como red de seguridad para identificar literatura científica transversal que podría no estar indexada en repositorios altamente especializados. |
| **Consensus / Research Rabbit** | Asistencia IA | Estas herramientas de última generación facilitan el descubrimiento de literatura basada en la similitud semántica, permitiendo encontrar estudios que no comparten las mismas palabras clave pero sí el mismo objeto de estudio. |
| **Connected Papers** | Mapeo Relacional | Se utiliza para validar que no se han omitido "estudios seminales" mediante la visualización de grafos de citación y artículos conectados por contexto. |

* **Cadena de Búsqueda Formalizada (*Search String*):**
  ```text
  ("LLM-MAS" OR "LLM-based multi-agent" OR "multi-agent LLM") AND ("observability" OR "tracing" OR "provenance" OR "causal attribution") AND ("collective failure" OR "hallucination cascade" OR "emergent collusion" OR "epistemic drift" OR "systemic deception")
  ```

---

## 3. Studies Selection

### 3.1. Studies Definition

A fin de asegurar que la revisión sistemática se sustente en evidencia científicamente robusta y de alta calidad metodológica, se definen los siguientes criterios:

#### Criterios de Inclusión (CI):
1. **CI1 — Vigencia Temporal:** Se considerarán publicaciones realizadas entre 2021 y 2026, correspondiendo a la ventana temporal de consolidación del campo de sistemas multiagente basados en modelos de lenguaje de gran escala (LLM-MAS), período que garantiza la pertinencia de los métodos evaluados respecto a las arquitecturas y capacidades actuales de los LLMs.
2. **CI2 — Calidad de Publicación:** Se incluirán únicamente artículos publicados en conferencias y revistas revisadas por pares indexadas en Web of Science (WoS) o Scopus, lo que asegura el cumplimiento de estándares rigurosos de revisión y calidad académica reconocida en la comunidad científica.
3. **CI3 — Relevancia Académica:** El estudio deberá contar con al menos 5 citaciones académicas que respalden su impacto en la comunidad científica. Para publicaciones aparecidas en los últimos 12 meses, se aceptará un mínimo de 2 citaciones, considerando el ciclo propio de acumulación de referencias en un campo de evolución acelerada.
4. **CI4 — Rigor Metodológico:** Se considerarán estudios que presenten una descripción clara y estructurada de la metodología propuesta, incluyendo el diseño de la técnica, los supuestos teóricos y, cuando corresponda, ejemplos ilustrativos, casos de uso o validación experimental parcial. No se exige validación empírica completa sobre sistemas LLM-MAS reales, dado que gran parte de la investigación del área aún se desarrolla sobre prototipos, simulaciones o propuestas conceptuales en etapas tempranas.

#### Criterios de Exclusión (CE):
1. **CE1:** Estudios centrados exclusivamente en sistemas de un solo agente (*single-agent LLM*) o en técnicas generales de evaluación de modelos de lenguaje sin considerar la dimensión colaborativa entre múltiples agentes.
2. **CE2:** Propuestas orientadas únicamente a arquitecturas multiagente clásicas (MARL, BDI, agentes reactivos) que no incorporen modelos de lenguaje de gran escala como núcleo de razonamiento.
3. **CE3:** Publicaciones que aborden observabilidad, trazabilidad o auditoría de sistemas de IA exclusivamente desde una perspectiva normativa, ética, filosófica o regulatoria, sin proponer ni discutir mecanismos técnicos, arquitecturas o aproximaciones metodológicas vinculadas al diseño de sistemas LLM-MAS.
4. **CE4:** Artículos de opinión, editoriales o revisiones narrativas que no aporten datos experimentales nuevos, metodologías originales de evaluación o hallazgos empíricos verificables sobre sistemas LLM-MAS.

### 3.2. Procedures for Studies Selection

El procedimiento se organiza de manera secuencial con el fin de maximizar la eficiencia del trabajo investigativo y asegurar la trazabilidad metodológica de la muestra final:

1. **Formalización del Protocolo:** Consolidación del presente documento como marco metodológico de referencia, fijando de antemano las decisiones de búsqueda, selección y análisis que regirán toda la revisión.
2. **Ejecución de Consultas:** Aplicación de la *Search String* formalizada sobre cada uno de los repositorios bibliográficos definidos en la sección de *Sources Identification*, con las adaptaciones sintácticas necesarias según los operadores soportados por cada plataforma.
3. **Gestión de Metadatos:** Almacenamiento sistemático de los resultados recuperados en una matriz estructurada (hoja de cálculo electrónica), registrando campos como autor, año, *venue*, DOI, citaciones y resumen para asegurar la trazabilidad de cada estudio candidato.
4. **Filtrado por Elegibilidad:** Aplicación automatizada y manual de los criterios de inclusión y exclusión definidos previamente sobre los metadatos recolectados, considerando año de publicación, indexación en WoS/Scopus, citaciones y tipo de estudio.
5. **Evaluación de Pertinencia Temática:** Lectura crítica de títulos, resúmenes y conclusiones con el fin de determinar la alineación efectiva de cada estudio respecto a las preguntas de investigación, reduciendo la muestra a un conjunto final de entre 30 y 50 estudios primarios.
6. **Extracción de Datos Técnicos:** Construcción de tablas de síntesis que documenten, para cada estudio seleccionado, la técnica propuesta, el sistema LLM-MAS evaluado, la topología de comunicación empleada, las métricas reportadas y los tipos de fallo colectivo considerados.
7. **Síntesis y Análisis Estadístico:** Aplicación de los métodos de análisis descriptivo previamente definidos en el *Experimental Design*, con el fin de identificar patrones, tendencias y relaciones entre variables extraídas del corpus.
8. **Redacción de Resultados:** Elaboración del informe final asegurando la comunicación clara y rigurosa de los hallazgos a la comunidad científica.

---

## 4. Information Extraction

Una vez seleccionados los estudios primarios, se inicia la extracción sistemática de la información relevante. Para garantizar la homogeneidad, la trazabilidad y la replicabilidad de este proceso, la extracción se operacionaliza mediante una **Ficha de Extracción de Información** estandarizada, diseñada conforme al *template* de Mian et al. (2005) y a las directrices PRISMA. Cada estudio primario incluido en la revisión es documentado en una ficha individual e identificada unívocamente (campo *ID Hoja*), de modo que el conjunto de fichas constituye el corpus estructurado sobre el cual se ejecutará posteriormente el análisis estadístico descriptivo definido en el *Experimental Design*. En esta sección se describen los criterios que rigen qué información se extrae, la estructura del formulario, el procedimiento de llenado y el mecanismo de resolución de divergencias entre revisores.

### 4.1. Information Inclusion and Exclusion Criteria Definition

A diferencia de los criterios de la Sección 3 (que determinan qué *estudios* ingresan a la revisión), los siguientes criterios determinan qué **información interna de cada estudio ya seleccionado** resulta pertinente consignar en la ficha, evitando el registro de datos redundantes o ajenos a los objetivos de la revisión.

#### Criterios de inclusión de información:
* Información que responda de manera directa a alguna de las preguntas de investigación: técnicas de observabilidad y métricas de proceso colaborativo (PI1), métodos de atribución causal y la unidad de atribución empleada (agente, mensaje, memoria o *prompt*) (PI2), o mecanismos de detección de fallos colectivos (PI3).
* Caracterización técnica de la propuesta: sistema LLM-MAS evaluado, topología de comunicación, supuestos teóricos y tipo de validación reportada.
* Métricas cuantitativas asociadas al proceso colaborativo (p. ej., *coordination efficiency*, *attribution accuracy*, *detection rate*, *false positive rate*, *consistency score*) y, cuando se reporten como línea base, las métricas de *output* final (*task success rate*, *accuracy*, *exact match*).
* Categorías de fallo colectivo consideradas (cascada de alucinación, colusión emergente, deriva epistémica, engaño sistémico).

#### Criterios de exclusión de información:
* Datos orientados exclusivamente al *output* final que no se vinculen con el proceso colaborativo intermedio ni cumplan función de control comparativo.
* Detalles de implementación (hiperparámetros, infraestructura de cómputo, costos de *tokens*) sin relación con las preguntas de investigación.
* Información redundante ya consignada desde una fuente equivalente del mismo estudio.
* Afirmaciones cualitativas no respaldadas por evidencia, ejemplos ilustrativos o validación, según el criterio de rigor metodológico ya establecido.

### 4.2. Data Extraction Forms

El instrumento de extracción es la **Ficha de Extracción de Información**, organizada en cuatro bloques que estandarizan la representación de cada estudio:

* **a) Identificación y clasificación del estudio:** referencia bibliográfica completa, ID de hoja, año, tipo de estudio, base de datos de origen e indexación (WoS/Scopus).
* **b) Ejecución y resultados objetivos (evidencia):** objetivo o intención, problema/brecha abordada, metodología, población/ámbito e intervención o propuesta.
* **c) Análisis crítico y conclusiones (subjetivo):** valoración del investigador, limitaciones y sesgos, conclusión de los autores e impresión del revisor (escala de 1 a 5).
* **d) Observaciones generales y notas:** apreciaciones transversales relevantes que no encajan en los campos anteriores.

Cada ficha se vincula con la hoja de cálculo electrónica de metadatos descrita en la Sección 3.2 a través del campo *ID Hoja*, de modo que sus campos puedan ser agregados y tabulados para el análisis cuantitativo posterior.

### 4.3. Extraction Execution

El llenado de la ficha distingue dos tipos de resultados: objetivos y subjetivos.

* **Resultados objetivos (Bloques 1 y 2 de la ficha):** Corresponden a la información que puede extraerse directamente del texto de los estudios y se organiza como sigue:
  * **i) Identificación del estudio:** título de la publicación, autores y fuente o *venue* del que fue obtenido (Bloque 1).
  * **ii) Metodología del estudio:** objetivo, descripción de la metodología, población/ámbito e intervención o propuesta, incluyendo la topología de comunicación y el procedimiento de validación (Bloque 2).
  * **iii) Resultados del estudio:** efecto obtenido, expresado mediante las métricas de proceso, atribución o detección reportadas, contrastadas cuando corresponda con la línea base de *output* final (Bloque 2).
  * **iv) Problemas del estudio:** limitaciones reconocidas por los propios autores (campo *Limitaciones/Sesgos*).
* **Resultados subjetivos (Bloque 3 de la ficha):** Corresponden a la información que no puede extraerse directamente y se obtiene por dos vías:
  * **i) Información a través de los autores:** ante ambigüedades o datos faltantes, se contacta a los autores de los estudios para solicitar aclaraciones o detalles adicionales.
  * **ii) Impresiones generales y abstracciones:** los revisores formulan conclusiones propias tras la lectura crítica de cada estudio, en particular respecto de la madurez de la técnica y su aplicabilidad para auditar fallos colectivos en escenarios de despliegue real (campos *Valoración del Investigador*, *Impresión del Revisor* y *Observaciones Generales*).

### 4.4. Resolution of divergences among reviewers

Con el fin de optimizar el esfuerzo investigativo, la extracción de información se distribuye en partes iguales entre los dos revisores responsables de esta revisión, de modo que cada uno elabora la ficha de un subconjunto de los estudios primarios seleccionados (15 estudios cada uno). No obstante, para resguardar la objetividad y la consistencia del proceso, una submuestra de las fichas elaboradas por cada revisor es sometida a una revisión cruzada por parte del otro revisor, quien contrasta de forma independiente la información consignada frente al texto original del estudio.

Cuando esta verificación cruzada revela discrepancias (ya sea en la clasificación de la técnica propuesta, en la pregunta de investigación asociada o en la interpretación de las métricas reportadas) dichas divergencias deben registrarse explícitamente. Su resolución se realiza mediante discusión razonada entre ambos revisores hasta alcanzar un consenso; de persistir el desacuerdo, se recurre a la relectura conjunta del texto completo del estudio como criterio dirimente. El acuerdo final queda consignado en la ficha respectiva, asegurando que la extracción no quede sesgada por el juicio individual de un único revisor y preservando la replicabilidad del proceso.
