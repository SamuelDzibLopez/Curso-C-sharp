# 23. Bucle `foreach`.

También ``c#`` permite el uso de bucles `foreach`, que se usa exclusivamente para recorrer elementos en una **matriz** (u otros conjuntos de datos).

La sintaxis de un bucle `foreach`:

```csharp
foreach (type variableName in arrayName) 
{
  // code block to be executed
}
```

***Nota:*** Los bucles `foreach` son utilizados para recorrer por completo los elementos internos de un elemento padre.

En el siguiente ejemplo, se utiliza recorriendo los elementos de una `matriz`:

```csharp
string[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
foreach (string i in cars) 
{
  Console.WriteLine(i);
}
```

***Nota:*** Una `matriz` es un conjunto de elementos (en `c#` tienen que ser del mismo tipo de dato) almacenados para identificarse por orden, dentro de una variable.

---
## Diferencia entre `for` y `foreach`.

Los bucles `foreach` son una variación de `for`, pero recordemos que o-los bucles `for`, funcionan:

	for:
		- Utilizado para marcar un numero de veces a repetir el bucle
		- Tienen 3 instrucciones:
			- Primero: Creación de identificador.
			- Segundo: Condición para que el bucle sea repetido.
			- Tercero: Sumatoria o resta de identificador.
		- Funciona con numero de bucles a definirse por una condición.

Mientras:

	foreach:
		- Es utilizado para recorrer los elementos internos dentro de un elemento padre.
		- Tiene 2 instrucciones:
			- Primero: Elemento interno en turno de bucle.
			- Segundo: Elemento padre a recorrer.
		- Funciona con un numero de bucles dependiendo del tamaño y numero de elementos internos del elemento padre.

