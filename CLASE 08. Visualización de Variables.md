# 08.Visualización de Variables.

El método `WriteLine()` se utiliza a menudo para mostrar valores de variables en la ventana de la consola.

---
## Concatenación con ``strings``.

Para combinar texto y una variable, usamos el carácter:`+`

```csharp
string name = "John";
Console.WriteLine("Hello " + name);
```

También se pueden usar el carácter `+` para agregar una variable a otra variable:

```csharp
string firstName = "John ";
string lastName = "Doe";
string fullName = firstName + lastName;
Console.WriteLine(fullName);
```



Para valores numéricos y variables `int`, el carácter `+` funciona como un operador matemático.

Tal como el ejemplo:

```csharp
int x = 5;
int y = 6;
Console.WriteLine(x + y); // Resultado 11
```

Del ejemplo anterior, puede esperar:

	- x almacena el valor 5
	- y almacena el valor 6
	- Luego utilizando el método WriteLine() e imprimimos el valor de x + y, que es 11.

---
## Declaración de múltiples variables.

Para declarar más de una variable del ***mismo tipo***, ``c#`` permite la declaración por una lista separada por comas:

```c#
int x = 5, y = 6, z = 50;
//Declaracion de tres variables de tipo int, con su respectivo valor

Console.WriteLine(x + y + z);
```

También puede asignar el ***mismo valor*** a varias variables en una línea:

```c#
int x, y, z;
x = y = z = 50;
Console.WriteLine(x + y + z);
```

---
## Identificadores (nombres).

Todas las ***variables*** de ``C#`` deben **identificarse** con ***nombres únicos***.

Estos nombres únicos se denominan ***identificadores***, los cuales pueden ser nombres cortos (como ``x`` e ``y``) o nombres más descriptivos (``age``, ``sum``, ``totalVolume``).

***Nota*:** Se recomienda utilizar nombres descriptivos para que nuestro ***código*** sea ***comprensible*** y ***mantenible***.

```csharp
// Recomendado
int minutesPerHour = 60;

// Esta bien, pero tal vez en el futuro no sea entendible
int m = 60;
```

Las reglas generales para nombrar variables son:

	- Los nombres pueden contener letras, dígitos y el carácter de subrayado (_)
	- Los nombres deben comenzar con una letra o un guión bajo.
	- Los nombres deben comenzar con una letra minúscula y no pueden contener espacios en blanco
	- Los nombres distinguen entre mayúsculas y minúsculas ("myVar" y "myvar" son variables diferentes)
	- Las palabras reservadas (como las palabras clave de C#, como int o double) no se pueden usar como nombres.
