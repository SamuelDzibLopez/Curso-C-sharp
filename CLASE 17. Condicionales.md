# 17. Condicionales.

Ya sabe que`` C#`` admite ***condiciones de comparación*** conocidas de las matemáticas, como:

	- Menor que: a < b.
	- Menor o igual que: a <= b.
	- Mayor que: a > b.
	- Mayor o igual que: a >= b.
	- Igual que: a == b.
	- No es igual que: a != b.

Puede utilizar las condiciones para realizar diferentes acciones para diferentes decisiones.

	- Se usa "if" para especificar un bloque de código que se ejecutará, si una condición especificada es verdadera.
	- Se usa "else" para especificar un bloque de código que se ejecutará, si la misma condición es falsa.
	- Se usa "else if" para especificar una nueva condición para probar, si la primera condición es falsa.
	- Se usa "switch" para especificar muchos bloques de código alternativos que se ejecutarán.

---
## Declaración ``if``.

Utilizamos la ***instrucción*** `if` para especificar un bloque de código de ``C#`` que se ejecutará si una condición es `True`.

```csharp
if (condition) 
{
	//Codigo a ejecutarse si la condicion es True
}
```

Por ***ejemplo***:

```csharp
if (20 > 18) 
{
	Console.WriteLine("20 es mayor que 18");
}
```

No olvides que podemos utilizar variables:

```csharp
int x = 20;
int y = 18;
if (x > y) 
{
	Console.WriteLine("x es mayor que y");
}
```

---
## Declaración `else`.

Utilice la instrucción `else` para especificar un bloque de código que se ejecutará si la condición es `False`.

```csharp
if (condition)
{
	//Codigo a ejecutarse si la condicion es True
} 
else 
{
	//Codigo a ejecutarse si la condicion es False
}
```

Por ejemplo:

```csharp
int time = 20;

if (time < 18) 
{
  Console.WriteLine("Good day.");
} 
else 
{
  Console.WriteLine("Good evening.");
}
// Salida: "Good evening."
```

---
## Declaración `else if`.

Utilice la instrucción `else if` para especificar una nueva condición si la primera condición es `False`.

```csharp
if (condition1)
{
	//Codigo a ejecutarse si la condicion es True
} 
else if (condition2) 
{
  //Codigo a ejecutarse si las condiciones anteriores son False y la condicion de este bloque es True
} 
else
{
  //Codigo a ejecutarse si ninguna condicion es True
}
```

Ejemplo:

```csharp
int time = 22;

if (time < 10) 
{
  Console.WriteLine("Good morning.");
} 
else if (time < 20) 
{
  Console.WriteLine("Good day.");
} 
else 
{
  Console.WriteLine("Good evening.");
}
// Saloda: "Good evening."
```

`time` (``22``) es mayor que ``10``, por lo que la ***primera condición*** es `False`. La siguiente condición, en la declaración `else if`, también es `False`, por lo que pasamos a la condición `else` ya que ***condition1*** y ***condition2*** son ambas `False`, e imprimimos en la pantalla `"Good evening."`.