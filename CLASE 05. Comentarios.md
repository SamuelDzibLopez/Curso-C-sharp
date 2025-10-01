# 05. Comentarios.

Los ***comentarios*** se pueden usar para explicar el código de`` C#`` y hacerlo más legible. 

***Nota:*** También se puede utilizar para evitar la ejecución al probar código alternativo.

---
## Comentarios de una sola línea.

Los ***comentarios*** de una sola línea comienzan con dos barras diagonales (`//`). Cualquier texto entre y al final de la línea `//` es ignorado por ``C#`` (no se ejecutará).

El siguiente ejemplo usa un comentario de una sola línea antes de una línea de código:

~~~csharp
// This is a comment
Console.WriteLine("Hello World!");
~~~

También podemos utilizar un comentario de una sola línea al final de una línea de código.

~~~csharp
Console.WriteLine("Hello World!");  // This is a comment
~~~

---
## Comentarios de varias líneas.

Los comentarios de varias líneas comienzan con `/*` y terminan con `*/`.

Cualquier texto entre `/*` y `*/` será omitido por ``C#``.

Tal como el ejemplo:

~~~csharp
/* The code below will print the words Hello World
to the screen, and it is amazing */
Console.WriteLine("Hello World!"); 
~~~