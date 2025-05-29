$$i_{c}=I_{s}e^\frac{V_{BE}}{V_{r}}$$
$$I_{e}=I_{C}+I_{B}$$
La beta es:
$$\beta_{cd}=\frac{I_{c}}{I_{B}}; [h_{fe}]$$
$$\alpha_{cd}=\frac{I_{C}}{I_{E}}$$$$ \alpha_{cd}=\frac{\beta_{cd}}{\beta_{cd}+1}$$
La caída de voltaje a través de $R_{C}$
$$V_{RC}=I_{c}R_{c}$$
EL voltaje en el colector con respecto al emisor (ligado a tierra)
$$V_{CE}=V_{CC}-I_{C}R_{C}$$
El voltaje entre la base y el colector es
$$V_{CB}=V_{CE}-V_{BE}$$




# Transistor BJT (Bipolar Junction Transistor)

El transistor BJT es un dispositivo electrónico de tres terminales: **emisor (E)**, **base (B)** y **colector (C)**. Se utiliza comúnmente para amplificación y conmutación de señales.

## Tipos de BJT

Existen dos tipos:

- **NPN**
- **PNP**

> En un NPN, la corriente fluye del colector al emisor cuando la base es positiva respecto al emisor.  
> En un PNP, la corriente fluye del emisor al colector cuando la base es negativa respecto al emisor.

## Características generales

- Dispositivo controlado por corriente.
- La corriente de la base controla la corriente del colector.
- La ganancia de corriente en continua se representa con $$\beta$$:
  
  $$\beta = \frac{I_C}{I_B}$$
$$\beta=\frac{\alpha}{1-\alpha}\text{ y }\alpha=\frac{\beta}{\beta+1}$$
$$\alpha=\frac{I_{C}}{I_{E}}$$
## Corrientes en el BJT

Las tres corrientes principales se relacionan mediante:

$$I_E = I_C + I_B$$

Donde:

- $I_E$: Corriente del emisor  
- $I_C$: Corriente del colector  
- $I_B$: Corriente de la base

## Regiones de operación

### 1. **Región de corte**

- Ambas uniones (emisor-base y colector-base) están **polarizadas en inversa**.
- No hay conducción de corriente significativa.

**Condiciones:**

- $V_{BE} < V_{BE_{on}}$ (típicamente < 0.7V para NPN)
- $I_C \approx 0$, $I_B \approx 0$

---

### 2. **Región activa**

- La unión emisor-base está **en directa** y la unión colector-base **en inversa**.
- El transistor funciona como **amplificador**.

**Condiciones:**

- $V_{BE} > V_{BE_{on}}$ (típicamente ≈ 0.7V para NPN)
- $V_{CE} > V_{CE_{sat}}$
- $I_C \approx \beta I_B$

---

### 3. **Región de saturación**

- Ambas uniones están **en directa**.
- El transistor está **conduciendo completamente**, como un interruptor cerrado.

**Condiciones:**

- $V_{BE} > V_{BE_{on}}$
- $V_{CE} \approx V_{CE_{sat}}$ (típicamente ≈ 0.2V)

---

### 4. **Región de inversión activa (poco común)**

- Emisor y colector invierten sus roles. No se usa generalmente en aplicaciones prácticas.

---

## Configuraciones del BJT

### 1. **Configuración Base Común (CB)**

- Entrada: entre emisor y base  
- Salida: entre colector y base  
- **Ganancia de corriente menor a 1**  
- Alta ganancia de voltaje

### 2. **Configuración Emisor Común (CE)**

- Entrada: entre base y emisor  
- Salida: entre colector y emisor  
- **Alta ganancia de corriente y voltaje**  
- Inversión de fase entre entrada y salida

### 3. **Configuración Colector Común (CC) o Seguidor de Emisor**

- Entrada: entre base y colector  
- Salida: entre emisor y colector  
- **Ganancia de voltaje ≈ 1**, alta ganancia de corriente  
- Buena adaptación de impedancias

---

## Fórmulas importantes en circuitos con BJT

### Corrientes:

- $$I_C = \beta I_B$$
- $$I_E = (1 + \beta) I_B$$

### Voltajes:

- $$V_{BE} \approx 0.7\,V \text{ (NPN)}$$
- $$V_{CE} = V_C - V_E$$
- $$V_{CB} = V_C - V_B$$

### Punto de operación o Q-point:

Para polarización en región activa:

- Se establecen resistencias de polarización para fijar $I_B$.
- Se analiza con mallas de corriente y ley de Ohm.

Ejemplo:

- $$V_{BB} = I_B R_B + V_{BE}$$
- $$V_{CC} = I_C R_C + V_{CE}$$

---

## Aplicaciones comunes

- Amplificadores de señal
- Interruptores electrónicos
- Osciladores
- Reguladores de voltaje

---

## Notas adicionales

- La temperatura afecta significativamente el comportamiento del BJT.
- El diseño debe considerar estabilidad térmica y márgenes de saturación.

---
## Ejemplos
![[Pasted image 20250515223729.png]]
### Solución al Problema 2-1.7

**Datos:**  
- Corriente de base:  
  $$
  I_B = 50\,\mu A
  $$
- Resistencia de colector:  
  $$
  R_C = 1\,k\Omega
  $$
- Caída de voltaje en \(R_C\):  
  $$
  V_{RC} = 5\,V
  $$

---

### Cálculo de la corriente de colector

Centremos la ecuación de Ohm para \(R_C\):

$$
(E1)\quad I_C = \frac{V_{RC}}{R_C} = \frac{5\,V}{1\,k\Omega} = 5\,mA
$$

---

### Cálculo de \(\beta_{cd}\)

La ganancia en configuración emisor común (β) se define como:

$$
(E2)\quad \beta_{cd} = \frac{I_C}{I_B} = \frac{5\,mA}{50\,\mu A} = 100
$$

---

### Cálculo de \(\alpha_{cd}\)

Sabemos que \(\alpha\) (ganancia en configuración base común) y \(\beta\) están relacionadas por:

$$
(E3)\quad \alpha = \frac{\beta}{\beta + 1}
$$

Sustituyendo \(\beta_{cd}=100\):

$$
(E4)\quad \alpha_{cd} = \frac{100}{100 + 1} \approx 0.9901
$$

---
