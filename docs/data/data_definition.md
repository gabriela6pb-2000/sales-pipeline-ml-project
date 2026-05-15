# Definición de los datos

## Origen de los datos

- Fuente de los datos: CRM Sales Opportunities Dataset disponible en Kaggle.
- URL del dataset: https://www.kaggle.com/datasets/nilkamalsaha/crm-sales-opportunities-on-google-sheets
- Los datos fueron obtenidos desde la plataforma Kaggle en formato CSV.
- El dataset contiene información histórica relacionada con oportunidades comerciales B2B, clientes, representantes de ventas, productos y estados del pipeline comercial.

## Especificación de los scripts para la carga de datos

- El proyecto utilizará scripts en Python para la carga y procesamiento inicial de los datos.
- Los scripts de carga estarán almacenados en la carpeta `src/data/`.
- El archivo principal de carga de datos será `load_data.py`.
- Se utilizará la librería `pandas` para la lectura y manipulación de archivos CSV.

## Referencias a rutas o bases de datos origen y destino

### Rutas de origen de datos

- Los archivos de origen estarán almacenados en la carpeta:

```text
data/raw/
```

- Los archivos principales del dataset corresponden a:

```text
sales_pipeline.csv
accounts.csv
sales_teams.csv
products.csv
data_dictionary.csv
```

- Los archivos se encuentran en formato CSV y contienen información estructurada relacionada con el pipeline comercial B2B.

- Inicialmente se realizará una exploración y validación de calidad de datos incluyendo:
  - revisión de valores nulos
  - validación de tipos de datos
  - análisis de inconsistencias
  - transformación de variables categóricas
  - preparación de variables para modelamiento predictivo

### Base de datos de destino

- Para este proyecto no se utilizará una base de datos relacional como destino final.
- Los datos procesados serán almacenados temporalmente en estructuras de datos de Python y archivos procesados dentro del proyecto.
- Los datasets transformados podrán almacenarse en la carpeta:

```text
data/processed/
```

- Los procedimientos de transformación incluirán:
  - limpieza de datos
  - ingeniería de características
  - generación de variables derivadas
  - preparación de datasets para entrenamiento y evaluación de modelos de Machine Learning
