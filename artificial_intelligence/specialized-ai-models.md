<h1 align="center">MODELOS DE IA ESPECIALIZADOS</h1>

<p align="center">
Los modelos de inteligencia artificial pueden diseñarse para resolver diferentes tipos de problemas. Algunos se especializan en comprender y generar texto, otros en interpretar imágenes, ejecutar acciones o procesar información de manera eficiente.
Aunque existen muchas arquitecturas de IA, en este apunte estudiaremos ocho modelos o enfoques importantes: LLM, LCM, LAM, MoE, VLM, SLM, MLM y SAM.
</p>

---

## Model Types

| Model | Full Name              | Main Purpose                      |
| :---: | :---:                  | :---:                             |
| LLM   | Large Language Model   | Text generation and understanding |
| LCM   | Large Concept Model    | Concept-level reasoning           |
| LAM   | Large Action Model     | Action execution                  |
| MoE   | Mixture of Experts     | Specialized expert routing        |
| VLM   | Vision-Language Model  | Vision + language                 |
| SLM   | Small Language Model   | Lightweight language processing   |
| MLM   | Masked Language Model  | Predict masked tokens             |
| SAM   | Segment Anything Model | Image segmentation                |

---

## LLM — Large Language Model (Modelo de Lenguaje de Gran Escala)
- **¿Qué es?**
    Un LLM es un modelo de inteligencia artificial entrenado con grandes cantidades de datos para comprender y generar lenguaje natural. Puede responder preguntas, redactar textos, resumir documentos, traducir idiomas y generar código de programación.

- **¿Cómo funciona?**
    El diagrama muestra cómo un modelo de lenguaje transforma una entrada de texto en una respuesta generada mediante cinco etapas.
    1. **Entrada:** El usuario introduce una pregunta, una instrucción o un texto. Esta información es el punto de partida del procesamiento.
    2. **Tokenización:** El texto se divide en unidades llamadas tokens. Estos pueden representar palabras completas, partes de palabras o caracteres, dependiendo del sistema de tokenización.
    3. **Embedding:** Cada token se transforma en una representación numérica llamada vector. Estas representaciones permiten que la red neuronal procese información lingüística y relaciones entre tokens.
    4. **Transformer:** La arquitectura Transformer procesa las representaciones mediante mecanismos como la atención, que ayudan al modelo a identificar relaciones entre los tokens y utilizar el contexto para calcular qué texto generar.
    5. **Salida (texto generado):** El modelo predice los siguientes tokens y los va generando hasta construir una respuesta. El resultado puede ser una explicación, un resumen, una traducción o código de programación.

    <div align="center">
        <img src="/imgs/llm.avif" width="250" alt="Modelo LLM"/>
    </div>

    - **En resumen:** el texto se convierte en tokens, estos se representan numéricamente, el Transformer los procesa y el modelo genera una respuesta.

- **Características**
    - Comprende y genera texto.
    - Puede trabajar con diferentes idiomas.
    - Puede ayudar a resolver problemas y escribir código.
    - Puede producir información incorrecta, incluso cuando parece convincente.

- **Ejemplos**
    - GPT
    - Claude
    - Gemini
    - Llama

- **Aplicaciones**
    - Asistentes virtuales.
    - Generación de código.
    - Chatbots de atención al cliente.
    - Resumen y análisis de documentos.

- **Ejemplo práctico:** Un desarrollador puede utilizar un LLM para explicar una función de JavaScript, detectar errores en su código o generar una consulta SQL.

<details>
<summary><strong>Concepto clave</strong></summary>
Un LLM se especializa principalmente en procesar y generar lenguaje. No significa que pueda ejecutar automáticamente todas las acciones que describe en sus respuestas.
</details>

---

## LCM — Large Concept Model (Modelo de Conceptos de Gran Escala)
- **¿Qué es?**
    Un LCM es un enfoque de inteligencia artificial orientado a representar y procesar conceptos o unidades de significado más amplias que los tokens individuales. En lugar de centrarse exclusivamente en la siguiente palabra o token, busca trabajar con representaciones del significado de fragmentos completos de información.

