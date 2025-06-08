# Camino de Costo Mínimo en una Matriz (Bacterias)

## Explicación de la Solución

Este problema utiliza programación dinámica para encontrar el camino de costo mínimo desde la esquina superior izquierda (0,0) hasta la esquina inferior derecha (m-1,n-1) de una matriz, moviéndose solo hacia abajo o hacia la derecha.

La solución se basa en la siguiente idea:

- Para llegar a cualquier celda (i,j), solo podemos venir desde:
    1. La celda de arriba (i-1,j)
    2. La celda de la izquierda (i,j-1)
- El costo mínimo para llegar a (i,j) será el valor de la celda actual más el mínimo entre el costo para llegar a las celdas desde donde podemos venir.

La recurrencia DP se define como: $$dp[i][j] = grid[i][j] + min(dp[i-1][j], dp[i][j-1])$$
## Análisis de Complejidad

### Identificación del Patrón

El algoritmo utiliza dos ciclos anidados principales, además de dos ciclos iniciales para los casos base. La estructura es iterativa, no recursiva, por lo que no necesitamos resolver una recurrencia.

### Desarrollo del Análisis

1. **Inicialización de casos base:**
    - Para la primera fila: Un ciclo de 1 a m $$T_{fila} = O(m)$$
    - Para la primera columna: Un ciclo de 1 a n $$T_{columna} = O(n)$$
2. **Ciclos principales:**
    
    ```c
for (int i = 1; i < m; i++) {
    for (int j = 1; j < n; j++) {
        dp[i][j] = grid[i][j] + min(dp[i-1][j], dp[i][j-1]);
    }
}
```
    
    Esto genera la siguiente sumatoria: $$T_{principal} = \sum_{i=1}^{m-1} \sum_{j=1}^{n-1} 1 = (m-1)(n-1)$$
3. **Complejidad total:** $$T(m,n) = O(m) + O(n) + O(m \cdot n)$$ Como los términos $O(m)$ y $O(n)$ son dominados por $O(m \cdot n)$, la complejidad final es: $$T(m,n) = O(m \cdot n)$$
### Justificación Final

La complejidad es $O(m \cdot n)$ porque:

1. Cada celda de la matriz dp se calcula exactamente una vez
2. Para cada cálculo se realiza una operación constante (suma y mínimo)
3. La matriz tiene dimensiones m × n
4. Las inicializaciones lineales son dominadas por el término cuadrático

Por lo tanto, el algoritmo tiene una complejidad temporal de $$O(m \cdot n)$$
## Código
```c
#include <stdio.h> #include <limits.h>

#define MAX 101

int min(int a, int b) { 
	return (a < b) ? a : b; 
}

void calcularMinimoCompuesto(int m, int n, int grid[MAX][MAX], int dp[MAX][MAX]) 
{ 
	dp[0][0] = grid[0][0];

	for (int i = 1; i < m; i++) 
	{ 
		dp[i][0] = dp[i-1][0] + grid[i][0]; 
	}

	for (int j = 1; j < n; j++) 
	{ 
		dp[0][j] = dp[0][j-1] + grid[0][j]; 
	}

	for (int i = 1; i < m; i++) 
	{ 
		for (int j = 1; j < n; j++) 
		{ 
			dp[i][j] = grid[i][j] + min(dp[i-1][j], dp[i][j-1]); 
		} 
	} 
}

int main() { 
	int m, n; 
	int grid[MAX][MAX]; 
	int dp[MAX][MAX];

	scanf("%d", &m); 
	scanf("%d", &n);

	for (int i = 0; i < m; i++) 
	{ 
		for (int j = 0; j < n; j++) 
		{ 
			scanf("%d", &grid[i][j]); 
		} 
	}

	calcularMinimoCompuesto(m, n, grid, dp);

	printf("%d\n", dp[m-1][n-1]);

	return 0; 
}
```
![[Pasted image 20241117181113.png]]
# Problema de la Mochila (Knapsack Problem)

## Explicación de la Solución

Este es el clásico problema de la mochila, implementado con programación dinámica usando memorización (top-down). El objetivo es maximizar el valor total de los objetos seleccionados sin exceder la capacidad de la mochila.

La solución recursiva se basa en dos decisiones para cada ítem:

1. No tomar el ítem actual
2. Tomar el ítem actual (si es posible por el peso)

La función de recurrencia toma la mejor de estas opciones:

