# 21. Bucle Do While.

El bucle `do while` es una ***variante*** del bucle `while`. 

Este bucle ejecuta el bloque de código una vez primero, antes de verificar si la condición es verdadera, entonces repite el bucle siempre que la condición sea verdadera.

```csharp
do 
{
  // Codigo a ejecutarse una vez y repetirse si la condicion es necesaria
}
while (condition);
```

***Nota:*** El ***bucle*** `do while` es utilizado cuando necesitamos que el bloque de código deba ejecutarse al menos una vez.

El siguiente ejemplo utiliza un bucle `do while`:

El bucle `do/while` siempre será ejecutado al menos una vez, incluso si la condición es falsa, porque el bloque de código se ejecuta antes de probar la condición:

```csharp
int i = 0;

do 
{
  Console.WriteLine(i);
  i++;
}
while (i < 5);
```

***Nota:*** No olvidemos aumentar la variable utilizada en la condición, de lo contrario ¡el bucle nunca terminará!

