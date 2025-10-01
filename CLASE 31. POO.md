# 31. POO.

	POO significa Programación Orientada a Objetos.

La programación procedimental consiste en escribir procedimientos o métodos que realicen operaciones en los datos, mientras que la programación orientada a objetos se trata de crear objetos que contengan datos y métodos.

Esto es ***programación procedimental***:

```c#
string txt = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";

Console.WriteLine("La longitud de la cadena es: " + txt.Length);
```

***Nota:*** Porque la lógica y valores no se ejecutan ni se encuentran en clases y objetos.

Mientras que ***programación orientada a objetos*** es:

```csharp
using System;
namespace HelloWorld

{
	class Program
	{
		static void MyMethod() 
		{
		  Console.WriteLine("I just got executed!");
		}

		static void Main(string[] args)
		{
			MyMethod();   
		}
	}
}
```

***Nota:*** Porque ejecutamos el ***método*** ``MyMethod``, el cual pertenece a la clase `Program`.

***Nota:*** Ahora vamos entendiendo mejor el código. `Main` es un método que pertenece a la clase `Program`. el cual no regresa un valor al ejecutarse (`void`).

La programación orientada a objetos tiene varias ventajas sobre la programación procedimental programación:

	- POO es más rápido y fácil de ejecutar.
	- POO proporciona una estructura clara para los programas.
	- POO ayuda a mantener el código C# SECO "No te repitas", y hace que el Código más fácil de mantener, modificar y depurar.
	- POO permite crear Aplicaciones con menos código y menor tiempo de desarrollo.

***Nota:*** El principio de ``"No repetir código"`` se trata de reducir la repetición de código (de allí aprendimos para que sirven los métodos/funciones). Debe extraer los códigos que son común para la aplicación, y colóquelos en un solo lugar y reutilícelos en lugar de repetirlo.

---
## ¿Qué son las clases y los objetos?

Las ***clases*** y los ***objetos*** son los dos aspectos principales de la ***programación orientada a objetos***.

Para entender mejor y manera más simple:

	Clase:

	Una clase es un código que se utiliza para crear elementos con caracteristicas y funciones que tengan estos, definidos en el código de la clase.

	Objeto:

	Un objeto es un elemento creado por medio de una clase, de modo que obtiene (hereda) las caracteristicas (valores) y funciones (métodos) definidos en la clase con la que se creo.

***Nota:*** Podemos decir que las ***clases*** son como los ***moldes*** para crear ***objetos*** que tengan ***características*** que deseamos definir.

Por ejemplo:

	1. Queremos crear una clase para crear frutas, entonces:
		A. Creamos una clase a la que llamaremos "Fruta", que tenga caracteristicas (valores que se llenaran al crear objetos):
			a. Nombre.
			b. Color.
			c. Sabor.
		B. Utilizando la clase "Fruta" crearemos 3 objetos, los cuales seran y tendran los valores:
			Manzana = {
				Nombre: "Manzana",
				Color: "Rojo",
				Sabor: "Dulce"
			}
			Limon = {
				Nombre: "Limon",
				Color: "Verde",
				Sabor: "Agrio"
			}
			Mango = {
				Nombre: "Mango",
				Color: "Amarillo",
				Sabor: "Dulce"
			}

	2. Queremos crear una clase para crear coches, entonces:
		A. Creamos una clase a la que llamaremos "Coche", que tenga caracteristicas (valores que se llenaran al crear objetos) y métodos (funciones que puedan realizar los objetos):


			a. Marca. 
			b. Color.
			c. numeroRuedas.

			i. Encender.
			ii. Apagar.
			iii. Acelerar.

		B. Utilizando la clase "Coche" crearemos 3 objetos, los cuales seran y tendran los valores:
			Camioneta = {
				Marca: "Toyota",
				Color: "Blanco",
				numeroRuedas: 4
			}
			Trailer = {
				Marca: "Nissan",
				Color: "Negro",
				numeroRuedas: 16
			}
			Moto = {
				Marca: "Italika",
				Color: "Verde",
				numeroRuedas: 2
			}

		C. Al crear cada objeto de tipo/clase "Coche", todos los elementos tienen la habilidad y funciones de: 
			i. Encender.
			ii. Apagar.
			iii. Acelerar.

Así de fácil funciona la lógica de las clases y objetos.

***Nota:*** Recuerda, cuando se crean los objetos individuales, heredan todos los variables y métodos definidos en la clase.