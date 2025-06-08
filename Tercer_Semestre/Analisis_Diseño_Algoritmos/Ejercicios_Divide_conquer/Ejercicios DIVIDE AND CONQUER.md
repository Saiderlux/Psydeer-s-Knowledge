# Análisis del Algoritmo del Par de Puntos Más Cercanos

## Implementación mediante Divide y Vencerás

El presente código implementa una solución al problema clásico de encontrar el par de puntos más cercanos en un espacio bidimensional. La solución emplea el paradigma de divide y vencerás, descomponiendo el conjunto de puntos en subconjuntos que se procesan de manera recursiva y luego combinando sus resultados de manera eficiente.

### Fundamento Teórico

La implementación se basa en la estrategia de dividir el conjunto de puntos en dos mitades según su coordenada x, resolver recursivamente el problema en cada mitad, y luego considerar los puntos cercanos a la línea divisoria. Este enfoque aprovecha la ordenación de los puntos tanto en x como en y para lograr una solución eficiente.

La distancia mínima $d$ entre dos puntos se calcula utilizando la fórmula euclidiana:

$$d = \sqrt{(x_2-x_1)^2 + (y_2-y_1)^2}$$

El algoritmo mantiene dos arreglos ordenados de los puntos:

1. Un arreglo ordenado por coordenada x
2. Un arreglo ordenado por coordenada y

Esta doble ordenación es crucial para la eficiencia del algoritmo, especialmente durante la fase de combinación.

### Estructura del Algoritmo

El algoritmo se estructura en varias funciones clave:

1. `distanciaMinimaRecursiva`: Función principal que implementa la estrategia divide y vencerás.
2. `distanciaMinimaEnFranja`: Procesa los puntos cercanos a la línea divisoria.
3. `distanciaMinima`: Función envolvente que prepara los datos iniciales.

La parte más delicada del algoritmo es el manejo de la franja central, donde se deben considerar puntos que podrían estar más cerca entre sí que las distancias mínimas encontradas en las mitades izquierda y derecha.

### Casos Base

El algoritmo maneja los casos base cuando hay 3 o menos puntos mediante una búsqueda exhaustiva. Para n ≤ 3:

- Se comparan todas las posibles parejas de puntos
- Se retorna la distancia mínima encontrada

### Análisis de Complejidad

El análisis de complejidad del algoritmo se puede desglosar en varias partes:

1. **Ordenamiento inicial**:
    - $O(n \log n)$ para ordenar los puntos por x e y
2. **Recursión principal**:
    - Relación de recurrencia: $T(n) = 2T(n/2) + O(n)$
    - La división del problema: $O(1)$
    - La combinación (franja): $O(n)$
3. **Procesamiento de la franja**:
    - Aparentemente $O(n^2)$, pero debido a la propiedad geométrica de que solo un número constante de puntos puede estar dentro de un rectángulo de ancho d y altura d, es realmente $O(n)$ (mencionada en clase).

La complejidad total del algoritmo es $O(n \log n)$, que proviene del ordenamiento inicial y de la resolución de la recurrencia mediante el Teorema Maestro.

Este análisis muestra que el algoritmo es considerablemente más eficiente que una solución por fuerza bruta, que requeriría $O(n^2)$ comparaciones. La eficiencia se logra mediante el uso estratégico del ordenamiento y el manejo eficiente de la región de combinación.

### Construcción del código

La implementación utiliza el paradigma de divide y vencerás, permitiendo abordar el problema de manera eficiente al dividirlo en subproblemas más manejables.
#### Estructura de Datos

Primero, analizamos la estructura de datos fundamental:

```c
typedef struct {
    double x, y;
} Punto;
```

Esta estructura fue elegida por su simplicidad y eficiencia. Al usar `double`, obtenemos precisión suficiente para coordenadas reales, y la estructura agrupa lógicamente las coordenadas x, y, facilitando el manejo de los puntos como una sola unidad.