- Si el ítem actual pesa más que la capacidad restante, no se puede tomar
- Si se puede tomar, elegimos el máximo entre tomarlo y no tomarlo

## Análisis de Complejidad

### Identificación de la Recurrencia

La recurrencia base es: $$T(n,W) = T(n-1,W) + T(n-1,W-w_i) + c$$

Donde:

- n es el número de elementos
- W es la capacidad de la mochila
- $w_i$ es el peso del elemento actual
- c es una constante

### Desarrollo del Análisis

1. **Identificación del tipo de recurrencia:** Esta es una recurrencia no homogénea y no lineal, ya que:
    - Tiene dos llamadas recursivas con parámetros diferentes
    - Los parámetros se reducen de manera no uniforme
2. **Análisis del árbol de recursión:** Para cada estado (n,W), tenemos:
    - Una llamada con n-1 elementos y la misma capacidad
    - Una posible llamada con n-1 elementos y capacidad reducida
3. **Número de subproblemas únicos:**
    - Para n: valores de 1 a N
    - Para W: valores de 0 a S
    - Total de estados posibles: $N \times S$
4. **Trabajo por subproblema:** En cada llamada recursiva:
    - Verificación de casos base: O(1)
    - Verificación de memorización: O(1)
    - Cálculo del máximo: O(1)
5. **Análisis de la memorización:**
    - Cada estado (n,W) se calcula exactamente una vez
    - Las llamadas subsecuentes al mismo estado retornan el valor memorizado en O(1)
    - La matriz dp almacena resultados para cada combinación de n y W

### Resolución Final

La complejidad se puede calcular como: $$T(N,S) = O(N \times S)$$

Esto se justifica porque:

1. Hay $N \times S$ estados posibles
2. Cada estado se calcula una sola vez debido a la memorización
3. El trabajo por estado es O(1)
4. Una vez calculado, cada estado se recupera en O(1)

Por lo tanto, aunque la recurrencia parece generar un árbol exponencial, la memorización reduce la complejidad a $$O(N \times S)$$ donde N es el número de elementos y S es la capacidad de la mochila.

## Código

```c
#include <stdio.h>
#include <string.h>

#define MAX_ITEMS 2000
#define MAX_CAPACITY 2000

int dp[MAX_ITEMS + 1][MAX_CAPACITY + 1];
int weights[MAX_ITEMS + 1];
int values[MAX_ITEMS + 1];
  
int max(int a, int b) {
    return (a > b) ? a : b;
}

  

int knapsack(int n, int capacity) {
    if (n == 0 || capacity == 0)
        return 0;
    if (dp[n][capacity] != -1)
        return dp[n][capacity];
    if (weights[n - 1] > capacity)
        return dp[n][capacity] = knapsack(n - 1, capacity);
    else
        return dp[n][capacity] = max(knapsack(n - 1, capacity), values[n - 1] + knapsack(n - 1, capacity - weights[n - 1]));
}
  
int main() {
    int S, N;
    scanf("%d %d", &S, &N);
  
    for (int i = 0; i < N; i++) {
        scanf("%d %d", &weights[i], &values[i]);
    }
  
    memset(dp, -1, sizeof(dp));
  
    printf("%d\n", knapsack(N, S));
  
    return 0;
}
```
![[Pasted image 20241117181651.png]]
![[Pasted image 20241117181658.png]]

# Recolección Máxima de Piedras en Cuadrícula

## Explicación de la Solución

Este problema utiliza programación dinámica recursiva con memorización para encontrar la cantidad máxima de piedras que se pueden recolectar comenzando desde cualquier posición en la fila superior y moviéndose hacia abajo, con la posibilidad de moverse en diagonal.

Para cada posición (row,col), podemos:

1. Movernos directamente hacia abajo (row+1, col)
2. Movernos en diagonal hacia la izquierda (row+1, col-1)
3. Movernos en diagonal hacia la derecha (row+1, col+1)

La solución recursiva elige el máximo de estas tres opciones y suma el valor de la celda actual.

## Análisis de Complejidad

### Identificación de la Recurrencia

La recurrencia base es: $$T(n,m) = 3T(n-1,m) + c$$ Donde:

- n es la altura restante (h-row)
- m es el ancho de la cuadrícula
- c es el trabajo constante por llamada

### Desarrollo del Análisis

1. **Estructura de la recurrencia:**
    
