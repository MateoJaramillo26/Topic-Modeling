# Modelado de Tópicos con Detección de Comunidades

Este repositorio contiene un notebook de Jupyter que implementa un enfoque de modelado de tópicos utilizando grafos y detección de comunidades con el algoritmo Louvain. Se comparan dos medidas de similitud: coseno y euclidiana. El objetivo es identificar tópicos en un conjunto de datos de reseñas de aplicaciones, evaluar su calidad y decidir cuál medida produce mejores resultados.

## Descripción

El notebook explora técnicas de procesamiento de lenguaje natural (NLP) para extraer tópicos de reseñas de usuarios. Utiliza vectorización TF-IDF, construcción de grafos basados en similitudes, detección de comunidades y métricas de evaluación como modularidad y coherencia. Al final, se determina la mejor medida de similitud basada en resultados cuantitativos y cualitativos.

## Requisitos

- Python 3.8+
- Librerías requeridas (instalar con `pip install -r requirements.txt`):
  - pandas
  - numpy
  - networkx
  - scikit-learn
  - python-louvain
  - IPython

## Instalación

1. Clonar el repositorio:
   ```
   git clone https://github.com/tu-usuario/topic-modeling-repo.git
   cd topic-modeling-repo
   ```

2. Instalar las dependencias:
   ```
   pip install -r requirements.txt
   ```

3. Descargar el dataset `reviews.csv` (no incluido; asegurarse de tenerlo en el directorio raíz).

## Uso

1. Abrir el notebook:
   ```
   jupyter notebook TopicModeling.ipynb
   ```

2. Ejecutar las celdas secuencialmente para cargar datos, construir grafos, detectar comunidades, visualizar resultados y evaluar.

## Estructura del Notebook

### Paso 1: Importar Librerías y Cargar Datos
- Cargar el dataset de reseñas y verifica el total de entradas.

### Paso 2: Preprocesamiento y Construcción de Grafos
- Vectorización TF-IDF de las reseñas.
- Cálculo de matrices de similitud (coseno y euclidiana).
- Construcción de grafos y detección de comunidades con Louvain.
- Análisis de clusters, incluyendo palabras top y coherencia.

### Paso 3: Visualización de Tópicos
- Tablas coloreadas para mostrar tópicos y descripciones por medida de similitud.

### Paso 4: Evaluación y Comparación
- Cálculo de modularidad.
- Comparación de número de tópicos, modularidad y coherencia promedio.
- Discusión sobre interpretabilidad y separación de clusters.

### Paso 5: Decisión Final
- Selección de la mejor medida de similitud basada en métricas.
- Justificación con énfasis en modularidad, coherencia e interpretabilidad.

## Resultados Esperados
- Tópicos identificados como "practical, learning, environment" (ejemplo de usabilidad de apps).
- Comparación muestra que una medida (p.ej., coseno) suele superar en modularidad y coherencia.
