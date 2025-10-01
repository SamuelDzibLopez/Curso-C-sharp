# 09. Otros tipos de datos.

Como se explicó en la lección de variables, una variable en`` C#`` debe ser un tipo de datos especificado.

En `C#` existen ***tipos de datos***:

```csharp
int myNum = 5;               // Entero (numeros enteros)
double myDoubleNum = 5.99D;  // Flotante numeros con decimales
char myLetter = 'D';         // Caracteres
bool myBool = true;          // Booleanos
string myText = "Hello";     // Cadenas de texto
```

Un ***tipo de datos*** especifica el **tamaño** y el ***tipo de valores*** de una ***variable***.

***Nota:*** Es importante utilizar el tipo de datos correcto para la variable correspondiente; para evitar errores, para ahorrar tiempo y memoria, pero también hará que su código sea más fácil de mantener y leer. 

Los más comunes Los tipos de datos son:

| Data Type | Size                  | Description                                                                               |
| --------- | --------------------- | ----------------------------------------------------------------------------------------- |
| `int`     | 4 bytes               | Almacena números enteros desde -2.147.483.648 hasta 2.147.483.647                         |
| `long`    | 8 bytes               | Almacena números enteros desde -9,223,372,036,854,775,808 hasta 9,223,372,036,854,775,807 |
| `float`   | 4 bytes               | Almacena números fraccionarios. Suficiente para almacenar de 6 a 7 dígitos decimales      |
| `double`  | 8 bytes               | Almacena números fraccionarios. Suficiente para almacenar 15 dígitos decimales            |
| `bool`    | 1 byte                | Almacena valores verdaderos o falsos                                                      |
| `char`    | 2 bytes               | Almacena un solo carácter/letra, rodeado por comillas simples                             |
| `string`  | 2 bytes per character | Almacena una secuencia de caracteres, rodeada por comillas dobles                         |

---
## Tipos de datos enteros.

### int.

El tipo de datos `int` puede almacenar números enteros de -2147483648 a 2147483647. En general, el tipo de dato `int` es el tipo de dato preferido para crear variables con un valor numérico.

```csharp
int myNum = 100000;
Console.WriteLine(myNum);
```

### long.

El tipo de dato `long` puede almacenar números enteros de -9223372036854775808 a 9223372036854775807. Esto se usa cuando `int` no es lo suficientemente grande como para almacenar el valor. 

***Nota:*** Ten en cuenta que debe terminar el valor con una "L":

```csharp
long myNum = 15000000000L;
Console.WriteLine(myNum);
```

---
## Tipos de datos flotantes.

Se debe usar un tipo de punto flotante siempre que necesite un número con un decimal, como 9.99 o 3.14515.

Los tipos de datos `float` y `double` pueden almacenar números fraccionarios. Tenga en cuenta que debe terminar el valor con una "F" para los flotantes y una "D" para los dobles:

```csharp
float myNum = 5.75F;
Console.WriteLine(myNum);
```

Y:

```csharp
double myNum = 19.99D;
Console.WriteLine(myNum);
```
### Números científicos.

Un ***número flotante*** también puede ser un número científico con una "e" para indicar la potencia de 10:

```csharp
float f1 = 35e3F;
double d1 = 12E4D;
Console.WriteLine(f1);
Console.WriteLine(d1);
```

---
## Tipos de datos booleanos.

Un tipo de datos ***booleano*** se declara con la palabra clave `bool` y solo puede tomar los valores `true` o `false`.

```csharp
bool isCSharpFun = true;
bool isFishTasty = false;
Console.WriteLine(isCSharpFun);   // True
Console.WriteLine(isFishTasty);   // False
```

Los valores booleanos se utilizan principalmente para pruebas condicionales.

---
## Tipos de datos char.

El tipo de datos `char` se usa para almacenar un ***solo*** carácter. El personaje debe ser entre comillas simples, como ``'A'`` o ``'c'``:

```csharp
char myGrade = 'B';
Console.WriteLine(myGrade);
```

---
## Tipos de datos strings.

El tipo de datos `string` se utilizan para almacenar una secuencia de caracteres (texto). Los valores de cadena deben estar entre comillas dobles:

```csharp
string greeting = "Hello World";
Console.WriteLine(greeting);
```

