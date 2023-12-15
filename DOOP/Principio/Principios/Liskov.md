

# [[Principio]] de sutitución de Liskov
[Bárbara Liskov](https://es.wikipedia.org/wiki/Barbara_Liskov)

## Definición

Cuando tenemos una [[Herencia]], la clase padre podría ser sustituible por la clase hija sin que el código se rompa. Es decir, el hijo debe contener todos los métodos del padre, cuando esto no sucede, se le denomina [[herencia rechazada]]. El objetivo es tener bloques de código más intuitivos, intercmabiables y mantenibles.
Esta es una idea general, ahora veremos flexibilidades y requisitos para cumplirlo:
##### Covarianza
Los métodos pueden tener covarianza: si un método del padre devuelve un objeto de la clase A, el método hijo puede devolver un método A', hijo de A.
```
public class AnimalShelter{
	public Animal adopt(){
		return new Animal();
	}
}

public class DogShelter{
	@Override
	public Dog adopt(){
		return new Dog(); //Dog hereda de Animal
	}
}
```

##### Contravarianza
Los métodos pueden tener contravarianza: si un método padre recibe por parámetro un objeto de la clase A', el método hijo puede recibir A, padre de A'.
(No está permitido en java)
##### Precondiciones
Las precondiciones del método hijo no podrán ser más restrictivas que las del método padre, ya que si no, al sustituir y llamar al método con datos esperables para el padre, el hijo romperá el programa.

Método padre
```
public void metodoPadre(int numero){
	assert(numero>0);
	.......
}
```
Método hijo que respeta LSP
```
@Override
public void metodoPadre(int numero){
	assert(numero>0 || numero == -2);//respeta las condiciones del padre y añade otras (OR)
	........
}
```
Método hijo que **NO** respeta LSP
```
@Override
public void metodoPadre(int numero){
	assert(numero>0 && numero <= 100);//no respeta las condiciones del padre (and)
	........
}
```
##### Postcondiciones
Debemos respetar las postcondiciones del método padre, no podemos hacerlas más laxas, pero si más retrictivas.

Método padre
```
public void metodoPadre(int numero){
	.... //se ejecuta código
	....
	assert(resultado>100);
}
```
Método hijo que respeta LSP
```
@Override
public void metodoPadre(int numero){
	.... //se ejecuta código
	....
	assert(resultado>200);
}
```
Método hijo que no respeta LSP
```
@Override
public void metodoPadre(int numero){
	.... //se ejecuta código
	....
	assert(resultado>100 || resultado<0); // restricciones más laxas
}
```

##### Invariantes
Son condiciones que una clase siempre tiene que cumplir al interactuar con otra. La clase hija debe respetar estas condiciones y como mucho restringirlas.

##### History constraint
---TODO---
[enlace a una pagina con info sobre precondition postcondition etc](https://objectcomputing.com/resources/publications/sett/september-2011-design-by-contract-in-java-with-google)
[Cosas sobre variancia, contravarianza](https://typealias.com/concepts/contravariance/)
[Más cosas sobre varianza contravarianza](https://en.wikipedia.org/wiki/Covariance_and_contravariance_(computer_science)#Inheritance_in_object-oriented_languages)

---TODO---
Evitar por completo los instance of [[LuisFernández_5_Diseño.pdf#pag=71 | en apuntes]].
## Herencia rechazada
[[Herencia Rechazada]]
[[Delegación de comportamiento]]






