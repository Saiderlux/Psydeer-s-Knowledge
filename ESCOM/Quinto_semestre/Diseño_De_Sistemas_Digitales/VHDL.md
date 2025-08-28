\**Definición:** Lenguaje de descripción de hardware (_VHSIC Hardware Description Language_) usado para modelar y programar circuitos digitales.

**Elementos que todo programa debe incluir:**

1. **Librerías y paquetes**
    
    - `library IEEE;` [[IEEE]]
        
    - `use IEEE.std_logic_1164.all;` (y otros como `numeric_std` para operaciones aritméticas)
        
2. **Entidad (entity)**
    
    - Define nombre del módulo y puertos de entrada/salida.
        
3. **Arquitectura (architecture)** [[Arquitectura]]
    
    - Define la funcionalidad interna.
        
    - Tipos:
        
        - **Funcional** (_behavioral_)
            
        - **Flujo de datos** (_dataflow_)
            
        - **Estructurada** (_structural_)
            
        - **Concurrente** y **Secuencial**
            
4. **Ejemplo de sintaxis básica:**
    

```vhdl
library IEEE;
use IEEE.std_logic_1164.all;

entity ejemplo is
    port(
        A, B : in std_logic_vector(1 downto 0);
        Y    : out std_logic_vector(1 downto 0)
    );
end entity;

architecture Behavioral of ejemplo is
begin
    Y <= A when B = "00" else
         B;
end Behavioral;
```

## Asignación <=
La asignación `<=` en VHDL se llama **"signal assignment"** (asignación de señal) y se usa para asignar un valor a una señal. Su característica principal es que la asignación no es instantánea, sino que tiene un retraso inherente.
```vhdl
signal A, B, C : std_logic;
-- Asignación concurrente
A <= B and C;
```
Aquí, `A` **siempre tomará** el valor de `B and C`. Esto es **concurrente**, ocurre fuera de un proceso y representa lógica combinacional.
No solo asigna un valor binario, sino también asigna un voltaje

REVISADO