```c
maxStones(row, col) = grid[row][col] + max(
    maxStones(row+1, col),
    maxStones(row+1, col-1),
    maxStones(row+1, col+1)
)
```
    
2. **Casos base:** $$T(0,m) = 1$$ $$T(n,0) = 1$$
3. **Análisis sin memorización:**
    - Cada llamada genera 3 llamadas recursivas
    - La profundidad máxima es h (altura)
    - Sin memorización, tendríamos un árbol de recursión con: $$T(n) = 3T(n-1) + c$$Esta es una recurrencia homogénea lineal. Resolvámosla: $$T(n) = 3T(n-1) + c$$ $$T(n-1) = 3T(n-2) + c$$ Expandiendo: $$T(n) = 3(3T(n-2) + c) + c$$ $$T(n) = 3^2T(n-2) + 3c + c$$ $$T(n) = 3^2(3T(n-3) + c) + 3c + c$$ $$T(n) = 3^3T(n-3) + 3^2c + 3c + c$$ El patrón general sería: $$T(n) = 3^n + c(3^{n-1} + 3^{n-2} + ... + 3 + 1)$$ $$T(n) = O(3^n)$$
4. **Análisis con memorización:** Con memorización, cada estado (row,col) se calcula una sola vez:
    - Total de estados posibles: $h \times w$
    - Trabajo por estado: O(1)
    - Llamadas totales con memorización: O(h × w)
5. **Análisis del bucle principal:**
    
    ```c
for (int col = 0; col < w; col++) {
    maxStonesCollected = MAX(maxStonesCollected, maxStones(grid, h, w, 0, col,dp));
}
```
    Este bucle añade un factor de w al análisis.

### Resolución Final

1. **Sin memorización:** La complejidad sería $$O(3^h)$$ por cada columna inicial, resultando en $$O(w \cdot 3^h)$$
2. **Con memorización:**
    - Cada estado se calcula una vez: O(h × w)
    - El bucle principal: O(w)
    - Trabajo por estado: O(1)

La complejidad final con memorización es: $$T(h,w) = O(h \cdot w)$$
## Código
```c
#include <stdio.h>
#include <stdlib.h>
  
#define MAX(a, b) ((a) > (b) ? (a) : (b))
#define MAX3(a, b, c) (MAX(MAX(a, b), c))
  
int maxStones(int grid, int h, int w, int row, int col, int dp) {
    if (row == h) return 0;
    if (col < 0 || col >= w) return 0;
    if (dp[row][col] != -1) return dp[row][col];
  
    int down = maxStones(grid, h, w, row + 1, col, dp);
    int downLeft = maxStones(grid, h, w, row + 1, col - 1, dp);
    int downRight = maxStones(grid, h, w, row + 1, col + 1, dp);
  
    dp[row][col] = grid[row][col] + MAX3(down, downLeft, downRight);
    return dp[row][col];
}
  
int main() {
    int T;
    scanf("%d", &T);
  
    while (T--) {
        int h, w;
        scanf("%d", &h);
        scanf("%d", &w);
  
        int grid = (int )malloc(h * sizeof(int *));
        int dp = (int )malloc(h * sizeof(int *));
        for (int i = 0; i < h; i++) {
            grid[i] = (int *)malloc(w * sizeof(int));
            dp[i] = (int *)malloc(w * sizeof(int));
            for (int j = 0; j < w; j++) {
                scanf("%d", &grid[i][j]);
                dp[i][j] = -1;
            }
        }
  
        int maxStonesCollected = 0;
        for (int col = 0; col < w; col++) {
            maxStonesCollected = MAX(maxStonesCollected, maxStones(grid, h, w, 0,col, dp));
        }
  
        printf("%d\n", maxStonesCollected);
  
        for (int i = 0; i < h; i++) {
            free(grid[i]);
            free(dp[i]);
        }
        free(grid);
        free(dp);
    }
  
    return 0;
}
```
![[Pasted image 20241117181651.png]]![[Pasted image 20241117181658.png]]

# Subsecuencia Creciente Más Larga (LIS - Longest Increasing Subsequence)

## Explicación de la Solución

Este problema utiliza programación dinámica recursiva con memorización para encontrar la longitud de la subsecuencia creciente más larga en un arreglo.

La idea principal es:

