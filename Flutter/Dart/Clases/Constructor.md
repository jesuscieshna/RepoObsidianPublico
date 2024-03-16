# Constructor simplificado
Podemos reducir el código de un constructor usando la siguiente sintaxis:
```
class Alumno{

  String nombre;
  String apellido;

  Alumno({this.nombre="", this.apellido=""});

}

void main(){
  Alumno alumno = new Alumno(nombre: "Nacho",apellido: "Pérez");
}
```
Este constructor hace dos cosas, al estar entre llaves conseguimos los [[Parámetros nombrados]] y además al expresar los parámetros con *this* también tenemos que no tenemos porque escribir el típico código para realizar la asignación.

# Constructor con nombre

```
class Alumno{

  String nombre="";
  String apellido="";

  Alumno({this.nombre="", this.apellido=""});

  Alumno.copy(Alumno alumno){
    //cosas
  }
}

void main(){
  Alumno alumno = new Alumno(nombre: "Pepe", apellido: "Gómez");
  Alumno copia = new Alumno.copy(alumno);
}
```


