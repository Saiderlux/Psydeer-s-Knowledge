**Least-to-Most Prompting**, o "prompting de menos a más", es una técnica avanzada de ingeniería de [[Prompt]] que descompone un problema complejo en una serie de pasos más simples, resolviéndolos de manera secuencial. A diferencia de otras técnicas que intentan resolver el problema completo de una sola vez, este enfoque se basa en la idea de que la solución a un problema difícil se puede construir a partir de las soluciones de sus partes más sencillas.

### ¿Cómo funciona?

El proceso se divide en dos etapas principales:

1. **Descomposición del problema:** El primer prompt que le das al modelo es para que analice el problema principal y lo divida en una lista de subproblemas. Por ejemplo, si la tarea es "Describe el ciclo del agua y explica cómo la actividad humana lo afecta", el modelo podría descomponerlo en:
    
    - ¿Qué es la evaporación y cómo funciona?
        
    - ¿Qué es la condensación y cómo se relaciona con las nubes?
        
    - ¿Qué es la precipitación?
        
    - ¿Cómo la deforestación afecta la evaporación y la precipitación?
        
    - ¿Cómo la contaminación afecta la calidad del agua en el ciclo?
        
2. **Resolución secuencial:** Una vez que el modelo ha identificado los subproblemas, se le pide que resuelva cada uno de ellos, uno por uno. Lo crucial aquí es que la respuesta a cada subproblema se usa como **información de contexto** para el siguiente. Esto crea una "cadena" de conocimiento donde cada paso se construye sobre el anterior, guiando al modelo hacia la solución final.
    

### ¿Cuál es la diferencia con Chain-of-Thought?

Aunque suenan similares, **Least-to-Most** lleva la lógica de **Chain-of-Thought** un paso más allá.

- **Chain-of-Thought (CoT)**: Se enfoca en el "razonamiento en voz alta". Le pides al modelo que muestre sus pasos de pensamiento para resolver el problema, todo dentro del mismo prompt. Es como si el modelo estuviera pensando para sí mismo.
    
- **Least-to-Most (LtM)**: Va más allá al **dividir la tarea en múltiples prompts** y resolver los subproblemas de forma secuencial. La información generada en cada paso se incorpora explícitamente en el siguiente prompt, asegurando que el modelo tenga toda la información necesaria para el siguiente paso.