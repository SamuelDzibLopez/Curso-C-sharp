# 20. Bucle ``While``.

	Los bucles pueden ejecutar un bloque de código siempre y cuando una condición especificada sea verdadera.

Los ***bucles*** son útiles porque ahorran tiempo, reducen errores y hacen que el código sea más legible.

---
## Bucle ``While``.

El ***bucle*** `while` recorre un ***bloque de código*** siempre que una condición especificada sea :`True`.

```csharp
while (condition) 
{
  // Codigo que se ejecuta mientras la condicion sea True
}
```

En el siguiente ejemplo, el ***código del bucle*** se ejecutará, una y otra vez, siempre que ``i`` sea menor que 5.

	Es decir, el codigo se ejecuta mientras i < 5 sea igual a True.

```csharp
int i = 0;
while (i < 5) 
{
  Console.WriteLine(i);
  i++;
}
```

***Nota:*** No olvidemos aumentar la variable utilizada en la ***condición***, de lo contrario ¡el bucle nunca terminará!



