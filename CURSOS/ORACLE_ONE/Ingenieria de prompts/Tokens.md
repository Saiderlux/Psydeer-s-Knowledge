En el contexto de la inteligencia artificial, un **token** es la unidad fundamental de datos que un modelo de IA procesa para entender y generar lenguaje. Es el resultado de la **tokenización**, que es el proceso de dividir un texto en fragmentos más pequeños, conocidos como tokens.

---

### ¿Cómo funciona la tokenización?

Antes de que un modelo de lenguaje grande ([[LLM's]], por sus siglas en inglés) como GPT o Gemini pueda analizar y responder a una solicitud, el texto de entrada se descompone en tokens. Estos tokens pueden variar en tamaño, desde una palabra completa, un signo de puntuación, hasta una sub-palabra o un carácter individual.

Por ejemplo, la frase "El perro juega" podría ser tokenizada de varias maneras:

- **Tokenización por palabras:** ["El", "perro", "juega"]
    
- **Tokenización por sub-palabras:** ["El", "perro", "jue", "ga"]
    

La elección del método de tokenización puede influir en la eficiencia y el rendimiento del modelo. Los modelos modernos, como los basados en la arquitectura Transformer, a menudo utilizan la tokenización por sub-palabras para manejar palabras nuevas o poco comunes de manera más efectiva.

### La importancia de los tokens

El uso de tokens es crucial por varias razones:

- **Eficiencia:** Permite que los modelos procesen grandes volúmenes de texto de manera más rápida y precisa.
    
- **Contexto:** Al descomponer el texto en unidades manejables, los modelos pueden comprender mejor el contexto y las relaciones entre las palabras.
    
- **Coste:** En muchos modelos de IA, el coste de procesamiento se basa en el número de tokens utilizados tanto en la entrada como en la salida.
    
- **Límites de contexto:** Los modelos tienen un límite máximo de tokens que pueden procesar a la vez. Este límite define la "[[Ventana de contexto]]" del modelo, es decir, cuánta información puede "recordar" para generar una respuesta coherente.