#### Funciones de Comparación

```c
int compararX(const void *a, const void *b) {
    Punto *p1 = (Punto *)a;
    Punto *p2 = (Punto *)b;
    return (p1->x < p2->x) ? -1 : (p1->x > p2->x);
}
```

Estas funciones de comparación están diseñadas para trabajar con `qsort()`. El uso de `const void *` como parámetros permite la genericidad, y el casting a `Punto *` nos permite acceder a las coordenadas. La comparación retorna -1, 0, o 1 según la convención de C para funciones de comparación.

#### Manejo de la Franja Central

La parte más crucial del algoritmo es el manejo de la franja central:

```c
double distanciaMinimaEnFranja(Punto franja[], int tamano, double d) {
    double minDist = d;
    for (int i = 0; i < tamano; i++) {
        for (int j = i + 1; j < tamano && (franja[j].y - franja[i].y) < minDist; j++) {
            minDist = min(minDist, distancia(franja[i], franja[j]));
        }
    }
    return minDist;
}
```

Este código es particularmente inteligente porque:

- Solo compara puntos cuya diferencia en y es menor que la distancia mínima actual
- Aprovecha que los puntos están ordenados por y para reducir comparaciones
- Mantiene un invariante: la distancia mínima solo puede mejorar o mantenerse igual

#### Proceso Recursivo

La función recursiva principal:

```c
double distanciaMinimaRecursiva(Punto puntosX[], Punto puntosY[], int n) {
    if (n <= 3) {
        // Caso base
    }
    
    int mitad = n / 2;
    Punto puntoMedio = puntosX[mitad];
    // División y conquista
}
```

La elección de 3 como caso base no es arbitraria:

- Con 3 o menos puntos, la comparación exhaustiva es eficiente
- Simplifica el manejo de casos especiales
- Evita la complejidad de manejar casos muy pequeños en la recursión
### Código final

```c
#include <stdio.h>
#include <stdlib.h>
#include <math.h>
#include <float.h>

typedef struct {
    double x, y;
} Punto;

int compararX(const void *a, const void *b) { 
    Punto *p1 = (Punto *)a;
    Punto *p2 = (Punto *)b;
    return (p1->x < p2->x) ? -1 : (p1->x > p2->x);
}

int compararY(const void *a, const void *b) {
    Punto *p1 = (Punto *)a;
    Punto *p2 = (Punto *)b;
    return (p1->y < p2->y) ? -1 : (p1->y > p2->y);
}

double distancia(Punto p1, Punto p2) {
    return sqrt((p1.x - p2.x) * (p1.x - p2.x) + (p1.y - p2.y) * (p1.y - p2.y));
}

double min(double x, double y) {
    return (x < y) ? x : y;
}

double distanciaMinimaEnFranja(Punto franja[], int tamano, double d) {
    double minDist = d;
    for (int i = 0; i < tamano; i++) {
        for (int j = i + 1; j < tamano && (franja[j].y - franja[i].y) < minDist; j++) {
            minDist = min(minDist, distancia(franja[i], franja[j]));
        }
    }
    return minDist;
}

double distanciaMinimaRecursiva(Punto puntosX[], Punto puntosY[], int n) {
    if (n <= 3) {
        double minDist = DBL_MAX;
        for (int i = 0; i < n; i++) {
            for (int j = i + 1; j < n; j++) {
                minDist = min(minDist, distancia(puntosX[i], puntosX[j]));
            }
        }
        return minDist;
    }
    
    int mitad = n / 2;
    Punto puntoMedio = puntosX[mitad];
    Punto puntosYIzq[mitad];
    Punto puntosYDer[n - mitad];
    int li = 0, ld = 0;

    for (int i = 0; i < n; i++) {
        if (puntosY[i].x <= puntoMedio.x) {
            puntosYIzq[li++] = puntosY[i];
        } else {
            puntosYDer[ld++] = puntosY[i];
        }
    }
    
    double distanciaIzq = distanciaMinimaRecursiva(puntosX, puntosYIzq, mitad);
    double distanciaDer = distanciaMinimaRecursiva(puntosX + mitad, puntosYDer, n - mitad);
    double d = min(distanciaIzq, distanciaDer);

    Punto franja[n];
    int j = 0;

    for (int i = 0; i < n; i++) {
        if (fabs(puntosY[i].x - puntoMedio.x) < d) {
            franja[j++] = puntosY[i];
        }
    }
    return min(d, distanciaMinimaEnFranja(franja, j, d));
}

double distanciaMinima(Punto puntos[], int n) {
    Punto puntosX[n];
    Punto puntosY[n];
    for (int i = 0; i < n; i++) {
        puntosX[i] = puntos[i];
        puntosY[i] = puntos[i];
    }
    qsort(puntosX, n, sizeof(Punto), compararX);
    qsort(puntosY, n, sizeof(Punto), compararY);
    return distanciaMinimaRecursiva(puntosX, puntosY, n);
}

  

int main() {
    int n;
    scanf("%d", &n);
    Punto puntos[n];
    for (int i = 0; i < n; i++) {
        scanf("%lf %lf", &puntos[i].x, &puntos[i].y);
    }
    
    double resultado = distanciaMinima(puntos, n);
    printf("%.3f\n", resultado);
    return 0;
}
```

