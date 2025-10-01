# 15. Caracteres Especiales.

Imagina que deseamos imprimir en consola el siguiente texto:

	We are the so-called "Vikings" from the north.

Dado que las cadenas deben escribirse entre comillas, ``C#`` malinterpretará esta cadena, y genere un error:

```csharp
string txt = "We are the so-called "Vikings" from the north.";
```

La solución para evitar este problema es usar el carácter de **escape de barra invertida**.

El carácter de escape de barra invertida (\\) convierte los caracteres especiales en caracteres de cadena:

| Escape character | Result | Description  |
| ---------------- | ------ | ------------ |
| ``\'``           | '      | Single quote |
| ``\"``           | "      | Double quote |
| `\\`             | `\`    | Backslash    |

La secuencia inserta una comilla doble en una cadena:`\"`

```csharp
string txt = "We are the so-called \"Vikings\" from the north.";
```

La secuencia inserta una comilla simple en una cadena:`\'`

```csharp
string txt = "It\'s alright.";
```

La secuencia inserta una sola barra invertida en una cadena:`\\`

```csharp
string txt = "The character \\ is called backslash.";
```

Otros caracteres de escape útiles en C# son:

| Code | Result    |
| ---- | --------- |
| \n   | New Line  |
| \t   | Tab       |
| \b   | Backspace |