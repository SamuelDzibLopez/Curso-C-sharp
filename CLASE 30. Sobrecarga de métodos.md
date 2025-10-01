# 30. # Sobrecarga de métodos.

	Sobrecargar métodos, es definir varios métodos pueden tener el mismo nombre pero tienen diferentes parámetros (tipos de datos).

Supongamos que deseamos realizar un método que desea sumar 2 números (`int` o `double`).

Por lo que deberíamos crear ***2 funciones***, para cada caso, algo así:

```csharp
static int PlusMethodInt(int x, int y)
{
  return x + y;
}

static double PlusMethodDouble(double x, double y)
{
  return x + y;
}

static void Main(string[] args)
{
  int myNum1 = PlusMethodInt(8, 5);
  double myNum2 = PlusMethodDouble(4.3, 6.26);
  Console.WriteLine("Int: " + myNum1);
  Console.WriteLine("Double: " + myNum2);
}
```

Pero esto, tal vez sea mucho código, podríamos utilizar ***sobrecarga de métodos*** para hacer que:

	Una sola función pueda aceptar entrada de 2 tipos de datos como parametros.

En lugar de definir dos métodos que deberían hacer lo mismo, es mejor sobrecargar uno.

Entonces:

```csharp
static int PlusMethod(int x, int y)
{
  return x + y;
}

static double PlusMethod(double x, double y)
{
  return x + y;
}

static void Main(string[] args)
{
  int myNum1 = PlusMethod(8, 5);
  double myNum2 = PlusMethod(4.3, 6.26);
  Console.WriteLine("Int: " + myNum1);
  Console.WriteLine("Double: " + myNum2);
}
```

***Nota:*** En el ejemplo, sobrecargamos el método `PlusMethod` para que funcione para ambos, `int` y `double`.

---

***Nota:*** Varios métodos pueden tener el mismo nombre siempre que el número y/o tipo de parámetros sean diferentes.
