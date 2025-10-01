# 18. Operador Ternario.

En `C#` existe una abreviatura`` if else``, que se conoce como ***operador ternario***, y consta de tres operandos.

Se puede utilizar para reemplazar varias líneas de código por una sola línea. A menudo se usa para reemplazar condicionales simples de `if else`:

```csharp
variable = (condition) ? expressionTrue :  expressionFalse;
```

Por lo que, viendo un ejemplo, donde:

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
```

Simplificamos:

```csharp
int time = 20;
string result = (time < 18) ? "Good day." : "Good evening.";
Console.WriteLine(result);
```