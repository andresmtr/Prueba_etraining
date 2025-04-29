# Prueba_etraining

# Análisis de Ventas y Efecto de Lluvias

Este proyecto realiza un proceso completo de ETL, análisis exploratorio y modelado predictivo para entender y predecir el comportamiento de las ventas considerando, entre otros factores, datos meteorológicos (lluvia) obtenidos de sensores.

## Estructura

* 1_get_data.ipynb: Extracción y transformación de datos desde bases MySQL y MongoDB.
* 2_ETL_model.ipynb: Procesamiento adicional, exploración de datos, entrenamiento de modelos de predicción y análisis de resultados.

1. Objetivo

El objetivo principal es predecir la cantidad de ventas en función de:

Características de los productos.
Información de tiendas (región, tamaño, empleados).
Factores climáticos (lluvia, ubicación de sensores).
Se realiza una combinación de fuentes de datos y se entrena múltiples modelos de regresión para encontrar el mejor predictor.

2. Requisitos

Python 3.8 o superior
Librerías:
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
pymongo
geopy
shap
joblib
Instalar dependencias:

pip install pandas numpy matplotlib seaborn scikit-learn xgboost pymongo geopy shap joblib


3. Instalación y Ejecución

Clonar el repositorio.
Ejecutar 1_get_data.ipynb para:
Conectar a bases de datos MySQL y MongoDB.
Extraer información de productos, tiendas, ventas y sensores meteorológicos.
Procesar y unir la información en un solo dataset (all_data.csv).
Ejecutar 2_ETL_model.ipynb para:
Realizar limpieza y transformación de datos.
Aplicar análisis exploratorio (EDA).
Entrenar modelos predictivos.
Evaluar modelos y seleccionar el mejor.
Analizar importancia de variables usando SHAP.

4. Modelos Entrenados

Se compararon los siguientes modelos:

Linear Regression
Decision Tree Regressor
Random Forest Regressor
XGBoost Regressor
Random Forest Regressor obtuvo el mejor desempeño en R².

5. Principales Análisis Realizados

Distribución de lluvias
Relación lluvia vs tipo de venta
Relación ventas vs características de tienda
Correlación entre variables numéricas
Importancia de variables en la predicción usando SHAP

6. Resultados y Conclusiones

La variable "lluvia" impacta moderadamente en las ventas.
El modelo Random Forest logra capturar mejor las relaciones no lineales entre variables.
La cantidad de empleados y el tamaño de la tienda también son variables relevantes.
La información meteorológica mejoró ligeramente la capacidad predictiva.
