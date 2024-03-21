
# Intro

flutter pub get (descargar dependencias que ya están en el pubspec.yml)

VS code extensions:
dart
flutter
awesome flutter snippets

# Packages:

## **dart pub add dev:build_runner** 

(flutter pub run build_runner build para buildear la clase de parseo de objtos a json y viceversa, configurar con el build.yml para ir directamente a las clases necesarias, meterl el codigo generado al gitignore para evitar conflictos)

## **dart pub add dev:json_serializable**


## **dart pub add json_annotation**
(a la hora de usar build runner nos sirvé para anotar como queremos que se genere el mapeo de dato para encajar nuestra api con el modelo del frontend)

## **dart pub add freezed**
(autogeneracion de codigo, se puede utilizar conjuntamente con el json annotation)
potente para crear **[[sealed unions]]**, enums de dart son débiles y esto viene a suplir esto, nos permite generar de forma rápida estructuras de decisión con los estados que le hayamos dado gracias a los métodos when(), maybeWhen() etc que nos genera freezed
[Flutter State Management: Going from setState to Freezed & StateNotifier with Provider (en concreto los sealed unions)](https://codewithandrea.com/videos/flutter-state-management-setstate-freezed-state-notifier-provider/#solution-immutable-state-and-sealed-unions) (Rompemos O/C?, es un códio mantenible??)

TODO! qué facilita freeze conjutamente con json annotation????

## **flutter pub add freezed_annotation**


## **dart pub add fluter_gen_runner --dev** 
(nos ayuda con el path de assets y otros recursos, el path pasa de ser un string hardcodeado a una especie de objeto, si no existe nos avisa)

## **flutter pub add provider**
(inyecion de dependencas) En los vídeos utiliza provider para inyectar una única instancia creada de los repositorios a las pantallas que lo necesiten

## **flutter pub add http** (Para el manejo de fetch y responses)

Para conexion a internet:
android permission.INTERNET
La configuración en ios se necesita mac

## **flutter pub add dio**

es un poco más completa que Http, también necesitamos los permisos para internet en android

## **flutter pub add flutter_hooks** 

**Disclaimer** es un paquete interesante, reduce tu código, para un principiante tal vez no sea lo mejor ya que te abstrae de clases y métodos interesantes de flutter vanilla

(facilita la creacion de stateFullWidgets, sin useState().... guardan variables internamente y tienen listeners para ver cuando cambia).

final contador = **useState()** almacena un valor y está atento a cambios para rebuildear la vista entera, por ejemplo un contador.value = contador.value++;

final contador = **UseValueNotifier()** almacena un valor, está atento a cambios para rebuildear únicamente aquellas parte del código que utilicen ValueListenableBuilder con el contador como parámetro

**useIsMounted()**, cuando tenemos un widget asincrono es bueno comprobar que la pantalla sigue activa (tiene estado activo), utilizamos el booleano mounted que es una propiedad de la clase, Si utilizamos hooks tenemos la posibildad de crear un final mounted = useIsMounted(); para seguir haciendo estas comprobaciones 
- [Video 44 sobre el useIsMounted()](https://www.udemy.com/course/flutter-avanzado/learn/lecture/35971308#overview)
- [mounted property  flutter docs](https://api.flutter.dev/flutter/widgets/State/mounted.html)

**useEffect()** [Video 45](https://www.udemy.com/course/flutter-avanzado/learn/lecture/35971318#overview)

**useRef()** Al contrario que el useState() que rebuildea la vista cuando cambia de estado, una propiedad, por ejemplo boolean inicializdo = useRef(false); es un valor que podrá cambiar pero cuando esto pase no reiniciará la vista 
- [Video 47](https://www.udemy.com/course/flutter-avanzado/learn/lecture/35971340#overview) 
- [Video 49, formulario interesante utilizando el useRef()](https://www.udemy.com/course/flutter-avanzado/learn/lecture/36588946#overview)

**useValueChanged()** 
- [Video 47 (a partir del 5:24)](https://www.udemy.com/course/flutter-avanzado/learn/lecture/35971340#overview) 

**useAutomaticKeepAlive()** Para preservar el estado de por ejemplo una lista cuando cambiamos de pantalla
- [video 48](https://github.com/darwin-morocho/flutter-avanzado/blob/final/hooks/lib/views/tabs.dart)
- [linea 40](https://github.com/darwin-morocho/flutter-avanzado/blob/final/hooks/lib/views/tabs.dart)

**useAnimationController()** 
- [viedo 50](https://www.udemy.com/course/flutter-avanzado/learn/lecture/36588950#overview)

**useMemoized()** 
**useFuture()** 
- [Video 51](https://www.udemy.com/course/flutter-avanzado/learn/lecture/36588954#overview)
- [video 52, interesante para trabajar con fetcheos futuros, generando por ejemplo un efecto de loading, solo recarga la vista si el useFuture() cambia su clave](https://www.udemy.com/course/flutter-avanzado/learn/lecture/36588960#overview)
En el 52 utiliza el useState() tal vez sea negativo a nivel de rendimiento el recargar la vista por completo

**Hooks y streams**
- [video 54](https://www.udemy.com/course/flutter-avanzado/learn/lecture/36588972#overview) trabaja con la conectividad a internet a través de hooks.

## **flutter pub add flutter_secure_storage**

para esta dependencia necesitamos una versión mínima de la api 18 en minSdkVersion

![[cambio de la api minima soportada por nuestra app en android.png|2000]]


## **flutter pub add flutter_svg**

para renderizar svgs

