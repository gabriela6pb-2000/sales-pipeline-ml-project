# Reporte del Modelo Final

## Resumen Ejecutivo

El presente proyecto tuvo como objetivo desarrollar un modelo de Machine Learning capaz de predecir la probabilidad de éxito de oportunidades comerciales B2B utilizando información histórica de un pipeline de ventas. La solución busca apoyar la toma de decisiones comerciales mediante la identificación temprana de oportunidades con mayor potencial de cierre exitoso.

Durante el proceso de modelamiento se evaluaron tres algoritmos de clasificación: Regresión Logística, Random Forest y XGBoost. Los modelos fueron comparados utilizando las métricas Accuracy, Precision, Recall, F1-Score y ROC-AUC.

Los resultados obtenidos muestran que el modelo Random Forest presentó el mejor desempeño general, alcanzando un Accuracy de 70.74%, un Recall de 93.51% y un F1-Score de 75.49%. Estos resultados representan una mejora significativa respecto al modelo baseline basado en Regresión Logística.

Por esta razón, Random Forest fue seleccionado como modelo final para la solución propuesta.

---

## Descripción del Problema

Las organizaciones que operan bajo esquemas de ventas B2B suelen gestionar simultáneamente múltiples oportunidades comerciales. Sin embargo, no todas las oportunidades tienen la misma probabilidad de convertirse en ventas efectivas, lo que dificulta la priorización de esfuerzos comerciales y la asignación eficiente de recursos.

El problema abordado en este proyecto consiste en predecir si una oportunidad comercial será ganada o perdida utilizando información histórica disponible durante el ciclo comercial.

La capacidad de anticipar el resultado de una oportunidad ofrece beneficios estratégicos para la organización, entre ellos:

* Priorización de oportunidades con mayor probabilidad de éxito.
* Optimización del tiempo y esfuerzo de los representantes comerciales.
* Mejor asignación de recursos comerciales.
* Incremento en la eficiencia de los procesos de ventas.
* Apoyo a la toma de decisiones basada en datos.

La variable objetivo utilizada fue **is_won**, donde:

* 1 representa una oportunidad ganada.
* 0 representa una oportunidad perdida.

---

## Descripción del Modelo

El desarrollo del modelo siguió las etapas de la metodología CRISP-DM:

1. Entendimiento del negocio.
2. Entendimiento de los datos.
3. Preparación de los datos.
4. Modelamiento.
5. Evaluación.
6. Propuesta de despliegue.

### Preparación de Datos

Durante el proceso de preparación se realizaron las siguientes actividades:

* Tratamiento de valores faltantes mediante imputación.
* Codificación de variables categóricas utilizando One-Hot Encoding.
* Estandarización de variables numéricas.
* División de datos en conjuntos de entrenamiento (80%) y prueba (20%).

Adicionalmente, se identificó y eliminó fuga de información (data leakage) en variables como deal_stage y close_value, las cuales contenían información directamente relacionada con el resultado final de la oportunidad comercial.

### Selección de Características

Como técnica de análisis de características se realizó una evaluación de correlación entre variables numéricas y la variable objetivo.

Este análisis permitió identificar relaciones relevantes entre las variables del negocio y el resultado de las oportunidades comerciales, además de detectar posibles redundancias entre variables explicativas.

### Modelos Evaluados

Se evaluaron tres modelos de clasificación:

* Regresión Logística (Baseline)
* Random Forest
* XGBoost

El objetivo fue comparar diferentes enfoques de modelamiento y seleccionar el algoritmo con mejor desempeño predictivo.

### Modelo Seleccionado

El modelo seleccionado fue Random Forest debido a que presentó el mejor desempeño general en las métricas más relevantes para el negocio, especialmente Recall y F1-Score.

Random Forest es un algoritmo basado en conjuntos de árboles de decisión que combina múltiples modelos para generar predicciones más robustas y reducir el riesgo de sobreajuste.

---

## Evaluación del Modelo

### Métricas Utilizadas

Se utilizaron las siguientes métricas de evaluación:

* Accuracy
* Precision
* Recall
* F1-Score
* ROC-AUC

Estas métricas permiten evaluar diferentes aspectos del desempeño del modelo y proporcionar una visión integral de su capacidad predictiva.

### Comparación de Modelos

| Modelo              | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
| ------------------- | -------- | --------- | ------ | -------- | ------- |
| Logistic Regression | 0.6432   | 0.5991    | 0.7842 | 0.6793   | 0.6890  |
| Random Forest       | 0.7074   | 0.6329    | 0.9351 | 0.7549   | 0.7638  |
| XGBoost             | 0.7006   | 0.6554    | 0.7983 | 0.7198   | 0.7940  |

### Interpretación de Resultados

Los resultados muestran una mejora significativa respecto al modelo baseline.

Random Forest obtuvo el mayor Accuracy (70.74%), indicando una mejor capacidad para clasificar correctamente las oportunidades comerciales.

Asimismo, alcanzó un Recall de 93.51%, lo que significa que identifica correctamente más del 93% de las oportunidades que finalmente terminan siendo ganadas. Esta característica es especialmente valiosa para el negocio, ya que reduce la probabilidad de perder oportunidades potencialmente exitosas.

El F1-Score de 75.49% demuestra un equilibrio adecuado entre precisión y cobertura, convirtiéndolo en el modelo más robusto entre los evaluados.

Aunque XGBoost obtuvo el mejor ROC-AUC (79.40%), el desempeño general de Random Forest fue superior considerando las métricas prioritarias para el contexto comercial.

Por estas razones, Random Forest fue seleccionado como modelo final.

---

## Conclusiones y Recomendaciones

### Conclusiones

* El uso de técnicas de Machine Learning permitió mejorar significativamente la capacidad de predicción respecto al modelo baseline.
* Random Forest presentó el mejor desempeño global entre los modelos evaluados.
* La eliminación de variables con fuga de información permitió obtener resultados realistas y confiables.
* El modelo seleccionado demuestra una capacidad adecuada para apoyar procesos de priorización comercial y toma de decisiones.

### Fortalezas

* Alta capacidad para identificar oportunidades ganadas.
* Buen equilibrio entre precisión y cobertura.
* Robustez frente a ruido y variabilidad de los datos.
* Interpretabilidad mediante análisis de importancia de variables.

### Limitaciones

* El modelo depende de la calidad y representatividad de los datos históricos.
* Cambios futuros en las estrategias comerciales podrían afectar el desempeño del modelo.
* Algunas variables relevantes para el proceso de ventas podrían no estar disponibles en el conjunto de datos.

### Recomendaciones

* Actualizar periódicamente el modelo utilizando nuevos datos.
* Incorporar variables adicionales relacionadas con comportamiento de clientes y actividades comerciales.
* Implementar monitoreo continuo del desempeño del modelo.
* Evaluar técnicas avanzadas de optimización de hiperparámetros para mejorar aún más el desempeño predictivo.

