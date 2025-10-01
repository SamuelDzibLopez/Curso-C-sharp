# 37. Herencia.

En ``C#``, es posible heredar campos y métodos de una clase a otra. Agrupamos el "concepto de herencia" en dos categorías:

	- Clase derivada (secundaria): la clase que hereda de otra clase.
	- Clase base (padre): la clase que se hereda de.

Para heredar de una clase, use el símbolo.`:`

En el ejemplo siguiente, la clase (hijo) `Car` hereda los campos y métodos de la clase (padre): `Vehicle`.

```csharp
class Vehicle  // Clase base (padre) 
{
  public string brand = "Ford";  // Atributo de clase padre
  public void honk()             // Metodo de clase padre 
  {                    
    Console.WriteLine("Tuut, tuut!");
  }
}

class Car : Vehicle  // Clase derivada (hijo)
{
  public string modelName = "Mustang";  // Atributo de clase hijo
}

class Program
{
  static void Main(string[] args)
  {
    // Crear objeto myCar de clase Car (Es decir, es de la clase Vehicle tambien, porque Car es una clase hija de Vehicle)
    Car myCar = new Car();

    // Llamar al metodo honk (Como myCar es de clase Car, y Car es hijo de la clase Vehicle, entonces myCar hereda los atributos y metodos de Vehicle tambien)
    myCar.honk();

    // Impresion
    Console.WriteLine(myCar.brand + " " + myCar.modelName);
  }
}

// Salida: "Ford Mustang"
```

- La ***herencia*** es útil para la ***reutilización*** del ***código***: reutiliza campos y métodos de una clase existente cuando creas una ***nueva clase***.

***Nota:*** En cortas palabras, la herencia es crear clases que hereden los atributos y métodos de las clases superiores, las como crear subclases para crear categorías de los objetos a crear de una clase.

---
## Palabra clave `sealed` (sellado).

Si no deseamos que otras clases hereden de una clase, use la palabra clave:`sealed`.

```csharp
ealed class Vehicle 
{
  ...
}

class Car : Vehicle 
{
  ...
}
```

***Nota:*** Si intenta acceder a una clase `sealed`, ``C#`` generará un error:

	'Car': cannot derive from sealed type 'Vehicle'.

