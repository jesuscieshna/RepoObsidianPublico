### Recursos Externos
- [Bloc (bloclibrary.dev)](https://bloclibrary.dev/getting-started/)
- [Curso Fernando Herrera Youtube](https://www.youtube.com/playlist?list=PLCKuOXG0bPi3P1T460Dgh9G_1JVMIeUaX)
- [Patron bloc medium](https://medium.com/flutter-community/using-the-bloc-pattern-for-clean-flutter-apps-theory-and-a-practical-example-b5dcad728a2b)
- [Curso avanzado de Darwin, sección 5, el patrón bloc](https://www.udemy.com/course/flutter-avanzado/learn/lecture/36598490#overview)
- [Código final del curso avanzado de Darwin](https://github.com/darwin-morocho/flutter-avanzado/tree/final/bloc_pattern)

## Intro

Bloc (Business logic components) es un patrón recomendado por flutter para el manejo de estado de una aplicación, Destacar que bloc es un patrón de diseño específico para el stateManagement de flutter, además existe el paquete flutter_bloc que facilita la generación de código
## Dependencias

Dependencias que facilitan el uso de bloc
- [bloc](https://pub.dev/packages/bloc) Clases para facilitar la implementación de bloc
- [flutter_bloc](https://pub.dev/packages/flutter_bloc) Widgets que facilitan la integración de bloc, se puede usar conjuntamente con bloc

## Teoría

Se puede apreciar que la comunicación de **datos** entre la UI y el bloc es unidireccional, la UI se comunica con el bloc mediante **eventos** 

![[blocSimpleStructure.png]]
El objetivo de Bloc como de otros patrones de StateManagement es separar a la vista de la lógica de negocio 

Un bloc es una estructura algo compleja ya que une mucha abstracción mediante un sistema de herencias de clases abstractas para escribir menos código, el manejo de eventos y refrescos de una vista y algo de programación funcional.

## bloc package

Aporta la clase Bloc, donde ya tenemos esa estructura abstracta para implementar rápidamente nuestros blocs.

Esta clase Bloc necesita dos estructuras de datos parametrizadas, los eventos y los estados (de hecho lo que tendremos son varios estados y varios eventos con los que la clase podrá trabajar). Como en Dart no tenemos enums suficientemente potentes utilizamos freezed para generar [[sealed unions]] y aporta comportamiento a estos enums. Es una solución algo engorrosa, llena de magia y de la que desconozco sus limitaciones.

## flutter_bloc package

Nos aporta widgets para facilitar el uso de los blocs en nuestras vistas.

BlocProvider, que nos retorna un bloc del tipo que necesitemos

BlocBuilder, que nos permite escuchar los cambios en propidades de nuestro estado y renderizar widgets concretos de nuestra vista




