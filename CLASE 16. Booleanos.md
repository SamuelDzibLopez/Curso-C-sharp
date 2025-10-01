# 16. Booleanos.

Muy a menudo, en programación, necesitará un tipo de datos que solo pueda tener uno de dos valores, como:

	- SÍ / NO
	- ENCENDIDO / APAGADO
	- VERDADERO / FALSO

Para esto, ``C#`` tiene el tipo de dato `bool`, que puede tomar los valores `true` o `false`.

---
## Valores booleanos.

Un tipo booleano se declara con la palabra clave `bool` y solo puede tomar los valores `true` o `false`:

```csharp
bool isCSharpFun = true;
bool isFishTasty = false;
Console.WriteLine(isCSharpFun);   // Salida: True
Console.WriteLine(isFishTasty);   // Salida: False
```

Sin embargo, es más común devolver valores booleanos de expresiones booleanas, para pruebas condicionales.

---
## Expresión booleana.

Una ***expresión booleana*** devuelve un valor booleano: `True` o `False`, comparando valores/variables.

Por ejemplo, podemos utilizar un ***operador de comparación***, como el operador ***mayor que*** (`>`) para averiguar si una expresión (o una ***variable***) es verdadera:

```c#
int x = 10;
int y = 9;
Console.WriteLine(x > y); //True, porque 10 es mayo a 9
```

O incluso más fácil:

```c#
Console.WriteLine(10 > 9); // returns True, because 10 is higher than 9
```

En los ejemplos siguientes, se utiliza el operador **igual a** (`==`) para evaluar una expresión:

```c#
int x = 10; //Asignacion de valor
Console.WriteLine(x == 10); // True, porque x es igual a 10
```

O:

```c#
int myAge = 25;
int votingAge = 18;
Console.WriteLine(myAge >= votingAge);
```


