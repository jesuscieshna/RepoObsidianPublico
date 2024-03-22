### Recursos

[Flutter internals](https://www.flutteris.com/blog/en/flutter-internals)

[Documentacion oficial sobre performance](https://api.flutter.dev/flutter/widgets/StatefulWidget-class.html#performance-considerations)
Aquí el enlace de arriba embebido

<iframe width=700 height=500 src="https://api.flutter.dev/flutter/widgets/StatefulWidget-class.html#performance-considerations"></iframe>

Sobre las recomendaciones de flutter en Performance.
- Lleva el manejo de estado a las hojas, así sólo rebuildearás esos widgets concretos
- Minimizar el número de nodos creados por todos los build de los widgets? (no entendí bien esto)
- Declarar widgets como variables finales si vas a utilizar el mismo Widget con los mismos datos varias veces
- También habal a nivel de profundidad de subWidgets, imagina que en un estado devolvemos 3 capas de Widgets, pero en otro utilizamos estas 3 más otra que los envuelve, entonces estas 3 capas iguales volverán a ser renderizadas, si puedes, envuelve estas 3 en ambos estados para evitar rebuildear
- si la profundidad tiene que cambiar, evalúa envolver los Widgets comunes en Widgets con [GlobalKey](https://api.flutter.dev/flutter/widgets/GlobalKey-class.html), que no es más que una key global para encontrar ese Widget
## Intro

Este apartado viene encaminado a resumir la información encontrada entorno al rendiminto debido al renderiazado de las vistas. Nuestro objetivo será renderizar el menor número Widgets que podamos, sólo haciendolo con aquellos que tengan que cambiar

## Uso de Const

con const es la palabra reservada de Dart para que no cambie la instancia de un objeto. En un widget implica que este no se volverá a renderizar

## Uso de Builders