- **¿Cómo funciona?**
    El diagrama muestra una representación simplificada del enfoque de Large Concept Model de Meta, que trabaja con secuencias de conceptos en lugar de tratar únicamente con tokens individuales.
    1. **Entrada:** El sistema recibe un texto que utilizará como punto de partida para extraer y procesar información conceptual.
    2. **Segmentación de oraciones:** El texto se divide en oraciones o unidades linguisticas. Esto permite trabajar con fragmentos que expresan ideas, en lugar de procesar exclusivamente palabras aisladas.
    3. **Embedding SONAR:** Las unidades de texto se convierten en vectores mediante SONAR, una familia de modelos y espacios de representación semántica multilingüe y multimodal. Estos vectores representan información relacionada con el significado de las unidades de entrada.
    4. **Difusión:** En el enfoque descrito, un modelo de difusión aprende a predecir o generar secuencias de representaciones conceptuales. Durante la generación, este tipo de modelo parte de representaciones ruidosas y las refina progresivamente.
    5. **Patrones avanzadas:** El modelo aprende patrones y relaciones entre las representaciones conceptuales para producir secuencias coherentes. No es una etapa universal independiente, sino una forma de ilustrar lo que aprende el sistema.
    6. **Proceso oculto:** Representa las operaciones internas del modelo que transforman y refinan las representaciones. El término «proceso oculto» del dibujo no corresponde a una etapa técnica estándar con ese nombre.
    7. **Cuantización:** La cuantización convierte valores continuos en representaciones discretas o reduce la precisión numérica, según la técnica utilizada. Sin embargo, no debe interpretarse como una fase obligatoria de todo LCM; el dibujo es una simplificación.
    8. **Salida (conceptos):** El sistema obtiene una secuencia de representaciones conceptuales generadas. Según el proceso completo, estas pueden convertirse nuevamente en texto u otra forma de salida.

    <div align="center">
        <img src="/imgs/lcm.avif" width="250" alt="Modelo LCM"/>
    </div>

    - **En resumen:** el enfoque representa el texto mediante vectores semánticos, procesa secuencias de conceptos y genera nuevas representaciones que pueden convertirse en contenido comprensible.

> [!NOTE]
> El diagrama no debe interpretarse como un esquema técnico exacto de todas las implementaciones de LCM; combina elementos conceptuales y operaciones que dependen del sistema.

- **Características**
    - Se centra en unidades de significado.
    - Busca representar relaciones semánticas.
    - Puede facilitar el procesamiento de secuencias extensas de información.
    - Su funcionamiento depende de la arquitectura y del entrenamiento utilizados.

- **Ejemplo**
    - Large Concept Model de Meta, una propuesta de investigación orientada a modelar secuencias de conceptos.
    
- **Aplicaciones potenciales**
    - Resumen de documentos extensos.
    - Organización de información.
    - Procesamiento semántico.
    - Generación de contenido a partir de representaciones conceptuales.

- **Ejemplo práctico:** En un sistema que analiza documentación técnica, una representación conceptual podría ayudar a relacionar ideas como autenticación, autorización, sesiones y seguridad.

<details>
<summary><strong>Concepto clave</strong></summary>
Un LCM busca trabajar con representaciones del significado, no solamente con secuencias de tokens. Es una categoría menos consolidada comercialmente que los LLM y sus implementaciones pueden variar.
</details>

---

## LAM — Large Action Model (Modelo de Acción de Gran Escala)
- **¿Qué es?**
    Un LAM es un modelo de inteligencia artificial diseñado para interpretar objetivos y traducirlos en acciones que un sistema puede ejecutar. Mientras que un LLM puede explicar cómo realizar una tarea, un LAM busca participar directamente en su ejecución mediante herramientas, interfaces o sistemas conectados.

