**Self-Consistency (Autoconsistencia)** es una técnica de **ingeniería de prompts** que mejora la precisión de las respuestas de los [[LLM's]], especialmente en tareas de razonamiento complejo. En lugar de confiar en una sola respuesta, el modelo genera múltiples respuestas diferentes y luego elige la que es más consistente entre todas.

---

### ¿Cómo funciona la autoconsistencia?

El proceso se basa en tres pasos principales:

1. **Generación de respuestas diversas:** Se le pide al modelo de lenguaje que genere varias respuestas diferentes para la misma pregunta, a menudo usando una técnica de muestreo. Esto anima al modelo a explorar múltiples caminos de razonamiento.
    
2. **Selección de la respuesta mayoritaria:** Se analizan todas las respuestas generadas. La respuesta final se elige basándose en un "voto de mayoría" o por la solución que es más coherente y se repite en la mayoría de las respuestas.
    
3. **Filtrado del resultado final:** Se presenta al usuario la respuesta que fue seleccionada por ser la más consistente, lo que aumenta la confianza en su veracidad.
    

---

### ¿Cuál es la diferencia con Chain-of-Thought (CoT)?

Mientras que **Chain-of-Thought** se enfoca en que el modelo muestre un solo camino de razonamiento, **Self-Consistency** utiliza múltiples caminos.

- **CoT:** Pide al modelo que "piense en voz alta" y siga una lógica paso a paso para llegar a una única respuesta. El modelo puede cometer un error en un paso inicial, lo que afectaría toda la cadena.
    
- **Self-Consistency:** Reconoce que el primer "pensamiento" del modelo no siempre es el correcto. Al generar varias respuestas y ver cuál es la que más se repite, reduce la posibilidad de un error inicial. Es como si el modelo estuviera "autoconsultando" a varias de sus propias "personalidades" para llegar a la mejor conclusión.
    

### Ejemplo práctico

Imagina que le preguntas a un modelo: **"¿Si 5 es el 25% de un número, cuál es ese número?"**

- **Sin Self-Consistency:** El modelo podría dar una respuesta incorrecta de inmediato, como "1.25".
    
- **Con Self-Consistency:**
    
    - **Respuesta 1:** "Si 5 es el 25%, entonces 100% es 5 * 4 = 20."
        
    - **Respuesta 2:** "El 25% se puede escribir como 0.25. La ecuación es 0.25 * x = 5. Entonces x = 5 / 0.25 = 20."
        
    - **Respuesta 3:** "El 25% es un cuarto. Un cuarto del número es 5, así que el número completo es 4 * 5 = 20."
        
    - **Resultado:** Como la mayoría de las respuestas (en este caso, todas) llegan a 20, el modelo concluirá que 20 es la respuesta correcta, lo que le da una mayor confianza en el resultado.