- Para cada posición i, encontrar la LIS que termina en el elemento arr[i]
- Para cada elemento, comparar con todos los elementos anteriores
- Si encontramos un elemento menor, podemos extender esa subsecuencia

## Análisis de Complejidad

### Identificación de la Recurrencia

La recurrencia base es: $$T(n) = \sum_{i=1}^{n-1} T(i) + c \cdot (n-1)$$

Donde:

- n es el tamaño del subproblema actual
- El sumatorio representa las llamadas recursivas para cada i menor que n
- c·(n-1) es el trabajo del bucle for en cada nivel

### Desarrollo del Análisis

1. **Análisis sin memorización:** Expandamos la recurrencia: $$T(n) = \sum_{i=1}^{n-1} T(i) + c(n-1)$$ $$T(n-1) = \sum_{i=1}^{n-2} T(i) + c(n-2)$$ Restando estas ecuaciones: $$T(n) - T(n-1) = T(n-1) + c$$ $$T(n) = 2T(n-1) + c$$ Esta es una recurrencia lineal homogénea con término no homogéneo. Resolviendo por expansión: $$T(n) = 2(2T(n-2) + c) + c$$ $$T(n) = 2^2T(n-2) + 2c + c$$ $$T(n) = 2^2(2T(n-3) + c) + 2c + c$$ $$T(n) = 2^3T(n-3) + 2^2c + 2c + c$$ El patrón general es: $$T(n) = 2^nT(0) + c(2^{n-1} + 2^{n-2} + ... + 2 + 1)$$ $$T(n) = O(2^n)$$
2. **Análisis con memorización:** Con memorización, cada subproblema se resuelve una sola vez:
    - Número total de subproblemas: n
    - Para cada subproblema i:
        - Se hace un bucle de 1 a i-1
        - Trabajo en el bucle: O(1)Para el subproblema i, el trabajo es O(i). Sumando el trabajo para todos los subproblemas: $$T(n) = \sum_{i=1}^n O(i) = O(n^2)$$
3. **Justificación de la complejidad cuadrática:**
    
   ```c 
for (int i = 1; i < n; i++) {
    res = lis_helper(arr, i, max_ref, memo);
    if (arr[i-1] < arr[n-1] && res + 1 > max_ending_here) {
        max_ending_here = res + 1;
    }
}
```
    - Cada estado memorizado requiere O(n) operaciones
    - Hay n estados en total
    - Por lo tanto, el trabajo total es O(n²)

### Resolución Final

1. **Sin memorización:** La complejidad sería exponencial: $$O(2^n)$$
2. **Con memorización:** La complejidad es cuadrática: $$O(n^2)$$

La memorización reduce drásticamente la complejidad de exponencial a cuadrática porque:

- Cada estado se calcula una sola vez
- Para cada estado, se realiza un trabajo lineal (el bucle for)
- El número total de estados es n

Por lo tanto, la complejidad temporal final del algoritmo es $$O(n^2)$$
## Código
```c
#include <stdio.h>
#include <stdlib.h>
  
int lis_helper(int arr[], int n, int *max_ref, int memo[]) {
    if (n == 1) {
        return 1;
    }
  
    if (memo[n-1] != -1) {
        return memo[n-1];
    }
  
    int res, max_ending_here = 1;
    for (int i = 1; i < n; i++) {
        res = lis_helper(arr, i, max_ref, memo);
        if (arr[i-1] < arr[n-1] && res + 1 > max_ending_here) {
            max_ending_here = res + 1;
        }
    }
  
    if (*max_ref < max_ending_here) {
        *max_ref = max_ending_here;
    }
  
    memo[n-1] = max_ending_here;
    return max_ending_here;
}
  
int longest_increasing_subsequence(int arr[], int n) {
    int max = 1;
    int *memo = (int *)malloc(n * sizeof(int));
    for (int i = 0; i < n; i++) {
        memo[i] = -1;
    }
    lis_helper(arr, n, &max, memo);
    free(memo);
    return max;
}
  
int main() {
    int n;
    scanf("%d", &n);
  
    int arr[n];
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }
  
    int result = longest_increasing_subsequence(arr, n);
    printf("%d\n", result);
  
    return 0;
}
```

![[Pasted image 20241117181651.png]]![[Pasted image 20241117181658.png]]
# Subsecuencia Común Más Larga (LCS - Longest Common Subsequence)

## Explicación de la Solución

