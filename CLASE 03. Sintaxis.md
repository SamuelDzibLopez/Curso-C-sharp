# 03. Sintaxis.

En el capítulo anterior, creamos un archivo de ``C#`` con extensión ``.cs`` y utilizando el ***código siguiente*** para imprimir ``"Hello World"`` en la pantalla:

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

Expliquemos el ***código***:

	Línea 1: Significa que podemos usar clases del espacio de nombres. using System System.
	Línea 2: Una línea en blanco. C# omite los espacios en blanco. Sin embargo, varias líneas hacen que el código sea más legible.
	Línea 3: Se utiliza para organizar su código y es un contenedor para clases y otros espacios de nombres.
	Línea 4: Las llaves marcan el principio y el final de un bloque de código.
	Línea 5: Es un para datos y métodos, que aporta funcionalidad a su programa. Cada línea de código que se ejecuta en C# debe estar dentro de una clase. En nuestro ejemplo, llamamos a la clase Program.
	Línea 7: Otra cosa que siempre aparece en un programa de C# es el método Main. Se ejecutará cualquier código dentro de sus llaves.
	Línea 9: Es una clase del espacio de nombres, que tiene un método que se utiliza para generar / imprimir texto. En nuestro ejemplo, generará "¡Hola mundo!".

	Si omite la línea `using System`, tendría que escribir en texto de impresión/salida como `System.Console.WriteLine()`.

Recuerda:

	- Cada instrucción de C# termina con un punto y coma.
	- C# distingue entre mayúsculas y minúsculas; "MiClase" y "miclase" tienen significado diferente.
	- A diferencia de Java, el nombre del archivo C# no tiene que coincidir con el nombre de la clase, pero a menudo lo hacen (para una mejor organización). Al guardar el archivo, guárdelo con un nombre propio y agregue ".cs" al final de el nombre del archivo.