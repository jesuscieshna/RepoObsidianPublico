#Matriz

# Definición
Es la representación en forma matricial de todas las derivadas parciales para cada dimensión de salida

$$
\mathbb{J}=\left[\begin{array}{ccc}
\dfrac{\partial \mathbf{f}(\mathbf{x})}{\partial x_{1}} & \cdots & \dfrac{\partial \mathbf{f}(\mathbf{x})}{\partial x_{n}}
\end{array}\right]=\left[\begin{array}{c}
\nabla^{T} f_{1}(\mathbf{x}) \\
\vdots \\
\nabla^{T} f_{m}(\mathbf{x})
\end{array}\right]=\left[\begin{array}{ccc}
\dfrac{\partial f_{1}(\mathbf{x})}{\partial x_{1}} & \cdots & \dfrac{\partial f_{1}(\mathbf{x})}{\partial x_{n}} \\
\vdots & \ddots & \vdots \\
\dfrac{\partial f_{m}(\mathbf{x})}{\partial x_{1}} & \cdots & \dfrac{\partial f_{m}(\mathbf{x})}{\partial x_{n}}
\end{array}\right]
$$

Como se ve en la última representación, cada fila contiene el cambio con respecto a un parámetro de $f$ mientras que la columna contiene los cambios con respecto a los parámetros de entrada ($x_{1},x_{2}\dots$)

El jacobiano es la mejor aproximación linear([[Aplicación Lineal]]) en un punto concreto de esta, tal y como es la pendiente en una dimensión.

[Video 3blue1brown](https://www.youtube.com/watch?v=bohL918kXQk) 

Es más, en una región muy pequeña, el determinante del jacobiano es una aproximación del estiramiento de un cierto área.

[Determinante 3Blue1Brown](https://www.youtube.com/watch?v=p46QWyHQE6M)