- **¿Cómo funciona?**
    El diagrama representa cómo un sistema orientado a acciones interpreta una instrucción, planifica los pasos necesarios y utiliza la retroalimentación para mejorar la ejecución.
    1. **Procesamiento de entrada:** El sistema recibe una instrucción y procesa la información necesaria para comprender qué se le está solicitando.
    2. **Sistema de percepción:** Analiza el contexto disponible para identificar el estado actual del entorno. Puede interpretar información de una interfaz, una aplicación o los resultados de acciones anteriores, según el sistema.
    3. **Reconocimiento de intención:** Determina el objetivo que se desea alcanzar a partir de la instrucción. Por ejemplo, distingue entre consultar los datos de un contacto y registrar uno nuevo.
    4. **Descommposición de tareas:** Divide el objetivo en pasos más pequeños y manejables. Para registrar un contacto, podría identificar la necesidad de abrir el formulario, completar los campos y guardar la información.
    5. **Planificación de acciones:** Organiza los pasos y determina qué acciones deben ejecutarse, en qué orden y qué herramientas o interfaces se necesitan para completar la tarea.
    6. **Sistema de memoria:** Puede conservar información relevante, como el contexto de la tarea, los resultados anteriores o las preferencias necesarias para continuar el proceso.
    7. **Cuantización:** En el diagrama, esta etapa aparece después de la planificación. Sin embargo, técnicamente la cuantización suele ser una técnica para reducir la precisión numérica de los parámetros de un modelo y disminuir su consumo de memoria o cómputo. No es una etapa universal de ejecución de acciones.
    8. **Integración de retroalimentación:** El sistema utiliza los resultados obtenidos para comprobar si las acciones funcionaron. Si algo falla, puede ajustar el plan o intentar otra estrategia.

    <div align="center">
        <img src="/imgs/lam.avif" width="250" alt="Modelo LAM"/>
    </div>

    - **En resumen:** el sistema interpreta un objetivo, analiza su contexto, planifica acciones y utiliza los resultados para comprobar si la tarea se completó correctamente.

> [!NOTE]
> LAM no es una arquitectura única y estandarizada. El diagrama representa un flujo conceptual; no todos los modelos de acción incluyen estas mismas etapas.

- **Características**
    - Orientado a ejecutar tareas.
    - Puede interactuar con herramientas externas.
    - Puede dividir objetivos complejos en pasos.
    - Puede requerir permisos y supervisión para acciones importantes.

- **Ejemplos**
    - Rabbit r1 se presentó como un dispositivo centrado en la interacción con aplicaciones mediante un modelo de acción.
    - Los agentes de IA que utilizan herramientas para realizar tareas son una categoría relacionada, aunque no todos son LAM en sentido estricto.

- **Aplicaciones**
    - Automatización de tareas.
    - Interacción con aplicaciones.
    - Control de interfaces.
    - Ejecución de flujos de trabajo.

- **Ejemplo práctico:** En lugar de limitarse a explicar cómo registrar un contacto, un agente conectado a una aplicación podría abrir un formulario, introducir los datos y guardar el registro.

<details>
<summary><strong>Concepto clave</strong></summary>
Un LAM está orientado a convertir instrucciones en acciones. La ejecución real depende de las herramientas, los permisos y los sistemas a los que tenga acceso.
</details>

---

## MoE — Mixture of Experts (Mezcla de Expertos)
- **¿Qué es?**
    MoE es una arquitectura de redes neuronales que utiliza varios componentes especializados, conocidos como expertos, dentro de un mismo modelo. Un mecanismo denominado router determina qué expertos participan en el procesamiento de una entrada. Su objetivo es aumentar la capacidad del modelo sin tener que activar necesariamente todos sus parámetros para cada entrada.

- **¿Cómo funciona?**
    El diagrama muestra cómo una entrada pasa por un mecanismo de enrutamiento, se dirige a determinados expertos y combina sus resultados.
    1. **Entrada:** El modelo recibe información, como los tokens de una pregunta o una instrucción, que necesita procesar.
    2. **Mecanismos de enrutamiento (Router):** Analiza la representación de la entrada y calcula qué expertos son los más adecuados para procesarla. En muchas implementaciones, este mecanismo asigna puntuaciones a los expertos disponibles.
    3. **Expertos:** Son componentes neuronales que procesan la información mediante parámetros aprendidos. Cada experto puede aprender patrones diferentes, aunque no necesariamente está dedicado a una tarea humana concreta.
    4. **Selección Top-K:** Se seleccionan los *K* expertos que el mecanismo de enrutamiento considera más relevantes para la entrada. Por ejemplo, si *K=2*, se pueden activar dos expertos para procesar un token en esa capa.
    5. **Combinación ponderada:** Los resultados de los expertos seleccionados se combinan utilizando pesos calculados por el mecanismo de enrutamiento. La contribución de cada experto depende de esos pesos.
    6. **Salida:** El resultado combinado continúa hacia las siguientes capas del modelo o contribuye a generar la respuesta final, según la arquitectura.

    <div align="center">
        <img src="/imgs/moe.avif" width="250" alt="Modelo MoE"/>
    </div>

    - **En resumen:** el router selecciona los expertos, los expertos procesan la entrada y sus resultados se combinan para continuar el procesamiento.

