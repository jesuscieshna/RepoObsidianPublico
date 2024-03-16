
Cuando tenemos una función en Dart, podemos forzar a que desde fuera se ponga el nombre de dicho parámetro para aumentar la legibilidad de la función y saber a ciencia cierta que parámetro y significado tendrá para la función.

```
void main(){

  double result = division(dividendo: 4, divisor: 3);

  print(result);

}

  

double division({required int dividendo,required int divisor}){

  return dividendo/divisor;

}
```

En este caso también he añadido la opción required en los parámetros para así asegurarme de que el valor es obligatorio, si no viene el parámetro el valor por defecto es null.