# 12. Operadores.

Los ***operadores*** se utilizan para realizar ***operaciones*** en ***variables*** y ***valores***.

En el siguiente ejemplo, usamos el ***operador*** `+` para sumar dos valores:

```csharp
int x = 100 + 50;
```

Aunque el operador `+` se usa a menudo para ***sumar*** dos valores, como en el ejemplo anterior, también se puede usar para sumar una variable y un valor, o una variable y otra variable:

```csharp
int sum1 = 100 + 50;        // 150 (100 + 50)
int sum2 = sum1 + 250;      // 400 (150 + 250)
int sum3 = sum2 + sum2;     // 800 (400 + 400)
```

---
## Operadores aritméticos.

Los ***operadores aritméticos*** se utilizan para realizar operaciones matemáticas comunes:

| Operator | Name           | Description                            | Example |
| -------- | -------------- | -------------------------------------- | ------- |
| +        | Addition       | Adds together two values               | x + y   |
| -        | Subtraction    | Subtracts one value from another       | x - y   |
| *        | Multiplication | Multiplies two values                  | x * y   |
| /        | Division       | Divides one value by another           | x / y   |
| %        | Modulus        | Returns the division remainder         | x % y   |
| ++       | Increment      | Increases the value of a variable by 1 | x++     |
| --       | Decrement      | Decreases the value of a variable by 1 | x--     |

---
## Operadores de asignación.

Los ***operadores de asignación*** se utilizan para asignar valores a las variables.

En el siguiente ejemplo, se utiliza el operador **de asignación** (`=`) Para asignar el valor ``10`` a una variable llamada `x`:

```csharp
int x = 10;
```

El operador de ***asignación de suma*** (`+=`) agrega un valor a una variable:

```csharp
int x = 10;
x += 5;
```

Una lista de todos los operadores de asignación:

| Operador | Ejemplo | Equivale a |
| -------- | ------- | ---------- |
| =        | x = 5   | x = 5      |
| +=       | x += 3  | x = x + 3  |
| -=       | x -= 3  | x = x - 3  |
| *=       | x *= 3  | x = x * 3  |
| /=       | x /= 3  | x = x / 3  |
| %=       | x %= 3  | x = x % 3  |
| &=       | x &= 3  | x = x & 3  |
| \|=      | x \|= 3 | x = x \| 3 |
| ^=       | x ^= 3  | x = x ^ 3  |
| >>=      | x >>= 3 | x = x >> 3 |
| <<=      | x <<= 3 | x = x << 3 |

---
## Operadores de comparación.

Los ***operadores de comparación*** se utilizan para ***comparar*** dos valores (o variables). Esto es importante en la programación, porque nos ayuda a encontrar respuestas y tomar decisiones.

El valor devuelto de una comparación es `True` o `False`. Es decir, valores ***booleanos***.

En el siguiente ejemplo, usamos el ***operador mayor que*** (`>`) para averiguar si ``5`` es mayor que `3`:

```csharp
int x = 5;
int y = 3;
Console.WriteLine(x > y); // True, porque 5 es mayor a 3
```

Una lista de todos los operadores de comparación:

| Operador | Nombre          | Ejemplo |
| -------- | --------------- | ------- |
| ==       | Igual a         | x == y  |
| !=       | No igual        | x != y  |
| >        | Mayor que       | x > y   |
| <        | Menor que       | x < y   |
| >=       | Mayor o igual a | x >= y  |
| <=       | Menor o igual a | x <= y  |

---
## Operadores lógicos.

Al igual que con los ***operadores de comparación***, también puede probar valores `True`o `False` con **operadores lógicos**.

Los ***operadores lógicos*** se utilizan para determinar la lógica entre variables o valores:

| Operador | Nombre          | Descripción                                                        | Ejemplo            |
| -------- | --------------- | ------------------------------------------------------------------ | ------------------ |
| &&       | AND lógico      | Devuelve True si ambas afirmaciones son verdaderas                 | x < 5 &&  x < 10   |
| \|       | OR lógico       | Devuelve True si una de las declaraciones es verdadera             | x < 5 \| x < 4     |
| !        | Negación logica | Invierte el resultado, devuelve Falso si el resultado es verdadero | !(x < 5 && x < 10) |
