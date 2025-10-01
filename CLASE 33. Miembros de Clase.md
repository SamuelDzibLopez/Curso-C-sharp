# 33. Miembros de Clase.

	Los campos y métodos dentro de las clases a menudo se denominan "miembros de clase":

```C#
// La clase
class MyClass
{
  // Miembros de Clase
  string color = "red";        // atributo
  int maxSpeed = 200;          // atributo
  public void fullThrottle()   // metodo
  {
    Console.WriteLine("The car is going as fast as it can!");
  }
}
```

También podemos definir nosotros los valores de los ***atributos*** de cada objeto nosotros mismos al momento de crearlos:

```csharp
class Car 
{
  string color; //Atributo solo definido, sin valor
  int maxSpeed; //Atributo solo definido, sin valor

  static void Main(string[] args)
  {
	//Creacion de objeto llamado myObj
    Car myObj = new Car();
    
    //Asignacion de valor "red" a atributo color de objeto myObj
    myObj.color = "red";
    
    //Asignacion de valor 200 a atributo maxSpeed de objeto myObj
    myObj.maxSpeed = 200;
    
    //Impresion de valor de atributos color y maxSpeed de objeto myObj
    Console.WriteLine(myObj.color);
    Console.WriteLine(myObj.maxSpeed);
  }
}
```

Esto es especialmente útil cuando se crean varios objetos de una clase:

```csharp
class Car 
{
  string model;
  string color;
  int year;

  static void Main(string[] args)
  {
	// Creacion de objeto Ford de clase Car
    Car Ford = new Car();
    //Definicion de los valores de sus atributos
    Ford.model = "Mustang";
    Ford.color = "red";
    Ford.year = 1969;

	// Creacion de objeto Opel de clase Car
    Car Opel = new Car();
    //Definicion de los valores de sus atributos
    Opel.model = "Astra";
    Opel.color = "white";
    Opel.year = 2005;

	//Impresion de atributo model de objeto Ford
    Console.WriteLine(Ford.model);
    //Impresion de atributo model de objeto Opel
    Console.WriteLine(Opel.model);
  }
}
```

---
## Métodos.

	Los métodos son funciones o acciones definidas en una clase que al crearse objetos, son obtenidos para que puedan ejecutarse.

Los métodos normalmente pertenecen a una clase y definen cómo se comporta un objeto de una clase.

Al igual que con los campos, puede acceder a los métodos con la sintaxis de puntos. Sin embargo, tenga en cuenta que El método debe ser `public`. Y recuerda que usamos el nombre del método seguido de dos paréntesis y un punto y coma para llamar (ejecutar) al método:`();`

```csharp
class Car 
{
  string color;                 // atributo
  int maxSpeed;                 // atributo
  public void fullThrottle()    // metodo
  {
    Console.WriteLine("¡El coche va tan rápido como puede!"); 
  }

  static void Main(string[] args)
  {
	//Creacion de objeto
    Car myObj = new Car();
    
    myObj.fullThrottle();  // llamado a ejecutar el metodo 
  }
}
```

***Nota:*** Recordemos para que sirven las palabras:

	- public: Permite que el método o atributo del objeto que tenga ese atributo/método pueda utilizarse o ser accesible desde otra clase.
	- void: Que la función/método no devuelve un valor.
	- fullThrottle: Nombre de la función/metodo.
	- (): Dentro van los argumentos a pasar a la función/metodo, en el ejemplo, no recibe ningunno.

Para llamar al método:

	- myObj.fullThrottle(); : Accedemos al objeto creado (myObj), luego con la notacion punto, llamamos al metodo llamado fullThrottle, y "();" para decir que se ejecute. (Esta instruccion podra definirse como: Ejecuta (();) en el objeto (myObj) el método fullThrottle).

---

***Nota:*** ¿Por qué declaramos el método como `public`, y no como `static`?, ¿tal como hemos realizado en clases anteriores?: La razón es simple: con `static` se puede acceder a un método sin crear un objeto de la clase (definiendo en vez del objeto donde se encuentra el método, la clase), mientras que los métodos `public` solo pueden ser accedidos por objetos.