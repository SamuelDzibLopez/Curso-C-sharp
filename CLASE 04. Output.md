# 04. Output.

Para generar valores o imprimir texto en ``C#``, utilizamos el método: `WriteLine()`.

Por ejemplo:

~~~c#
Console.WriteLine("Hello World!");
~~~

***Nota:*** Podemos agregar tantos métodos `WriteLine()` como deseemos. Pero tengamos en cuenta que agregará una nueva línea para cada método.

~~~csharp
Console.WriteLine("Hello World!");
Console.WriteLine("I am Learning C#");
Console.WriteLine("It is awesome!");
~~~

También puede generar números y realizar cálculos matemáticos:

~~~csharp
Console.WriteLine(3 + 3);
~~~

---
## Método `Write()`

También hay un método, que es similar a `WriteLine()`. El cual es:

	Write()

La única diferencia es que no inserta una nueva línea al final de la salida:

~~~csharp
Console.Write("Hello World! ");
Console.Write("I will print on the same line.");
~~~

***Nota:*** Tengamos en cuenta que agregamos un espacio adicional cuando es necesario (después de ``"¡Hola mundo!"`` en el ejemplo anterior), para una mejor legibilidad.

