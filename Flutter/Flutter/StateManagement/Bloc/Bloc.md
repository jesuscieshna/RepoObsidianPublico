- [Bloc (bloclibrary.dev)](https://bloclibrary.dev/getting-started/)
- [Curso Fernando Herrera Youtube](https://www.youtube.com/playlist?list=PLCKuOXG0bPi3P1T460Dgh9G_1JVMIeUaX)
- [Patron bloc medium](https://medium.com/flutter-community/using-the-bloc-pattern-for-clean-flutter-apps-theory-and-a-practical-example-b5dcad728a2b)
- [Curso avanzado de Darwin, sección 5, el patrón bloc](https://www.udemy.com/course/flutter-avanzado/learn/lecture/36598490#overview)
- [Código final del curso avanzado de Darwin](https://github.com/darwin-morocho/flutter-avanzado/tree/final/bloc_pattern)


Bloc proviene de las siglas Business logic components, es un patrón recomendado por flutter para el manejo de estado de una aplicación, Destacar que bloc es un patrón de diseño específico para el stateManagement de flutter, además existe el paquete flutter_bloc que facilita la generación de código

Se puede apreciar que la comunicación de **datos** entre la UI y el bloc es unidireccional, la UI se comunica con el bloc mediante **eventos** 

![[blocSimpleStructure.png]]
El objetivo de Bloc como de otros patrones de StateManagement es separar a la vista de la lógica de negocio 
