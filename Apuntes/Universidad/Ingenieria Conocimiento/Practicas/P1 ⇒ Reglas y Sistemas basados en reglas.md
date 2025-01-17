- 
- Definiciones:
- Hechos::Afirmaciones que en un caso concretos serán verdad o mentira (lógica clásica)
- Reglas::Construcciones con el formato: ''Si **antecedente 1, ... , y antecendenteN** Entonces consecuente1,... y consecuente n'' donde los antecentes y los consecuentes son hechos
- Componentes del conocimiento:
	- Base de conocimiento→Contiene las reglas y, a veces, también algunas afirmaciones iniciales (los hechos que son validos en cualquier caso). La base de Conocimiento es específica del dominio en que el sistema puede considerarse experto.
	- Base de hechos actuales::También conocida como **memoria de trabajo.** Contiene las afirmaciones que se consideran ciertas para el caso actual en el momento actual
	- Base de datos::Contiene información acerca a variables que se utilizan en la resolución del problema. Pueden contener información relativa al histórico de casos. 
	- Ejemplo:
		- ![](https://remnote-user-data.s3.amazonaws.com/XO3Sn7WT7uMeM53ZIERP8GPmWeOocfeN6H6LF2QS1Fzo1BXnooWqNlfDDKLai3FGmRAt1f6jbQyCEGZOaq09Yp-MunEbQm4DYMdTnseKD_JxH72sfLiRx2ru2lFEkq_A.png) 
- Uso de reglas en la IA
    - Newel y Simon (No los conocen ni en su casa) proponen las **Reglas** como modelo para describir comportamiento inteligente.
    - Comportamiento inteligente→Conjunto de reglas que indiquen en cada momento **como actuar en función de la información disponible.** 

    - Cómo actuar
        - Deducir nuevos ¨hechos¨
        - Eliminar ¨hechos¨
        - Realizar acciones 
            - Obtener Datos
            - Interactuar con usuarios
            - añadir tareas a realizar 
            - etc
    - Deducción con reglas (Modus Ponem o razonamiento hacia delante)
        - Dada una base de conocimiento formada por un conjunto de reglas ↓ 
            - Se mantiene una base de hechos que son ciertos en este momento
            - Si todos los hechos del antecedente de una regla están o casan con los hechos de la base de hechos, se realiza todo lo indicado en el consecuente: añadir hechos, eliminar hechos, realizar acciones,...
            - Se reitera hasta que no haya ninguna regla que se pueda disparar

### Sistemas de reglas vs Lógica clásica

- Los sistemas basados en reglas incluyen a la lógica clásica
- Los sistemas basados en reglas incluyen con la retractación una lógica monótona con mas posibilidades de representación (puede deducir hechos como ciertos que después se elimina)
- ![](https://remnote-user-data.s3.amazonaws.com/06d7nEMHfEvmBkttZG16aLE1aQ0_7IFqc8JVIB812xJ456PRdNBeM1m7TDNK9bZU497Z-W3Qlx4RAPZHiIuFkZHo85QruJKHO5mfGHRxH1juIdKZGFC4R6UhrgWpvU7H.png) 
## Motor de inferencia:
- Motor de inferencia→Decida que regla disparar y ejecuta la acción de dicha regla (añadir nuevos hechos a la base de hechos, eliminar hechos de la base de hechos, interaccionar con el usuario, o obtener nuevos hechos a partir de cálculos con la base de datos.
- Interacción con usuarios y base de datos
    - Interfaz de usuario→Se encarga de pedirla indormación al usuario y de mostrarle la información que va deduciendo
    - Comunicación con BD→es aconsejable realizar y almacenar todos los cálculos del sistema en BD, y reducir la comunicación al proceso de leer y añadir datos. De esta forma la parte procedimental se separa del conocimiento, y así se puede midificar depurar o adaptar el conocimiento sin necesidad de reprogramar. 
## Estructura de una regla:

- Una regla consta de dos partes ↓ 
	- Antecedente
	- Consecuente

- Antecedente::o parte izquierda. Contiene las cláusulas que deben cumplirse para que la regla pueda evaluarse o ejecutarse

- **Consecuentes**::o parte derecha. Indica las conclusiones que se deducen de las premisas (declarativo) o las acciones que el sistema debe realizar cuando ejecuta la regla (imperativo)
 ^8sfluw
- El antecedente
	- Es la condición para que la regla pueda dispararse. Es la parte del "Si" o la parte izquierda
	- Eta formado normalmente por una conjunción de literales.
	- Un literal es una afirmación simple o una negación de la misma.
	- Cada afirmación simple puede ser una hipótesis o una relación de comparación
- Tipos de acciones de las reglas.
	- Los tipos de acciones que pueden aparecer en el consecuente de una regla son ↓ 
		- Afirmar
		- Retractar
		- Actuar
	- **Afirmar**::se establece algún tipo de afirmación
	- **Retractar**::se modifica una afirmación anterior
	- **Actuar**::se envía una orden a los actuadores con los que está conectado el sistema 
