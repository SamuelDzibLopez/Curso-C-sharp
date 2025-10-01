# 27. Métodos.

Un ***método*** es un bloque de código que solo se ejecuta cuando se llama.

Puede pasar datos, conocidos como parámetros, a un método.

Los métodos se utilizan para realizar ciertas acciones y también se conocen como **funciones**.

	¿Por qué usar métodos? Para reutilizar el código: defina el código una vez y use muchas veces.

---
## Creación de un método.

Se define un ***método*** con el ***nombre*** del método que deseamos que tenga, seguido de paréntesis ``()``.

``C#`` proporciona algunos ***métodos predefinidos***, con los que ya está familiarizado, como `Main()`, pero también puede crear sus propios métodos para realizar ciertas acciones.

```csharp
class Program
{
  static void MyMethod() 
  {
    // Codigo a ejecutar
  }
}
```

Expliquemos:

	- MyMethod: es el nombre del método.
	- static: significa que el método pertenece a la clase Program y no a un objeto de la clase Program. (Esto no es necesario que lo entiendas).
	- void: significa que este método no devuelve un valor. (Esto no es necesario que lo entiendas).

***Nota:*** En ``C#``, se recomienda comenzar con una letra mayúscula al asignar nombres a los métodos, ya que facilita la lectura del ***código***.

---
## Llamar a un método.

Para llamar (ejecutar) a un ***método***, escriba el nombre del método seguido de dos paréntesis ``()`` y punto y coma ``;``.

Veamos el ejemplo:

```csharp
static void MyMethod() 
{
  Console.WriteLine("I just got executed!");
}

static void Main(string[] args)
{
  MyMethod();
}

// Salida: "I just got executed!"
```

	C# es similar a Java, ya que el método "Main" es el método que se utiliza para insertar todo código que se ejecutará al iniciar el programa., por lo que colocamos la llamada de la función/método MyMethod dentro de este. (Este es solo un dato que necesitas saber para entender esto, explicaremos mejor esto).

***Nota:*** Definimos la función `MyMethod` y luego la mandamos a llamar (dentro de la función mayor `Main`).

	Recuerda, el código dentro de un función/método no se ejecuta solo por definirse, sino hasta la linea de código donde se llama.

Se puede llamar a un método varias veces:

```csharp
static void MyMethod() 
{
  Console.WriteLine("I just got executed!");
}

static void Main(string[] args)
{
  MyMethod();
  MyMethod();
  MyMethod();
}

// I just got executed!
// I just got executed!
// I just got executed!
```

