# 36. Propiedades y encapsulación.

Antes de comenzar a explicar las propiedades, debe tener una comprensión básica de la ***encapsulación***.

El significado de ***encapsulación*** es asegurarse de que los datos "confidenciales" estén ocultos de los usuarios.

Para lograrlo, debes:

	- Declarar campos/variables como `private`.
	- proporcionar métodos `public`, a través de propiedades `get` Y `set`, para acceder y actualizar el valor de un campo `private`.

---
## Propiedades.

Recordemos que las variables `private` solo pueden ser se accede dentro de la misma clase (una clase externa no tiene acceso a ella). Sin embargo A veces necesitamos acceder a ellos, y se puede hacer con propiedades.

Una propiedad es como una combinación de una variable y un método, y tiene dos métodos: a `get` y un método `set`:

```csharp
class Person
{
  private string name; // atributo

  public string Name //Propiedad
  {
    get { return name; }   // metodo get
    set { name = value; }  // metodo set
  }
}
```

La ***propiedad*** `Name` está asociada al campo `name`. Es una buena práctica usar el mismo nombre tanto para la propiedad como para el campo privado, pero con una primera letra mayúscula.

El método `get` devuelve el valor de la variable `name`.

El método `set` asigna `value` a la variable `name`. La palabra clave `value` representa el valor que asignamos a la propiedad.

En otras palabras:

	get: Se utiliza para obtener el valor de un atributo de tipo "private".
	set: Se utiliza para asignar/modificar el valor de un atributo de tipo "private".

Ahora podemos usar la propiedad `Name` para acceder y actualizar el campo `private` de la clase `Person`:

```csharp
class Person
{
  private string name; // Atributo
  public string Name   // Propiedad
  {
    get { return name; }
    set { name = value; }
  }
}

class Program
{
  static void Main(string[] args)
  {
	//Creacion de objeto
    Person myObj = new Person();
    
    //set se ejecuta enviando y asignando un valor
    myObj.Name = "Liam";
    
    //get se ejecuta consultando su valor
    Console.WriteLine(myObj.Name);
  }
}

//Salida: Liam
```

---
## Propiedades automáticas (mano abreviada).

``C#`` también proporciona una manera de usar propiedades abreviadas o automáticas, donde no tiene que definir el campo para la propiedad, y solo tiene que escribir `get;` y `set;` dentro de la propiedad.

El siguiente ejemplo producirá el mismo resultado que el ejemplo anterior. La única diferencia es que hay menos código:

```csharp
class Person
{
  public string Name  // Propiedad
  { get; set; }
}

class Program
{
  static void Main(string[] args)
  {
    Person myObj = new Person();
    myObj.Name = "Liam";
    Console.WriteLine(myObj.Name);
  }
}

// Salida: Liam
```

---
## ¿Por qué encapsulación?

	- Mejor control de los miembros de la clase (reducir la posibilidad de que usted (u otros) estropee el código).
	- Los campos se pueden convertir en de solo lectura (si solo usa el método get) o de solo escritura (si solo usa el método set).
	- Flexible: el programador puede cambiar una parte del código sin afectar a otras partes.
	- Mayor seguridad de los datos.





