# 29. Valores devueltos en métodos.

Recuerda que cuando utilizamos la palabra clave `void`, indica que el método no debe devolver un valor.

Pero si deseamos que el ***método*** que creamos devuelva un valor, podemos usar un ***tipo de dato*** (`int`, `string`, etc..) al definir el método y usar la palabra clave dentro del método: `return`.

Veamos un ***ejemplo***:

```csharp
static int MyMethod(int x) 
{
  return 5 + x;
}

static void Main(string[] args)
{
  Console.WriteLine(MyMethod(3));
}

// Salida: 8. Porque (5 + 3)
```

***Nota:*** Al definir nuestro método `MyMethod`, y colocar `int` (en lugar de `void`), quiere decir que deseamos que al ejecutarse la función, se piensa devolver un valor de tipo `int`.

Entonces, al ejecutar `MyMethod(3)` esto devuelve `8`, el cual es un `int`. 

```csharp
static int MyMethod(int x, int y) 
{
  return x + y;
}

static void Main(string[] args)
{
  Console.WriteLine(MyMethod(5, 3));
}

// Salida: 8. Porque (5 + 3)
```

También puede almacenar el resultado en una variable (recomendado, ya que es más fácil de leer y mantener):

```csharp
static int MyMethod(int x, int y) 
{
  return x + y;
}

static void Main(string[] args)
{
  int z = MyMethod(5, 3);
  Console.WriteLine(z);
}

// Salida: 8, porque z es igual a: (5 + 3)
```

