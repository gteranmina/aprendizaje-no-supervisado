# Aprendizaje No Supervisado

## Descripción

Este proyecto tiene como objetivo aplicar técnicas de **reducción de dimensionalidad** y **clusterización** para analizar y clasificar un conjunto de datos. Se implementaron dos métodos principales de reducción:

- **Isomap:** Se exploraron configuraciones variando el número de componentes (3, 5 y 7) y el número de vecinos (5 y 10).
- **MDS (Multidimensional Scaling):** Se evaluó utilizando diferentes números de componentes (3, 5 y 7).

Posteriormente, se aplicó el algoritmo de **K-Means** tanto en el espacio original de los datos como en cada uno de los espacios reducidos, probando diferentes números de clusters (k de 2 a 8). El objetivo fue comparar el desempeño de cada esquema de clasificación mediante métricas no supervisadas.

## Metodología

1. **Carga y Preprocesamiento:**
   - Se carga el dataset (en formato Excel) y se eliminan datos faltantes para asegurar la calidad del análisis.

2. **Reducción de Dimensionalidad:**
   - **Isomap:** Se implementó variando los parámetros `n_components` y `n_neighbors`, generando visualizaciones en subplots de los espacios reducidos.
   - **MDS:** Se aplicó para generar representaciones en diferentes dimensiones, permitiendo evaluar el desempeño gráfico.

3. **Clusterización y Evaluación:**
   - Se aplicó el algoritmo **K-Means** en el dataset original y en cada uno de los espacios reducidos.
   - Para cada configuración se calcularon métricas de validación, como el **Silhouette Score** y el **Davies-Bouldin Index**, que evalúan la cohesión interna de los clusters y la separación entre ellos.

## Resultados

Tras evaluar diversas configuraciones, se identificó que el **mejor esquema de clasificación** se obtuvo con:

- **Reducción de Dimensionalidad (Isomap):**
  - `n_components = 3`
  - `n_neighbors = 5`
- **Clusterización (K-Means):**
  - `k = 3 clusters`

### Métricas del Mejor Esquema

- **Silhouette Score:** 0.998868  
  _Indicador de una excelente separación y cohesión interna de los clusters._
- **Davies-Bouldin Index:** ≈ 0.0865  
  _Un índice bajo que señala una buena separación entre los clusters._

## Visualizaciones

El repositorio incluye gráficos que ilustran:

- Los espacios reducidos obtenidos mediante Isomap y MDS.
- La distribución de los clusters en cada configuración evaluada.
- Comparativas de las métricas (Silhouette Score y Davies-Bouldin Index) para identificar el esquema óptimo.

## Conclusiones

Este proyecto demuestra que combinar técnicas de reducción de dimensionalidad con algoritmos de clustering permite:
- Simplificar la estructura de datos complejos.
- Resaltar patrones y relaciones que no son evidentes en el espacio original.
- Determinar de manera efectiva el esquema óptimo para la clasificación no supervisada.

Es un ejemplo práctico de la aplicación de técnicas avanzadas de Machine Learning y Data Mining para extraer insights valiosos a partir de datos complejos.
