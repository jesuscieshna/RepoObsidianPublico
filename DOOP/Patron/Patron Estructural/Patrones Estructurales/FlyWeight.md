
## [[Patron Estructural]] FlyWeight

## Definición

El objetivo de FlyWeight es reducir el tamaño en memoria de los objetos. ¿Cómo lo hace? Subdivide al objeto en la parte con tendencia a repetirse y en la parte única, utiliza una factory con una lista de partes comunes para cuando lo necesite añadirsela a la parte única. 

Así consigue almacenar información común para los objetos que la necesiten en vez de tenerla repetida en todos los objetos concretos que la compartan.

Un ejemplo con árboles. Siendo TreeType lo común y Tree la parte concreta teniendo sus características únicas más su TreeType.

![[FlyWeightConcreteDiagram.png]]