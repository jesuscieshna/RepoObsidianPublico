
# Intro

flutter pub get (descargar dependencias)

VS code extensions:
dart
flutter
awesome flutter snippets

# Packages:

**dart pub add dev:build_runner** 
(flutter pub run build_runner build para buildear la clase de parseo de objtos a json y viceversa, configurar con el build.yml para ir directamente a las clases necesarias, meterl el codigo generado al gitignore para evitar conflictos)

**dart pub add dev:json_serializable**

**dart pub add json_annotation**
(a la hora de usar build runner nos sirvé para anotar como queremos que se genere el mapeo de dato para encajar nuestra api con el modelo del frontend)

**dart pub add freezed**
(nos sirve para autogenerar el codigo de los toString y los copyWith, se puede utilizar conjuntamente con el json annotation)

**dart pub add fluter_gen_runner --dev** 
(nos ayuda con el path de assets y otros recursos, el path pasa de ser un string hardcodeado a una especie de objeto, si no existe nos avisa)

**flutter pub add provider**
(inyecion de dependencas)

**flutter pub add http** (Para el manejo de fetch y responses)

Para conexion a internet:
android permission.INTERNET
La configuración en ios se necesita mac
