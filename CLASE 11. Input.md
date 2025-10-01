# 11. Input.

Ya hemos aprendido que `Console.WriteLine()` se utiliza para generar (imprimir) valores. Ahora usemos `Console.ReadLine()` para obtener la ***entrada del usuario***.

En el siguiente ejemplo, el usuario puede ingresar su nombre de usuario, que se almacena en la variable `userName`. Luego imprimimos el valor de : `userName`.

```csharp
// Type your username and press enter
Console.WriteLine("Ingrese username:");

// Create a string variable and get user input from the keyboard and store it in the variable
string userName = Console.ReadLine();

// Print the value of the variable (userName), which will display the input value
Console.WriteLine("Su username es: " + userName);
```

---
## Entrada de usuario y números

El método `Console.ReadLine()` devuelve un valor `string`. Por lo tanto, no puede obtener información de otro tipo de datos, como `int`. Por ejemplo, el siguiente programa provocará un error:

```csharp
Console.WriteLine("Ingrese su edad:");

int age = Console.ReadLine();

Console.WriteLine("Tu edad es: " + age);
```

El mensaje de error será algo como esto:

	Cannot implicitly convert type 'string' to 'int'.

Como dice el mensaje de error, no puede convertir implícitamente el tipo `string` en `int`.

Afortunadamente, para ti, podemos convertir cualquier tipo explícitamente, mediante uno de los métodos: `Convert.To`.

```csharp
Console.WriteLine("Ingrese su edad:");

int age = Convert.ToInt32(Console.ReadLine());

Console.WriteLine("Tu edad es: " + age);
```

***Nota:*** Si ingresamos una entrada incorrecta (por ejemplo, texto en una entrada numérica), obtendrá un mensaje de ***excepción/error*** (como ``System.FormatException: 'La cadena de entrada no estaba en un formato correcto'``).

