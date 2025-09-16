En el contexto de la inteligencia artificial y los [[LLM's]], **Chain-of-Thought (CoT)**, o **cadena de pensamiento**, es una técnica de **ingeniería de prompts** que instruye a un modelo de lenguaje para que **muestre los pasos intermedios de su razonamiento** antes de llegar a la respuesta final. 🧠 Esto hace que el proceso de resolución de problemas sea más transparente y preciso.

---

### ¿Cómo funciona el Chain-of-Thought?

En lugar de pedirle al modelo que dé la respuesta de golpe, CoT le pide que "piense en voz alta". Esto se logra añadiendo frases como "Pensemos paso a paso" o proporcionando ejemplos que incluyan la secuencia de razonamiento.

- **Sin CoT:**
    
    - **Prompt:** "¿El 17 es un número primo? Explica."
        
    - **Respuesta (posible):** "Sí, el 17 es un número primo porque solo es divisible por 1 y por sí mismo." (La respuesta es correcta, pero el modelo no muestra su proceso mental).
        
- **Con CoT:**
    
    - **Prompt:** "El 13 es un número primo porque sus únicos divisores son 1 y 13. Ahora, ¿el 17 es un número primo? Explica tu razonamiento paso a paso."
        
    - **Respuesta (posible):**
        
        - "Paso 1: ¿Qué es un número primo? Es un número que solo se puede dividir por 1 y por sí mismo sin dejar residuo."
            
        - "Paso 2: Busquemos los divisores del 17. Intentemos con números pequeños."
            
        - "Paso 3: 17 / 2 = 8.5 (no es divisible). 17 / 3 = 5.66 (no es divisible)... y así sucesivamente."
            
        - "Paso 4: El único número entero que divide al 17, además del 1, es el propio 17."
            
        - "Conclusión: Por lo tanto, el 17 es un número primo."
            

---

### ¿Por qué es importante el Chain-of-Thought?

- **Mejora la precisión:** Al obligar al modelo a seguir una secuencia lógica, se reduce la probabilidad de errores, especialmente en problemas complejos que involucran matemáticas, lógica o razonamiento.
    
- **Aumenta la interpretabilidad:** Permite a los usuarios entender cómo el modelo llegó a una conclusión. Si la respuesta es incorrecta, se puede identificar en qué paso del razonamiento se cometió el error.
    
- **Permite resolver tareas complejas:** Lo que parece una tarea simple para un humano puede ser un desafío para la IA. CoT descompone estos problemas en sub-tareas más manejables, facilitando la resolución de problemas de múltiples pasos.
    
- **Es una forma de "Few-Shot Prompting":** A menudo, se incluyen ejemplos de cadenas de pensamiento en el prompt para guiar al modelo. Esto le enseña a la IA el formato y el estilo de razonamiento que se espera.