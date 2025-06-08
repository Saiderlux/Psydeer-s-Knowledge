Un amplificador operacional es aquel que solo responde a la diferencia entre dos voltajes y que tiene una ganancia en voltaje muy grande y resistencia de entrada muy alta.
Se le da el nombre de amplificador operacional a un amplificador lineal, muy estable, de alta ganancia, con acoplamiento directo y una entrada diferencial.

El op amp es un amplificador CC multietapa con entrada diferencial, cuyas características se aproximan a un amplificador ideal.

**Categorías de aplicación**
1. Lineales (amplificadores, reguladores, filtros activos, etc)
2. Matemáticas (sumadores, integradores, derivadores, etc)
3. No lineales (rectificadores, limitadores, comparadores, osciladores, etc)

*Retroalimentación positiva y negativa*
## Amplificador de corriente

Un **amplificador de corriente** es un dispositivo electrónico cuya función principal es tomar una corriente de entrada y entregar una corriente de salida proporcionalmente mayor. Es decir, **amplifica la corriente**, manteniendo idealmente la forma de la señal.

---

### 🔧 **Características Generales del Amplificador de Corriente:**

- **Entrada:** corriente
    
- **Salida:** corriente
    
- **Ganancia:** relación entre corriente de salida y corriente de entrada
    

Ai=IoutIinA_i = \frac{I_{out}}{I_{in}}Ai​=Iin​Iout​​

- **Impedancia de entrada (ZiZ_iZi​):** idealmente **cero** para absorber toda la corriente de la fuente de señal.
    
- **Impedancia de salida (ZoZ_oZo​):** idealmente **infinita** para que toda la corriente vaya hacia la carga y no se derive.
    

---

### 🎯 **Características Ideales:**

|Parámetro|Valor Ideal|
|---|---|
|Impedancia de entrada ZiZ_iZi​|0 Ω (cortocircuito)|
|Impedancia de salida ZoZ_oZo​|∞ Ω (circuito abierto)|
|Ganancia de corriente AiA_iAi​|Constante, independiente de la carga|
|Tipo de señal de entrada|Corriente|
|Tipo de señal de salida|Corriente|

---

### 🧰 **Características Prácticas:**

|Parámetro|Valor Típico (Real)|
|---|---|
|Impedancia de entrada ZiZ_iZi​|Muy baja, pero no cero|
|Impedancia de salida ZoZ_oZo​|Muy alta, pero finita|
|Ganancia de corriente AiA_iAi​|Alta, pero puede depender de condiciones externas|
|Linealidad|Limitada; puede haber distorsión|
|Rango de operación|Limitado por la fuente de alimentación|

---

### 🔌 **Configuraciones Comunes para Implementar Amplificadores de Corriente:**

1. **Transistor en configuración de colector común (emisor seguidor)** — utilizado en algunas etapas de acoplamiento.
    
2. **Amplificador operacional con retroalimentación de corriente** — para hacer un amplificador transconductancia (entrada voltaje, salida corriente).
    
3. **Convertidor corriente-corriente con amplificador OTA o transistor de efecto de campo (FET)**.
    

---

### 📈 Aplicaciones Comunes:

- Sensores de corriente (shunt)
    
- Amplificación de señales en buses de corriente
    
- Cargas controladas por corriente (LEDs, láseres, motores)
    
- Etapas de salida en sistemas de transmisión analógica
    

---


---

## 🔌 1. **Amplificador de Voltaje**

### 📥 Entrada: voltaje

### 📤 Salida: voltaje

### 📈 **Ganancia:**

$$A_v = \frac{V_{out}}{V_{in}}
$$
---

### 🎯 **Características Ideales:**

|Parámetro|Valor Ideal|
|---|---|
|Impedancia de entrada ZiZ_iZi​|∞ Ω (circuito abierto, no carga la fuente)|
|Impedancia de salida ZoZ_oZo​|0 Ω (fuente ideal de voltaje)|
|Ganancia de voltaje AvA_vAv​|Constante (idealmente muy alta)|

---

### 🧰 **Características Prácticas:**

|Parámetro|Valor Típico|
|---|---|
|Impedancia de entrada ZiZ_iZi​|Alta, pero finita|
|Impedancia de salida ZoZ_oZo​|Baja, pero no cero|
|Ganancia de voltaje AvA_vAv​|Alta, depende del diseño|

---

### 🛠️ **Ejemplos comunes:**

- Amplificadores operacionales (configuración no inversora o inversora)
    
- Etapas de ganancia en audio o RF
    

---

## ⚡ 2. **Amplificador de Corriente**

Ya cubierto anteriormente, pero aquí va el resumen:

### 📥 Entrada: corriente

### 📤 Salida: corriente

### 📈 **Ganancia:**

$$A_i = \frac{I_{out}}{I_{in}}$$

---

### 🎯 **Características Ideales:**

|Parámetro|Valor Ideal|
|---|---|
|ZiZ_iZi​|0 Ω|
|ZoZ_oZo​|∞ Ω|
|AiA_iAi​|Constante|

---

### 🧰 **Características Prácticas:**

|Parámetro|Valor Típico|
|---|---|
|ZiZ_iZi​|Muy baja|
|ZoZ_oZo​|Muy alta|
|AiA_iAi​|Alta, pero no perfecta|

