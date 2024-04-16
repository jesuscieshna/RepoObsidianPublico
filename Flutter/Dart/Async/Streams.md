Flujo de valores

![[Sync_Async_Data.png]]

El stream se encarga de desencadenar eventos cuando un nuevo dato llega. A quién? A listeners que hayamos registrado para tratarlos.

```
final myStream = NumberCreator().stream;

final subscription = myStream.listen(
  (data) => print('Data: $data'),
);
```

Por defecto los streams están seteados para ser de **suscripción única**. es decir, sólo pueden tener un listener.

Si quieres varios listener entonces puedes utilizar el método asBroadcastStream

```dart
final myStream = NumberCreator()
    .stream
    .asBroadcastStream;

final subscription = myStream.listen(
    (data) => print('Data: $data'),
);

final subscription2 = myStream.listen(
    (data) => print('Data again: $data'),
);
```

#### .listen(), .onError() & onDone()
en función de la respuesta del stream se llamarán a estos métodos de nuestro listener

#### cancelOnError
Si el stream nos envía algún tipo de error por defecto la suscripción se rompe. Si no se quiere que la suscripción se rompa se setea cancelOnError: false;

estos son métodos y propiedades que se setean cuando se crea la suscripción. 

#### .pause(), .resume() & .cancel()
También podemos pausar, reanudar y cancelar la suscripción accediendo a estos métodos de una suscripción

## Utilizando Streams para procesar datos

Al igual que en java, podemos transformar los datos que contiene el stream.
where(), map(), distinct() ....
También podemos suscribirnos a este stream con .listen() al final, sin streams intermedios

## StreamController

Nos sirve para crear desde cero streams, encargarnos de añadir los datos con el .sink.add(), pararlo, reanudarlo o cerrarlo

Todo esto nos sirve para un tipo de Widget muy útil [[Builders#^706f5e|StreamBuilders]] que rehace el elmento hijo siempre que lleguen nuevos datos
