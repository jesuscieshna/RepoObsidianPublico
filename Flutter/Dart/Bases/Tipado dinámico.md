se pueden declarar variables en Dart cuyo tipo es dinámico, esto sucede cuando en la declaración de la variable no le asignamos un tipo ni tampoco una instancia. Esta variable podrá contener cualquier tipo en diferentes puntos del programa, algo que es mejor evitar especificando el tipo de la variable.

```
main(){

  var pruebaDinamica;

  pruebaDinamica="Soy string";

  pruebaDinamica=0;

}
```

Esto no daría error en Dart