---

## 📡 3. **Amplificador de Transconductancia**

También llamado **convertidor voltaje a corriente**.

### 📥 Entrada: voltaje

### 📤 Salida: corriente

### 📈 **Ganancia (transconductancia):**

$$G_m = \frac{I_{out}}{V_{in}}$$

---

### 🎯 **Características Ideales:**

|Parámetro|Valor Ideal|
|---|---|
|ZiZ_iZi​|∞ Ω|
|ZoZ_oZo​|∞ Ω|
|GmG_mGm​|Constante|

---

### 🧰 **Características Prácticas:**

|Parámetro|Valor Típico|
|---|---|
|ZiZ_iZi​|Alta, pero finita|
|ZoZ_oZo​|Alta, pero finita|
|GmG_mGm​|Depende del diseño (transistores, OTA, etc.)|

---

### 🛠️ **Ejemplos comunes:**

- Amplificador operacional con realimentación resistiva nula
    
- OTA (Amplificadores de Transconductancia Operacionales)
    
- Controladores de LED o motores (donde se desea controlar corriente con voltaje)
    

---

## 🔁 4. **Amplificador de Transimpedancia**

También llamado **convertidor corriente a voltaje**.

### 📥 Entrada: corriente

### 📤 Salida: voltaje

### 📈 **Ganancia (transimpedancia):**

$$
R_m = \frac{V_{out}}{I_{in}} \quad \text{(Ω)}$$


---

### 🎯 **Características Ideales:**

|Parámetro|Valor Ideal|
|---|---|
|ZiZ_iZi​|0 Ω|
|ZoZ_oZo​|0 Ω|
|RmR_mRm​|Constante|

---

### 🧰 **Características Prácticas:**

|Parámetro|Valor Típico|
|---|---|
|ZiZ_iZi​|Muy baja|
|ZoZ_oZo​|Baja|
|RmR_mRm​|Determinada por resistor de realimentación|

---

### 🛠️ **Ejemplos comunes:**

- Convertidor I/V en fotodetectores (p. ej. fotodiodos)
    
- Amplificadores para sensores de corriente
    
- Amplificadores con opamps en modo inversor con entrada de corriente
    

---

## 🧾 Tabla Comparativa Rápida

|Tipo de Amplificador|Entrada|Salida|Impedancia de entrada|Impedancia de salida|Ganancia|
|---|---|---|---|---|---|
|Voltaje (A_v)|V|V|Alta (ideal: ∞)|Baja (ideal: 0)|Av=VoutVinA_v = \frac{V_{out}}{V_{in}}Av​=Vin​Vout​​|
|Corriente (A_i)|I|I|Baja (ideal: 0)|Alta (ideal: ∞)|Ai=IoutIinA_i = \frac{I_{out}}{I_{in}}Ai​=Iin​Iout​​|
|Transconductancia (G_m)|V|I|Alta (ideal: ∞)|Alta (ideal: ∞)|Gm=IoutVinG_m = \frac{I_{out}}{V_{in}}Gm​=Vin​Iout​​|
|Transimpedancia (R_m)|I|V|Baja (ideal: 0)|Baja (ideal: 0)|Rm=VoutIinR_m = \frac{V_{out}}{I_{in}}Rm​=Iin​Vout​​|

---

¿Te gustaría que te hiciera esquemas de cada tipo de amplificador usando amplificadores operacionales?

### **Libros Recomendados**

1. **"Diseño con amplificadores operacionales y circuitos integrados analógicos" (3ra edición) – Sergio Franco**
    
    - Este libro es una referencia clave en español para el diseño de circuitos con amplificadores operacionales. Cubre ampliamente temas como convertidores corriente a voltaje, voltaje a corriente, amplificadores de corriente y de transimpedancia.
        
    - 📘 Acceso al libro en Academia.edu
        
2. **"Amplificadores operacionales y circuitos integrados lineales" (4ta edición) – Robert F. Coughlin y Frederick F. Driscoll**
    
    - Este texto es ampliamente utilizado en cursos de ingeniería electrónica. Aborda en detalle amplificadores de transconductancia, transimpedancia y de corriente, además de ofrecer ejercicios prácticos y ejemplos de diseño.
        
    - 📘 Acceso al libro en PDF
        
3. **"Op Amps For Everyone" (5ta edición) – Bruce Carter y Ron Mancini**
    
    - Publicado por Newnes, este libro es una guía práctica para diseñadores de circuitos con amplificadores operacionales. Incluye ejemplos de circuitos y aplicaciones reales.
        
    - 📘 [Más información en Wikipedia](https://en.wikipedia.org/wiki/Operational_amplifier)
        
4. **"Operational Amplifiers – Theory and Design" (3ra edición) – Johan Huijsing**
    
    - Este libro ofrece una visión profunda sobre el diseño teórico de amplificadores operacionales, incluyendo aspectos de transconductancia y transimpedancia.
        
    - 📘 [Más información en Wikipedia](https://en.wikipedia.org/wiki/Operational_amplifier)
        

---

### 📘 **Recursos Adicionales en Español**

- **"Análisis y diseño de circuitos lineales" (8va edición) – Roland Thomas, Albert Rosa y Gregory Toussaint**

