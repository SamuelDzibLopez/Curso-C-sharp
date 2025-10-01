# 35. Modificadores de Acceso.

A estas alturas, ya estamos bastante familiarizado con la palabra clave `public`, la cual aparece en muchos de los ejemplos:

	"public" se utiliza para poder ser utilizar el atributo/método fuera de su clase.

```csharp
public string color;
```

La palabra clave `public` es un ***modificador de acceso***, que se utiliza para establecer el ***nivel de acceso/visibilidad*** de las ***clases***, ***campos***, ***métodos*** y ***propiedades***.

``C#`` tiene los siguientes modificadores de acceso:

| Modifier    | Description                                                                                 |
| ----------- | ------------------------------------------------------------------------------------------- |
| `public`    | El código es accesible para todas las clases                                                |
| `private`   | El código solo es accesible dentro de la misma clase                                        |
| `protected` | El código es accesible dentro de la misma clase, o en una clase que se hereda de esa clase. |
| `internal`  | El código solo es accesible dentro de su propio ensamblaje, pero no desde otro ensamblaje.  |
También hay dos combinaciones: `protected internal` y `private protected`.

Por ahora, centrémonos en `public` y `private`.

---
## Modificador `private`.

Si declara un campo con un modificador de acceso `private`, solo puede ser accedido dentro de la misma clase:

```csharp
class Car
{
  private string model = "Mustang";
  
  static void Main(string[] args)
  {
    Car myObj = new Car();
    Console.WriteLine(myObj.model);
  }
}

//Salida: Mustang
```

Si intentamos acceder a él fuera de la clase, se producirá un error:

```csharp
class Car
{
  private string model = "Mustang";
}

class Program
{
  static void Main(string[] args)
  {
    Car myObj = new Car();
    Console.WriteLine(myObj.model);
  }
}

//Salida: Error
```

a salida será:

	`'Car.model' es inaccesible debido a su nivel de protección. El campo 'Car.model' está asignado pero su valor nunca se utiliza`.

---
## Modificador `public`.

Si declara un campo con un modificador de acceso `public`, es accesible para utilizarse dentro de todas las clases.

```csharp
class Car
{
  public string model = "Mustang";
}

class Program
{
  static void Main(string[] args)
  {
    Car myObj = new Car();
    Console.WriteLine(myObj.model);
  }
}
```

La salida será:

	Mustang

---
## ¿Por qué acceder a los modificadores?

Para controlar la visibilidad de los miembros de la clase (el nivel de seguridad de cada clase individual y miembro de la clase).

Para lograr la "***encapsulación***", que es el proceso de asegurarse de que los datos "confidenciales" estén ocultos para los usuarios. Esto se hace declarando los campos como `private`.

***Nota:*** De forma predeterminada, todos los miembros de una clase son si no especifica un modificador de acceso:`private`.

```csharp
class Car
{
  string model;  // private
  string year;   // private
}
```

---
