## Ej 18

![[Screenshot_2024-04-29-12-24-33-101_com.orion.notein.global.png]]

### Solución:
Para demostrar la equivalencia de los Dos criterios, construiremos Dos máquinas de Turing, M' y M'', que aceptan el lenguaje L con cada uno de los criterios respectivamente. El ejercicio concluye demostrando que M acepta L si y solo si M' acepta a L y viceversa.

#### Ejemplo concreto:

>[!important] Enunciado Concreto
>Diseñar una máquina de Turing que acepte la siguiente expresión: $\{a^na^b,n>1\}$

##### Máquina 1 -> M'

>[!seealso] Condición de parada
>M acepta la palabra w si, al tener w como entrada, en un paso de cómputo se llega un estado de parada

###### Definición:
$M=(Q,A,B,\delta,q_0,\# F)$
Donde:
- $Q=\{q_0,q_1,q_2,q_{final}\}$
- $A=\{a,b\}$
- $B=\{a,b,X,Y,\#\}$
- $\delta=\{$
	- $(q_0,a)=(q_1,X,D)$
	- $(q_0,Y)=(q_0,Y,D)$
	- $(q_0,\#)=(q_{final},\#,D)$
	- $(q_1,a)=(q_1,a,D)$
	- $(q_1,Y)=(q_f,Y,D)$
	- $(q_1,b)=(q_2,Y,I)$
	- $(q_2,Y)=(q_2,Y,I)$
	- $(q_2,a)=(q_2,a,I)$
	- $(q_2,X)=(q_0,X,D)$
- $q_0$
- $\#$
- $F=\{q_f\}$

###### Explicación:
El estado 0 cambia la a por X y se mueve al estado 1, este busca la primera b la cuál cambia por una Y y se desplaza a la Izquierda buscando una X, cuando la encuentra desplaza el cabezal una posición a la derecha y repite desde q0, si q0 no encuentra *a*s sino que encuentra una Y, busca el símbolo vacío a la derecha de la palabra, si no encuentra ninguna b antes de llegar al símbolo blanco, se pasa al estado de aceptación.


##### Máquina 2 ->M''

>[!seealso] Condición de parada
M acepta la palabra w si, al tener w como entrada, la máquina se para en algún momento (no por llegar a un estado de parada)

###### Definición
$M=(Q,A,B,\delta,q_0,\# F)$
Donde:
- $Q=\{q_0,q_1,q_f\}$
- $A=\{1\}$
- $B=\{1,\#\}$
- $\delta=\{$
	- $(q_0,a)=(q_1,X,D)$
	- $(q_0,Y)=(q_0,Y,D)$
	- $(q_0,b)=(q_{fallo},\#,D)$
	- $(q_1,a)=(q_1,a,D)$
	- $(q_1,Y)=(q_f,Y,D)$
	- $(q_1,b)=(q_2,Y,I)$
	- $(q_2,Y)=(q_2,Y,I)$
	- $(q_2,a)=(q_2,a,I)$
	- $(q_2,X)=(q_0,X,D)$
- $q_0$
- $\#$
- $F=\{q_0\}$

###### Explicación:
El funcionamiento intrínseco es igual al de la máquina M', la diferencia es, cuando se está en los estados q1 y q2, si estos encuentran una X o una b respectivamente, saltan al estado de error, lo mismo pasa con q0 cuando recorre por ultima vez la palabra que si encuentra un b salta al estado de error.


#### Resolución
Ámbas máquinas aceptan el mismo lenguaje, la primera cuando acepta la palabra, pasa a un estado de aceptación, y la segunda salta a un estado de fallo si detecta alguna malformación en la palabra
## Ej 20

![[Screenshot_2024-04-29-12-24-46-334_com.orion.notein.global.png]]