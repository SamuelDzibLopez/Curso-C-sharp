# 42. Archivos.

La clase `File` `System.IO`, nos permite trabajar con archivos: 

```csharp
using System.IO;  // include the System.IO namespace

File.SomeFileMethod();  // use the file class with methods
```

La clase `File` tiene muchos métodos útiles para crear y obtener información acerca de los archivos. Por ejemplo:

| Method           | Description                                                                                    |
| ---------------- | ---------------------------------------------------------------------------------------------- |
| `AppendText()`   | Agrega texto al final de un archivo existente                                                  |
| `Copy()`         | Copia un archivo                                                                               |
| `Create()`       | Crea o sobrescribe un archivo                                                                  |
| `Delete()`       | Elimina un archivo                                                                             |
| `Exists()`       | Prueba si el archivo existe                                                                    |
| `ReadAllText()`  | Lee el contenido de un archivo                                                                 |
| `Replace()`      | Reemplaza el contenido de un archivo con el contenido de otro archivo                          |
| `WriteAllText()` | Crea un nuevo archivo y escribe su contenido en él. Si el archivo ya existe, se sobrescribirá. |

Para una mejor documentación:

	https://learn.microsoft.com/en-us/dotnet/api/system.io.file?view=netframework-4.8

---
## Escribir en un archivo y leerlo.

En siguiente ejemplo, usamos el método `WriteAllText()` para crear un archivo llamado "filename.txt" y escribir contenido en él. Luego usamos el método `ReadAllText()` para leer el contenido del archivo:

```c#
using System.IO;  // include the System.IO namespace

string writeText = "Hello World!";  // Create a text string
File.WriteAllText("filename.txt", writeText);  // Create a file and write the content of writeText to it

string readText = File.ReadAllText("filename.txt");  // Read the contents of the file
Console.WriteLine(readText);  // Output the content
```

La salida será:

	Hello World!

