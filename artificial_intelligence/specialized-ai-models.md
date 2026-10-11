<h1 align="center">MODELOS DE IA ESPECIALIZADOS</h1>

<p align="center">
Los modelos de inteligencia artificial pueden diseñarse para resolver diferentes tipos de problemas. Algunos se especializan en comprender y generar texto, otros en interpretar imágenes, ejecutar acciones o procesar información de manera eficiente.
Aunque existen muchas arquitecturas de IA, en este apunte estudiaremos ocho modelos o enfoques importantes: LLM, LCM, LAM, MoE, VLM, SLM, MLM y SAM.
</p>

---

## Model Types

| Model | Full Name             | Main Purpose                      |
| :---: | :---:                 | :---:                              |
| LLM   | Large Language Model  | Text generation and understanding |
| LCM   | Large Concept Model   | Concept-level reasoning           |
| LAM   | Large Action Model    | Action execution                  |
| MoE   | Mixture of Experts    | Specialized expert routing        |
| VLM   | Vision-Language Model | Vision + language                 |
| SLM   | Small Language Model  | Lightweight language processing   |
| MLM   | Masked Language Model | Predict masked tokens             |
| SAM   | Segment Anything Model | Image segmentation               |

---

## LLM — Large Language Model
- **¿Qué es?**
    Un LLM es un modelo de inteligencia artificial entrenado con grandes cantidades de datos para comprender y generar lenguaje natural. Puede responder preguntas, redactar textos, resumir documentos, traducir idiomas y generar código de programación.

- **¿Cómo funciona?**
    <div align="center">
        <img src="/imgs/llm.avif" width="250" alt="Modelo LLM" />
    </div>

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

## LCM — Large Concept Model
- **¿Qué es?**
    Un LCM es un enfoque de inteligencia artificial orientado a representar y procesar conceptos o unidades de significado más amplias que los tokens individuales. En lugar de centrarse exclusivamente en la siguiente palabra o token, busca trabajar con representaciones del significado de fragmentos completos de información.

- **¿Cómo funciona?**
    <div align="center">
        <img src="/imgs/lcm.avif" width="250" alt="Modelo LCM" />
    </div>

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

## LAM — Large Action Model
- **¿Qué es?**
    Un LAM es un modelo de inteligencia artificial diseñado para interpretar objetivos y traducirlos en acciones que un sistema puede ejecutar. Mientras que un LLM puede explicar cómo realizar una tarea, un LAM busca participar directamente en su ejecución mediante herramientas, interfaces o sistemas conectados.

- **¿Cómo funciona?**
    <div align="center">
        <img src="/imgs/lam.avif" width="250" alt="Modelo LAM" />
    </div>

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

## MoE — Mixture of Experts
- **¿Qué es?**
    MoE es una arquitectura de redes neuronales que utiliza varios componentes especializados, conocidos como expertos, dentro de un mismo modelo. Un mecanismo denominado router determina qué expertos participan en el procesamiento de una entrada. Su objetivo es aumentar la capacidad del modelo sin tener que activar necesariamente todos sus parámetros para cada entrada.

- **¿Cómo funciona?**
    <div align="center">
        <img src="/imgs/moe.avif" width="250" alt="Modelo MoE" />
    </div>

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

## VLM — Vision-Language Model
- **¿Qué es?**
    Un VLM es un modelo de inteligencia artificial capaz de procesar información visual y relacionarla con el lenguaje natural. Puede analizar fotografías, interpretar gráficos, describir imágenes y responder preguntas sobre su contenido.

- **¿Cómo funciona?**
    <div align="center">
        <img src="/imgs/vlm.avif" width="250" alt="Modelo VLM" />
    </div>

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

## SLM — Small Language Model
- **¿Qué es?**
    Un SLM es un modelo de lenguaje relativamente pequeño en comparación con los grandes modelos de propósito general. Está diseñado para realizar determinadas tareas lingüísticas utilizando menos recursos computacionales, aunque su rendimiento depende del entrenamiento, la arquitectura y la tarea.
- **¿Cómo funciona?**
    <div align="center">
        <img src="/imgs/slm.avif" width="250" alt="Modelo SLM" />
    </div>

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

## MLM — Masked Language Model
- **¿Qué es?**
    Un MLM es un modelo de lenguaje entrenado para predecir tokens ocultos dentro de una secuencia de texto. Durante el entrenamiento, algunos tokens se sustituyen por una máscara o se ocultan de otra manera. El modelo aprende a reconstruirlos utilizando el contexto disponible.

- **¿Cómo funciona?**
    <div align="center">
        <img src="/imgs/mlm.avif" width="250" alt="Modelo MLM" />
    </div>

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

## SAM — Segment Anything Model
- **¿Qué es?**
    SAM es un modelo de visión artificial desarrollado por Meta para segmentar objetos o regiones dentro de una imagen. La segmentación consiste en identificar qué píxeles pertenecen a un objeto o región determinada, en lugar de limitarse a clasificar la imagen completa. SAM permite orientar la segmentación mediante indicaciones, como puntos, cuadros delimitadores o máscaras, dependiendo de la versión.

- **¿Cómo funciona?**
    <div align="center">
        <img src="/imgs/sam.avif" width="250" alt="Modelo SAM" />
    </div>

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