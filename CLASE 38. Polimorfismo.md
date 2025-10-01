# 38. Polimorfismo.

***Polimorfismo*** significa "muchas formas", y ocurre cuando tenemos muchas clases que están relacionadas entre sí por herencia.

La ***herencia*** nos permite heredar campos y métodos de otra clase. 

El ***polimorfismo*** usa esos métodos para realizar diferentes tareas. Esto nos permite realizar una solo acción de diferentes maneras.

Por ejemplo, piense en una clase base llamada `Animal` que tiene un método llamado `animalSound()`. Las clases derivadas de animales podrían ser cerdos, gatos, perros, pájaros, y también tienen su propia implementación de un sonido animal (el cerdo aúlla y el gato maúlla, etc.):

```csharp
class Animal  // Base class (parent) 
{
  public void animalSound() 
  {
    Console.WriteLine("The animal makes a sound");
  }
}

class Pig : Animal  // Derived class (child) 
{
  public void animalSound() 
  {
    Console.WriteLine("The pig says: wee wee");
  }
}

class Dog : Animal  // Derived class (child) 
{
  public void animalSound() 
  {
    Console.WriteLine("The dog says: bow wow");
  }
}
```

Ahora podemos crear objetos `Pig` y `Dog`, y llamar al método en ambos: `animalSound()`

```csharp
class Animal  // Base class (parent) 
{
  public void animalSound() 
  {
    Console.WriteLine("The animal makes a sound");
  }
}

class Pig : Animal  // Derived class (child) 
{
  public void animalSound() 
  {
    Console.WriteLine("The pig says: wee wee");
  }
}

class Dog : Animal  // Derived class (child) 
{
  public void animalSound() 
  {
    Console.WriteLine("The dog says: bow wow");
  }
}

class Program 
{
  static void Main(string[] args) 
  {
    Animal myAnimal = new Animal();  // Create a Animal object
    Animal myPig = new Pig();  // Create a Pig object
    Animal myDog = new Dog();  // Create a Dog object

    myAnimal.animalSound();
    myPig.animalSound();
    myDog.animalSound();
  }
}
```

Sin embargo, esto devolverá:

	The animal makes a sound
	The animal makes a sound
	The animal makes a sound

El resultado del ejemplo anterior no fue lo que esperábamos. Esto se debe a que el ***método*** de ***clase base*** invalida el ***método*** de ***clase derivada***, cuando comparten el mismo nombre.

Sin embargo, ``C#`` proporciona una opción para invalidar el método de clase base, agregando la palabra clave `virtual` al método dentro de la ***clase base*** y usando la palabra clave `override` para cada ***método*** de ***clase derivada***:

Realizando:

```csharp
class Animal  // Base class (parent) 
{
  public virtual void animalSound() 
  {
    Console.WriteLine("The animal makes a sound");
  }
}

class Pig : Animal  // Derived class (child) 
{
  public override void animalSound() 
  {
    Console.WriteLine("The pig says: wee wee");
  }
}

class Dog : Animal  // Derived class (child) 
{
  public override void animalSound() 
  {
    Console.WriteLine("The dog says: bow wow");
  }
}

class Program 
{
  static void Main(string[] args) 
  {
    Animal myAnimal = new Animal();  // Create a Animal object
    Animal myPig = new Pig();  // Create a Pig object
    Animal myDog = new Dog();  // Create a Dog object

    myAnimal.animalSound();
    myPig.animalSound();
    myDog.animalSound();
  }
}
```

Salida

	The animal makes a sound  
	The pig says: wee wee  
	The dog says: bow wow

---
## ¿Por qué y cuándo utilizar "herencia" y "polimorfismo"?

Es útil para la reutilización del código: reutiliza campos y métodos de una clase existente cuando creas una nueva clase.