> [!NOTE]
> En modelos MoE de lenguaje, la selección suele realizarse por token y por capa, no necesariamente una sola vez para toda la pregunta.

- **Características**
    - Contiene múltiples redes o componentes expertos.
    - Utiliza un mecanismo de selección.
    - Puede activar solamente una parte de sus parámetros en cada paso.
    - Puede mejorar la eficiencia computacional, aunque introduce complejidad de entrenamiento e infraestructura.

- **Ejemplos**
    - Mixtral, de Mistral AI.
    - GPT-4 ha sido objeto de reportes sobre un posible diseño MoE, pero sus detalles arquitectónicos completos no son públicos.

- **Aplicaciones**
    - Modelos de lenguaje de gran capacidad.
    - Sistemas de generación de código.
    - Procesamiento de grandes cantidades de información.
    - Modelos que necesitan combinar diferentes patrones de especialización.

- **Ejemplo práctico:** Imagina un sistema con expertos que aprenden patrones relacionados con programación, matemáticas y lenguaje. El router puede seleccionar los expertos más útiles para procesar una entrada determinada.

Esta analogía ilustra la idea general; los expertos de un MoE real no necesariamente corresponden a disciplinas específicas.

<details>
<summary><strong>Concepto clave</strong></summary>
MoE no es necesariamente un tipo de tarea, sino una arquitectura que combina múltiples expertos mediante un mecanismo de selección.
</details>

---

## VLM — Vision-Language Model (Modelo de Visión y Lenguaje)
- **¿Qué es?**
    Un VLM es un modelo de inteligencia artificial capaz de procesar información visual y relacionarla con el lenguaje natural. Puede analizar fotografías, interpretar gráficos, describir imágenes y responder preguntas sobre su contenido.

- **¿Cómo funciona?**
    El diagrama muestra cómo un modelo de visión y lenguaje procesa una imagen y un texto por separado, relaciona sus representaciones y produce una respuesta conjunta.
    1. **Entrada de imagen:** El sistema recibe una imagen que puede contener objetos, personas, texto, gráficos o escenas que se desean analizar.
    2. **Codificador visual:** Extrae características de la imagen y las convierte en representaciones numéricas que describen su contenido visual.
    3. **Entrada de texto:** Recibe la pregunta o instrucción relacionada con la imagen, por ejemplo: *¿Qué objetos aparecen en esta fotografía?*.
    4. **Codificador de texto:** Transforma la pregunta en una representación numérica que el modelo puede procesar y relacionar con la información visual.
    5. **Interfaz de proyección (alineación):** Adapta las representaciones visuales y textuales para que puedan comunicarse dentro del modelo. La implementación concreta depende de la arquitectura utilizada.
    6. **Procesador multimodal:** Integra la información visual y textual para interpretar la imagen en función de la pregunta. Así puede relacionar los objetos detectados con las palabras del usuario.
    7. **Salida (respuesta):** Genera una respuesta basada en la información combinada. Puede describir la imagen, responder preguntas sobre ella o interpretar determinados elementos visuales.

    <div align="center">
        <img src="/imgs/vlm.avif" width="250" alt="Modelo VLM"/>
    </div>

    - **En resumen:** el VLM procesa la imagen y el texto, relaciona sus representaciones y genera una respuesta que utiliza ambas fuentes de información.

- **Características**
    - Combina visión artificial y lenguaje.
    - Puede interpretar contenido visual.
    - Puede relacionar imágenes con preguntas escritas.
    - Puede cometer errores al interpretar detalles pequeños o imágenes ambiguas.

- **Ejemplos**
    - GPT-4o.
    - LLaVA.
    - Gemini, en sus versiones con capacidades visuales.

- **Aplicaciones**
    - Reconocimiento y descripción de imágenes.
    - Análisis de gráficos y documentos.
    - Asistentes visuales.
    - Interpretación de capturas de pantalla.
    - Apoyo en la revisión de interfaces.

