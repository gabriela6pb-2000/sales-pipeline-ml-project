# Reporte de Datos

---

# 1. Reporte de Datos

Este documento contiene los resultados del análisis exploratorio de datos realizado sobre el dataset CRM de oportunidades comerciales.

---

# 1.1 Resumen General de los Datos

El dataset utilizado corresponde a un pipeline comercial B2B compuesto por múltiples tablas relacionadas con oportunidades comerciales, cuentas, productos y equipos de ventas. Las tablas principales utilizadas fueron:

- `sales_pipeline`
- `accounts`
- `sales_teams`
- `products`

Posteriormente, las tablas fueron integradas mediante relaciones tipo *left join* utilizando las llaves correspondientes (`account`, `sales_agent` y `product`).

El dataset consolidado contiene información relacionada con:

- Clientes y cuentas comerciales.
- Representantes comerciales.
- Productos ofrecidos.
- Estados del pipeline comercial.
- Valores de cierre.
- Fechas de engagement y cierre.
- Revenue y características organizacionales.

Durante el preprocesamiento se identificaron variables numéricas, categóricas y temporales. Las variables de fecha fueron transformadas correctamente al formato `datetime` para facilitar análisis temporales y cálculos asociados al ciclo comercial.

---

# 1.2 Resumen de Calidad de los Datos

Durante la evaluación de calidad de datos se identificaron registros con valores faltantes principalmente en las variables:

- `account`
- `close_date`
- `close_value`

Se encontró que muchos registros sin cuenta asociada pertenecían a etapas tempranas del pipeline comercial (`Prospecting` y `Engaging`). Debido a esto, dichos registros fueron reclasificados utilizando el valor `"TBD"` (*To Be Defined*), interpretando que corresponden a oportunidades comerciales aún en proceso de definición.

Asimismo:

- Las columnas `close_date` y `close_value` se mantuvieron vacías para oportunidades aún no cerradas.
- Se realizó validación de registros duplicados.
- Se verificaron tipos de datos y consistencia de las relaciones entre tablas.
- Se creó la variable `sales_cycle_days` para medir la duración del ciclo comercial.

La duración del ciclo comercial fue calculada mediante:

$$
Sales\ Cycle\ Days = close\_date - engage\_date
$$

---

# 1.3 Variable Objetivo

La variable objetivo del proyecto corresponde al estado de éxito de la oportunidad comercial (`deal_stage`), particularmente las categorías:

- `Won`
- `Lost`

A partir de esta variable se construyó una variable binaria (`is_won`) para representar si una oportunidad fue exitosa o no:

- `1` → Won
- `0` → Lost

La distribución general del pipeline mostró un comportamiento relativamente balanceado:

- `Won`: 25.9%
- `Lost`: 25.9%
- `Engaging`: 25.9%
- `Prospecting`: 22.3%

La tasa de conversión comercial (*Conversion Rate*) fue calculada mediante:

$$
Conversion\ Rate = \frac{Won}{Won + Lost} \times 100
$$

El *Conversion Rate* mensual osciló entre aproximadamente 48.8% y 58.7%, evidenciando un comportamiento relativamente estable del pipeline comercial.

---

# 1.4 Variables Individuales

Se realizó un análisis individual de las principales variables numéricas y categóricas.

## Productos

El producto con mayor valor de cierre acumulado fue:

- **GTXPro** → 3,510,578 USD (35.09%)

Seguido por:

- **GTX Plus Pro** → 2,629,651 USD (26.28%)
- **MG Advanced** → 2,216,387 USD (22.15%)

Estos resultados muestran una fuerte concentración del revenue en los productos premium del portafolio.

## Comerciales

El comercial con mejor desempeño fue:

- **Darcel Schlecht** → 1,153,214 USD (11.53% del revenue total)

Seguido por:

- Vicki Laflamme → 478,396 USD
- Kary Hendrixson → 454,298 USD
- Cassey Cress → 450,489 USD
- Donn Cantrell → 445,860 USD

## Pipeline Comercial

El análisis temporal mostró que las oportunidades en estado `Engaging` alcanzaron su máximo en julio de 2017 con aproximadamente 69 cuentas activas, indicando un incremento importante de actividad comercial durante ese periodo.

---

# 1.5 Ranking de Variables

Durante el análisis exploratorio se identificaron variables potencialmente relevantes para el modelo predictivo:

Variables con mayor relevancia potencial:

- `close_value`
- `product`
- `sales_agent`
- `revenue`
- `employees`
- `sector`
- `regional_office`
- `sales_cycle_days`

Estas variables podrían influir significativamente en la probabilidad de éxito de oportunidades comerciales.

En fases posteriores se utilizarán técnicas adicionales para evaluar importancia de variables, incluyendo:

- Correlación
- Feature Importance
- PCA

---

# 1.6 Relación entre Variables Explicativas y la Variable Objetivo

El análisis exploratorio permitió identificar relaciones importantes entre variables explicativas y el resultado de las oportunidades comerciales.

Principales hallazgos:

- Los productos premium (`GTXPro` y `GTX Plus Pro`) concentran gran parte del revenue generado por oportunidades exitosas.
- Algunos comerciales generan una proporción significativamente superior del revenue total.
- Las cuentas con mayor número de empleados suelen estar asociadas a mayores niveles de revenue.
- El pipeline comercial mantiene un comportamiento relativamente estable entre oportunidades ganadas y perdidas.
- El *Conversion Rate* mensual se mantuvo generalmente entre 50% y 56%, indicando estabilidad en la capacidad de conversión comercial.

