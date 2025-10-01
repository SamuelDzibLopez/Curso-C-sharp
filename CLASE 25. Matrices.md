# 25. Matrices.

Las ***matrices*** se utilizan para almacenar varios valores en una sola variable, en lugar de declarar variables separadas para cada una valor.

Para declarar una ***matriz***, defina el tipo de variable con ***corchetes***:

```csharp
string[] cars;
```

Ahora hemos declarado una ***variable*** que contiene una ***matriz*** de ***cadenas***.

Para insertarle valores, podemos usar un literal de matriz: coloque los valores en una lista separada por comas, dentro de llaves.

Tal como:

```csharp
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
```

Para crear una matriz de números enteros, puede escribir:

```csharp
int[] myNum = {10, 20, 30, 40};
```

---
## Acceder a elementos de una matriz.

Para acceder a un ***elemento*** de la ***matriz***, haga referencia al ***número de índice***.

Por ejemplo:

```csharp
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
Console.WriteLine(cars[0]);
// Salida: Volvo
```

***Nota:*** Recordemos que los elementos de una matriz empiezan con el valor `0`.

---
## Modificar un elemento de matriz.

Para modificar el valor de un elemento específico, debemos consultar el número de índice:

```csharp
cars[0] = "Opel";
```

Por ejemplo:

```csharp
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
cars[0] = "Opel";
Console.WriteLine(cars[0]);
// Cambiamos Opel por en antiguo valor Volvo
```

---
## Longitud de matriz.

Para saber cuántos elementos tiene una matriz, utilizamos la propiedad: `Length`.

Por ejemplo:

```csharp
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
Console.WriteLine(cars.Length);
// Salida: 4
```

***Nota:*** Para elementos de tipo de dato `string`, el atributo ``Length`` obtiene el tamaño de la ***cadena de texto***, mientras que para ***matrices***, obtenemos el numero de elementos internos almacenados dentro de la ***variable***.

---
## Otras formas de crear una matriz.

Si estas familiarizado con ``C#``, es posible que haya visto matrices creadas con la palabra clave `new` y quizás también haya visto matrices con un tamaño especificado.

En ``C#``, hay diferentes maneras de crear una matriz:

```csharp
// Crear un arreglo de cuatro elementos y agregar valores más tarde
string[] cars = new string[4];

// Crear un arreglo de cuatro elementos y agregar valores de inmediato
string[] cars = new string[4] {"Volvo", "BMW", "Ford", "Mazda"};

// Crear un arreglo de cuatro elementos sin especificar el tamaño
string[] cars = new string[] {"Volvo", "BMW", "Ford", "Mazda"};

// Crea un arreglo de cuatro elementos, omitiendo la palabra clave new y sin especificar el tamaño
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
```

Depende de qué opción elijamos.

Sin embargo, debemos tener en cuenta que si declara una matriz y la inicializa más tarde, debe usar la palabra clave `new`:

```csharp
// Declarar un arreglo
string[] cars;

// Agregar valores, usando new
cars = new string[] {"Volvo", "BMW", "Ford"}; // Bien

// Agregar valores sin usar new (esto causará un error)
cars = {"Volvo", "BMW", "Ford"}; // Error
```

---
## Bucles a través de una matriz.

Podemos utilizar los ***bucles*** para recorres los elementos dentro de una matriz.

```csharp
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};

for (int i = 0; i < cars.Length; i++) 
{
  Console.WriteLine(cars[i]);
}
```

También con un bucle `foreach`:

```csharp
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};

foreach (string i in cars) 
{
  Console.WriteLine(i);
}
```

***Nota:*** El ejemplo anterior se puede leer así: ***para cada*** elemento (llamado ``i`` - como en ***index***) en `cars`, imprima el valor de ``i``.`string`.

---
## Ordenar una matriz.

Existen muchos métodos de matriz disponibles, por ejemplo `Sort()`, que ordena una matriz alfabéticamente o en orden ascendente.

Para elementos `string`, el método `Sort()` ordena los elementos en forma alfabética:

```csharp
// Ordenar strings
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
Array.Sort(cars);
foreach (string i in cars)
{
  Console.WriteLine(i);
}
```

Mientras que para elementos `int`, ordena elementos de manera ascendente por valor:

```csharp
// Ordenar ints
int[] myNumbers = {5, 1, 8, 9};
Array.Sort(myNumbers);
foreach (int i in myNumbers)
{
  Console.WriteLine(i);
}
```

---
## ``System.Linq`` (Espacio de nombres)

Otros métodos de matriz útiles, como `Max`, `Min`, `Sum` y `System.Linq`, se pueden encontrar en el espacio de nombres:

```csharp
using System;
using System.Linq;

namespace MyApplication
{
  class Program
  {
    static void Main(string[] args)
    {
      int[] myNumbers = {5, 1, 8, 9};
      Console.WriteLine(myNumbers.Max());  // returns the largest value
      Console.WriteLine(myNumbers.Min());  // returns the smallest value
      Console.WriteLine(myNumbers.Sum());  // returns the sum of elements
    }
  }
}
```