- **Ejemplo práctico:** Puedes proporcionar una captura de una página web y pedirle al modelo que identifique problemas de diseño, explique los elementos de la interfaz o sugiera mejoras en su distribución.

<details>
<summary><strong>Concepto clave</strong></summary>
Un VLM conecta información visual con lenguaje para interpretar imágenes y responder preguntas sobre ellas.
</details>

---

## SLM — Small Language Model (Modelo de Lenguaje Pequeño)
- **¿Qué es?**
    Un SLM es un modelo de lenguaje relativamente pequeño en comparación con los grandes modelos de propósito general. Está diseñado para realizar determinadas tareas lingüísticas utilizando menos recursos computacionales, aunque su rendimiento depende del entrenamiento, la arquitectura y la tarea.
- **¿Cómo funciona?**
    El diagrama representa un flujo de procesamiento parecido al de un LLM, pero orientado a reducir los recursos necesarios para ejecutar el modelo.
    1. **Procesamiento de entrada:** El modelo recibe la pregunta o instrucción y prepara el texto para su procesamiento.
    2. **Tokenización compacta:** El texto se divide en tokens según el tokenizador del modelo. La palabra *compacta* del diagrama es ilustrativa: la tokenización no tiene que ser necesariamente más compacta en todos los SLM.
    3. **Transformer eficiente:** Las capas neuronales procesan los tokens para interpretar el contexto y calcular las respuestas. El modelo puede utilizar una arquitectura o configuración optimizada para reducir el coste computacional.
    4. **Cuantización del modelo:** Los parámetros pueden almacenarse con menor precisión numérica, por ejemplo, utilizando menos bits. Esto puede reducir el consumo de memoria y facilitar la ejecución en equipos con recursos limitados, con posibles compromisos de precisión.
    5. **Optmización de memoria:** Se aplican técnicas para reducir el uso de memoria durante la carga y ejecución del modelo. Algunas optimizaciones también pueden reducir la latencia o el coste de procesamiento.
    6. **Salida (respuesta):** El modelo genera una respuesta a partir de la entrada procesada. Puede ser texto, una clasificación o el resultado de la tarea para la que fue diseñado.

    <div align="center">
        <img src="/imgs/slm.avif" width="250" alt="Modelo SLM"/>
    </div>
    
    - **En resumen:** un SLM procesa texto y genera respuestas utilizando un modelo relativamente pequeño que puede complementarse con técnicas de optimización para ahorrar memoria y cómputo.

> [!NOTE]
> La cuantización y la optimización de memoria son técnicas opcionales; no todos los SLM las utilizan ni siguen exactamente esta secuencia.  

- **Características**
    - Generalmente necesita menos memoria.
    - Puede ejecutarse localmente en computadoras personales o dispositivos compatibles.
    - Puede reducir la latencia y los costes de determinadas aplicaciones.
    - Puede ser más limitado en tareas complejas que los modelos mayores.

- **Ejemplos**
    - Phi-3 Mini.
    - Gemma 2B.
    - Mistral 7B, dependiendo del criterio utilizado para definir un modelo pequeño.

- **Aplicaciones**
    - Asistentes locales.
    - Clasificación de textos.
    - Extracción de información.
    - Chatbots especializados.
    - Aplicaciones que necesitan funcionar con recursos limitados.

- **Ejemplo práctico:** Una aplicación podría utilizar un SLM para clasificar los mensajes de sus usuarios en categorías como consulta, queja o solicitud, sin tener que enviar cada mensaje a un modelo remoto de gran tamaño.

<details>
<summary><strong>Concepto clave</strong></summary>
Un SLM prioriza un equilibrio entre capacidad y eficiencia. Un modelo pequeño no es necesariamente inferior en todas las tareas: puede funcionar muy bien cuando está especializado.
</details>

---

## MLM — Masked Language Model (Modelo de Lenguaje Enmascarado)
- **¿Qué es?**
    Un MLM es un modelo de lenguaje entrenado para predecir tokens ocultos dentro de una secuencia de texto. Durante el entrenamiento, algunos tokens se sustituyen por una máscara o se ocultan de otra manera. El modelo aprende a reconstruirlos utilizando el contexto disponible.

