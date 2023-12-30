El output está dentro de un set de valores
$y\in\{1,\dots,C\}$ donde $C$ es el número de posibles outputs, si es $C=2$ se llama [[Clasificación Binaria]] y si $C>2$ se llama [[Clasificación Multiclase]]. Además si no son excluyentes, se llaman *Multi-Labeled Classification*, aunque si se puede reducir a predecir varias [[Clasificación Binaria]] se llama *Multiple output model*.

El resultado se representa como una probabilidad para cada valor del set de salida: $p(y|x,D)$, siendo la suma de $\sum_{i=1}^Cp(y_{i}|x,D)=1$.

Si estamos trabajando con varios modelos $M$ se denota la probabilidad como $p(y|x,D,M)$.







