ARBOLES DE DECISION



Pueden ser de clasificación o de regresión

También pueden ser binarios o no. Cuando las preguntas son SI o NO son binarios.



Son algoritmos no paramétricos, porque no asumen ninguna distribución en tus datos

No hace falta escalar, estandarizar o normalizar.



ONE-HOT ENCODER



Convierte una variable categórica en numérica. 

A partir de una columna, te crea columnas como valores únicos de categoría y coloca un 1



Ejemplo. Países: ESPAÑA, PORTUGAL, FRANCIA



Creamos 3 columnas viajes\_España, viajes\_Portugal, viajes\_Francia



ESPAÑA 			1		0		0

PORTUGAL 		0		1		0

FRANCIA 		0		0		1



Esto sirve cuando hay poco valores de la categórica. Si tuviéramos 50 valores, crearíamos 50 columnas --> No interesa.

ONE HOT ENCODER tiene una trampa: En la regresión lineal la colinealidad hace mucho daño. Al crear nuevas columnas existe colinealidad



GET\_DUMMIES(drop\_first = True) --> poniéndolo a True, te elimina la primera columna generada, de esta forma elimina la colinealidad. Cuando no es ni Portugal ni Francia, será España por descarte. Por lo que quitamos colinealidad.



ONE HOT ENCODER tiene un parámetro que se llama (handle\_unknown = "error"). Se puede poner en "ignore" cuando piensas que se van a añadir más países a futuro. De tal forma que te 



GINI O ENTROPIA --> Miden la **DESIGUALDAD**, o lo que es lo mismo la **PUREZA**

**GINI** funciona mejor en datasets grandes (más rápido) y gestiona mejor las categorías abusonas

**ENTROPIA** funciona mejor con datasets pequeños y más balanceados



RANDOM FOREST():

- La gran ventaja del bosque es que es robusto frente a OVERFITTING
- max_features --> IMPORTANTE. Son las columnas que coge el algoritmo para cada ARBOL y para cada NODO. LOL
- oob_score --> 

- Bootstrap --> Coges aleatoriamente registros de tus datos originales pero los vuelves a meter en la "bolsa". Es decir, en una Bootstrap sample puedes tener más de 1 vez cada 	registro (calcado).

- Bagging = Bootstrap + agreggating



El peligro de un árbol es que haga overfitting


CAT BOOST es la solución a este problema --> Cascada con categóricas.

BOOSTING es ensamblado en cascada 

- ADA BOOST --> Combinacion de las salidas de clasificador (aunque suelen ser arboles). Aportando más peso a los valores mal clasificados y volviendolo a pasar por el siguiente arbol (cascada).
    - Learning_rate --> Inercia de la cascada. Cuanto mayor sea más cambios produce en cada salida. Mejor ajustarlo a un rtio pequeño para que el aprendizaje vaya de poco a poco.