![[Pasted image 20241103222916.png]]
# Análisis del Algoritmo de Conteo de Cadenas Binarias

## Implementación mediante Divide y Vencerás

El presente código implementa una solución al problema de contar cadenas binarias con una restricción específica: no pueden contener tres unos consecutivos. La solución emplea el paradigma de divide y vencerás, descomponiendo el problema en subproblemas más pequeños que se resuelven de manera recursiva.

### Fundamento Teórico

La implementación se basa en la observación de que para construir una cadena binaria válida de longitud N, podemos partir de cadenas más cortas y agregarles ciertos sufijos. Este enfoque nos permite dividir el problema en tres subproblemas más pequeños, cada uno correspondiente a un sufijo posible.

La relación recurrente que gobierna este proceso se puede expresar matemáticamente como:

$$f(n) = f(n-1) + f(n-2) + f(n-3)$$

Donde $f(n)$ representa el número de cadenas binarias válidas de longitud n. Esta recurrencia se fundamenta en las siguientes observaciones:

1. Podemos agregar un '0' a cualquier cadena válida de longitud n-1
2. Podemos agregar '01' a cualquier cadena válida de longitud n-2
3. Podemos agregar '011' a cualquier cadena válida de longitud n-3

### Casos Base

La recursión se ancla en tres casos base fundamentales:

$$f(1) = 2$$ (correspondiente a las cadenas "0" y "1") $$f(2) = 4$$ (correspondiente a "00", "01", "10", "11") $$f(3) = 7$$ (correspondiente a "000", "001", "010", "011", "100", "101", "110")
### Análisis de Complejidad

La complejidad del algoritmo se puede analizar considerando su estructura recursiva:

1. **Árbol de Recursión**:
    - Cada llamada genera tres llamadas recursivas
    - La profundidad del árbol es N
    - No hay memorización de resultados
2. **Complejidad Temporal**:
    - Sea T(n) el tiempo para entrada n
    - T(n) = T(n-1) + T(n-2) + T(n-3) + O(1)
    - Esto resulta en una complejidad de O(3^n)
### Construcción del código

El siguiente código implementa una solución recursiva para contar cadenas binarias que cumplen con una restricción específica: no pueden contener tres unos consecutivos. Veamos en detalle cómo funciona esta implementación.
#### Estructura del Código

```c
int contar_cadenas_binarias(int N) {
    if (N == 1) return 2;  // "0", "1"
    if (N == 2) return 4;  // "00", "01", "10", "11"
    if (N == 3) return 7;  // "000", "001", "010", "011", "100", "101", "110"
    
    return contar_cadenas_binarias(N - 1) + 
           contar_cadenas_binarias(N - 2) + 
           contar_cadenas_binarias(N - 3);
}
```

