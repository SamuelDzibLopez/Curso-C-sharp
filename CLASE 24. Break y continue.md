# 24. `Break` y `continue`.

Ya hemos visto la instrucción `break`, utilizada en lecciones anteriores de `switch`.

	Recordemos que "break" se utiliza para "saltar" o "romper" una declaración o salir de un bucle.

Este ejemplo salta fuera del bucle cuando `i` es igual a `4`:

```csharp
for (int i = 0; i < 10; i++) 
{
  if (i == 4) 
  {
    break;
  }
  Console.WriteLine(i);
}
```

***Nota:*** De modo que cuando `i` sea igual a `4`, el bucle se terminará y la lógica saltara hacia afuera del bucle, sin necesidad de llegar a que `i == 4` sea `False`.

---
## Palabra reservada `continue`.

La instrucción `continue` interrumpe una iteración (en el bucle), si se produce una condición especificada, y continúa con la siguiente iteración en el bucle.

En este ejemplo se omite el valor de :`4`

```csharp
for (int i = 0; i < 10; i++) 
{
  if (i == 4) 
  {
    continue;
  }
  Console.WriteLine(i);
}
```

***Nota:*** De modo que si `i == 4`, el bucle en turno se termina, omitiendo cualquier código del ***bloque del código*** de abajo y iniciando el siguiente bucle en turno; 

`Continue` no sale del bucle, solo cierra el bucle en turno.

También puedes usar `break` y `continue` en bucles ``while``.



