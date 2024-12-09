# Clasificación y recomendación de canciones en base a las emociones de parte de Usuarios de Spotify con Machine Learning


## Índice
- [Introducción](#introducción)
  - [Métodos Utilizados](#métodos-utilizados)
  - [Tecnologías](#tecnologías)
- [Descarga y Configuración](#descarga-y-configuración)
  - [Requisitos Previos](#requisitos-previos)
  - [Cómo Ejecutar](#cómo-ejecutar)
- [Declaración del Problema](#declaración-del-problema)
  - [Objetivo Comercial](#objetivo-comercial)
  - [Preparación de Datos](#preparación-de-datos)
  - [Construcción y Evaluación del Modelo](#construcción-y-evaluación-del-modelo)
  - [Conclusiones](#conclusiones)


---


## Introducción


La **Clasificación y recomendación de canciones en base a las emociones de parte de Usuarios de Spotify con Machine Learning** Es un proyecto basado en técnicas de aprendizaje automático (ML) diseñado para predecir la emoción que siente el ser humano al escuchar las canciones. 


### Métodos Utilizados


- **Modelos de Clasificación**: Modelos supervisados K-Means.
- **Evaluación**: Métricas como precisión, recall, F1-score.


### Tecnologías


Este proyecto utiliza las siguientes tecnologías:
- **Python**: Lenguaje principal de desarrollo.
- **Bibliotecas**:
  - `scikit-learn`
  - `Matplotlib`
  - `pandas`
  - `numpy`
  - `optuna`
  - `API Spotify`


- **Entorno de ejecución**: Jupyter Notebook o cualquier IDE compatible con Python.


---


## Descarga y Configuración


### Requisitos Previos


1. Clonar este repositorio


```
git clone <GITHUB_REPO_URL>
```


2. Abra el archivo notebook ** *.ipynb** en Anaconda.


## Declaración del problema


### Objetivo Comercial


Diseñar e implementar un sistema de clasificación de emociones que identifique y prediga la emoción asociada a una canción específica de Spotify, basada en características de audio y patrones de escucha del usuario. 
Este sistema se usará para agrupar canciones en diferentes categorías emocionales, ayudando a Spotify (o cualquier otra plataforma de música) a recomendar canciones que se alineen mejor con el estado de ánimo del usuario en un momento determinado.


### Preparación de Datos
1. En este proyecto se utilizaron 2 datasets que fueron combinados con el objetivo de desarrollar un sistema para la clasificación y recomendación de canciones basado en las emociones de los usuarios de Spotify.
- Spotify dataset:  Este dataset contiene información relacionada con las canciones de Spotify. Consta de 24 columnas y 20,595 registros, cada uno representando una canción. Entre las columnas más importantes se encuentran: danceability (danzabilidad), energy (energía), loudness (nivel de ruido), speechiness (presencia de canto o elementos hablados), acousticness (probabilidad de ser acústica), instrumentalness (presencia de elementos instrumentales), liveness (sensación de estar en vivo), valence (positividad emocional), tempo (velocidad del ritmo) y duration_min (duración en minutos).
- Positive Affirmations Dataset: Contiene información relacionada con afirmaciones positivas y sus respectivas emociones. Consta de las siguientes columnas principales: Affirmaton (contenido textual de la afirmacion) y Tag (Categoria o emocion asociada a la afirmacion, como love, happiness, etc).


2. El proyecto está diseñado en 2 etapas: Clasificador de emociones para enriquecer preferencias musicales, Clasificador de emociones para música escuchada en el historial reciente


### Construcción y Evaluación del Modelo


Una vez obtenidos los datos mediante el proceso de ETL, se realiza un análisis
PCA. De forma exploratoria se muestra al usuario la varianza que explica dada
componente principal. Luego se presenta un gráfico biplot con las dos primeras
componentes principales, y vectores que muestran las cargas de las distintas variables.
Los vectores de mayor módulo son aquellos que mayormente contribuyen a generar las componentes. De esta forma se provee una primera aproximación donde intuitivamente el usuario ve cuales son las características que mejor clasifican las canciones que escucha, generando foco en las variables más importantes. Finalmente, se le presentan al usuario los nombres de estas variables.
Una vez realizado este primer análisis de PCA, se evalúan los agrupamientos que se generan aplicando primero KMeans y luego SOM. Se hace un ajuste de
hiperparámetros para buscar la configuración que mejores resultados provea. En el caso de KMeans se prueba con distintos números de clusters. En el de SOM con distintas dimensionalidades de matriz.


## Conclusiones


El trabajo cumplió con el objetivo general, de desarrollar una herramienta que permite a un usuario de Spotify conocer mejor los patrones de música que escucha. Se provee una interfaz que permite comprender cómo se agrupan las canciones y qué variables son las que mayormente contribuyen a estos agrupamientos.




### Futuras mejoras incluyen:
- Obtener una base de datos diferente que consiga marcar otro tipo de emociones como ser triste o relajado.
- Se podría probar el mantener más descriptores de cada audio de la base de datos, al tener más información se podría estudiar el comportamiento a la hora de clasificar las emociones y comprobar la existencia de mejoras en la recomendación. 



