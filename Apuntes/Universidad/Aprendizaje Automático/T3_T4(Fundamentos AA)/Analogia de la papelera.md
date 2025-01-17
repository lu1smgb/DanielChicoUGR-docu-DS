Disponemos de una bolsa infinita de bolas verdes y roja, con una probabilidad de que salgan rojas de $\mu$, y de que salgan verdes $1- \mu$ 
![[Pasted image 20230419163258.png]]

Tenemos $\nu$ que es la fracción de bolas rojas de la muestra.
# Qué porcentaje de canicas verdes hay en la bolsa?

En este punto podemos tenemos dos posibles caminos para responder a la pregunta:

## No se puede extraer información sobre la caja solo con una muestra finita sobre una población infinita

Si es así, se acabaron los problemas, esto es un muro contra el que no se puede luchar.

## Si se puede extraer información de $\nu$? 

Si tomamos esta  última afirmación como válida que se extrae?
1. Se puede garantizar que $\%\text{verdes}_{muestra}\approx\%\text{verdes}_{bolsa}$
2. Identidad de Hoeffding: $P(|\%\text{rojas}_{muestra} - \%\text{rojas}_{bolsa}| < \epsilon) \leq 2*e^{-2*\epsilon^2*N}$  -> La probabilidad de que el % de bolas rojas en la muestra y en la bolsa difiera menos de $\epsilon$, es menor que la parte derecha de la inecuación.
3. Esta expresión devuelve una cota superior a dicha probabilidad.
 