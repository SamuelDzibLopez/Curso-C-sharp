# 32. Clases y Objetos.

Todo en`` C#`` está asociado con ***clases*** y ***objetos***, junto con su ***atributos*** y ***métodos***. 

Por ejemplo: en la vida real, un ***automóvil*** es un objeto. El ***automóvil*** tiene ***atributos***, como el peso y el color, y ***métodos***, como la conducción y el freno.

	Una clase es como un constructor de objetos o un "modelo" para crear objetos.

---
## Creación de una clase.

Para crear una ***clase***, use la palabra clave:`class`

```csharp
class Car 
{
  string color = "red";
}
```


***Nota:*** Cuando una ***variable*** se declara directamente en una ***clase***, a menudo se la denomina ***campo*** (o ***atributo***).

No es obligatorio, pero es una buena práctica comenzar con una primera letra mayúscula al nombrar clases. Además, es común que el nombre del archivo ``C#`` y la clase coincidan, ya que hace que nuestro código esté organizado. Sin embargo, no es necesario (como en ***Java***).

---
## Crear un objeto.

Un ***objeto*** se crea a partir de una ***clase***. Ya hemos creado la clase llamada `Car`, así que ahora podemos usar esto para crear ***objetos***. 

```csharp
class Car 
{
  string color = "red";

  static void Main(string[] args)
  {
	//Creacion de objeto de clase Car llamado myObt
    Car myObj = new Car();
    
	//Impresion de atributo color de objeto myObj
    Console.WriteLine(myObj.color);
  }
}
```

---
## Creación de múltiples objetos.

Podemos crear varios objetos de una ***clase***:

```csharp
class Car
{
  string color = "red";
  static void Main(string[] args)
  {
	
	//Creacion de objetos
    Car myObj1 = new Car();
    Car myObj2 = new Car();
    
    //Impresiones
    Console.WriteLine(myObj1.color);
    Console.WriteLine(myObj2.color);
  }
}
```

---
## Uso de varias clases.

También puede crear un objeto de una clase y acceder a él en otra clase. 

Éste se usa a menudo para una mejor organización de las clases (una clase tiene todos los campos y métodos, mientras que la otra clase contiene el método `Main()` (código a ser ejecutado)).


	- Archivo Car.cs:

```csharp
class Car 
{
  public string color = "red";
}
```

	- Program.cs

```csharp
class Program
{
  static void Main(string[] args)
  {
    Car myObj = new Car();
    Console.WriteLine(myObj.color);
  }
}
```


***Nota:*** Para acceder a un atributo de una clase diferente dentro de otra, utilizamos algo que se llama ***modificador de acceso*** (con la palabra `public`), que especifica que la variable/campo `color` de `Car` también es accesible para otras clases, como dentro de `Program`.

