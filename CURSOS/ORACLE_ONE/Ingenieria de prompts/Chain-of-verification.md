**Chain-of-Verification (CoVe)**, o "Cadena de Verificación", es una técnica de **ingeniería de prompts** que busca mejorar la precisión y confiabilidad de los [[LLM's]]. A diferencia de otras técnicas que solo se centran en generar una respuesta, CoVe instruye al modelo a **verificar su propia respuesta** antes de presentarla.

## Cómo funciona

El proceso de CoVe se divide en cuatro pasos principales, que se realizan de forma secuencial:

1. **Generación de la respuesta inicial:** El modelo genera una primera respuesta a la pregunta o [[Prompt]].
    
2. **Generación de planes de verificación:** A continuación, el modelo crea una lista de afirmaciones o puntos clave de su propia respuesta que necesitan ser verificados. Esto es como un plan de auditoría. Por ejemplo, si la respuesta es sobre un hecho histórico, el modelo podría crear un punto para "verificar la fecha" y otro para "confirmar los nombres de los personajes".
    
3. **Ejecución de la verificación:** El modelo genera nuevas consultas o prompts internos para buscar información y verificar cada uno de los puntos del plan. Esto le permite cotejar la información de su primera respuesta con su conocimiento interno o incluso con la información en tiempo real, si tiene acceso a ella.
    
4. **Generación de la respuesta final verificada:** Finalmente, el modelo utiliza los resultados de la verificación para reescribir o corregir su respuesta original. La versión final es la que se le presenta al usuario, con la información verificada y corregida.
    

---

## Por qué es importante

CoVe es una técnica muy útil para combatir las **alucinaciones** de la IA, que son respuestas incorrectas o inventadas que los modelos a veces generan con mucha confianza. Al obligar al modelo a auditarse a sí mismo, se reduce significativamente la probabilidad de errores y se aumenta la fiabilidad de la información.

En esencia, mientras que **Chain-of-Thought** le pide al modelo que muestre cómo llega a una respuesta, **Chain-of-Verification** le pide que demuestre que su respuesta es correcta.