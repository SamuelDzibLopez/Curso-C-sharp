# 19. Switch.

La instrucción `switch` permite seleccionar uno de los muchos bloques de código que se pueden ejecutar, dependiendo que las posibles respuestas de una expresión.

```csharp
switch(expression) 
{
  case x:
    // Codigo a ejecutar
    break;
  case y:
    // Codigo a ejecutar
    break;
  default:
    // Codigo a ejecutar
    break;
}
```

Así es como funciona:

	- La expresión `switch` se evalúa una única vez.
	- El valor de la expresión se compara con los valores de cada `case`.
	- Si hay una coincidencia, se ejecuta el bloque de código asociado

***Nota:*** Las palabras clave `break` y `default` se describirán más adelante en este capítulo.

Veamos un ejemplo:

```csharp
int day = 4;
switch (day) 
{
  case 1:
    Console.WriteLine("Monday");
    break;
  case 2:
    Console.WriteLine("Tuesday");
    break;
  case 3:
    Console.WriteLine("Wednesday");
    break;
  case 4:
    Console.WriteLine("Thursday");
    break;
  case 5:
    Console.WriteLine("Friday");
    break;
  case 6:
    Console.WriteLine("Saturday");
    break;
  case 7:
    Console.WriteLine("Sunday");
    break;
}
// Salida: "Thursday" (day 4)
```

---
## Palabra reservada `break`.

Cuando ``C#`` encuentra una palabra clave `break`, sale del bloque ``switch``.

Esto detendrá la ejecución de más código y pruebas de casos en el interior el bloque.

***Nota:*** `break` sirve como un identificador hasta donde termina el ***bloque de código*** a ejecutar si el caso se cumple.

---
## Palabra reservada `default`.

La palabra clave `default` es opcional y especifica un código que se ejecutará si no hay coincidencia en ninguno de los casos especificados:

```csharp
int day = 4;
switch (day) 
{
  case 6:
    Console.WriteLine("Today is Saturday.");
    break;
  case 7:
    Console.WriteLine("Today is Sunday.");
    break;
  default:
    Console.WriteLine("Looking forward to the Weekend.");
    break;
}
// Salida: "Looking forward to the Weekend."
```






