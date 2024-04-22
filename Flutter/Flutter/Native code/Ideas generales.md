[Writing custom platform-specific code | Flutter](https://docs.flutter.dev/platform-integration/platform-channels)

![[NativeCodeEscheme.png]]

En resumen, desde flutter podemos establecer un canal de comunicación mediante el MethodChannel, este nos permite mandar y recibir información del código nativo que escribamos.

La forma de tratar estos procesos entre android y IOS es algo distinta como podemos ver en el diagrama de arriba. 
### ¿Para qué?

Cada sistema operativo tiene sus peculiaridades, sobre todo cuando hablamos de procesos internos y permisos. Esto nos obliga a escribir código nativo en las plataformas necesarias para tener el comportamiento deseado en cada una de ellas, ya que no nos es posible desde flutter.

Un ejemplo claro podría ser los permisos de geolocalización, android y IOS tienen sus procedimientos y clases para manejar solicitudes y dotación de permisos, además de el código interno independiente para trabajar con la localización del dispositivo.

TODO! profundizar en como establecer comunicación, enviar datos desde flutter y procesar permisos

### Platform channel


### EventChannels 

[Video 174](https://www.udemy.com/course/flutter-avanzado/learn/lecture/21813018#overview)
Para recibir datos del código nativo siguiendo el patrón observer, el código nativo nos notifica y recibimos un Stream
### Android

Guía oficial en torno a los permisos en android
[Permisos en Android  |  Android Developers](https://developer.android.com/guide/topics/permissions/overview?hl=es-419)
[Buenas prácticas al pedir permisos](https://developer.android.com/guide/topics/permissions/overview?hl=es-419#best-practices)

Aquí se puede ver una clase de android para manejar los permisos, escucha y envío de la geolocalización
[Repo de Darwin Morocho](https://github.com/meedu-app/flutter-platform-channels-example)
[Clase de conexión Dart](https://github.com/meedu-app/flutter-platform-channels-example/blob/master/lib/native/geolaction.dart)
[Clase de conexión Android](https://github.com/meedu-app/flutter-platform-channels-example/blob/master/android/app/src/main/java/app/meedu/platform_channels_demo/Geolocation.java)

TODO! aplicar geolocalización a algún proyecto


### IOS



