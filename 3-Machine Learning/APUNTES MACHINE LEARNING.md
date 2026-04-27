**APUNTES MACHINE LEARNING**



A la regresión le afecta la colinealidad, mientras que a los arboles de regresión, no

A la regresión logística le afectan los outlayers, mientras que a los arboles de clasificación, no



Histograma de las features para ver la distribución y plantear preprocesado



Optimizar hiperparámetros --> GridSearch CV --> best\_params / best\_score







**MÉTRICAS DE CLASIFICACION**



Balanced\_accuracy es lo mismo que el recall (SENSIBILIDAD) medio --> 

RECALL --> de los que SON SÍ, cuantos aciertas? --> Le afectan los FALSOS NEGATIVOS (Cuando dices que NO y es que SÍ) (TP / TP + FN)

ACCURACY --> cuanto acierto en general (TP + TN / TODO) 

PRECISION --> de los que DICES SÍ, cuantos aciertas? --> Le afectan los FALSOS POSITIVOS (cuando dices que SÍ y es que NO) (TP / TP + FP)



F-SCORE --> Te dice el ratio recall / precisión. Cuanto mayor sea el valor de Beta, mayor importancia le da al recall frente a la precisión. Cuando Beta = 1, importancia equivalente entre recall y precisión.



UMBRAL (threshold) --> A partir de qué porcentaje dices que SÍ. Apruebas con un 51% o con un 80%? Van cambiando las métricas dependiendo del umbral que le pongas.



ROC AUC --> Mide el área bajo la curva de la relación entre el TPR y FPR (True positive rate y false positive rate)





