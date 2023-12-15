

# [[Principio]] de indirección


## Definición

La indirección es un proceso de abstracción de la dependencia de una clase, mediante una clase intermedia que la contiene (interfaz, clase abstracta ...). El objetivo es conseguir la independencia de una clase con otra 
clase concreta, permitiendo conectarle otra clase con un comportamiento similar.

Ejemplo:
```
Public class email(){
	private String;

	
}

Public class notificator(){
	private email;

	public String notificate(){
		
	}
}
```

Con la indirección
```
Public class email(){
	private String;

	
}

public class MessageSystem{
	private email;
	
	public notificate(){
		email.notificate();
	}
}

Public class notificator(){
	private messagSystem;

	public String notificate(){
		messageSystem.notificate();
	}
}
```



