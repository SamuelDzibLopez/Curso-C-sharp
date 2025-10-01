# 34. Contructores.

Un ***constructor*** es un ***método especial*** que se usa para inicializar ***objetos***. La ***ventaja*** de un ***constructor*** es que se llama cuando se crea un objeto de una clase. 

Puede se utilizará para establecer valores iniciales para los campos:

```csharp
// Create a Car class
class Car
{
  public string model;  // Create a field

  // Create a class constructor for the Car class
  public Car()
  {
    model = "Mustang"; // Set the initial value for model
  }

  static void Main(string[] args)
  {
    Car Ford = new Car();  // Create an object of the Car Class (this will call the constructor)
    Console.WriteLine(Ford.model);  // Print the value of model
  }
}

// Outputs "Mustang"
```

***Nota:*** Tenga en cuenta que el nombre del constructor debe ***coincidir*** con el ***nombre*** de la ***clase*** y no puede tener un **t*ipo de valor devuelto*** (como `void` o `int`). 

	Tenga en cuenta también que se llama al constructor cuando se crea el objeto.

Todas las clases tienen constructores de forma predeterminada: si no crea una clase constructor usted mismo, C# crea uno para usted. Sin embargo, entonces no puedes para establecer valores iniciales de esa manera para los campos.

Entonces:

	Un contructor es un método de la clase que al invocarse, crea un objeto de esa clase.

---
## Parámetros del constructor.

Los constructores también pueden tomar ***parámetros***, que se utilizan para inicializar los ***atributos***.

En el ejemplo siguiente se agrega un ***parámetro*** al constructor.

```csharp
class Car
{
  public string model;

  // Constructor con parametro 
  public Car(string modelName)
  {
	//modelName toma el valor del atributo model del objeto a crear
    model = modelName;
  }

  static void Main(string[] args)
  {
	//Creacion de objeto Ford de clase Car, pasando parametro (el cual tomara el valor de model en el constructor)
    Car Ford = new Car("Mustang");
    
    //Impresion de valor de atributo model de objeto ford
    Console.WriteLine(Ford.model);
  }
}

// Salida: "Mustang"
```

***Nota:*** Los ***parámetros*** enviados al ***constructor*** son utilizados para definir los valores de los atributos del ***objeto*** a crear.

Puedes tener tantos parámetros como quieras:

```C#
class Car
{
  public string model;
  public string color;
  public int year;

  // Constructor con multiples parametros
  public Car(string modelName, string modelColor, int modelYear)
  {
    model = modelName;
    color = modelColor;
    year = modelYear;
  }

  static void Main(string[] args)
  {
    Car Ford = new Car("Mustang", "Red", 1969);
    Console.WriteLine(Ford.color + " " + Ford.year + " " + Ford.model);
  }
}


// Salida: "Red 1969 Mustang"
```

***Nota:*** Al igual que otros ***métodos***, los constructores se pueden ***sobrecargar*** mediante el uso de diferentes números de parámetros.

---
## Los constructores ahorran tiempo.

	Los constructores son muy útiles, ya que ayudan a reducir la cantidad de código

	- Sin Contructor:

```csharp
class Program
{
  static void Main(string[] args)
  {
    Car Ford = new Car();
    Ford.model = "Mustang";
    Ford.color = "red";
    Ford.year = 1969;

    Car Opel = new Car();
    Opel.model = "Astra";
    Opel.color = "white";
    Opel.year = 2005;

    Console.WriteLine(Ford.model);
    Console.WriteLine(Opel.model);
  }
}
```

	- Con constructor:

```csharp
class Program
{
  static void Main(string[] args)
  {
    Car Ford = new Car("Mustang", "Red", 1969);
    Car Opel = new Car("Astra", "White", 2005);

    Console.WriteLine(Ford.model);
    Console.WriteLine(Opel.model);
  }
}
```


