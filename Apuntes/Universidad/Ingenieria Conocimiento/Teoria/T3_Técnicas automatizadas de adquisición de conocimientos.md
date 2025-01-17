 
# Tareas a automatizar  
?
- La conceptualización de dominio por medio de la obtención de conceptos y factores relevantes
- La obtención de reglas, por medio de la obtención de reglas candidatas a partir de ejemplos

# Rejilla de repertorio:

También conocida como emparrillado o "Repertory Grid" se aplica en una amplitud de campos:
1. Asesoramiento
2. Estudios demográficos
3. Dinámica de grupo
4. Adquisición de conocimiento

> [!important] Idea de la rejilla de repertorio:
> Cada persona tiene su propia visión del mundo, asocia y distingue elementos de acuerdo a sus propios criterios. Su propia forma de agrupar diferentes conceptos. Esto se le denomina como **Constructor/Construcción**  

## Utilidad de la rejilla de repertorio en la IC

El grid es un sistema de ==correspondencia entre elementos y construcciones==. Esta técnica es útil para los expertos o ingenieros del conocimiento por:
1. Hace que el experto piense sobre el problema y por tanto ayuda a clarificar [[P1 ⇒ Reglas y Sistemas basados en reglas#^8sfluw|Consecuentes]] en su mente. 
2. Los grids se pueden analizar para encontrar modelos, clases y conceptos o asociaciones a investigar con mayor profundidad.

## Proceso de obtención de la rejilla repertorio

Pasos de los que se compone
?
- Dialogo inicial
- Sesión de valoración
- Análisis de los resultados

### Constructores:

>[!Def] 
>**Constructor**::es una característica bipolar en la cual cada elemento tiene un cierto grado o escala.
>>[!example]
>> Pesado-Ligero. Valiente-Cobarde...

Estas características se pueden presentar en una escala lineal con valores ponderados relativos a la característica. No son características binarias de Si o No solamente, aunque pueden incluir valores binarios de ser necesario

#### Valoración de objetos según el constructor:
Como es el experto quien crea las construcciones, es trabajo suyo comprender qué hace que una construcción sea válida y cómo se usa. Los ratios pueden expresarse también con nombres en vez de números:

![[Pasted image 20240320192144.png|Ejemplo escala contructor]]


>[!important] 
>- La escala no debe variar en una misma construcción aunque podrá variar de una construcción a otra.
>- Un elemento se clasifica según cada construcción usando un ratio subjetivo dado por el experto; esto permite **clasificar** los elementos en vez de **compararlos**.

#### Obtención de la rejilla
##### Preparación:

Se elige el problema:
- Clasificación de objetos (Taxonomía)
- Evaluación de candidatos o alternativas
- Obtención de las características que determinan una varias clases de objetos
- Recoger una lista de objetos iniciales.

##### Rellenado:
- Implica repetidas comparaciones de elementos, se suelen elegir un grupo de tres elementos para empezar a describir similitudes o diferencias
- Los grupos de tres pueden elegirse al azar o sistemáticamente
- Luego de tener ese constructo, se aplica al resto de elementos y se comienza otra comparación
	- ![](https://remnote-user-data.s3.amazonaws.com/32ab9c8AZ-Q_asUFe9cbVSs0R05YiSd6OGFbC_Gq0WZxkyy_C6n236O1o2SXlAUFTXUVop6WVuYP-w1RryH3TgACUWLaOcqT5sQJsEIBCVZCMPTHSbLQMyy-Umika4cC.png) 
##### Análisis de entidades
- Es necesario para ejecutar la técnica del clustering un criterio que mida la distancia entre pares de elementos, en este caso se puede utilizar la suma de diferencias absolutas entre cada par de elementos.
- Es decirm resta absoluta entre los valores de una fila y los de otra fila
- Luego se realiza una matriz de entidades con Entidades con los valores obtenidos.
	- ![[T3 ⇒ Técnicas automatizadas de adquisición de conocimientos-20240620115647866.webp]] 
- A partir de esta tabla se construye un árbol siguiendo el siguiente procedimiento:
	1. Señala en la rejilla los elementos con distancia mínima
	2. Esos elementos se reemplazan en la rejilla por el conjunto de ambos, por ejemplo si se elige E2 y E6, se reemplaza por [E2,E6]
	3. La distancia del resto de los elementos al conjunto wes el mínimo de las distancias de los elementos del conjunto
	4. Se repite el proceso con la matriz resultante hasta que solo quedan dos categorías en la tabla
	- ![[T3 ⇒ Técnicas automatizadas de adquisición de conocimientos-20240620115702370.webp]] 
##### Analisis de construcciones:
- El procedimiento es el mismo que para las entidades/elementos aunque la distancia entre las construcciones requiere de observarla en ambas direcciones, es decir obtener la resta absoluta de las dos columnas de arriba hacia abajo y otra resta absoluta con una de las columnas en dirección invertida. Luego se reduce el valor pequeño que se obtiene.
	- ![[T3 ⇒ Técnicas automatizadas de adquisición de conocimientos-20240620115729938.webp]]

##### Análisis de resultados
- Cuando se analizan las categorizaciones, el Experto puede corroborar, refutar o matizar los agrupamientos realizados, pudiendo producirse los casos siguientes:
	1. **Dos elementos aparecen ligados cuando no deberían estarlo**, en este caso se pueden reconsiderar valores atribuidos a los objetos, si los valores parecen correctos el IC debe solicitar un motivo para diferenciar esos elementos, dicha característica debe añadirse al estudio y generar dos nuevos árboles de agrupamiento.
	2. **Dos elementos aparecen como disjuntos cuando no deberían estar ligados**, el proceso es similar al anterior. Se añade una característica que los ligue.
	3. **Dos características aparecen ligadas cuando no deberían estarlo**, si los valores atribuidos a los objetos para esas dos características parecen correctos se le solicita al experto un ejemplo de un elemento que contradiga la relación. Si existe, se añade el elemento a la rejilla inicial y se repite el proceso.


# Arboles de decisión

**Árbol de decisión**:: Son una estructura lógica que toma como entrada un objeto o situación descrita a través de un conjunto de atributos y devuelven una "decisión", el valor previsto de la salida dada la entrada.

## Características:

### Según su salida:
?
- Salida Discreta→Clasificación
- Salida Continua→Regresión

Los árboles se pueden convertir en reglas "if-then" siguiendo cada rama del árbol. Pueden tener en las hojas diferentes casos e inclusive casos en lo que la regla no se cumple (**Certeza de la regla**)

Es posible que un *nodo hoja* posea un solo caso esto no es muy representativo, esa regla no está bien respaldada. Se conoce como el "==soporte==" y en el árbol **se descartan aquellas reglas que tengan un ==soporte== mínimo**.

Es necesario que los árboles tengan un grado de profundidad **bajo** para que sean entendibles por una persona Lo que se obtiene en un árbol de decisión es un "pre-conocimiento" el cual luego debe ser validado por el experto, el experto luego añade excepciones a la reglas o bien localizar reglas que no tengan sentido, lo cual luego debe modificarse.

Existe la posibilidad en que dado un grupo de entrenamiento no sea posible generarse un árbol de decisión, se puede aproximar con un cierto grado de **certeza**. 

El conjunto de ejemplos completos se denomina **conjunto de entrenamiento**

#### Ejemplos positivos y negativos:
- Ejemplos positivos→Aquellos los cuales la meta es positiva?
- Ejemplos negativos→Aquellos cuya meta es falsa?


## Inducción de árboles de decisión

- Existen múltiples maneras de inferir el árbol ↓ 
?
	- Trivial
	- Óptimo
	- Pseudo-Óptimo

### Trivial:
?
- Se crea una ruta del árbol por cada instancia de entrenamiento
- Producen árboles excesivamente grandes
- No funciona bien con instancias nuevas

### Óptimo

**Definición**::Consiste en aplicar la heurística de la Navaja de Ockham al árbol. Es inviable a nivel computacional

### Pseudo-Óptimo (Heurístico)

**Definición**::Selección del atributo en cada nivel en función de la calidad de la división que lo produce.
Los principales programas de generación de árboles utilizan procedimientos similares


## Elección de Atributos

>[!important] Diferencias entre un buen atributo y un atributo perfecto
> Un **buen atributo** debería dividir el conjunto de ejemplos en subconjuntos que sean o "todos positivos" o "todos negativos".
> 
> Un **atributo perfecto** dividirá los ejemplos en conjuntos que contienen solo ejemplos positivos y solo ejemplos negativos

Se tiene que definir una medida de atributo "adecuado" y "no adecuado"
Para un conjunto de entrenamiento que contenga $p$ ejemplos positivos y $n$ ejemplo negativos, se utiliza la función del grado de entropía: $$I(\frac{p}{p+n},\frac{n}{p+n})=-\frac{p}{p+n} log_2(\frac{p}{p+n})-\frac{n}{p+n} log_2(\frac{n}{p+n})$$ De manera intuitiva mide la ausencia de homogeneidad de la clasificación.
![[T3 ⇒ Técnicas automatizadas de adquisición de conocimientos-20240620121325551.webp]]

### Heurística de Gini

>[!info] 
>Es otro criterio  similar a la ganancia de información, pero reemplaza la entropía por $$g(A) = 1 - \sum^{v}_{i=1}p^2_{i}$$
>
>La calidad de las particiones quedan de la siguiente forma:
>$$\text{Gini}(A)=g(a)-\sum^v_{i=1}(p_{i}* g(A_{i}))$$

## Atributos de salida continuos (Regresión)
![[T3 ⇒ Técnicas automatizadas de adquisición de conocimientos-20240620121939773.webp]]