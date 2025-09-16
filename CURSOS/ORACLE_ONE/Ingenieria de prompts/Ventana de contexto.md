La **ventana de contexto** de un modelo de lenguaje grande ([[LLM's]]) es la cantidad de texto que puede "recordar" y procesar en un momento dado. Piensa en ello como la **memoria a corto plazo** del modelo. A diferencia de la memoria humana que puede recordar toda una vida, la memoria de un LLM es limitada y se mide en **tokens**, que son las unidades más pequeñas de texto (pueden ser palabras, sílabas o caracteres).

---

### ¿Cómo funciona?

Cuando interactúas con los [[LLM's]], todo el texto que ingresas, junto con la respuesta que genera, se cuenta dentro de esta ventana de contexto. El modelo solo puede considerar los tokens que están dentro de esta ventana para generar la siguiente respuesta.

- **Límite de memoria**: Si tu conversación o el documento que le proporcionas excede el tamaño de la ventana de contexto, el modelo **empieza a olvidar la información más antigua** para hacer espacio a la nueva. Por esta razón, en conversaciones muy largas, un LLM puede "olvidar" lo que se discutió al principio y perder coherencia.
    
- **Tokenización**: La ventana de contexto no se mide en palabras, sino en [[Tokens]]. Esto significa que la longitud de la ventana varía según el idioma y el tipo de texto. Un token puede ser una palabra completa como "casa", una parte de una palabra como "con-" o incluso un signo de puntuación.
    
- **Analizando grandes documentos**: La ventana de contexto determina el tamaño máximo de un documento, un artículo o un fragmento de código que el modelo puede analizar de una sola vez. Si un documento es más grande que la ventana, debe ser resumido o procesado en partes para que el modelo pueda manejarlo.
    

---

### Limitaciones

El tamaño de la ventana de contexto es una de las limitaciones más importantes de los [[LLM's]]. Una ventana de contexto pequeña puede llevar a respuestas incoherentes y "alucinaciones" (generar información incorrecta). Por el contrario, las ventanas más grandes permiten conversaciones más largas y una mayor precisión, pero requieren más potencia computacional y son más costosas de operar.