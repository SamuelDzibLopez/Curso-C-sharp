# 39. Abstracción.

## Clases y métodos abstractos

La ***abstracción*** de datos es el proceso de ocultar ciertos detalles y mostrar solo información esencial al usuario.

La ***abstracción*** se puede lograr con ***clases abstractas*** o ***interfaces***.

La palabra clave `abstract` se usa para ***clases*** y ***métodos***:

- ***Clase abstracta:*** Es una clase restringida que no se puede usar para crear objetos (para acceder a ella, debe heredarse de otra clase).
  
- ***Método abstracto:*** Solo se puede usar en una ***clase abstracta*** y no tiene cuerpo. El cuerpo es proporcionado por la ***clase derivada*** (heredada de).

Una ***clase abstracta*** puede tener ***métodos abstractos*** y ***regulares***:

```c#
abstract class Animal 
{
  public abstract void animalSound();
  public void sleep() 
  {
    Console.WriteLine("Zzz");
  }
}
```

A partir del ejemplo anterior, no es posible crear un ***objeto*** de la clase ``Animal``:

```csharp
Animal myObj = new Animal(); // Error
```

***Nota:*** Para acceder a la ***clase abstracta***, debe heredarse de otra clase.

```csharp
// Clase abstracto
abstract class Animal
{
  // Metodo abstracto (sin contenido)
  public abstract void animalSound();

  // Metodo regular
  public void sleep()
  {
    Console.WriteLine("Zzz");
  }
}

// Clase derivada 
class Pig : Animal
{
  public override void animalSound()
  {
    // Contenido de metodo abstracto, definido en la clase derivada
    Console.WriteLine("The pig says: wee wee");
  }
}

class Program
{
  static void Main(string[] args)
  {
    Pig myPig = new Pig(); // Create a Pig object
    myPig.animalSound();  // Call the abstract method
    myPig.sleep();  // Call the regular method
  }
}
```

---
## ¿Por qué y cuándo usar clases y métodos abstractos?

Para lograr la seguridad, oculte ciertos detalles y muestre solo los importantes detalles de un objeto.

**Nota:** La ***abstracción*** también se puede lograr con ***interfaces***.