- **¿Cómo funciona?**
    El diagrama representa el proceso de entrenamiento de un modelo que aprende a recuperar tokens ocultos utilizando el contexto de la secuencia completa.
    1. **Entrada de texto:** El modelo recibe una secuencia de texto que servirá como base para aprender relaciones entre palabras y otros tokens.
    2. **Enmascaramiento de tokens:** Durante el entrenamiento, algunos tokens se ocultan o se sustituyen por una máscara. Por ejemplo, *JavaScript es un [MASK]* oculta una palabra que el modelo debe predecir.
    3. **Capa de embedding:** Los tokens visibles y las máscaras se convierten en representaciones numéricas. Estas representaciones sirven como entrada para las capas de la red neuronal.
    4. **Atención bidireccional:** El modelo utiliza el contexto que aparece antes y después de cada posición para interpretar la secuencia. Esto le permite aprovechar las pistas de ambos lados del token oculto.
    5. **Predicción de tokens enmascarados:** El modelo calcula las probabilidades de los posibles tokens que podrían ocupar las posiciones ocultas, basándose en el contexto disponible.
    6. **Salida (tokens predichos):** Se obtienen las predicciones para los tokens ocultos. Durante el entrenamiento, estas predicciones se comparan con los tokens originales para ajustar los parámetros del modelo.

    <div align="center">
        <img src="/imgs/mlm.avif" width="250" alt="Modelo MLM"/>
    </div>

    - **En resumen:** se ocultan algunos tokens, el modelo analiza el contexto de ambos lados y predice cuáles deberían ocupar las posiciones enmascaradas.

> [!NOTE]
> Este diagrama describe principalmente el entrenamiento de un MLM. En modelos como BERT, la salida habitual para una tarea posterior puede ser una clasificación u otra predicción, no necesariamente un texto reconstruido.

- **Características**
    - Aprende a partir del contexto de una secuencia.
    - Puede utilizar información anterior y posterior al token oculto.
    - Es útil para aprender representaciones lingüísticas.
    - Su objetivo de entrenamiento es diferente del habitual en los modelos autorregresivos que predicen el siguiente token.

- **Ejemplos**
    - BERT.
    - RoBERTa.
    - ALBERT.

- **Aplicaciones**
    - Clasificación de textos.
    - Análisis de sentimientos.
    - Reconocimiento de entidades.
    - Búsqueda semántica.
    - Comprensión de documentos.

- **Ejemplo práctico:** Un sistema de análisis de comentarios puede utilizar representaciones aprendidas por un modelo como BERT para identificar si un mensaje expresa una opinión positiva o negativa.

<details>
<summary><strong>Concepto clave</strong></summary>
Un MLM aprende a predecir tokens ocultos utilizando el contexto de ambos lados. BERT es uno de sus ejemplos más conocidos.
</details>

---

## SAM — Segment Anything Model (Modelo de Segmentación de Cualquier Elemento)
- **¿Qué es?**
    SAM es un modelo de visión artificial desarrollado por Meta para segmentar objetos o regiones dentro de una imagen. La segmentación consiste en identificar qué píxeles pertenecen a un objeto o región determinada, en lugar de limitarse a clasificar la imagen completa. SAM permite orientar la segmentación mediante indicaciones, como puntos, cuadros delimitadores o máscaras, dependiendo de la versión.

- **¿Cómo funciona?**
    El diagrama muestra cómo SAM combina una imagen con una indicación para generar una máscara que delimita un objeto o una región.
    1. **Entrada de prompt:** El usuario proporciona una indicación para señalar qué desea segmentar. Puede ser un punto, un cuadro delimitador u otra entrada compatible con la versión del modelo.
    2. **Entrada de imagen:** Se proporciona la imagen que contiene el objeto o la región que se desea identificar.
    3. **Codificador de prompt:** Convierte la indicación del usuario en una representación numérica que el modelo puede utilizar para determinar qué región debe segmentar.
    4. **Codificador de imagen:** Procesa la imagen y extrae características visuales que ayudan a distinguir objetos, formas, bordes y otras estructuras.
    5. **Generación de embeddings:** Las características de la imagen y la información de la indicación se utilizan conjuntamente para orientar la segmentación hacia el objeto solicitado.
    6. **Decodificador de máscara:** Combina las representaciones procesadas para calcular una máscara de segmentación, identificando qué píxeles pertenecen a la región seleccionada.
    7. **Salida (máscara de segmentación):** El modelo genera una máscara que delimita el objeto o la región identificada. Esta máscara puede utilizarse para separar objetos, editar imágenes o preparar datos para otros sistemas.

    <div align="center">
        <img src="/imgs/sam.avif" width="250" alt="Modelo SAM"/>
    </div>

    - **En resumen:** SAM recibe una imagen y una indicación, procesa ambas y genera una máscara que identifica los píxeles correspondientes al objeto solicitado.

