
## IIC3633 - Sistemas Recomendadores | 2021-2
Recomendación no personalizada, basada en feedback implícito y basada en contenido.

Profesor
- Ph.D. Denis Parra

Alumnos
- Víctor Tirreau - 17637171
- Diego Iruretagoyena - 14619164

Dataset: Anime Recommendation Database  [ Anime Recommendation Database]( https://www.kaggle.com/hernan4444/)

El contenido de este repo se presenta con los siguientes componentes:

## RST01.ipynb
Contiene código ejecutado con la siguiente estructura

- [X] [Set-up inicial](#set)
- [X] [Actividad 1: Exploración de Datos](#ac01)
- [X] [Actividad 2: Recomendación no personalizada](#ac02)
- [X] [Actividad 3: Recomendación basada en feedback implícito](#ac03)
- [X] [Actividad 4: Recomendación basada en contenido](#ac04)
- [X] [Actividad 5: Comparación de métodos](#ac05)
- [X] [Actividad 6: Ejemplos de recomendación](#ac06)

## models_results
- PCA_results.csv
- random_results.csv
- most_popular_results.csv
- BPR_results.csv
- ALS_results.csv

Los resultados de cada método fueron guardados en archivos CSV luego de ser procesados, con el fin de guardar los cómputos finales y no tener que reprocess en cada iteración.

## final_recommendations

Esta carpeta contiene un archivo JSON que contiene las recomendaciones obtenidas luego de aplicar el mejor método recomendador a todos los usuarios en test.csv

## Informe.PDF
Documento PDF descriptivo acerca de los resultados obtenidos

## imgs
Esta carpeta contiene todas las imágenes de los gráficos que obtuvimos al evaluar los métodos.


## RST01 versión Colab
Este trabajo puede encontrarse en mejor formato en un  [Google Colab](https://colab.research.google.com/drive/1fwjehmsehLo-4_wcujF3lWlnpRuquNEZ?usp=sharing)


## Acerca de los datos

## **animelist.csv** 

has the list of all animes register by the user with the respective score, watching status and numbers of episodes watched. This dataset contains 109 Million row, 17.562 different animes and 325.772 different users. 

The file have the following columns:
- user_id: non identifiable randomly generated user id.
- anime_id: MyAnemlist ID of the anime. (e.g. 1).
- score: score between 1 to 10 given by the user. 0 if the user didn't assign a score. (e.g. 10)
- watching_status: state ID from this anime in the anime list of this user. (e.g. 2)
- watched_episodes: numbers of episodes watched by the user. (e.g. 24)


## **watching_status.csv** 

describe every possible status of the column: "watching_status" in animelist.csv.

## **rating_complete.csv**

is a subset of animelist.csv. This dataset only considers animes that the user has watched completely (watching_status==2) and gave it a score (score!=0). This dataset contains 57 Million ratings applied to 16.872 animes by 310.059 users. 

This file have the following columns
- user_id: non identifiable randomly generated user id.
- anime_id: - MyAnimelist ID of the anime that this user has rated.
- rating: rating that this user has assigned.


## **anime.csv**

contains general information of every anime (17.562 different anime) like genre, stats, studio, etc. This file have the following columns:

- MAL_ID: MyAnimelist ID of the anime. (e.g. 1)
- Name: full name of the anime. (e.g. Cowboy Bebop)
- Score: average score of the anime given from all users in MyAnimelist database. (e.g. 8.78)
- Genres: comma separated list of genres for this anime. (e.g. Action, Adventure, Comedy, Drama, Sci-Fi, Space)
- English name: full name in english of the anime. (e.g. Cowboy Bebop)
- Japanese name: full name in japanses of the anime. (e.g. カウボーイビバップ)
- Type: TV, movie, OVA, etc. (e.g. TV)
- Episodes': number of chapters. (e.g. 26)
- Aired: broadcast date. (e.g. Apr 3, 1998 to Apr 24, 1999)
- Premiered: season premiere. (e.g. Spring 1998)
- Producers: comma separated list of produducers (e.g. Bandai Visual)
- Licensors: comma separated list of licensors (e.g. Funimation, Bandai Entertainment)
- Studios: comma separated list of studios (e.g. Sunrise)
- Source: Manga, Light novel, Book, etc. (e.g Original)
- Duration: duration of the anime per episode (e.g 24 min. per ep.)
- Rating: age rate (e.g. R - 17+ (violence & profanity))
- Ranked: position based in the score. (e.g 28)
- Popularity: position based in the the number of users who have added the anime to their list. (e.g 39)
- Members: number of community members that are in this anime's "group". (e.g. 1251960)
- Favorites: number of users who have the anime as "favorites". (e.g. 61,971)
- Watching: number of users who are watching the anime. (e.g. 105808)
- Completed: number of users who have complete the anime. (e.g. 718161)
- On-Hold: number of users who have the anime on Hold. (e.g. 71513)
- Dropped: number of users who have dropped the anime. (e.g. 26678)
- Plan to Watch': number of users who plan to watch the anime. (e.g. 329800)
- Score-10': number of users who scored 10. (e.g. 229170)
- Score-9': number of users who scored 9. (e.g. 182126)
- Score-8': number of users who scored 8. (e.g. 131625)
- Score-7': number of users who scored 7. (e.g. 62330)
- Score-6': number of users who scored 6. (e.g. 20688)
- Score-5': number of users who scored 5. (e.g. 8904)
- Score-4': number of users who scored 4. (e.g. 3184)
- Score-3': number of users who scored 3. (e.g. 1357)
- Score-2': number of users who scored 2. (e.g. 741)
- Score-1': number of users who scored 1. (e.g. 1580)

