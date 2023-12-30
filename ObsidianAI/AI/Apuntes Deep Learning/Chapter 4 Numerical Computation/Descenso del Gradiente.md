#Optimización #Algoritmo
# Introducción

Cuando no podemos conocer le mínimo de una función de manera analítica a partir de la información de la **derivada** conocemos la dirección en la que una **función disminuye** su valor, nos movemos **en esa dirección de forma iterativa** para encontrar un mínimo lo suficientemente pequeño, a este proceso se le llama **descenso del gradiente**.

De esta forma conocemos que:
$$f(x)>f(x-\epsilon(sign\,f'(x)))$$
Siendo $\epsilon>0$ y $signf'(x)$ la [[Función signo]] de la derivada de $f(x)$.
Es decir que el valor de $f(x)$  es mayor que un valor cercano moviéndonos en la dirección en la que la pendiente es negativa.

Si $f'(x)=0$ nos encontramos ante un [[Punto Crítico]], que en el caso de ser un mínimo lo suficientemente pequeño como para dar resultado a una buena optimización nuestra tarea ha terminado.

# El gradiente

El caso de f(x) es una función del tipo $f\,:\mathbb{R}\,\rightarrow\,\mathbb{R}$.

Si ahora pasamos a funciones del tipo $f\,:\mathbb{R}^{n}\,\rightarrow\,\mathbb{R}$. Deberemos trabajar con el concepto de derivada parcial  $\frac{\partial}{\partial x_{i}}f(x_{1},x_{2},\dots,x_{i})$, que es la variación de $f$ con respecto a $x_{i}$ y generalizamos el concepto de derivada en el de **gradiente**, que es un vector que contiene todas las derivadas parciales de una función $f$.

Se expresa como $\nabla f(x)=(\frac{\partial f(x)}{\partial x_{1}},\frac{\partial f(x)}{\partial x_{2}},\dots)$   

En la [[deep-learning-adaptive-computation-and-machine-learning-series BY Ian Goodfellow.pdf#page=100|pagina 100]] se desarrolla el hecho de que el gradiente apunta justo en la dirección de máximo crecimiento y por tanto para encontrar un mínimo local iremos justo en la dirección contraria al gradiente.
A esto se le llama descenso del gradiente (*gradient descent o steepest descent*).
$$x'=x-\epsilon\nabla_{x}f(x)$$
Donde $\epsilon$ es el ratio de aprendizaje.

Si se escogen varios valores de $\epsilon$ y se evalúan en  $f(x-\epsilon\nabla_{x}f(x))$ para escoger el que minimice la función, es la estrategia conocida como *line search*.

# Mejora con el Jacobiano y el Hessiano

Ahora trabajaremos con funciones del tipo $f\,:\mathbb{R}^{n}\,\rightarrow\,\mathbb{R}^{m}$, en este caso el símil del gradiente es el [[Jacobiano]].

La *"segunda derivada"* se llama [[Hessiano]] y nos aporta información útil en cuanto a si una zona de descenso va a descender aún más rápido o va a descender menos rápido que antes. Esto es muy útil para cambiar el ratio de aprendizaje $\epsilon$ en función de si la curvatura es beneficiosa para encontrar el mínimo que buscamos.

Conociendo la serie de Taylor:
$$f(x)\simeq f(x_{0})+(x-x_{0})^\top g+\frac{1}{2}(x-x_{0})^\top H(x-x_{0})$$
Y haciendo que nuestro nuevo punto $x$ sea $x_{0}-\epsilon g$, es decir, un desplazamiento en la dirección contraria al gradiente por $\epsilon$, nos da una aproximación tal que:     
$$f(x_{0}-\epsilon g)\simeq f(x_{0})-\epsilon g^\top g+\frac{1}{2}\epsilon ^2g^\top Hg$$
 El primer término es el valor actual de la función, el segundo es la disminución esperada por el gradiente y por último una corrección por la curvatura de la función (en esa dirección?? creo que sí)

[Profundizando](https://www.cs.cornell.edu/courses/cs4780/2015fa/web/lecturenotes/lecturenote07.html)

En el caso de que $g^\top Hg$ sea negativo o cero, la ecuación obtenida nos dice que se puede hacer $\epsilon$ todo lo grande que se quiera que la función siempre disminuirá, aunque esto es probablemente erróneo ya que la serie de Taylor sólo es una aproximación en el punto $f(x_{0})$.

En el caso de que $g^\top Hg$ sea positivo el valor óptimo de $\epsilon$ es:
$$\epsilon=\frac{g^\top g}{g^\top Hg}$$
En el peor caso posible, en el que el gradiente coincide con el mayor autovalor de $H$, es decir la pendiente va a crecer en la dirección contraria al gradiente, el valor optimo para $\epsilon$ es $\frac{1}{\lambda_{max}}$ 

Problemas del descenso del gradiente:

Mejora: utilizar el [[Método De Newton]] cerca del mínimo












