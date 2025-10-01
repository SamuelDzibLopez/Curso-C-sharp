# 40. Interfaces.

Otra forma de lograr la ***abstracción*** en ``C#`` es con ***interfaces***.

Una `interface` es una **"clase abstracta**" completa, que solo puede contener métodos y propiedades abstractas (con cuerpos vacíos):

```java
// interface
interface Animal 
{
  void animalSound(); // interface method (does not have a body)
  void run(); // interface method (does not have a body)
}
```

Se considera una buena práctica comenzar con la letra "I" al comienzo de una interfaz, ya que hace que sea más fácil recordar eso es una interfaz y no una clase.

De forma predeterminada, los miembros de una interfaz son `abstract` y `public`.

***Nota:*** Las ***interfaces*** pueden contener ***propiedades*** y ***métodos***, pero no campos.

Para acceder a los métodos de interfaz, la interfaz debe estar "implementada" (más o menos como heredado) por otra clase. Para implementar una interfaz, use el símbolo `:` (al igual que con la herencia). El cuerpo del método de interfaz es proporcionado por la clase "implement". Tenga en cuenta que no tiene que usar la palabra clave `override` al implementar una interfaz:

```c#
// Interface
interface IAnimal 
{
  void animalSound(); // interface method (does not have a body)
}

// Pig "implements" the IAnimal interface
class Pig : IAnimal 
{
  public void animalSound() 
  {
    // The body of animalSound() is provided here
    Console.WriteLine("The pig says: wee wee");
  }
}

class Program 
{
  static void Main(string[] args) 
  {
    Pig myPig = new Pig();  // Create a Pig object
    myPig.animalSound();
  }
}
```

---
## Notas sobre las interfaces:

	- Al igual que las clases abstractas, las interfaces no se pueden usar para crear objetos (en el ejemplo anterior, no es posible crear un objeto "IAnimal" en la clase Program)
	- Los métodos de interfaz no tienen un cuerpo: el body es proporcionado por la clase "implement"
	- En la implementación de una interfaz, debe anular todos sus métodos
	- Las interfaces pueden contener propiedades y métodos, pero no Campos/variables
	- Los miembros de la interfaz son de forma predeterminada `abstract` y `public`
	- Una interfaz no puede contener un constructor (ya que no se puede usar para crear objetos)

---
## ¿Por qué y cuándo usar interfaces?

	1) Para lograr la seguridad: oculte ciertos detalles y muestre solo los importantes detalles de un objeto (interfaz).

	2) C# no admite la "herencia múltiple" (una clase solo puede heredar de una clase base). Sin embargo, se puede lograr con interfaces, porque la clase puede implementar varias interfaces.

---
## Interfaces Múltiples.

Para implementar varias ***interfaces***, sepárelas con una coma:

```c#
interface IFirstInterface 
{
  void myMethod(); // interface method
}

interface ISecondInterface 
{
  void myOtherMethod(); // interface method
}

// Implement multiple interfaces
class DemoClass : IFirstInterface, ISecondInterface 
{
  public void myMethod() 
  {
    Console.WriteLine("Some text..");
  }
  public void myOtherMethod() 
  {
    Console.WriteLine("Some other text...");
  }
}

class Program 
{
  static void Main(string[] args)
  {
    DemoClass myObj = new DemoClass();
    myObj.myMethod();
    myObj.myOtherMethod();
  }
}
```