$D=\{(x_{i}\}^n_{i=1}$ 
Aquí no tenemos el output real para comparar, estos algoritmos tratan de encontrar patrones en el set de datos (**Knowledge discovery**) 

No sabemos que exactamente que buscamos, procesamos los datos en busca de patrones. La formalización es una **[[estimación de densidad]]**.

En el [[Aprendizaje Supervisado]] buscamos $p(y_{i}|x_{i_{i}},\theta)$ (que es estimación de densidad condicional) mientras que en el no supervisado es $p(x_{i},\theta)$

# Clusters

Nos centramos en **modelaje basado en clusters**
Clusters: grupos de datos similares. 

# Factores latentes

Muchas dimensiones en los datos, proyectamos los datos hacia las variables latentes (aquellas que si determinan diferencia y cambio). *Principal component analysis o PCA*

# Graph Structure

Tenemos variables como nodos y líneas que los unen

# Matrix completion

Una  matriz de muchos valores, algunos de ellos están nulos. Estimar el valor de estos campos puede ser interesante.

Para quitar el ruido de una imágen mirando los pixeles alrededor para dar un color parecido al real, estimar una película que te podría gustar...