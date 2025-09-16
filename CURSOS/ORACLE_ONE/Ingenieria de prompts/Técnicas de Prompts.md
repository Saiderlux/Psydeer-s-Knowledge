En el contexto de la inteligencia artificial y los [[LLM's]], **Zero-Shot** y **Few-Shot** prompts son técnicas de **ingeniería de prompts** que determinan la cantidad de ejemplos que le proporcionas a un modelo de lenguaje para que realice una tarea.

---

### Zero-Shot Prompts (Sin ejemplos) 📉

Esta es la técnica más simple. Se le da al modelo una instrucción directa, sin proporcionar ejemplos de la tarea que debe realizar. El modelo utiliza su conocimiento general y el vasto conjunto de datos con el que fue entrenado para generar una respuesta.

- **¿Cómo funciona?** Le pides a la IA que haga algo basándose únicamente en su entrenamiento previo. No le das ningún ejemplo de cómo debe ser la respuesta.
    
- **Ejemplo:** "Clasifica el siguiente comentario como positivo, negativo o neutral: 'El servicio al cliente fue muy lento, pero la comida era excelente.'"
    
- **Uso:** Ideal para tareas sencillas o cuando buscas respuestas rápidas y directas, como preguntas de conocimiento general, resúmenes o ideas.
    

---

### Few-Shot Prompts (Con pocos ejemplos) 📈

En esta técnica, le das al modelo un pequeño número de ejemplos de pares de entrada y salida (input-output) para guiarlo. Esto ayuda a la IA a entender el formato, el estilo o el tipo de respuesta que esperas.

- **¿Cómo funciona?** Le muestras a la IA un patrón para que lo siga. Los ejemplos actúan como un "mini-entrenamiento" dentro del mismo prompt. A menudo, se incluyen 2 o más ejemplos. Si solo incluyes uno, se conoce como **One-Shot Prompting**.
    
- **Ejemplo:**
    
    - _Input:_ "Una manzana es una fruta. Un brócoli es una verdura."
        
    - _Prompt:_ "Un perro es un __________."
        
    - El modelo, al ver el patrón, probablemente respondería "mamífero".
        
- **Uso:** Es muy útil para tareas que requieren un formato o estilo específico, como análisis de sentimiento en un contexto particular, la generación de descripciones de productos, o la resolución de problemas lógicos. Permite una mayor precisión y control sobre la respuesta final.