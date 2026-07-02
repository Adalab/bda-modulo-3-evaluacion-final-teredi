# Análisis de Datos de Clientes de Aerolínea

## Descripción del proyecto

Este proyecto se centra en el análisis de datos de clientes de una aerolínea. El objetivo es analizar y comprender su situación y comportamiento para ver los factores que influyen en su fidelizacion a la aerolinea.

## Datasets utilizados

El proyecto parte de dos datasets originales que se combinan en un tercero:

- **`df_custflight`** (Customer Flight Analysis): registro mensual de vuelos por cliente. Cada cliente puede aparecer varias veces (una fila por mes).
- **`df_custloyalty`** (Customer Loyalty History): datos únicos por cliente, incluyendo variables como `Education`, `Salary` y `CLV`. Cada cliente aparece una sola vez.
- **`df_customer`**: resultado de unir ambos datasets mediante la columna común `Loyalty Number`.

## Metodología

### 1. Exploración inicial de los datos, limpieza y transformación

- Búsqueda de registros duplicados en ambos datasets.
- Comprobación de valores nulos por columna, identificando patrones (por ejemplo, en la columna `Salary`).
- Revisión de las columnas categóricas (`Education`, entre otras), incluyendo el conteo de categorías y su distribución.

### 2. Unión de los datasets

- Unión de `df_custflight` y `df_custloyalty` mediante `merge()`, usando `Loyalty Number` como clave de unión, para generar `df_customer`.
- Verificación de la coherencia entre ambos datasets antes de la unión (número de clientes únicos en cada tabla).

### 3. Análisis estadístico

- **Variables numéricas**: cálculo de media, mediana, moda, varianza, desviación estándar, coeficiente de variación, mínimo, máximo y rango para las principales variables (`Salary`, `CLV`, `Flights Booked`, entre otras). Detección de valores atípicos (outliers).
- **Variables categóricas**: análisis de frecuencias y distribución por categoría (por ejemplo, `Education`).

### 4. Visualización

- Generación de gráficos (boxplots, gráficos de tarta, barsplot, etc.) para responder a las preguntas planteadas en el ejercicio.

## Herramientas y librerías

- **Python**
- **Jupyter Notebook**
- **Pandas** 
- **Numpy**
- **Matplotlib**
- **Seaborn** 

## Autora: 
Teresa Diaz-Toledo Fernandez