Este problema utiliza programación dinámica recursiva con memorización para encontrar la longitud de la subsecuencia común más larga entre dos cadenas.

La solución se basa en dos casos:

1. Si los caracteres actuales son iguales, incluimos el carácter y continuamos con el resto de ambas cadenas
2. Si son diferentes, tomamos el máximo entre omitir un carácter de cualquiera de las dos cadenas

## Análisis de Complejidad

### Identificación de la Recurrencia

La recurrencia base es: $$T(m,n) = \begin{cases} 1 & \text{si } m = 0 \text{ o } n = 0 \ T(m-1,n-1) + c & \text{si } A[m] = B[n] \ T(m-1,n) + T(m,n-1) + c & \text{si } A[m] \neq B[n] \end{cases}$$

Donde:

- m y n son las longitudes de las subcadenas actuales
- c es el trabajo constante por llamada

### Desarrollo del Análisis

1. **Análisis sin memorización:** En el peor caso (cuando todos los caracteres son diferentes): $$T(m,n) = T(m-1,n) + T(m,n-1) + c$$ Esta es una recurrencia no lineal. Resolvamos para entender la complejidad: Para un nivel dado con coordenadas (m,n), se generan dos llamadas:
    
    - T(m-1,n)
    - T(m,n-1)
    
    El árbol de recursión tendrá:
    - Profundidad máxima: m + n (cada llamada reduce m o n en 1)
    - En cada nivel, el número de nodos se duplicaPor lo tanto, sin memorización: $$T(m,n) = O(2^{m+n})$$
2. **Análisis con memorización:** Con memorización, cada estado (m,n) se calcula una sola vez:
    
    - Número total de estados posibles: m × n
    - Trabajo por estado: O(1)
    
    Para cada estado (m,n):
    ```c
if (A[m - 1] == B[n - 1])
    memo[m][n] = 1 + lcs_recursive_memo(A, B, m - 1, n - 1, memo);
else
    memo[m][n] = max(lcs_recursive_memo(A, B, m, n - 1, memo), 
                     lcs_recursive_memo(A, B, m - 1, n, memo));
```
    
3. **Análisis de los estados:**
    - Estados totales: (m+1) × (n+1) incluyendo casos base
    - Cada estado se calcula exactamente una vez
    - Trabajo por estado: O(1)
4. **Espacio de estados:** La matriz de memorización tiene dimensiones: $$(m+1) \times (n+1)$$
### Resolución Final

1. **Sin memorización:** La complejidad sería exponencial: $$O(2^{m+n})$$
2. **Con memorización:**
    - Total de estados: O(m × n)
    - Trabajo por estado: O(1)
    - Cada estado se visita una vez

Por lo tanto, la complejidad temporal con memorización es: $$O(m \times n)$$

La memorización reduce la complejidad de exponencial a polinomial porque:

1. Elimina cálculos redundantes
2. Cada estado (m,n) se calcula una sola vez
3. El acceso a estados ya calculados es O(1)
4. El número total de estados distintos es m × n

## Código
```c
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
  
int max(int a, int b) {
    return (a > b) ? a : b;
}
  
int lcs_recursive_memo(char *A, char *B, int m, int n, int **memo) {
    if (m == 0 || n == 0)
        return 0;
    if (memo[m][n] != -1)
        return memo[m][n];
    if (A[m - 1] == B[n - 1])
        memo[m][n] = 1 + lcs_recursive_memo(A, B, m - 1, n - 1, memo);
    else
        memo[m][n] = max(lcs_recursive_memo(A, B, m, n - 1, memo), lcs_recursive_memo(A, B, m - 1, n, memo));
    return memo[m][n];
}
  
int main() {
    char A[1000], B[1000];
  
    scanf("%s", A);
    scanf("%s", B);
  
    int m = strlen(A);
    int n = strlen(B);
  
    int memo = (int )malloc((m + 1) * sizeof(int *));
    for (int i = 0; i <= m; i++) {
        memo[i] = (int *)malloc((n + 1) * sizeof(int));
        for (int j = 0; j <= n; j++) {
            memo[i][j] = -1;
        }
    }
  
    printf("%d\n", lcs_recursive_memo(A, B, m, n, memo));
  
    for (int i = 0; i <= m; i++) {
        free(memo[i]);
    }
    free(memo);
  
    return 0;
}
```

![[Pasted image 20241117181651.png]]![[Pasted image 20241117181658.png]]