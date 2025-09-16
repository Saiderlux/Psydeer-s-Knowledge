En el contexto de los [[LLM's]], la **temperatura** es un parámetro de configuración que controla la aleatoriedad de las respuestas del modelo. Es un valor numérico, típicamente entre 0 y 1, que influye en cómo el modelo elige la siguiente palabra en la secuencia.

---

### ¿Cómo afecta la salida del modelo?

La temperatura determina el nivel de creatividad o predictibilidad de la respuesta. Para entenderlo, piensa en el modelo calculando la probabilidad de cada palabra en su vocabulario para continuar una frase.

- **Temperatura Baja (cerca de 0)**: El modelo se vuelve más **conservador y determinista**. Tiende a elegir la palabra con la probabilidad más alta. Esto produce respuestas más seguras, coherentes y predecibles. Es ideal para tareas que requieren precisión, como resúmenes, traducciones o respuestas a preguntas factuales.
    
- **Temperatura Alta (cerca de 1)**: El modelo se vuelve más **creativo y aleatorio**. Aumenta la probabilidad de que se elijan palabras con una probabilidad más baja, suavizando la distribución. Esto produce respuestas más diversas, originales y, a veces, impredecibles. Es útil para tareas creativas como la generación de poesía, narrativas o ideas innovadoras.