La función principal está estructurada de manera muy elegante, utilizando casos base explícitos y una relación recursiva simple. Esta estructura refleja directamente la naturaleza del problema.
El programa principal es simple pero efectivo:

```c
int main() {
    int N;
    scanf("%d", &N);
    printf("%d\n", contar_cadenas_binarias(N));
    return 0;
}
```

#### Casos Base

Los casos base son fundamentales para el funcionamiento correcto del algoritmo:

```c
if (N == 1) return 2;  // "0", "1"
if (N == 2) return 4;  // "00", "01", "10", "11"
if (N == 3) return 7;  // "000", "001", "010", "011", "100", "101", "110"
```

Estos valores no son arbitrarios:

- Para N=1: tenemos las cadenas "0" y "1"
- Para N=2: todas las combinaciones son válidas: "00", "01", "10", "11"
- Para N=3: todas excepto "111" son válidas

### Código final

```c
#include <stdio.h>
int contar_cadenas_binarias(int N) {
    if (N == 1) return 2; 
    if (N == 2) return 4;  
    if (N == 3) return 7;  
    return contar_cadenas_binarias(N - 1) + contar_cadenas_binarias(N - 2) + contar_cadenas_binarias(N - 3);

}

int main() {
    int N;
    scanf("%d", &N);
    printf("%d\n", contar_cadenas_binarias(N));
    return 0;
}
```

![[Pasted image 20241103215208.png]]

# Análisis del Algoritmo de Suma Máxima de Subarreglo

## Implementación mediante Divide y Vencerás

Este código implementa una solución al problema clásico de encontrar la suma máxima de un subarreglo continuo dentro de un arreglo de números enteros. La implementación utiliza el paradigma de divide y vencerás, descomponiendo el problema en subproblemas más pequeños y considerando casos especiales cuando el subarreglo máximo cruza la frontera entre las mitades.

### Fundamento Teórico

El algoritmo se basa en la observación de que el subarreglo con suma máxima puede estar en una de tres posiciones:

1. Completamente en la mitad izquierda del arreglo
2. Completamente en la mitad derecha del arreglo
3. Cruzando la mitad del arreglo (parte en la izquierda y parte en la derecha)

La suma máxima se puede expresar matemáticamente como:

$$MaxSum(A[i..j]) = max\begin{cases} MaxSum(A[i..m]) \ MaxSum(A[m+1..j]) \ MaxCrossingSum(A[i..m..j]) \end{cases}$$

Donde m es el punto medio del subarreglo $A[i..j]$.

### Estructura del Algoritmo

El algoritmo se organiza en tres funciones principales:

1. `SumaMaximaSubarreglo`: Implementa la estrategia principal de divide y vencerás
2. `SumaMediaMaxima`: Maneja el caso especial de la suma que cruza la mitad
3. `main`: Función que maneja la entrada/salida y llama al algoritmo

La parte más delicada del algoritmo es el manejo del caso que cruza la mitad, donde debemos encontrar la suma máxima que incluye elementos de ambos lados del punto medio.

### Casos Base

Para el caso más simple (un solo elemento):

- Se retorna el valor del elemento
- Este caso base es fundamental para la recursión
- Ocurre cuando izquierda == derecha

### Análisis de Complejidad

La eficiencia del algoritmo se puede analizar en varias partes:

1. **División del problema**:
    - Complejidad $O(1)$ para encontrar el punto medio
2. **Proceso recursivo**:
    - Relación de recurrencia: $T(n) = 2T(n/2) + O(n)$
    - La división es constante
    - Combinar (encontrar suma cruzada) es $O(n)$
3. **Cálculo de suma cruzada**:
    - Requiere dos recorridos lineales
    - Complejidad $O(n)$

