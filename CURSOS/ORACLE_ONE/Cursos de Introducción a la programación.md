## Selectores en JavaScript

Para seleccionar elementos del HTML y modificarlos con JavaScript:

*   Se define una variable que seleccionará una etiqueta HTML [1].
*   Es posible seleccionar elementos con **cualquier etiqueta** HTML [1].

**Ejemplo de selección y modificación de un título:**

```js
let titulo = document.querySelector("h1"); // Selecciona la primera etiqueta <h1> [1]
````

Ahora, para cambiar el contenido de un elemento en el HTML, se puede usar la propiedad `innerHTML`:

```js
titulo.innerHTML = "Nuevo titulo"; // Modifica el contenido HTML del elemento seleccionado [1]
```

## Funciones básicas de consola y para interactuar con el usuario

• Para imprimir mensajes en la consola del navegador, se usa `console.log()`:

• Para pedir información al usuario, `prompt()` abre un cuadro de texto donde el usuario puede introducir datos. El valor ingresado puede guardarse en una variable.

## Eventos y Funciones en JavaScript

La forma en que JavaScript selecciona elementos del HTML es clave para gestionar eventos en nuestra página web.

• Ejemplo de un elemento HTML típico, como un botón:

• La palabra clave `on` se refiere a los **eventos** en JavaScript.

-  `onclick` es un tipo de evento que se dispara al hacer clic en un elemento.
-  Cuando se usa `onclick` en HTML, se le asigna el código JavaScript que debe ejecutarse:
- _(Nota: onclick = "código Java Script", indica la asignación directa de código o una llamada a función dentro de las comillas.)_

Se recomienda utilizar **Camel case** (por ejemplo, `nombreFuncion`) para nombrar las funciones en JavaScript. Al gestionar eventos, lo ideal es que el código JavaScript que responde al evento sea una función ya declarada en tu archivo JavaScript.

### Declaración de funciones

Las funciones en JavaScript se declaran de la siguiente manera:

```js
function nombreFuncion() {
    // El cuerpo de la función contiene el código a ejecutar [2]
}
```

• JavaScript **no requiere una función** **main** como punto de entrada, a diferencia de otros lenguajes de programación.

• Puedes llamar a las funciones desde cualquier parte, incluso fuera de un bloque de código.

#### Concepto de Hoisting

Las notas describen el concepto de "Hoisting" de la siguiente manera:

• Hoisting: Implica que, no importa dónde declares las variables (y funciones), estas siempre estarán disponibles en su ámbito antes de su declaración física en el código.

## Generar un número aleatorio sin decimales

Para generar un número aleatorio entero, por ejemplo, entre 1 y 10:

```js
Math.floor(Math.random() * 10) + 1; // Genera un número aleatorio entero entre 1 y 10 [2]
```

## Operador de Comparación Estricta

La diferencia entre los operadores de comparación `===` y `==` es importante:

• `===` Se utiliza para comparar si dos valores son iguales, pero a diferencia de `==`, también exige que sean **del mismo tipo de dato** para que la comparación sea verdadera.

## Limpiar un campo de texto

Para borrar el contenido de un campo de texto (como un `<input type="text">` o `<textarea>`), asumiendo que el campo tiene un `id`:

• Primero, selecciona el elemento utilizando su `id`:

• Luego, asigna una cadena vacía a su propiedad `value`:

## Habilitar/Deshabilitar elementos HTML

Los elementos HTML pueden tener una propiedad `disabled` que los desactiva. Para quitar esta propiedad y, por lo tanto, habilitar un elemento (como un botón):

```js
document.getElementById('Id_boton').removeAttribute('disabled'); // Elimina el atributo 'disabled' del elemento con id 'Id_boton' [3]
```

## Template Strings (Cadenas de Plantilla)

Las cadenas de plantilla son una característica de JavaScript que permite incrustar expresiones y variables directamente dentro de cadenas de texto.

• Se definen utilizando **comillas al revés** (backticks: `` ` ``), en lugar de comillas simples o dobles.

• Ejemplo de uso, donde `nombre` es una variable:

## Arreglos (Arrays)

Los arreglos son estructuras de datos que permiten almacenar una colección de elementos.

• Declaración de un arreglo vacío:

    ◦ Los elementos dentro de un arreglo se separan por comas.

### Métodos comunes de Arreglos

• **push()**: Este método se utiliza para añadir uno o más elementos al **final** de un arreglo.

• **.length**: Esta propiedad devuelve el número de elementos que contiene un arreglo, es decir, su tamaño.

### Acceder a elementos de un Arreglo

• Los elementos de un arreglo se acceden mediante un índice numérico. La primera posición (el primer elemento) de un arreglo siempre es el índice `0`.

   ◦ Los índices van de `0` a `n-1`, donde `n` es el tamaño total del arreglo.

• Para obtener un elemento específico utilizando su índice:

### Verificar la existencia de un elemento en un Arreglo

• **.includes()**: Este método determina si un arreglo incluye un determinado elemento, devolviendo `true` o `false` según si el elemento está presente o no.