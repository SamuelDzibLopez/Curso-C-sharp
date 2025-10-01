# 28. Parámetros y argumentos.

La información se puede pasar a los métodos como parámetros. 

	Los parámetros actúan como variables dentro del método.

Se especifican después del nombre del método, dentro de los paréntesis. Puede agregar tantos parámetros como desee, simplemente sepárelos con una coma.


```csharp
  MyMethod("Liam");
```

***Nota:*** Al momento de llamar al ***método/función*** `MyMethod`, pasamos un ***parámetro*** con valor `"Liam"` el cual, es un ``string``.

Veamos el ejemplo:

```csharp
static void MyMethod(string fname) 
{
  Console.WriteLine(fname + " Refsnes");
}

static void Main(string[] args)
{
  MyMethod("Liam");
  MyMethod("Jenny");
  MyMethod("Anja");
}

// Liam Refsnes
// Jenny Refsnes
// Anja Refsnes
```

En el ejemplo siguiente, en la función se define un `string` de nombre ``fname`` como ***parámetro*** (al enviar un valor, debe coincidir con el mismo ***tipo de dato*** definido). Cuando se llama al ***método***, pasamos un ``string``, que se usa dentro del método para imprimir el nombre completo.

***Nota:*** Cuando se pasa un ***parámetro*** al método, se denomina ***argumento***. Entonces, del ejemplo anterior: `fname` es un ***parámetro***, mientras que `Liam`, `Jenny` y `Anja` son ***argumentos***.

Los ***parámetros*** solo existen y pueden ser utilizados dentro del ***código*** del ***método/función***.

---
## Múltiples parámetros.

Se pueden tener tantos parámetros como se desee, simplemente debemos separarlos con comas:

```csharp
static void MyMethod(string fname, int age) 
{
  Console.WriteLine(fname + " is " + age);
}

static void Main(string[] args)
{
  MyMethod("Liam", 5);
  MyMethod("Jenny", 8);
  MyMethod("Anja", 31);
}

// Liam is 5
// Jenny is 8
// Anja is 31
```

***Nota:*** Debemos definir los tipos de datos que deben cumplir los ***parámetros***.

***Nota:*** Cuando se trabaja con varios parámetros, la llamada al método debe tener el mismo número de argumentos que parámetros, y los argumentos deben pasarse en el mismo orden.

---
## Parámetros con valor predeterminado.

También puede usar un valor de parámetro predeterminado, usando el signo igual (`=`).

Si llamamos al método sin pasar el argumento, el ***método/función*** utilizará el valor predeterminado (``"Noruega"``):

```csharp
static void MyMethod(string country = "Norway") 
{
  Console.WriteLine(country);
}

static void Main(string[] args)
{
  MyMethod("Sweden");
  MyMethod("India");
  MyMethod();
  MyMethod("USA");
}

// Sweden
// India
// Norway
// USA
```

***Nota:*** Un ***parámetro*** con un valor predeterminado a menudo se conoce como ***"parámetro opcional***". En el ejemplo anterior,`country` es un parámetro opcional y `"Norway"` es el valor predeterminado.

---
## Argumentos por nombre.

También es posible enviar argumentos con la sintaxis.`key: value`.

De esa manera, el orden de los argumentos no importa:

```csharp
static void MyMethod(string child1, string child2, string child3) 
{
  Console.WriteLine("The youngest child is: " + child3);
}

static void Main(string[] args)
{
  MyMethod(child3: "John", child1: "Liam", child2: "Liam");
}

// The youngest child is: John
```

***Nota:*** Recordemos que si no pasamos por tipo `key: value`, se pasa por orden.