- [x] Encontrar cambio a dependencias: get_version y splash_screen
- [ ] Estudiar warnings de la apliacación
- [ ] Aplicar null safety
- [ ] Levantar servicio propio
- [ ] Ver aplicación .net como punto de referencia


### Historias de usuario

#### Inicio sesión
- Un usuario podrá iniciar sesión con un almacén seleccionado, esta sesión se guarda en el secureStorage.

#### Home page
- El usuario podrá cambiar el almacén seleccionado cambiando la sesión actual
- Se le mostrará al usuario un menú de botones con 5 opciones: Consultar bultos, Camiones, Consultar pedido,  Opciones palets, Realizar inventario

#### Consultar bultos
- Se le mostrará al usuario dos opciones: Bulto y devolución
- Estas vistas son prácticamente iguales
- [ ] TODO!  Entender diferencia 
##### Bulto
- El usuario podrá cambiar bultos de ubicación (zona: String y casillero: int)
- Primero deberá introducir el código de palet para seleccionarlo

#### Camiones
- Se le mostrará al usuario tres opciones: Asignar muelle, cargar camión y reimprimir albarán.
##### Asignar Muelle
- El usuario podrá rellenar campos para asignar al muelle, numéricos del 1 al x, un tipo de camión (trailer, chico...) con su matrícula
- El usuario podrá pulsar el botón asignar muelle para asignar con estos cambios
- Si el muelle no existe se le muestra al usuario
- Si la matrícula no está registrada se le muestra al usuario
- Si el camión ya está asignado a un muelle se le pregunta si quiere cambiarlo
##### Cargar camión
- El usuario podrá seleccionar el muelle que quiere cargar
- Si el muelle no existe se le muestra al usuario
- Si el muelle está vacío se le muestra al usuario
- Se le mostrará al usuario la matrícula, el código de camión, una serie de comentarios que se han ido dejando, un desplegable que muestra algo más de información de los palets, una opción de albaranar
- La tabla (ord (conteo), cliente(nombre cliente), referencia(referencia al tipo de caja), ubic(ubicacion del palet), palets(cuantos palets han sido cargados???), un???, com???, C???, Ñ???, TC???, cant???)

Cargar camión:

##### Reimprimir Albarán
- Existe un código de camión único para cada envío
- A partir del código de camión se muestra información de este envío: Matrícula T, Matrícula R y estado
- [ ] TODO! se reimprime el albarán? donde?

#### Consultar pedidos
- Se pueden consultar los pedidos por Pedido (ni idea), por pedido cliente (OM-23002711), por referencia, por cliente(nombre cliente) y por ubicación(zona y casilero)
- A parte del filtro se le da la opción de agrupar por palets o por pedidos
- La información mostrada al usuario es:
	- información general del pedido(cliente, referencia(tipo caja), numero palets)
	- tabla con gtin, nº pedido, palet, codigo pedido cliente, ubicación, fecha alta, estado