La complejidad temporal total es $O(n \log n)$ debido a:

- El árbol de recursión tiene profundidad $\log n$
- En cada nivel se realiza trabajo $O(n)$
- Por el teorema maestro, resulta en $O(n \log n)$
### Aspectos Numéricos

El algoritmo maneja cuidadosamente los límites numéricos:

- Usa -2147483648 (INT_MIN) como valor inicial para comparaciones
- Esto asegura que funcione correctamente con números negativos
- Permite encontrar el subarreglo máximo incluso cuando todos los números son negativos

La implementación demuestra cómo un problema aparentemente simple puede resolverse de manera eficiente mediante la aplicación del paradigma de divide y vencerás. 

### Construcción del código

#### Función SumaMediaMaxima
```c 
int SumaMediaMaxima(int arreglo[], int izquierda, int medio, int derecha) {
    int suma = 0;
    int suma_izquierda = -2147483648;
    for (int i = medio; i >= izquierda; i--) {
        suma += arreglo[i];
        if (suma > suma_izquierda) {
            suma_izquierda = suma;
        }
    }

    suma = 0;
    int suma_derecha = -2147483648;
    for (int i = medio + 1; i <= derecha; i++) {
        suma += arreglo[i];
        if (suma > suma_derecha) {
            suma_derecha = suma;
        }
    }

    return suma_izquierda + suma_derecha;
}
```

Esta función maneja el caso crucial de encontrar la suma máxima que cruza el punto medio. Analicemos sus componentes:

1. **Inicialización**:
    - Usa `-2147483648` (INT_MIN) como valor inicial
    - Este valor asegura que cualquier suma real será mayor
    - Es crucial para manejar casos con números negativos
2. **Búsqueda hacia la izquierda**:
    - Comienza desde el punto medio
    - Acumula sumas y mantiene el máximo encontrado
    - El ciclo se mueve hacia la izquierda (i--)
3. **Búsqueda hacia la derecha**:
    - Similar a la izquierda pero en dirección opuesta
    - Mantiene una suma independiente
    - Se mueve hacia la derecha (i++)

#### Función Principal de Recursión

```c
int SumaMaximaSubarreglo(int arreglo[], int izquierda, int derecha) {

    if (izquierda == derecha) {
        return arreglo[izquierda];
    }
    int medio = (izquierda + derecha) / 2;
    
    int suma_izquierda = SumaMaximaSubarreglo(arreglo, izquierda, medio);
    int suma_derecha = SumaMaximaSubarreglo(arreglo, medio + 1, derecha);
    int suma_cruzada = SumaMediaMaxima(arreglo, izquierda, medio, derecha);

    if (suma_izquierda >= suma_derecha && suma_izquierda >= suma_cruzada) {
        return suma_izquierda;
    } else if (suma_derecha >= suma_izquierda && suma_derecha >= suma_cruzada) {
        return suma_derecha;
    } else {
        return suma_cruzada;
    }
}
```

Los elementos clave de esta función son:

1. **Caso Base**:
    
	```c
if (izquierda == derecha) {
    return arreglo[izquierda];
}
```
    
    - Maneja subarreglos de un solo elemento
    - Es el punto de terminación de la recursión
2. **División del Problema**:
    
    ```c
int medio = (izquierda + derecha) / 2;
```
    
    - Calcula el punto medio del subarreglo actual
    - Divide el problema en dos partes iguales
3. **Llamadas Recursivas**:
    
    ```c
int suma_izquierda = SumaMaximaSubarreglo(arreglo, izquierda, medio);
int suma_derecha = SumaMaximaSubarreglo(arreglo, medio + 1, derecha);
```
    
    - Resuelve recursivamente cada mitad
    - Mantiene la estructura divide y vencerás
4. **Selección del Máximo**:
    
    ```c
if (suma_izquierda >= suma_derecha && suma_izquierda >= suma_cruzada) {
    return suma_izquierda;
}
```
    
    - Compara las tres posibles soluciones
    - Retorna el máximo encontrado

