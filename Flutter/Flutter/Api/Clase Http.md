Ya sea usando el paquete Http o el paquete Dio:
Definimos una serie de clases que nos van a ayudar a manejar las request y responses a un servicio externo

[Código de Darwin en el curso avanzado, clase para el manejo de peticiones http](https://github.com/darwin-morocho/flutter-avanzado/blob/final/blockchain_bloc_authentication/lib/app/data/http/http.dart) Este utiliza Http, en la rama Dio lo podemos encontrar con la dependencia Dio

Además genera una clase de utilidad para manejar los errores de las posibles peticiones. Las clases que utilizan la clase Http utilizan el método **performHttpRequest** para que los errores sean más manejables

[Fichero dart de utilidad para manejo de errores](https://github.com/darwin-morocho/flutter-avanzado/blob/final/blockchain_bloc_authentication/lib/app/data/utils.dart)

Esta clase utliza [[sealed unions]] para los posibles errores

TODO! problemas para realizar dart run run_builder build, por lo que no se está generando el código necesario, en concreto la [[sealed unions]] de los errores. Podría ser por un tema de dependencias deprecadas, o por un problema de configuración.


 