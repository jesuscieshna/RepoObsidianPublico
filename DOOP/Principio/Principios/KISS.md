

# [[Principio]] KISS
*"Keep it simple, stupid"*

## Definición

[[LuisFernández_5_Diseño.pdf#page=27 | Definición de Luis Fernámdez (28 y 29)]]

En el desarrollo anteponemos la legibilidad del código a su complejidad, por mucho que se crea que esa solución es muy eficiente u otras ventajas. 

El objetivo es acelerar la etapa de desarrollo, ya que tanto la implementación como posterior lectura (para entenderlo o realizar algún cambio) serán más rápidos. Así no tendremos bloques de código intocables que nadie entiende excepto la persona que lo hizo.

## ¿Cómo mantenerlo simple?

##### Mi interpretación
No me veo con el nivel de dar una respuesta amplia y real a esta pregunta.

A las conclusiones que he llegado hasta el momento es que mantenerlo simple en parte es (a partir de un buen análisis y diseño) la abstracción del problema en bloques de alto nivel. Es decir, sirvete de las clases que tienes o incluso ,si es necesario, crea otras para abstraer el problema en pequeñas partes que en definitiva nos aportará una mayor legibilidad.

También he nombrado un buen análisis y diseño ya que es posible que la implementación la funcionalidad sea más sencilla desde otra clase por su propia naturaleza, y por tanto tenga más sentido que sea su responsabilidad.
##### Violaciones de KISS
[[LuisFernández_5_Diseño.pdf#page=29 |Sacado de los apuntes de Luis Fernández]]

