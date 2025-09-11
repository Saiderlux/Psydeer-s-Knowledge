## [[Arquitectura]] de la práctica
Para la arquitectura de la práctica se usará un [[Multiplexor]] 4x1 con 5 entradas (A,B,C,D y SEL) cada una de dos bits; una salida, también de dos bits que a su vez será la entrada del [[Comparador de magnitud]] junto con REF, de dos bits igual, posteriormente se hará la comparación y tendrá tres salidas, MA (mayor), ME (menor), I (igual); este a su vez será la entrada del [[Decodificador CM-7seg]].

El display deberá mostrar un mayor, menor o igual, dependiendo de la comparación realizada.


```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "ESCOM/Quinto_semestre/Diseño_De_Sistemas_Digitales/ANEXOS/Ink/Drawing/2025.8.27 - 17.50pm.drawing",
	"width": 585.9111938476562,
	"aspectRatio": 1.7078713274670063
}
```

### MUX 4x1

Esta tabla describe la funcionalidad del multiplexor, mostrando cómo las entradas de selección (SEL) eligen cuál de las entradas de datos (Dato) se envía a la salida.

|SEL|Dato|
|---|---|
|00|A|
|01|B|
|10|C|
|11|D|
#### Código en [[VHDL]] del [[Multiplexor]]

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "ESCOM/Quinto_semestre/Diseño_De_Sistemas_Digitales/ANEXOS/Ink/Drawing/2025.8.27 - 18.04pm.drawing",
	"width": 402,
	"aspectRatio": 2.0946404323317642
}
```

Entidad:
La entidad define los puertos de entrada y salida del MUX. El nombre de la entidad, `prac_1`, es el mismo que el del archivo. Los puertos `A`, `B`, `C`, `D`, y `SEL` son de entrada (`IN`), y `Dato` es de salida (`OUT`). Todos son vectores lógicos (`std_logic_vector`) de 1 bit, lo que se indica con `(1 downto 0)`.

```VHDL
library IEEE;
use IEEE.std_logic_1164.ALL;

entity prac_1 is
    port (
        A, B, C, D, SEL: in std_logic_vector (1 downto 0);
        Dato: out std_logic_vector (1 downto 0)
    );
end entity;
```
##### [[Arquitectura]] concurrente

```VHDL
architecture a_prac1 of prac_1 is
begin
    with SEL select
        Dato <= A when "00",
                B when "01",
                C when "10",
                D when others;
end a_prac1;
```
##### [[Arquitectura]] secuencial

```vhdl
architecture a_prac1 of prac_1 is
begin
    process (SEL)
    begin
        case SEL is
            when "00" => Dato <= A;
            when "01" => Dato <= B;
            when "10" => Dato <= C;
            when others => Dato <= D;
        end case;
    end process;
end a_prac1;
```
---

### Comparador de magnitud y decodificador a display

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Ink/Drawing/2025.8.28 - 7.01am.drawing",
	"width": 510,
	"aspectRatio": 1.6248873096904721
}
```


Esta tabla combina la lógica del comparador de magnitud con la codificación para el display de 7 segmentos. La primera columna muestra la relación entre DATO y REF. Las siguientes columnas indican la salida del comparador de magnitud (MA, ME, C) y la codificación para encender los segmentos del display (ABCDEFG). La codificación de los segmentos es para un display de cátodo común, ya que la tarjeta Tang Nano 9K usa este tipo de display donde la fuente da la corriente y se enciende con un alto lógico.

| REF DATO   | MA  | ME  | C   | ABCDEFG |
| ---------- | --- | --- | --- | ------- |
| DATO > REF | 1   | 0   | 0   | 1100110 |
| DATO < REF | 0   | 1   | 0   | 1110010 |
| DATO = REF | 0   | 0   | 1   | 1110110 |
#### Código en VHDL del comparador de magnitud
```vhdl
library IEEE;
use IEEE.std_logic_1164.all;
use IEEE.numeric_std.all;

entity comparador is
    port (
        DATO : in  std_logic_vector(3 downto 0);
        REF  : in  std_logic_vector(3 downto 0);
        MA, ME, C : out std_logic
    );
end entity;
```
##### Arquitectura Recurrente
```vhdl
architecture concurrente of comparador is
begin
    MA <= '1' when (DATO) > (REF) else '0';
    ME <= '1' when (DATO) < REF) else '0';
    C  <= '1' when (DATO) = (REF) else '0';
end architecture;
```

##### Arquitectura secuencial
```vhdl
architecture secuencial of comparador is
begin
    process(DATO, REF)
    begin
        MA <= '0';
        ME <= '0';
        C  <= '0';

        if (DATO) > (REF) then
            MA <= '1';
        elsif (DATO) < (REF) then
            ME <= '1';
        else
            C <= '1';
        end if;
    end process;
end architecture;
```

#### Código en VHDL del decodificador
```vhdl
library IEEE;
use IEEE.std_logic_1164.all;

entity decodificador is
    port (
        MA, ME, C : in  std_logic;
        SEG       : out std_logic_vector(6 downto 0) -- A B C D E F G
    );
end entity;
```

##### Arquitectura concurrente
```vhdl
architecture concurrente of decodificador is
begin
    SEG <= "1100110" when (MA = '1') else -- DATO > REF
           "1110010" when (ME = '1') else -- DATO < REF
           "1110110";                     -- DATO = REF
end architecture;
```

##### Arquitectura secuencial
```vhdl
architecture secuencial of decodificador is
begin
    process(MA, ME, C)
    begin
        if MA = '1' then
            SEG <= "1100110"; -- DATO > REF
        elsif ME = '1' then
            SEG <= "1110010"; -- DATO < REF
        else
            SEG <= "1110110"; -- DATO = REF
        end if;
    end process;
end architecture;

```
REVISADO
