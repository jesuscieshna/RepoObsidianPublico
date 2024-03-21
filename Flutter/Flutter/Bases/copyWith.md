Muy utilizado en clases de modelo. Nos sirve para crear copias de un objeto con los cambios que necesitemos.

```
class Person {
  final String name;
  final int age;
  
  Person(this.name, this.age);

  Person copyWith({String? name, int? age}) {
    return Person(
      name ?? this.name,//si name no es nulo metemos ese nuevo valor al constructor
      age ?? this.age,  //Si es nulo cogemos el valor antiguo
    );
  }
}
```

Como se puede apreciar el método copyWith espera dos parámetros opcionales, el nombre y la edad, si no se introduce un valor coge el valor que tenga la instancia a la que estamos llamando. En cambio si introducimos una nueva propiedad la cambiamos co respecto a la instancia anterior.
