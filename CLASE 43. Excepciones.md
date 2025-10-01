# 43. Excepciones.

Al ejecutar código ``C#``, pueden ocurrir ***diferentes errores***: errores de codificación cometidos por el programador, errores debidos a una entrada incorrecta, u otras cosas imprevisibles.

Cuando se produce un error, ``C#`` normalmente se detendrá y generará un mensaje de error. El término técnico para esto es: ``C#`` producirá una **excepción** (lanzará un error).

---
## `try` y `catch`.

La instrucción `try` le permite definir un bloque de código para que se probado en busca de errores mientras se ejecuta.

La instrucción `catch` le permite definir un bloque de código para si se produce un error en el bloque ``try``.

Las palabras clave `try` y `catch` se dividen en pares:

```csharp
try 
{
  //  Block of code to try
}
catch (Exception e)
{
  //  Block of code to handle errors
}
```

Consideremos el siguiente ejemplo, donde creamos una matriz de tres enteros:

Esto generará un error, porque ``myNumbers[10]`` no existe.

```csharp
int[] myNumbers = {1, 2, 3};
Console.WriteLine(myNumbers[10]); // error!
```

El mensaje de error será algo como esto:

`System.IndexOutOfRangeException: 'Index was outside the bounds of the array.'`

Si ocurre un error, podemos usar `try...catch` para detectar el error y ejecutar algún código para manejarlo.

En el siguiente ejemplo, usamos la variable `e` dentro del bloque catch () junto con la propiedad `Message` incorporada, que genera un mensaje que describe la excepción:

```csharp
try
{
  int[] myNumbers = {1, 2, 3};
  Console.WriteLine(myNumbers[10]);
}
catch (Exception e)
{
  Console.WriteLine(e.Message);
}
```

a salida será:

	Index was outside the bounds of the array.

También puede generar su propio mensaje de error:

```csharp
try
{
  int[] myNumbers = {1, 2, 3};
  Console.WriteLine(myNumbers[10]);
}
catch (Exception e)
{
  Console.WriteLine("Something went wrong.");
}
```

La salida será:

	Something went wrong.

---
## `finally`.

La instrucción `finally` le permite ejecutar código, después de `try...catch`, independientemente del resultado:

```csharp
try
{
  int[] myNumbers = {1, 2, 3};
  Console.WriteLine(myNumbers[10]);
}
catch (Exception e)
{
  Console.WriteLine("Something went wrong.");
}
finally
{
  Console.WriteLine("The 'try catch' is finished.");
}
```

La salida será:

	Something went wrong.
	The 'try catch' is finished.

---
## La palabra clave ``throw``

La instrucción `throw` le permite crear un error personalizado.

La instrucción `throw` se usa junto con una ***clase de excepción***. Hay muchas clases de excepción disponibles en C#: `ArithmeticException`, `FileNotFoundException`,  `IndexOutOfRangeException`, `TimeOutException`, etc.

```csharp
static void checkAge(int age)
{
  if (age < 18)
  {
    throw new ArithmeticException("Access denied - You must be at least 18 years old.");
  }
  else
  {
    Console.WriteLine("Access granted - You are old enough!");
  }
}

static void Main(string[] args)
{
  checkAge(15);
}
```

El mensaje de error que se muestra en el programa será:

	System.ArithmeticException: 'Access denied - You must be at least 18 years old.'

Si `age` tuviera 20 años, **no** obtendría una excepción:

---

