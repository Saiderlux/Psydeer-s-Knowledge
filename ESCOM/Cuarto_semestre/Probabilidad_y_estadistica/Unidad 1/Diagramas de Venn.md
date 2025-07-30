# Diagramas de Venn en Probabilidad

Los **diagramas de Venn** son herramientas visuales muy útiles para representar eventos en un espacio muestral. Permiten identificar las relaciones entre eventos —como la unión, intersección y complemento— y facilitan la aplicación de fórmulas probabilísticas.

## 1. Representación Básica

Considera dos eventos, $A$ y $B$, en un espacio muestral. Su representación mediante un diagrama de Venn es la siguiente:

$$
\text{Diagrama:} \quad \begin{array}{c}
\text{[ }A\text{ ]} \quad \text{[ }B\text{ ]}
\end{array}
$$
```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Cuarto_semestre/Probabilidad_y_estadistica/ANEXOS/Ink/Drawing/2025.4.10 - 18.08pm.drawing",
	"width": 502,
	"aspectRatio": 1.5998937134852864
}
```

Donde:
- La **intersección** $A \cap B$ representa los elementos comunes a ambos eventos.
- El **complemento** $A^c$ (o $B^c$) representa los elementos que no están en $A$ (o $B$).

## 2. Unión de Eventos

La unión de los eventos, $A \cup B$, se representa como la suma de las áreas ocupadas por $A$ y $B$, contando **una sola vez** la intersección:

$$
P(A \cup B) = P(A) + P(B) - P(A \cap B)
$$

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Cuarto_semestre/Probabilidad_y_estadistica/ANEXOS/Ink/Drawing/2025.4.10 - 18.09pm.drawing",
	"width": 508,
	"aspectRatio": 1.7800436441624516
}
```


En el diagrama, $A \cup B$ abarca todos los elementos dentro de las figuras correspondientes a $A$ y $B$.

## 3. Complemento de la Unión

El complemento del evento unión se expresa como:

$$
P((A \cup B)^c) = 1 - P(A \cup B)
$$

```handdrawn-ink
{
	"versionAtEmbed": "0.3.4",
	"filepath": "Cuarto_semestre/Probabilidad_y_estadistica/ANEXOS/Ink/Drawing/2025.4.10 - 18.13pm.drawing",
	"width": 478,
	"aspectRatio": 1.6742535442032924
}
```

Este representa la región fuera de las figuras de $A$ y $B$, es decir, aquellos elementos que **no pertenecen ni a $A$ ni a $B$**.

## 4. Diagramas de Venn con Más de Dos Eventos

Para tres eventos, $A$, $B$ y $C$, se utiliza un diagrama de Venn con tres círculos que se superponen parcialmente. Este diagrama permite distinguir varias regiones:
- Regiones donde sólo ocurre un evento (por ejemplo, "solo $A$").
- Regiones donde ocurren **exactamente dos** eventos (por ejemplo, $A \cap B \setminus C$).
- La región donde ocurren los **tres** eventos simultáneamente: $A \cap B \cap C$.

![[Diagramas]]


La **fórmula de inclusión-exclusión** para tres eventos es:

$$
P(A\cup B\cup C) = P(A) + P(B) + P(C) - \Big[ P(A\cap B) + P(A\cap C) + P(B\cap C) \Big] + P(A\cap B\cap C)
$$

Esta fórmula corrige el conteo múltiple de las intersecciones.


![[Diagramas de Venn 2025-04-10 18.21.59.excalidraw]]

