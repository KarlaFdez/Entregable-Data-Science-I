# Análisis de Presidentes de los Estados Unidos

Este repositorio contiene un análisis exploratorio de datos sobre los presidentes de los Estados Unidos, utilizando un archivo CSV con información relevante de cada mandato presidencial. El análisis se encuentra desarrollado en el archivo Jupyter Notebook `ProyectoDS_Parte_l_Fernandez_final.ipynb`, el cual se puede ejecutar de manera interactiva en Google Colab (liga más abajo).
El presente análisis explora un conjunto de datos históricos que documenta a los presidentes de los Estados Unidos desde George Washington hasta periodos más recientes. El dataset contiene información relevante como el nombre del presidente, su período de mandato, el vicepresidente correspondiente, el partido político al que pertenecía y el cargo que ocupaban antes de asumir la presidencia. Este análisis busca no solo describir los datos, sino también extraer patrones históricos, hacer comparaciones entre partidos y evaluar trayectorias profesionales comunes antes de asumir la presidencia.
Entre los aspectos más destacados se encuentra la evolución del sistema bipartidista en los Estados Unidos, la duración promedio de los mandatos, y la relación entre los cargos ocupados previamente y la probabilidad de llegar a la presidencia. Asimismo, se realiza una caracterización de los partidos políticos predominantes a lo largo del tiempo, observando su permanencia o desaparición del sistema político estadounidense.
La metodología utilizada incluye análisis univariados, bivariados y multivariados. Para la interpretación de los datos se hace uso de estadísticas descriptivas como promedios, frecuencias y distribuciones, así como de visualizaciones gráficas para facilitar la comprensión de los patrones subyacentes.
Este análisis permite responder a preguntas como: ¿Cuál ha sido el partido político más común entre los presidentes? ¿Qué cargos previos son más comunes antes de asumir la presidencia? ¿Cuánto duran los mandatos en promedio? ¿Hay una relación entre el partido y la duración del mandato?
Finalmente, el propósito principal es proveer una visión comprensiva y visualmente intuitiva sobre las características históricas y políticas de los presidentes de los Estados Unidos, apoyando tanto fines educativos como de investigación histórica.

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

### 2. Cálculo de duración de mandatos, se hicieron preguntas y se establecieron hipótesis

Se calculó la duración de cada mandato presidencial en años, lo cual permite realizar análisis comparativos entre distintos presidentes o periodos históricos.

Preguntas:
¿Cuál ha sido el partido político más frecuente entre los presidentes?
¿Cuál es la duración promedio de los mandatos presidenciales?
¿Qué cargos previos al mandato presidencial son más comunes?
¿Existen diferencias en la duración del mandato según el partido político?

Hipótesis:
H1: El partido con mayor número de presidentes ha sido el Republicano o el Demócrata.
H2: Los presidentes con experiencia previa como Vicepresidente tienen mandatos más largos.
H3: La duración promedio de los mandatos es de aproximadamente 8 años (2 periodos).
H4: Los partidos históricos como el Federalista o el Demócrata-Republicano tuvieron menos permanencia que los actuales.

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
