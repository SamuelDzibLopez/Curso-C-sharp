# 10. Conversión de tipos de datos.

La ***conversión*** de tipos es cuando se asigna un valor de un tipo de datos a otro tipo.

En ``C#``, hay dos tipos de fundición:

- **Conversión implícita** (automáticamente): conversión de un tipo más pequeño a un tamaño de letra más grande  
    `char` -> `int` -> `long` -> `float` -> `double`  

- **Conversión explícita** (manualmente): conversión de un tipo más grande a un tipo de tamaño más pequeño  
    `double` -> `float` -> `long` -> `int` -> `char`

---
## Conversión implícita.

La ***conversión implícita*** se realiza automáticamente al pasar un tipo de tamaño más pequeño a un Tipo de tamaño más grande:

```csharp
int myInt = 9;
double myDouble = myInt;       // conversion implícita: int a double

Console.WriteLine(myInt);      // Salida: 9
Console.WriteLine(myDouble);   // Salida: 9
```

---
## Conversión explicita.

La ***conversión explícita*** debe realizarse manualmente colocando el tipo entre paréntesis delante del valor:

```csharp
double myDouble = 9.78;
int myInt = (int) myDouble;    // conversion explicita: double a int

Console.WriteLine(myDouble);   // Salida: 9.78
Console.WriteLine(myInt);      // Salida: 9
```

---
## Métodos de conversión de tipos.

También es posible convertir tipos de datos explícitamente mediante métodos integrados, como:

```csharp
int myInt = 10;
double myDouble = 5.25;
bool myBool = true;

Console.WriteLine(Convert.ToString(myInt));    // Convertir int a string
Console.WriteLine(Convert.ToDouble(myInt));    // Convertir int a double
Console.WriteLine(Convert.ToInt32(myDouble));  // Convertir double a int
Console.WriteLine(Convert.ToString(myBool));   // Convertir bool a string
```

***Nota:*** Muchas veces, no es necesario realizar una conversión de tipos. Pero a veces tienes que hacerlo para realizar ciertas acciones.

