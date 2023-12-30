$D=\{(x_{i},y_{i})\}^n_{i=1}$ 
$D$ es el set de entrenamiento, que está conformado por:
- $x_{i}$ los inputs
- $y_{i}$ los outputs

$x_{i}$ es un array de *D* dimensiones, a cada dimensión se le llama *features, attributes o covariates* (atributos).
Por ejemplo la altura y el peso de una persona expresado en un array de 2 dimensiones.

$y_{i}$ normalmente será un set de posibles resultados: Ej.: (Hombre, Mujer) o un escalar real.
Si es categórico hablamos de un problema de **[[Clasificación]]**, en cambio si es un escalar real hablamos de un problema de **[[Regresión]]**.