### Código final

```c 
#include <stdio.h>

int SumaMediaMaxima(int arreglo[], int izquierda, int medio, int derecha) {
    int suma = 0;
    int suma_izquierda = -2147483648;
    for (int i = medio; i >= izquierda; i--) {
        suma += arreglo[i];
        if (suma > suma_izquierda) {
            suma_izquierda = suma;
        }
    }
  
    suma = 0;
    int suma_derecha = -2147483648;
    for (int i = medio + 1; i <= derecha; i++) {
        suma += arreglo[i];
        if (suma > suma_derecha) {
            suma_derecha = suma;
        }
    }
    return suma_izquierda + suma_derecha;
}
  
int SumaMaximaSubarreglo(int arreglo[], int izquierda, int derecha) {
    if (izquierda == derecha) {
        return arreglo[izquierda];
    }
  
    int medio = (izquierda + derecha) / 2;
  
    int suma_izquierda = SumaMaximaSubarreglo(arreglo, izquierda, medio);
    int suma_derecha = SumaMaximaSubarreglo(arreglo, medio + 1, derecha);
    int suma_cruzada = SumaMediaMaxima(arreglo, izquierda, medio, derecha);
  
    if (suma_izquierda >= suma_derecha && suma_izquierda >= suma_cruzada) {
        return suma_izquierda;
    } else if (suma_derecha >= suma_izquierda && suma_derecha >= suma_cruzada) {
        return suma_derecha;
    } else {
        return suma_cruzada;
    }
}

int main() {
    int N;
    scanf("%d", &N);
    int arreglo[N];
    for (int i = 0; i < N; i++) {
        scanf("%d", &arreglo[i]);
    }

    int suma_maxima = SumaMaximaSubarreglo(arreglo, 0, N - 1);
    printf("%d\n", suma_maxima);

    return 0;
}
```
![[Pasted image 20241103215229.png]]

# Análisis del Algoritmo de Conteo de Inversiones

## Implementación mediante Merge Sort

El presente código implementa una solución al problema de conteo de inversiones en un arreglo utilizando una modificación del algoritmo de Merge Sort. Una inversión se define cuando para dos índices i,j donde i < j, se cumple que arr[i] > arr[j]. La solución aprovecha la naturaleza del ordenamiento por mezcla para contar estas inversiones durante el proceso de fusión.

### Fundamento Teórico

La implementación se basa en la observación de que durante la fase de mezcla del Merge Sort, cuando un elemento del subarreglo derecho es menor que un elemento del subarreglo izquierdo, esto implica que ese elemento forma una inversión con todos los elementos restantes del subarreglo izquierdo. Esta observación nos permite contar las inversiones mientras realizamos el ordenamiento.

La relación recurrente que gobierna este proceso se puede expresar matemáticamente como: $$T(n) = 2T(n/2) + O(n)$$ Donde T(n) representa el tiempo de ejecución para un arreglo de tamaño n. El término O(n) corresponde al tiempo de la operación de mezcla y conteo.

### Casos Base

La recursión se maneja con los siguientes casos base: $$T(1) = 0$$ (un solo elemento no tiene inversiones) $$T(2) = \begin{cases} 1 & \text{si } a[0] > a[1] \ 0 & \text{si } a[0] \leq a[1] \end{cases}$$

### Análisis de Complejidad

La complejidad del algoritmo se puede analizar considerando su estructura recursiva:

1. **Árbol de Recursión**:
    - Cada llamada divide el problema en dos subproblemas de tamaño n/2
    - La profundidad del árbol es log n
    - En cada nivel se realiza trabajo O(n) para la mezcla y conteo
2. **Complejidad Temporal**:
    - Sea T(n) el tiempo para entrada n
    - T(n) = 2T(n/2) + O(n)
    - Por el teorema maestro, esto resulta en O(n log n)

