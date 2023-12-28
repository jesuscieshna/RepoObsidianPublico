#Optimización 
# Introducción

Cuando no podemos conocer le mínimo de una función de manera analítica a partir de la información de la derivada conocemos la dirección en la que una función disminuye su valor, nos movemos en esa dirección de forma iterativa para encontrar un mínimo lo suficientemente pequeño, a este proceso se le llama descenso del gradiente.

De esta forma conocemos que:
$$f(x)>f(x-\epsilon(sign\,f'(x)))$$
Siendo $\epsilon>0$ y $signf'(x)$ la [[Función signo]] de la derivada de $f(x)$.
Es decir que el valor de $f(x)$  es mayor que un valor cercano moviéndonos en la dirección en la que la pendiente es negativa.

Si $f'(x)=0$ nos encontramos ante un [[Punto Crítico]], que en el caso de ser un mínimo lo suficientemente pequeño como para dar resultado a una buena optimización nuestra tarea ha terminado

# El gradiente

El caso de f(x) es una función del tipo $f\,:\mathbb{R}\,\rightarrow\,\mathbb{R}$.

Si ahora pasamos a funciones del tipo $f\,:\mathbb{R}^{n}\,\rightarrow\,\mathbb{R}$. Deberemos trabajar con el concepto de derivada parcial  $\frac{\partial}{\partial x_{i}}f(x_{1},x_{2},\dots,x_{i})$, que es la variación de $f$ con respecto a $x_{i}$ y generalizamos el concepto de derivada en el de **gradiente**, que es un vector que contiene todas las derivadas parciales de una función $f$.

Se expresa como $\nabla f(x)=(\frac{\partial f(x)}{\partial x_{1}},\frac{\partial f(x)}{\partial x_{2}},\dots)$   

En la [[deep-learning-adaptive-computation-and-machine-learning-series BY Ian Goodfellow.pdf#page=100|pagina 100]] se desarrolla el hecho de que el gradiente apunta justo en la dirección de máximo crecimiento y por tanto para encontrar un mínimo local iremos justo en la dirección contraria al gradiente.
A esto se le llama descenso del gradiente (*gradient descent o steepest descent*).
$$x'=x-\epsilon\nabla_{x}f(x)$$
Donde $\epsilon$ es el ratio de aprendizaje.

Si se selecciona $\epsilon$ escogiendo varios valores y evaluándolos en  $f(x-\epsilon\nabla_{x}f(x))$ para escoger el menor valor resultante, es la estrategia conocida como *line search*.