> [!NOTE]
> El diagrama simplifica el funcionamiento interno de SAM, los componentes exactos dependen de la versión.

- **Características**
    - Segmenta regiones a nivel de píxel.
    - Puede utilizar indicaciones visuales para orientar el resultado.
    - Está diseñado para generalizar a distintos tipos de objetos.
    - No garantiza una segmentación perfecta en todas las imágenes.

- **Ejemplo**
    - Segment Anything Model (SAM), de Meta.
    - SAM 2 amplía las capacidades de segmentación a imágenes y vídeos.

- **Aplicaciones**
    - Edición de imágenes.
    - Análisis de imágenes médicas, sujeto a validación especializada.
    - Robótica y percepción visual.
    - Preparación de conjuntos de datos.
    - Identificación de objetos en imágenes.

- **Ejemplo práctico:** Si tienes una fotografía de un automóvil estacionado en una calle, puedes indicar el automóvil mediante un punto o un cuadro y obtener una máscara que delimite su silueta.

<details>
<summary><strong>Concepto clave</strong></summary>
SAM se especializa en la segmentación visual: identifica qué píxeles pertenecen a una región u objeto determinado.
</details>

---

## ¿Cómo se relacionan con el desarrollo de software?
| Proyecto                           | Modelo o enfoque útil                                             | Ejemplo de uso                                              |
| :---:                              | :---:                                                             | :---:                                                       |
| Chatbot para una página web        | LLM                                                               | Responder preguntas de los usuarios.                        |
| Asistente para ejecutar tareas     | LAM o agente con herramientas                                     | Automatizar operaciones dentro de una aplicación.           |
| Aplicación de análisis de imágenes | VLM                                                               | Describir imágenes o interpretar capturas.                  |
| Clasificador de comentarios        | MLM o modelo de lenguaje especializado                            | Clasificar mensajes por categoría o sentimiento.            |
| Aplicación de IA local             | SLM                                                               | Procesar textos sin depender siempre de un servicio remoto. |
| Editor inteligente de fotografías  | SAM                                                               | Seleccionar objetos y eliminar sus fondos.                  |
| Plataforma de análisis semántico   | LCM                                                               | Experimentar con representaciones conceptuales.             |
| Sistema de IA de gran capacidad    | MoE                                                               | Aprovechar expertos seleccionados según la entrada.         |

> [!IMPORTANT]
> Estas son aplicaciones posibles, no correspondencias exclusivas. Un mismo proyecto puede combinar varios modelos y técnicas.

---

## Diferencias importantes
Para comprender mejor sus diferencias, conviene recordar que no todos estos modelos pertenecen a la misma categoría conceptual:
- **LLM** y **SLM:** Se distinguen principalmente por el tamaño y los recursos necesarios, aunque no existe un límite universal que separe ambas categorías.
- **LCM** y **MLM:** Se relacionan con formas diferentes de representar o aprender información lingüística.
- **LAM:** Se centra en la ejecución de acciones, no solamente en producir respuestas.
- **MoE:** Es una arquitectura que puede utilizarse dentro de modelos de lenguaje y otros sistemas.
- **VLM** y **SAM:** Trabajan con información visual, pero tienen objetivos diferentes: relacionar imágenes con lenguaje y segmentar regiones, respectivamente.

---

## En resumen
Los modelos de IA especializados representan diferentes maneras de abordar problemas computacionales. Mientras algunos se centran en el lenguaje, otros procesan conceptos, interpretan imágenes, segmentan objetos o ejecutan acciones. Por su parte, arquitecturas como MoE permiten organizar el procesamiento mediante componentes especializados.
**La idea fundamental es que no existe un único modelo ideal para todas las tareas:** la elección depende del problema, los datos disponibles, los recursos computacionales y los requisitos de la aplicación.