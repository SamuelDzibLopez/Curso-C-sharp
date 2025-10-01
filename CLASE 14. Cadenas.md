# 14. Cadenas.

Las ***cadenas*** se utilizan para almacenar texto.

Una ***variable*** `string` contiene una colección de caracteres entre comillas dobles:

```csharp
string greeting = "Hello";
```

Una ***variable*** de ***cadena*** puede contener muchas palabras, si lo desea:

```csharp
string greeting2 = "Nice to meet you!";
```

---
## Longitud de la cadena.

Una ***cadena*** en ``C#`` es en realidad un ***objeto***, que contiene ***propiedades*** y ***métodos*** que pueden realizar ciertas operaciones en cadenas. Por ejemplo, la longitud de una cadena se puede encontrar con la propiedad:`Length`.

```csharp
string txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
Console.WriteLine("La longitud de la cadena es: " + txt.Length);
```

---
## Otros métodos.

Hay muchos métodos de cadena disponibles, por ejemplo `ToUpper()` y `ToLower()`, que devuelve una copia de la cadena convertida a mayúsculas o minúsculas:

```csharp
string txt = "Hello World";
Console.WriteLine(txt.ToUpper());   // Salida: "HELLO WORLD"
Console.WriteLine(txt.ToLower());   // Salida: "hello world"
```

---
## Concatenación de cadenas.

El operador `+` se puede usar entre ***cadenas*** para combinarlas. Esto se llama ***concatenación***:

```csharp
string firstName = "John ";
string lastName = "Doe";

string name = firstName + lastName;

Console.WriteLine(name);
```

***Nota:*** Recuerda, si no dejamos un ***espacio*** dentro de las ***cadenas***, estas se ***concatenaran***, por completo.

También puede usar el método `string.Concat()` para concatenar dos cadenas:

```csharp
string firstName = "John ";
string lastName = "Doe";

string name = string.Concat(firstName, lastName);

Console.WriteLine(name);
```

---
## Sumar números y cadenas.

***Nota:*** ``C#`` usa el operador ``+`` para la ***suma*** y la ***concatenación***. Se suman ***números***. Las ***cadenas*** se concatenan.

Si sumas dos números, el resultado será un número:

```csharp
int x = 10;
int y = 20;
int z = x + y;  // z es 30 (un entero/numero)
```

Si agrega dos cadenas, el resultado será una concatenación de cadenas:

```csharp
string x = "10";
string y = "20";
string z = x + y;  // z es 1020 (un string)
```

---
## Interpolación de cadenas.

Otra opción de ***concatenación de cadenas*** es la ***interpolación de cadenas***, que sustituye los valores de las variables en marcadores de posición en una cadena. 

De este modo, no tenemos que preocuparnos por los espacios, como con la concatenación:

```csharp
string firstName = "John";
string lastName = "Doe";

string name = $"My full name is: {firstName} {lastName}";

Console.WriteLine(name);
```

Debemos usar el signo de dólar (`$`) cuando use el método de interpolación de cadenas, y los valores a imprimir dentro de `{}`.

***Nota:*** La interpolación de cadenas se introdujo en la ***versión 6*** de ***C#***.

---
## Acceso a caracteres de cadenas.

Podemos acceder a los ***caracteres*** de una ***cadena*** haciendo referencia a su número de índice con `[]`.

En el siguiente ***ejemplo*** se imprime el ***primer carácter**** de la variable ***myString***:

```csharp
string myString = "Hello";
Console.WriteLine(myString[0]);  // Salida: "H"
```

***Nota:*** Los índices de cadena comienzan con ``0``: ``[0]`` es el primer carácter. ``[1]`` es el segundo carácter, etc.

En este ejemplo se imprime el ***segundo carácter**** ``[1]`` en ***myString***:

```csharp
string myString = "Hello";
Console.WriteLine(myString[1]);  // Salida: "e"
```

---
## Método `IndexOf()`.

También puede encontrar la ***posición de índice*** de un carácter específico en una ***cadena***, utilizando el método:`IndexOf()`.

```csharp
string myString = "Hello";

Console.WriteLine(myString.IndexOf("e"));  // Salida: "1"
```

---
## Método `Substring()`.

Otro método útil es `Substring()`, que extrae los caracteres de una cadena, a partir de la posición/índice de caracteres especificados y devuelve una nueva cadena. Este método se usa a menudo junto con `IndexOf()` para obtener la posición específica del personaje:

```csharp
// Nombre completo
string name = "John Doe";

// Localización de letra D
int charPos = name.IndexOf("D");

// Obtener apellido
string lastName = name.Substring(charPos);

// Imprimir resultado
Console.WriteLine(lastName);
```