### Construcción del Código

El siguiente código implementa una solución mediante Merge Sort para contar el número de inversiones en un arreglo. Esta implementación hace uso eficiente de la fase de mezcla para realizar el conteo mientras ordena el arreglo.

#### Estructura del Código
```c
long long merge_and_count(int arr[], int temp[], int left, int mid, int right) {
    int i = left;
    int j = mid + 1;
    int k = left;
    long long inv_count = 0;
    
    while (i <= mid && j <= right) {
        if (arr[i] <= arr[j]) {
            temp[k++] = arr[i++];
        } else {
            temp[k++] = arr[j++];
            inv_count += (mid - i + 1);  // Conteo de inversiones
        }
    }
    // Completar con elementos restantes
    while (i <= mid) temp[k++] = arr[i++];
    while (j <= right) temp[k++] = arr[j++];
    
    // Copiar al arreglo original
    for (i = left; i <= right; i++)
        arr[i] = temp[i];
        
    return inv_count;
}
```

La función `merge_and_count` es el corazón del algoritmo, combinando la funcionalidad de mezcla con el conteo de inversiones. La función de ordenamiento recursiva implementa la estrategia divide y vencerás:

```c
long long merge_sort_and_count(int arr[], int temp[], int left, int right) {
    long long inv_count = 0;
    if (left < right) {
        int mid = (left + right) / 2;
        inv_count += merge_sort_and_count(arr, temp, left, mid);
        inv_count += merge_sort_and_count(arr, temp, mid + 1, right);
        inv_count += merge_and_count(arr, temp, left, mid, right);
    }
    return inv_count;
}
```

#### Manejo de Casos Múltiples

El programa principal está diseñado para manejar múltiples casos de prueba:
```c
int main() {
    int t;
    scanf("%d", &t);
    
    while (t--) {
        int n;
        scanf("%d", &n);
        
        int *arr = (int *)malloc(n * sizeof(int));
        int *temp = (int *)malloc(n * sizeof(int));
        
        for (int i = 0; i < n; i++)
            scanf("%d", &arr[i]);
            
        long long result = merge_sort_and_count(arr, temp, 0, n - 1);
        printf("%lld\n", result);
        
        free(arr);
        free(temp);
    }
    return 0;
}
```

### Código final
```c
#include <stdio.h>
#include <stdlib.h>

long long merge_and_count(int arr[], int temp[], int left, int mid, int right) {
    int i = left, j = mid + 1, k = left;
    long long inv_count = 0;
    
    while (i <= mid && j <= right) {
        if (arr[i] <= arr[j])
            temp[k++] = arr[i++];
        else {
            temp[k++] = arr[j++];
            inv_count += (mid - i + 1);
        }
    }
    
    while (i <= mid) temp[k++] = arr[i++];
    while (j <= right) temp[k++] = arr[j++];
    
    for (i = left; i <= right; i++)
        arr[i] = temp[i];
        
    return inv_count;
}

long long merge_sort_and_count(int arr[], int temp[], int left, int right) {
    long long inv_count = 0;
    if (left < right) {
        int mid = (left + right) / 2;
        inv_count += merge_sort_and_count(arr, temp, left, mid);
        inv_count += merge_sort_and_count(arr, temp, mid + 1, right);
        inv_count += merge_and_count(arr, temp, left, mid, right);
    }
    return inv_count;
}

int main() {
    int t;
    scanf("%d", &t);
    while (t--) {
        int n;
        scanf("%d", &n);
        int *arr = (int *)malloc(n * sizeof(int));
        int *temp = (int *)malloc(n * sizeof(int));
        for (int i = 0; i < n; i++)
            scanf("%d", &arr[i]);
        long long result = merge_sort_and_count(arr, temp, 0, n - 1);
        printf("%lld\n", result);
        free(arr);
        free(temp);
    }
    return 0;
}
```

![[Pasted image 20241103223006.png]]