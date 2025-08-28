**Definición:** Circuito digital que selecciona una entrada de entre varias y la envía a la salida, en función de señales de selección (**SEL**).

**Explicación detallada:**

- Es similar a un “conmutador” controlado electrónicamente.
    
- Compuesto por:
    
    - Entradas de datos (D0, D1, D2…)
        
    - Entradas de control o selección (SEL)
        
    - Una única salida.
        
- El caso de **4×1** significa 4 entradas de datos, 1 salida, y 2 bits de selección.
    

**Ejemplo funcional:** Un **MUX 4×1** con SEL = `01` enviará la señal de **D1** a la salida, ignorando las demás.

**Aplicación en práctica:** En el proyecto, el MUX seleccionará entre varias señales de referencia o datos provenientes de la lógica del comparador.