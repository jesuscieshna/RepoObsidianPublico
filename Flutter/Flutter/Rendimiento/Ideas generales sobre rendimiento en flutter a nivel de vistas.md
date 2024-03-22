### Recursos

[Flutter internals](https://www.flutteris.com/blog/en/flutter-internals)

[Documentacion oficial sobre performance](https://api.flutter.dev/flutter/widgets/StatefulWidget-class.html#performance-considerations)
Aquí el enlace de arriba embebido

<iframe width=700 height=500 src="https://api.flutter.dev/flutter/widgets/StatefulWidget-class.html#performance-considerations"></iframe>

Sobre las recomendaciones de flutter en Performance.
- Lleva el manejo de estado a las hojas, así sólo rebuildearás esos widgets concretos
- Minimizar el número de nodos creados por todos los build de los widgets? (no entendí bien esto) TODO!
- Declarar widgets como variables finales si vas a utilizar el mismo Widget con los mismos datos varias veces
- Utilizar const para indicar que el Widget no se vuelva a crear si se vuelve a ejecutar el método build
- También cuidado con el nivel de profundidad de subWidgets, imagina que en un estado devolvemos 3 capas de Widgets, pero en otro utilizamos estas 3 más otra que los envuelve, entonces estas 3 capas iguales volverán a ser renderizadas, si puedes, envuelve estas 3 en ambos estados para evitar rebuildear
- si la profundidad tiene que cambiar, evalúa envolver los Widgets comunes en Widgets con [GlobalKey](https://api.flutter.dev/flutter/widgets/GlobalKey-class.html), que no es más que una key global para encontrar ese Widget, nos permite reutilizar el mismo widget y otros beneficios como preservar el estado (?) [Stack overflow sobre global key](https://stackoverflow.com/questions/56895273/how-to-use-globalkey-to-maintain-widgets-states-when-changing-parents)
- Cuando queramos reutilizar un bloque de código es preferible crear un Widget nuevo en vez de crear un método de ayuda (helper method). Este Widget tendrá su método build y por tanto si rebuildeamos si tenemos estado sólo cambiaremos este Widget, contrariamente a si lo hubieramos hecho en un método que nos devuelve el Widget. Otro de los beneficios es que reduce la probabilidad de pasar un contexto obsoleto (entender bien esto último) TODO!





