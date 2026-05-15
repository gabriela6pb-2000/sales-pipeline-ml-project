# Diccionario de datos

## Base de datos 1: sales_pipeline.csv

Contiene información histórica relacionada con oportunidades comerciales dentro del pipeline de ventas B2B.

| Variable | Descripción | Tipo de dato | Rango/Valores posibles | Fuente de datos |
| --- | --- | --- | --- | --- |
| opportunity_id | Identificador único de la oportunidad comercial | Categórico | Valores únicos | CRM Sales Opportunities Dataset |
| sales_agent | Representante comercial asignado | Categórico | Nombre del agente | CRM Sales Opportunities Dataset |
| product | Producto ofertado | Categórico | Productos comerciales | CRM Sales Opportunities Dataset |
| account | Cliente o cuenta asociada | Categórico | Nombre de la cuenta | CRM Sales Opportunities Dataset |
| deal_stage | Estado de la oportunidad comercial | Categórico | Won, Lost, Engaging, Prospecting | CRM Sales Opportunities Dataset |
| engage_date | Fecha de inicio de la oportunidad | Fecha | YYYY-MM-DD | CRM Sales Opportunities Dataset |
| close_date | Fecha de cierre de la oportunidad | Fecha | YYYY-MM-DD | CRM Sales Opportunities Dataset |
| close_value | Valor económico de cierre | Numérico | Valores monetarios positivos | CRM Sales Opportunities Dataset |

- **Variable**: nombre de la variable.
- **Descripción**: breve descripción de la variable.
- **Tipo de dato**: tipo de dato que contiene la variable.
- **Rango/Valores posibles**: rango o valores que puede tomar la variable.
- **Fuente de datos**: fuente de los datos de la variable.

---

## Base de datos 2: accounts.csv

Contiene información descriptiva de clientes y cuentas comerciales.

| Variable | Descripción | Tipo de dato | Rango/Valores posibles | Fuente de datos |
| --- | --- | --- | --- | --- |
| account | Nombre de la cuenta o cliente | Categórico | Nombre de empresas | CRM Sales Opportunities Dataset |
| sector | Sector económico del cliente | Categórico | Retail, Technology, Finance, etc. | CRM Sales Opportunities Dataset |
| year_established | Año de fundación de la empresa | Numérico | Años válidos | CRM Sales Opportunities Dataset |
| revenue | Ingresos estimados de la empresa | Numérico | Valores monetarios | CRM Sales Opportunities Dataset |
| employees | Número de empleados | Numérico | Valores enteros positivos | CRM Sales Opportunities Dataset |
| office_location | Ubicación de oficinas del cliente | Categórico | Ciudades o regiones | CRM Sales Opportunities Dataset |
| subsidiary_of | Empresa matriz o subsidiaria | Categórico | Nombre de empresa | CRM Sales Opportunities Dataset |

- **Variable**: nombre de la variable.
- **Descripción**: breve descripción de la variable.
- **Tipo de dato**: tipo de dato que contiene la variable.
- **Rango/Valores posibles**: rango o valores que puede tomar la variable.
- **Fuente de datos**: fuente de los datos de la variable.

---

## Base de datos 3: sales_teams.csv

Contiene información relacionada con equipos y representantes comerciales.

| Variable | Descripción | Tipo de dato | Rango/Valores posibles | Fuente de datos |
| --- | --- | --- | --- | --- |
| sales_agent | Nombre del representante comercial | Categórico | Nombre del agente | CRM Sales Opportunities Dataset |
| manager | Gerente comercial asignado | Categórico | Nombre del manager | CRM Sales Opportunities Dataset |
| regional_office | Oficina regional asignada | Categórico | Regiones comerciales | CRM Sales Opportunities Dataset |

- **Variable**: nombre de la variable.
- **Descripción**: breve descripción de la variable.
- **Tipo de dato**: tipo de dato que contiene la variable.
- **Rango/Valores posibles**: rango o valores que puede tomar la variable.
- **Fuente de datos**: fuente de los datos de la variable.

---

## Base de datos 4: products.csv

Contiene información relacionada con los productos comercializados.

| Variable | Descripción | Tipo de dato | Rango/Valores posibles | Fuente de datos |
| --- | --- | --- | --- | --- |
| product | Nombre del producto | Categórico | Productos comerciales | CRM Sales Opportunities Dataset |
| series | Línea o categoría del producto | Categórico | Series comerciales | CRM Sales Opportunities Dataset |
| sales_price | Precio de venta del producto | Numérico | Valores monetarios positivos | CRM Sales Opportunities Dataset |

- **Variable**: nombre de la variable.
- **Descripción**: breve descripción de la variable.
- **Tipo de dato**: tipo de dato que contiene la variable.
- **Rango/Valores posibles**: rango o valores que puede tomar la variable.
- **Fuente de datos**: fuente de los datos de la variable.
