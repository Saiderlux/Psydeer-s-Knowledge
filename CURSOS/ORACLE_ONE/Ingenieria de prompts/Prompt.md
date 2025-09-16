En el contexto de la inteligencia artificial y los [[LLM's]], un **prompt** es la instrucción, pregunta o entrada de texto que le das a un modelo de lenguaje (como GPT, Gemini o Claude) para que genere una respuesta. Es la forma en que te comunicas con la IA para guiar su comportamiento.

Piensa en el prompt como el punto de partida de una conversación. La calidad de la respuesta del modelo está directamente relacionada con la calidad del prompt que le proporcionas.

---

### Componentes clave de un buen prompt

Aunque un prompt puede ser tan simple como una sola palabra, los prompts más efectivos suelen incluir varios elementos para guiar a la IA con mayor precisión:

- **Instrucción:** La tarea específica que el modelo debe realizar (ej. "Resume el siguiente texto", "Escribe un poema", "Traduce esta frase al inglés").
    
- **Contexto:** Información de fondo que ayuda al modelo a entender la situación o el propósito de la solicitud (ej. "Eres un experto en marketing digital...", "El público objetivo son estudiantes de secundaria...").
    
- **Datos de entrada:** La información que el modelo necesita para completar la tarea (ej. el texto a resumir, la frase a traducir).
    
- **Formato de salida:** La estructura o el estilo deseado para la respuesta (ej. "En formato de lista", "Con un tono profesional", "En 200 palabras").
    

---

### Tipos de prompts

Los prompts pueden variar en su complejidad y en cómo se construyen para lograr un resultado específico:

- **Prompts simples:** Una pregunta o instrucción directa.
    
    - **Ejemplo:** "¿Qué es la fotosíntesis?"
        
- **Prompts complejos (Ingeniería de prompts):** Utilizan técnicas avanzadas para guiar el modelo, como **Zero-Shot**, **Few-Shot**, o **Chain-of-Thought**. Estas técnicas buscan mejorar la coherencia y precisión de la respuesta.
    
    - **Ejemplo:** "Actúa como un profesor de historia. Explica las causas de la Primera Guerra Mundial en un tono didáctico y con un resumen al final."