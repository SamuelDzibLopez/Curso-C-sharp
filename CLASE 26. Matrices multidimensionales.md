# 26. Matrices multidimensionales.

	Los Arrays son conocidos como "matrices unidimensionales", debido a que tienen una sola dimensión (de ni a izquierda) por recorrer.

	Las matrices multidimencionales son Arrays que contienen arrays dentro de si, haciendo que estas matrices, contengas mas de una dimensión (filas y columnas).

Una ***matriz multidimensional*** es básicamente una matriz de matrices. Una matriz que contiene en cada uno de sus elementos internos otra matriz.

Las matrices pueden tener cualquier número de dimensiones. Los más comunes son las matrices bidimensionales (2D).

---
## Matrices bidimensionales.

Para crear una matriz 2D, agregue cada matriz dentro de su propio conjunto de llaves e inserte una coma (`,`) dentro de los corchetes.

```csharp
int[,] numbers = { {1, 4, 2}, {3, 6, 8} };
```

***Nota:*** Si entendemos bien este código, es solo un `array` con ***2 elementos internos***, los cuales contienen un ``array`` por cada uno, de ***3 elementos internos*** cada uno.

	La coma simple especifica que la matriz es bidimensional ([,]). Una matriz tridimensional tendría dos comas: int[,,].

---
## Acceder a elementos de una matriz 2D.

Para acceder a un elemento de una matriz bidimensional, debe especificar dos índices: uno para la matriz y otro para el elemento interno dentro de esa matriz.

O mejor aún, con la visualización de la tabla en mente; uno para la fila y otro para la columna.

```csharp
int[,] numbers = { {1, 4, 2}, {3, 6, 8} };
Console.WriteLine(numbers[0, 1]);  // Salida: 4
```

***Nota:*** En otras palabras, seleccionamos el primer elemento (`[0]`), el cual es `{1, 4, 2}`, y dentro de este, buscamos el segundo elemento (`[1]`), el cual es `4`.

***Nota:*** Recordemos que las posiciones de los elementos dentro de los `arrays` empiezan con `0`.

Esta lógica es la misma para matrices de más dimensiones.

---
## Modificar elementos de una matriz 2D.

También puede modificar el valor de un ***elemento*** dentro de ***matrices multidimensionales***.

```csharp
int[,] numbers = { {1, 4, 2}, {3, 6, 8} };
numbers[0, 0] = 5;  // Cambiar valor a 5
Console.WriteLine(numbers[0, 0]); // Salida: 5. 1 fue cambiado por 5
```

***Nota:*** En el código anterior, se selecciona el primero elemento el cual es `{1, 4, 2}` y de este, se selecciona el primer elemento, el cual es `1`, a este se cambia su valor por `5`, luego se imprime esa misma posición.

---
## Bucle a través de una matriz 2D.

Puede recorrer fácilmente los elementos de una matriz bidimensional con un bucle `foreach`.

```csharp
int[,] numbers = { {1, 4, 2}, {3, 6, 8} };

foreach (int i in numbers)
{
  Console.WriteLine(i);
} 
```

También puede usar un bucle ``for``. Para matrices multidimensionales, Necesita un bucle para cada una de las dimensiones de la matriz.

```csharp
int[,] numbers = { {1, 4, 2}, {3, 6, 8} };

for (int i = 0; i < numbers.GetLength(0); i++) 
{ 
  for (int j = 0; j < numbers.GetLength(1); j++) 
  { 
    Console.WriteLine(numbers[i, j]); 
  } 
} 
```

***Nota:*** Recordemos, esto ya lo aprendimos, son ***bucles anidados***.

