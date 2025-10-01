# 06. Variables.

Las variables son contenedores para almacenar valores de datos.

En  ``C#`` , hay diferentes ***tipos de variables*** (definidas con diferentes palabras clave), por ejemplo:

- `int` - almacena números enteros (números enteros), sin decimales, como 123 o -123
- `double` - almacena números de coma flotante, con decimales, como 19.99 o -19.99
- `char` - almacena caracteres individuales, como 'a' o 'B'. Los valores de caracteres están entre comillas simples.
- `string` - almacena texto, como "Hola mundo". Los valores de cadena están entre comillas dobles
- `bool` - Almacena valores con dos estados: verdadero o falso.

---
## Declaración (creación) de variables.

Para crear una variable, especifique el **tipo** y asígnele un **valor**:

~~~c#
type variableName = value;
~~~

Donde ***type*** es un tipo de ``C#`` (como `int` o `string`) y ***variableName*** es el nombre de la variable (como **x** o **name**). El **signo igual** se utiliza para asignar valores a la variable.

Tal como el ejemplo:

~~~csharp
//Declaracion de variable name de tipo string
string name = "John";

//Impresion de valor de name
Console.WriteLine(name);
~~~

Para crear una variable que debe almacenar un número, observe el siguiente ejemplo:

~~~csharp
//Declaracion de variable myNum de tipo int
int myNum = 15;

//Impresion de valor de myNum
Console.WriteLine(myNum);
~~~

***Nota:*** También puede declarar una variable sin asignar el valor y asignar el valor más adelante.

~~~csharp
// Declaracion de variable myNum con tipo de dato int
int myNum;

//Asignacion de valor a variable ya declarada
myNum = 15;

//Impresion de valor de myNum
Console.WriteLine(myNum);
~~~

***Nota:*** Tengamos en cuenta que si asignamos un nuevo valor a una variable existente, sobrescribirá el valor anterior:

---
## Otros tipos.

Una demostración de cómo declarar variables de otros tipos:

~~~csharp
int myNum = 5;
double myDoubleNum = 5.99D;
char myLetter = 'D';
bool myBool = true;
string myText = "Hello";
~~~

***Nota:*** Sobre estos datos, explicaremos mejor en futuras lecciones.