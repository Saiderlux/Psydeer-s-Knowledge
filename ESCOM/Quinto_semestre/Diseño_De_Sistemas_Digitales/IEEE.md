**Definición:** El _Institute of Electrical and Electronics Engineers_ es la organización que estandariza librerías y tipos de datos usados en VHDL.

**En [[VHDL]] es común:**

- `IEEE.std_logic_1164`: define el tipo `std_logic`.
    
- `IEEE.numeric_std`: operaciones aritméticas con enteros y vectores.
    

**Ejemplo de uso mínimo:**

```vhdl
library IEEE;
use IEEE.std_logic_1164.all;
```
