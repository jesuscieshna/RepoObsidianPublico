Principalmente cuidado con el jre que se está utilizando, las distintas versiones de gradele tienen una versión de java mínima con la que pueden trabajar
[Compatibility Matrix](https://docs.gradle.org/current/userguide/compatibility.html)

- [Solución 1](https://stackoverflow.com/questions/66920708/update-gradle-in-flutter-project)
Eliminar la carpeta android por completo y volver a crearla
También eliminar la carpeta build



- [Solución 2](https://docs.flutter.dev/release/breaking-changes/android-java-gradle-migration-guide)
Utilizando una versión de java 13/14 en la carpeta android de nuestro proyecto flutter, android studio nos ayudará con el upgrade a la versión de gradle deseada

Último paso, añadir el package al android manifest => [flutter - "Error running com.example.flutter_launcher - Stack Overflow](https://stackoverflow.com/questions/70817442/error-running-com-example-flutter-launcher)
