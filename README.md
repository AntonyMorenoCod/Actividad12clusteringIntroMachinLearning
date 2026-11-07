# Actividad semana 11

Trabajo académico de Introducción al Machine Learning sobre tres métodos de agrupamiento no supervisado: K-Means, DBSCAN y clustering jerárquico aglomerativo.

## Objetivo

Aplicar y analizar algoritmos de clustering, justificando el preprocesamiento, la selección de hiperparámetros y la interpretación de los resultados mediante métricas y visualizaciones.

## Contenido del repositorio

El repositorio contiene tres notebooks:

- **K-Means con Wine:** exploración y estandarización de datos, evaluación de K entre 2 y 6, selección de tres clústeres y análisis de sus características.
- **DBSCAN con dos medias lunas:** generación de datos, comparación de cinco configuraciones y selección de dos clústeres con eps = 0,30 y min_samples = 5.
- **Clustering jerárquico con Iris:** construcción del dendrograma con enlace de Ward, selección de dos clústeres y análisis de resultados. Al final se incluye la comparación de los tres algoritmos.

Los notebooks se encuentran en la carpeta principal del repositorio.

## Datos utilizados

- **Wine:** 178 observaciones y 13 variables, disponible mediante `sklearn.datasets.load_wine`.
- **Dos medias lunas:** 500 observaciones generadas con `make_moons`, usando `noise=0.07` y `random_state=42`.
- **Iris:** 150 observaciones y 4 variables, disponible mediante `sklearn.datasets.load_iris`.

No es necesario descargar archivos de datos adicionales. Las etiquetas originales no se utilizan para construir los clústeres.

## Herramientas y librerías

Los ejercicios se desarrollaron en Python mediante Google Colab y utilizan:

- pandas
- NumPy
- Matplotlib
- scikit-learn
- SciPy

## Ejecución en Google Colab

1. Descargar el notebook que se desea ejecutar desde este repositorio.
2. Abrir Google Colab y seleccionar **Archivo → Subir notebook**.
3. Seleccionar el archivo descargado.
4. Ejecutar las celdas en orden desde el inicio.

Cada notebook debe ejecutarse de forma independiente. Si falta alguna dependencia, ejecutar esta instrucción en una celda de código:

```python
%pip install pandas numpy matplotlib scikit-learn scipy
```

## Resultados principales

| Algoritmo | Dataset | Clústeres | Silhouette | Davies-Bouldin | Calinski-Harabasz |
|---|---|---:|---:|---:|---:|
| K-Means | Wine | 3 | 0,2849 | 1,3892 | 70,9400 |
| DBSCAN | Dos medias lunas | 2 | 0,3857 | 1,0215 | 433,8817 |
| Jerárquico con Ward | Iris | 2 | 0,5770 | 0,5917 | 240,2457 |

Las métricas corresponden a datasets diferentes y no permiten establecer una clasificación directa de los algoritmos. Las decisiones y limitaciones se explican en cada notebook.
