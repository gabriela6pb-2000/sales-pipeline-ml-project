# Reporte del Modelo Baseline

## Descripción del Modelo

El modelo baseline fue desarrollado con el objetivo de establecer una línea base de desempeño para la predicción del resultado de oportunidades comerciales B2B. Este modelo permite evaluar la capacidad predictiva de las variables disponibles y sirve como punto de referencia para comparar modelos más avanzados en etapas posteriores del proyecto.

Se seleccionó una Regresión Logística como modelo baseline debido a su simplicidad, interpretabilidad y amplio uso en problemas de clasificación binaria. Este algoritmo estima la probabilidad de que una oportunidad comercial sea ganada o perdida a partir de las características históricas disponibles en el pipeline comercial.

---

## Variables de Entrada

Para el entrenamiento del modelo se utilizaron variables relacionadas con las características de las oportunidades comerciales, los clientes y el contexto organizacional. Entre las principales variables utilizadas se encuentran:

* sales_agent
* product
* account
* sector
* year_established
* revenue
* employees
* office_location
* subsidiary_of
* manager
* regional_office
* series
* sales_price
* sales_cycle_days
* engage_year
* engage_month
* close_year
* close_month

Durante la fase de preparación de datos se identificaron variables que generaban fuga de información (data leakage), por lo que fueron excluidas del proceso de modelamiento. Estas variables fueron:

* opportunity_id
* deal_stage
* engage_date
* close_date
* close_value

La exclusión de estas variables permitió garantizar que el modelo realizara predicciones utilizando únicamente información que estaría disponible antes del resultado final de la oportunidad comercial.

---

## Variable Objetivo

La variable objetivo utilizada fue:

**is_won**

Esta variable indica el resultado final de cada oportunidad comercial:

* 1: Oportunidad ganada (Won)
* 0: Oportunidad perdida (Lost)

El objetivo del modelo consiste en predecir la probabilidad de que una oportunidad comercial sea ganada a partir de la información histórica disponible.

---

## Preparación de los Datos

Antes del entrenamiento del modelo se realizaron las siguientes actividades de preparación:

### Tratamiento de Valores Faltantes

* Las variables numéricas fueron imputadas utilizando la mediana.
* Las variables categóricas fueron imputadas utilizando la moda.

### Transformación de Variables

* Las variables categóricas fueron codificadas mediante One-Hot Encoding.
* Las variables numéricas fueron estandarizadas utilizando StandardScaler.

### División del Conjunto de Datos

El conjunto de datos fue dividido en:

* 80% para entrenamiento.
* 20% para prueba.

La división se realizó utilizando muestreo estratificado para mantener la proporción original de oportunidades ganadas y perdidas en ambos conjuntos.

---

## Evaluación del Modelo

### Métricas de Evaluación

Para evaluar el desempeño del modelo se utilizaron las siguientes métricas:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC

Estas métricas permiten evaluar diferentes aspectos del rendimiento del modelo, incluyendo la capacidad de clasificación general, la identificación correcta de oportunidades ganadas y el equilibrio entre precisión y cobertura.

---

## Resultados de Evaluación

| Métrica   | Resultado |
| --------- | --------- |
| Accuracy  | 0.643     |
| Precision | 0.599     |
| Recall    | 0.784     |
| F1-Score  | 0.679     |
| ROC-AUC   | 0.689     |

### Matriz de Confusión

|               | Predicción: Perdida | Predicción: Ganada |
| ------------- | ------------------: | -----------------: |
| Real: Perdida |                 467 |                445 |
| Real: Ganada  |                 183 |                665 |

---

## Análisis de los Resultados

El modelo baseline obtuvo un Accuracy de 64.3%, lo que indica que aproximadamente dos de cada tres oportunidades comerciales fueron clasificadas correctamente.

La métrica Recall alcanzó un valor de 78.4%, lo cual significa que el modelo logró identificar correctamente una alta proporción de las oportunidades que efectivamente terminaron siendo ganadas. Desde una perspectiva comercial, esta capacidad resulta especialmente relevante, ya que permite detectar una mayor cantidad de oportunidades con potencial de cierre exitoso.

Por otro lado, la métrica Precision obtuvo un valor de 59.9%, indicando que existe una cantidad considerable de falsos positivos. En otras palabras, algunas oportunidades clasificadas como ganadas finalmente resultan ser perdidas.

El valor de ROC-AUC de 68.9% refleja una capacidad moderada para diferenciar entre oportunidades ganadas y perdidas. Aunque el desempeño es aceptable para un modelo baseline, existen oportunidades de mejora mediante la utilización de algoritmos más avanzados y técnicas adicionales de selección y extracción de características.

Durante el desarrollo del modelo se identificó una situación de fuga de información (data leakage) asociada principalmente a las variables deal_stage y close_value. Estas variables contenían información directamente relacionada con el resultado final de la oportunidad comercial, generando inicialmente métricas artificialmente perfectas. Por esta razón fueron eliminadas del conjunto de entrenamiento para asegurar una evaluación realista y confiable del desempeño del modelo.

---

## Conclusiones

La Regresión Logística permitió construir una línea base sólida para la predicción de oportunidades comerciales B2B.

Los resultados obtenidos muestran que el modelo posee una capacidad predictiva moderada, especialmente en la identificación de oportunidades ganadas, lo cual representa un punto de partida adecuado para futuras mejoras.

La detección y eliminación de variables con fuga de información constituyó un paso fundamental para garantizar la validez de los resultados obtenidos.

Este modelo baseline servirá como referencia para comparar el desempeño de modelos más avanzados, tales como Random Forest, XGBoost y otros algoritmos de Machine Learning, que serán evaluados en etapas posteriores del proyecto con el objetivo de incrementar la precisión y capacidad predictiva del sistema.

---

## Referencias

* Géron, A. (2022). Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow. O'Reilly Media.
* James, G., Witten, D., Hastie, T., & Tibshirani, R. (2021). An Introduction to Statistical Learning. Springer.
* Pedregosa, F. et al. (2011). Scikit-learn: Machine Learning in Python. Journal of Machine Learning Research.
* Han, J., Kamber, M., & Pei, J. (2012). Data Mining: Concepts and Techniques. Morgan Kaufmann.
