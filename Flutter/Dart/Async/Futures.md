Tipo de dato promesa, contiene un tipo de dato parametrizado.
Como se ejecuta un future? Se realiza algún tipo de petición asíncrona, esto lo procesa el [[Event loop]] y estará atento al evento para realizar algún tipo de proceso que le indiquemos con .then, si no simplemente almacena el dato

### métodos interesantes

#### Future.value(value);
```
int cachedInt = 34
Future<int> myFuture = Future.value(cachedInt);
```

Si ya conocemos el resultado y no necesitamos volver a ejecutar código asíncrono pero el tipo de dato es un Future podremos utilizar Future.value(value);
#### Future.error(error);
```
Excption exception = Exception();
Future<int> myFuture = Future.error(exception);
```

Del mismo modo si conocemos que hay algún tipo de error podemos hacer Future.error(Exception());

#### Future.delayed()
```
Future<int> myFuture = Future.delayed(
	Duration(seconds: 3),
	() => 89,
)
```

Para mockear servicios para tests este método es muy útil, puedes simular un comportamiento asíncrono como pasaría con el servicio real

#### .then() &/o .catchError()

Nos permite ejecutar código cuando se completa el Future, con **.then** ejecutamos su bloque de código cuando el future se completa correctamente y con **.error** ejecutamos su bloque de código cuando el future se completa con un error

#### .whenComplete()

Aparte de los métodos anteriores podemos añadir un bloque de código que se ejecute independientemente de si el future se ha completado correctamente o con una excepción
