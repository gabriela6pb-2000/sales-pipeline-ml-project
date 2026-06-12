# Informe de salida

## Resumen Ejecutivo

El presente proyecto tuvo como objetivo desarrollar un modelo predictivo capaz de estimar la probabilidad de éxito de oportunidades comerciales B2B mediante técnicas de Machine Learning y el análisis de datos históricos del pipeline de ventas. La iniciativa surgió de la necesidad de apoyar la toma de decisiones comerciales en organizaciones orientadas a servicios de catering, food services y servicios técnicos generales, donde la adecuada priorización de oportunidades representa una ventaja competitiva significativa.

A lo largo del proyecto se ejecutaron las diferentes fases de la metodología de ciencia de datos, incluyendo el entendimiento del negocio, la exploración y preparación de los datos, el desarrollo y evaluación de modelos predictivos, así como la interpretación de los resultados obtenidos. El modelo final demostró capacidad para identificar patrones asociados al éxito o fracaso de las oportunidades comerciales, proporcionando una herramienta de apoyo para la gestión estratégica del pipeline de ventas.

## Resultados del proyecto

Durante el desarrollo del proyecto se alcanzaron los siguientes entregables y logros:

* Comprensión del proceso comercial y definición del problema de negocio.
* Consolidación y depuración de la base histórica de oportunidades comerciales.
* Desarrollo del análisis exploratorio de datos para identificar patrones, tendencias y variables relevantes.
* Implementación de técnicas de preprocesamiento, tratamiento de valores faltantes y transformación de variables.
* Construcción y evaluación de diversos modelos de clasificación supervisada.
* Comparación del desempeño de modelos base y modelos avanzados de Machine Learning.
* Selección del modelo con mejor capacidad predictiva e interpretación de sus resultados.

El desempeño del modelo final fue comparado con un modelo base, evidenciando mejoras en la capacidad de clasificación de las oportunidades comerciales. El modelo seleccionado obtuvo resultados satisfactorios en términos de métricas como Accuracy, Precision, Recall, F1-Score y ROC-AUC. Los resultados sugieren que es posible anticipar, con un nivel aceptable de precisión, la probabilidad de éxito de una oportunidad comercial utilizando información disponible durante las etapas tempranas del proceso de ventas. Esta capacidad resulta altamente relevante para el negocio, ya que permite optimizar la asignación de recursos comerciales y priorizar aquellas oportunidades con mayor potencial de generación de ingresos.

## Lecciones aprendidas

El desarrollo del proyecto permitió identificar diversos desafíos asociados a la implementación de soluciones analíticas en entornos empresariales reales.

Uno de los principales retos estuvo relacionado con la calidad y disponibilidad de los datos históricos. Fue necesario realizar procesos exhaustivos de limpieza, validación y transformación para garantizar la consistencia de la información utilizada en el entrenamiento de los modelos.

Asimismo, se evidenció la importancia de comprender el contexto del negocio antes de iniciar la fase de modelamiento. Variables aparentemente poco relevantes desde una perspectiva técnica demostraron tener una fuerte influencia sobre el resultado de las oportunidades debido a particularidades del proceso comercial.

En cuanto al modelamiento, se aprendió que modelos más complejos no necesariamente generan mejores resultados si no se acompaña su implementación con una adecuada selección de variables, balanceo de clases y validación rigurosa. De igual manera, la interpretabilidad del modelo constituye un aspecto fundamental para promover la confianza y adopción por parte de los usuarios finales.

Para futuros proyectos de Machine Learning se recomienda fortalecer los procesos de captura y gobierno de datos, incorporar mecanismos periódicos de actualización del modelo y promover la colaboración continua entre expertos del negocio y especialistas analíticos.

## Impacto del proyecto

La implementación de un modelo predictivo para la gestión de oportunidades comerciales tiene el potencial de generar beneficios significativos para la organización.

Entre los principales impactos identificados se encuentran:

* Priorización objetiva de oportunidades con mayor probabilidad de cierre exitoso.
* Optimización del tiempo y esfuerzo del equipo comercial.
* Mejor asignación de recursos para la preparación de propuestas y licitaciones.
* Incremento potencial de la tasa de conversión del pipeline.
* Reducción de costos asociados a oportunidades con baja probabilidad de éxito.
* Mayor capacidad para anticipar resultados y apoyar la toma de decisiones estratégicas basada en datos.

Adicionalmente, el proyecto abre oportunidades para futuras líneas de desarrollo, tales como la actualización automática de probabilidades en tiempo real, la integración del modelo con plataformas CRM y la incorporación de nuevas fuentes de información que permitan mejorar continuamente el desempeño predictivo.

## Resultados del proyecto

Como parte del proceso de modelamiento se evaluaron diferentes algoritmos de clasificación supervisada con el fin de identificar la alternativa con mejor capacidad predictiva para estimar el resultado de las oportunidades comerciales. Entre los modelos analizados se incluyeron modelos base y modelos más avanzados basados en técnicas de aprendizaje por conjuntos.

El modelo seleccionado fue **Random Forest**, debido a que presentó el mejor desempeño general en las métricas consideradas más relevantes para el objetivo del negocio, particularmente **Recall** y **F1-Score**.

La elección de este modelo estuvo alineada con las necesidades del contexto comercial. En este caso, el Recall fue una métrica prioritaria, ya que permitía identificar la mayor cantidad posible de oportunidades con potencial de convertirse en ventas exitosas, evitando que oportunidades valiosas pasaran desapercibidas. Por su parte, el F1-Score permitió evaluar el equilibrio entre Precision y Recall, garantizando un desempeño consistente del modelo.

Los resultados obtenidos evidenciaron que el modelo Random Forest superó el desempeño del modelo base, demostrando una mayor capacidad para clasificar correctamente las oportunidades comerciales y proporcionando una herramienta de apoyo para la toma de decisiones dentro del proceso de ventas.

## Conclusiones

El desarrollo de este proyecto permitió demostrar que las técnicas de Machine Learning pueden aplicarse de manera efectiva para apoyar la gestión de oportunidades comerciales B2B. A partir del análisis de datos históricos del pipeline de ventas, fue posible identificar patrones asociados al éxito o fracaso de las oportunidades y traducirlos en predicciones útiles para el negocio.

La selección del modelo Random Forest confirmó que los métodos basados en conjuntos representan una alternativa sólida para problemas de clasificación en entornos comerciales, especialmente cuando se busca un equilibrio entre desempeño predictivo, estabilidad e interpretabilidad. El énfasis en métricas como Recall y F1-Score permitió que la evaluación del modelo estuviera alineada con las prioridades estratégicas de la organización y no únicamente con la maximización de la exactitud global.

Desde una perspectiva empresarial, el modelo desarrollado puede contribuir a una mejor priorización de oportunidades, optimización de recursos comerciales y fortalecimiento de los procesos de toma de decisiones basados en datos. Asimismo, este proyecto constituye una base para futuras iniciativas analíticas, como la integración del modelo en plataformas CRM, la actualización periódica de las predicciones y la incorporación de nuevas variables que permitan mejorar continuamente su desempeño.

Finalmente, se concluye que la adopción de herramientas predictivas en los procesos comerciales no solo representa una oportunidad para incrementar la eficiencia operativa, sino también para impulsar una cultura organizacional orientada al aprovechamiento estratégico de los datos.

