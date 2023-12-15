
## [[Patron Creacional]] Factory

## Definición

Usaremos un factory cuando tenemos un set de objetos polimórficos que y se seleccionará uno concreto en ejecución. Con dos objetivos:
- Respetar O/C (sigues necesitando un switch???) ---TODO---
- Evitar que el cliente se encargue de instanciar objetos (para que????) ---TODO---


![[FactoryDiagram.png]]

Como podemos ver, tenemos dos clases principales, una interfaz producto un *creador abstracto* con un método que devuelve una implementación de producto.
- El producto es implementado por las clases concretas.
- Del creador heredan tantos creadores como productos concretos tengamos y se encargará, mediante el método createProduct() de devolver una nueva instancia para el cliente.



## Otros ejemplos

[[designPatternsElementOfReusableObject-OrientedSoftware.pdf#page=127|Design Patterns]]
[[RefactoringGurú.pdf#page=79|Refactoring gurú]]
