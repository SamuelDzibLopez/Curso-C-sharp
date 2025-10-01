# 22. Bucle `for`.

Cuando sabemos exactamente cuántas veces queremos recorrer un ***bloque de código***, podemos utilizar el bucle `for` en lugar de un bucle `while`.

Un bucle `for` sigue la ***sintaxis***:

```csharp
for (instruccion 1; instruccion 2; instruccion 3) 
{
  // Codigo a ejecutar
}
```

Donde:

	- La instrucción 1 se ejecuta (una vez) antes de la ejecución del bloque de código.
	- La instrucción 2 define la condición para ejecutar el bloque de código.
	- La instrucción 3 se ejecuta (cada vez) después de que se haya ejecutado el bloque de código.

Ejemplo:

```csharp
for (int i = 0; i < 5; i++) 
{
  Console.WriteLine(i);
}
```

Expliquemos:

	- La instrucción 1 establece una variable antes de que comience el bucle (int i = 0).
	- La instrucción 2 define la condición para que se ejecute el bucle (i debe ser menor que 5). Si la condición es true, el bucle comenzará de nuevo, si es false, el bucle terminará.
	- La instrucción 3 aumenta un valor (i++) cada vez que el bloque de código del bucle tiene ha sido ejecutado.

Otro ***ejemplo***, para entender mejor: 

```csharp
for (int i = 0; i <= 10; i = i + 2) 
{
  Console.WriteLine(i);
}
```

---
## Bucles anidados.

También es posible colocar un bucle dentro de otro bucle. Esto se denomina ***bucle anidado***.

El "bucle interno" se ejecutará una vez para cada iteración del "bucle externo":

```csharp
// Bucle externo
for (int i = 1; i <= 2; ++i) 
{
  Console.WriteLine("Outer: " + i);  // se ejecuta 2 veces

  // Bucle interno
  for (int j = 1; j <= 3; j++) 
  {
    Console.WriteLine(" Inner: " + j); //se ejecuta 6 veces (2 * 3)
  }
}
```

