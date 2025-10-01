# 02. Hola Mundo.

El programa ***"Hello, World"*** se usa tradicionalmente para introducir un lenguaje de programación. 

Escribiéndose de la siguiente manera en ``C#``:

~~~c#
// This line prints "Hello, World" 
Console.WriteLine("Hello, World");
~~~

---
## Comentarios.

Aprendiendo, del anterior ***código simple***:

La línea que comienza con es un ***comentario de una sola línea***. 

Los comentarios de una sola línea de ``C#`` comienzan con `//` y continúan hasta el final de la línea actual.

C# también admite ***comentarios de varias líneas***.

Los comentarios de varias líneas comienzan con `/*` y terminan con `*/`.

---
## Método `WriteLine()`

El método `WriteLine` de la clase `Console`, que se encuentra en el espacio de nombres `System`, genera la salida del programa.

Esta clase la proporcionan las bibliotecas de clases estándar, a las que, de forma predeterminada, se hace referencia automáticamente en cada programa de C#.

---
##  Método `static void Main(string[] args)`

	C# es muy similar a Java.

Cuando ejecutamos un programa en ``C#``, ***el punto de entrada obligatorio*** es un método llamado `Main`.

También podemos escribir otro formato de programa, el cual requiere que se declare la ***clase contenedora*** y el ***método*** para el punto de entrada del programa. El compilador sintetiza estos elementos cuando usas declaraciones a nivel superior.

Este formato alternativo sigue siendo válido y contiene muchos de los conceptos básicos en todos los programas ``C#``. 

Muchos ejemplos existentes de ``C#`` utilizan el ***siguiente formato*** equivalente:

~~~c#
using System;
namespace HelloWorld

{
	class Program
	{
		static void Main(string[] args)
		{
			Console.WriteLine("Hello World!");    
		}
	}
}
~~~

Donde:

	- static
	    - Significa que el método pertenece a la clase en sí y no a un objeto creado de esa clase.
	    - Esto permite que el runtime de .NET pueda ejecutarlo sin necesidad de instanciar la clase Program.
	- void
	    - Es el tipo de dato de retorno.
	    - void significa que no devuelve ningún valor al sistema operativo.
	    - (Opcionalmente se puede usar int para devolver un código de salida al SO, donde 0 suele significar “ejecución exitosa”).
	- Main
	    - Es el nombre reservado del método de entrada en C#.
	    - El runtime siempre busca este método para arrancar el programa.
	    - Puede haber varias versiones de Main, pero debe existir al menos una válida como punto de inicio.
	- string[] args
	    - Es un arreglo de cadenas que recibe los argumentos de línea de comandos.
	    - Ejemplo: si ejecutas en la terminal:

~~~
dotnet run hola mundo
~~~

		- entonces `args[0] = "hola"` y `args[1] = "mundo"`.
		- Si no pasas argumentos, `args` estará vacío.

Un ejemplo de código:

~~~c#
using System;

class Program
{
    static void Main(string[] args)
    {
        Console.WriteLine("Mi programa en C#");

        if (args.Length > 0)
        {
            Console.WriteLine("Argumentos recibidos:");
            foreach (string arg in args)
            {
                Console.WriteLine(arg);
            }
        }
        else
        {
            Console.WriteLine("No se pasaron argumentos.");
        }
    }
}
~~~

Ejecutando:

~~~
dotnet run uno dos tres
~~~

El cual debería devolver de salida:

	Mi programa en C#
	Argumentos recibidos:
	uno
	dos
	tres

***Nota:*** No se preocupe si no comprende el código anterior: lo discutiremos en detalle en capítulos posteriores. Por ahora, concéntrese en cómo ejecutar el código.