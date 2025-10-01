# 07. Constantes.

Si no deseemos que otros (o nosotros mismos) sobrescriban los valores existentes, puede agregar la palabra clave `const` delante del tipo variable.

Esto declarará la variable como "constante", lo que significa que no se puede cambiar y es de solo lectura:

```csharp
const int myNum = 15;
myNum = 20; // error
```

***Nota:*** La palabra clave `const` es útil cuando desea que una variable siempre almacene el mismo valor, Un ejemplo que a menudo se conoce como constante es ``PI`` ``(3.14159...)``.

**Nota:** No se puede declarar una ***constante*** sin asignar el valor. Si lo hace, se producirá un error: un campo ``const`` requiere que se proporcione un valor al instante.