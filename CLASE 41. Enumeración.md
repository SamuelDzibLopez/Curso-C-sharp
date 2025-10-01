# 41. Enumeración.

Una `enum` es una "clase" especial que representa un grupo de ***constantes*** (variables inmutables / de solo lectura).

Para crear un `enum`, use la palabra clave `enum` (en lugar de ``class`` o ``interface``) y separe Los elementos de enumeración con una coma:

```csharp
enum Level 
{
  Low,
  Medium,
  High
}
```

Puede acceder a los elementos `enum` con la sintaxis **de puntos**:

```csharp
Level myVar = Level.Medium;
Console.WriteLine(myVar);
```

***Nota:*** ``enum`` es la abreviatura de "enumeraciones", que significa "específicamente enumerado".

---
## Enumeración dentro de una clase.

También puedes tener una clase `enum` dentro de una clase:

```c#
class Program
{
  enum Level
  {
    Low,
    Medium,
    High
  }
  static void Main(string[] args)
  {
    Level myVar = Level.Medium;
    Console.WriteLine(myVar);
  }
}
```

La salida será:

	Medium

---
## Valores de enumeración.

De forma predeterminada, el primer elemento de una enumeración tiene el valor 0. El segundo tiene el valor 1, y así sucesivamente.

Para obtener el valor entero de un elemento, debe convertir ***explícitamente*** el elemento en un :`int`

```c#
enum Months
{
  January,    // 0
  February,   // 1
  March,      // 2
  April,      // 3
  May,        // 4
  June,       // 5
  July        // 6
}

static void Main(string[] args)
{
  int myNum = (int) Months.April;
  Console.WriteLine(myNum);
```

La salida:

	3

También puede asignar sus propios valores de enumeración, y los siguientes elementos actualizarán sus números en consecuencia:

```c#
enum Months
{
  January,    // 0
  February,   // 1
  March=6,    // 6
  April,      // 7
  May,        // 8
  June,       // 9
  July        // 10
}

static void Main(string[] args)
{
  int myNum = (int) Months.April;
  Console.WriteLine(myNum);
}
```

La salida será:

	7

---
## Enumeración en una instrucción ``switch``.

Las enumeraciones se utilizan a menudo en las instrucciones `switch` para comprobar los valores correspondientes:

```c#
enum Level 
{
  Low,
  Medium,
  High
}

static void Main(string[] args) 
{
  Level myVar = Level.Medium;
  switch(myVar) 
  {
    case Level.Low:
      Console.WriteLine("Low level");
      break;
    case Level.Medium:
       Console.WriteLine("Medium level");
      break;
    case Level.High:
      Console.WriteLine("High level");
      break;
  }
}
```

La salida será:

	Medium level

---
## ¿Por qué y cuándo usar enumeraciones?

Podemos utilizar las enumeraciones cuando tengamos valores que sepamos que no van a cambiar, como días de mes, días, colores, baraja de cartas, etc.

