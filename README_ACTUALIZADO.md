
# Análisis de Presidentes de los Estados Unidos

Este repositorio contiene un análisis exploratorio de datos sobre los presidentes de los Estados Unidos, utilizando un archivo CSV con información relevante de cada mandato presidencial. El análisis se encuentra desarrollado en el archivo Jupyter Notebook `ProyectoDS_Parte_l_Fernandez_final.ipynb`, el cual se puede ejecutar de manera interactiva en Google Colab (liga más abajo).

## 📊 Contenido del análisis

El notebook incluye los siguientes componentes clave:

### 1. Carga y limpieza de datos

Se lee el archivo `us_presidents 2.csv` que contiene datos como:
- Nombre del presidente
- Fecha de inicio y fin del mandato
- Vicepresidente
- Partido político
- Cargo anterior
- Duración del mandato

Se detectaron valores especiales como `"--"` para fechas abiertas (por ejemplo, el presidente actual), y se manejaron adecuadamente como valores nulos (`NaT`) para evitar errores en la conversión de fechas.

También se realizaron limpiezas textuales para eliminar dobles espacios y referencias de tipo `[13]` en los nombres de partidos.

### 2. Cálculo de duración de mandatos

Se calculó la duración de cada mandato presidencial en años, lo cual permite realizar análisis comparativos entre distintos presidentes o periodos históricos.

### 3. Visualizaciones

Se generan gráficos que ilustran aspectos relevantes como:
- Distribución de duración de los mandatos
- Agrupación por partidos políticos
- Evolución histórica del poder en Estados Unidos

Estas visualizaciones permiten observar patrones históricos, tendencias y anomalías a lo largo de más de 200 años de historia política en EE. UU.

### 4. Análisis descriptivo

Además de los gráficos, se presentan resúmenes estadísticos básicos que describen la centralidad y dispersión de las variables cuantitativas.

## 🚀 Cómo usar este notebook en Google Colab

Haz clic en la siguiente liga para abrir y ejecutar el notebook en Google Colab:

[![Abrir en Colab](https://colab.research.google.com/assets/colab-badge.svg)]
([https://colab.research.google.com/github/KarlaFdez/Entregable-Data-Science-I/blob/main/ProyectoDS_Parte_l_Fernandez_final.ipynb])

## 📁 Archivos incluidos

- `ProyectoDS_Parte_l_Fernandez_final.ipynb`: Notebook con el análisis completo
- `us_presidents 2.csv`: Datos de entrada en formato tabular
- `README.md`: Descripción del proyecto


### 5. Clasificación de duración del mandato

Se creó una variable categórica (`mandate_class`) que clasifica a los presidentes según la duración de su mandato:

- `short`: menos de 4 años
- `medium`: entre 4 y 6 años
- `long`: más de 6 años

Se entrenó un modelo de clasificación usando `RandomForestClassifier` con las variables `party`, `prior` y `vice`. El modelo obtuvo una precisión global del 55.6% en un conjunto de prueba. A pesar de su simplicidad, ilustra cómo aplicar técnicas de Machine Learning a datos históricos.

Se usaron herramientas como:

- `LabelEncoder` para codificar variables categóricas.
- `SelectKBest` para selección de características.
- `classification_report` y `confusion_matrix` para evaluación del modelo.

Este análisis puede ampliarse incluyendo más variables que representen el contexto político o social de cada mandato.


## 🧠 Conclusión

Este proyecto demuestra cómo aplicar técnicas de análisis exploratorio de datos (EDA) para estudiar figuras históricas y extraer información relevante a partir de datos estructurados. Puede ser extendido con más variables (como políticas públicas, desempeño económico o popularidad) para generar estudios más profundos sobre el liderazgo en Estados Unidos.


Elaborado por: Karla Fernández
