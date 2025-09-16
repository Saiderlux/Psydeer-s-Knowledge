Un **Word Embedding** es una representación numérica de una palabra en un espacio vectorial multidimensional. Su propósito principal es capturar la [[Proximidad semantica]], es decir, la relación de significado entre las palabras, de una manera que los algoritmos de aprendizaje automático puedan entender.

### ¿Cómo se relacionan con la proximidad semántica?

La clave es que los _embeddings_ se entrenan en grandes cantidades de texto para que las palabras que aparecen en contextos similares se ubiquen cerca unas de otras en este espacio vectorial. Así, la distancia geométrica entre los vectores de palabras se convierte en una medida de su proximidad semántica. Por ejemplo:

- **Palabras sinónimas o relacionadas**: Los vectores de "rey", "príncipe" y "gobernante" se agruparán en un mismo clúster o región del espacio, ya que todos se refieren a conceptos de realeza y poder.
    
- **Analogías**: Los _word embeddings_ pueden capturar relaciones complejas. Un ejemplo clásico es la operación vectorial "rey - hombre + mujer". El vector resultante estará extremadamente cerca del vector de "reina", demostrando que el modelo ha aprendido la relación de género y la ha codificado como una dirección y distancia específicas en el espacio.
    
- **Contexto**: El modelo es capaz de diferenciar entre palabras que se escriben igual pero tienen significados distintos (polisemia). Por ejemplo, el vector para "banco" en el contexto de un río será diferente al vector de "banco" en el contexto financiero, porque sus palabras circundantes (su contexto) son muy diferentes.
    

En esencia, la proximidad semántica es el concepto lingüístico, y los _word embeddings_ son la implementación matemática que convierte ese concepto en una herramienta funcional para la inteligencia artificial. Esta representación densa y contextual es lo que ha permitido avances significativos en el procesamiento del lenguaje natural, como la traducción automática, el análisis de sentimiento y la generación de texto.