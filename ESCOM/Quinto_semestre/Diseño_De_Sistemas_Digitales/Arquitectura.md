**Concurrente**

- Todas las instrucciones se ejecutan _en paralelo_.
    
- Útil para describir hardware con procesos independientes.
    
- Palabras clave: `with...select`, `when...else`, `generate`.
    

**Secuencial**

- Instrucciones dentro de un bloque `process` que se ejecutan de forma ordenada.
    
- Útil cuando la ejecución depende de condiciones o estados.
    
- Palabras clave: `if`, `case`, `loop`.
    

**Comparativa:**

|Tipo|Ventajas|Desventajas|
|---|---|---|
|Concurrente|Fácil de mapear a hardware paralelo|Menos control secuencial|
|Secuencial|Control preciso del flujo|Puede requerir más recursos|

**Por qué hoy predomina la secuencial:** En diseños complejos, el control de flujo y la sincronización son esenciales, lo que hace que la secuencial sea más conveniente para describir lógica controlada por relojes.