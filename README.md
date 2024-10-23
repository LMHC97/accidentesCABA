![image](https://github.com/user-attachments/assets/d57a1692-5b76-42d7-819b-abd9b05c247d)>


# Análisis de mortalidad por accidentes de tránsito en la ciudad de Buenos Aires, Argentina. Años 2016-2021.
Este proyecto de análisis de datos busca proporcionar información valiosa sobre las muertes por accidentalidad vial en Buenos Aires, Argentina. El análisis de datos, el dashboard interactivo y los KPIs definidos permiten comprender mejor el problema y sirven como base para la toma de decisiones informadas que contribuyan a la mejora de la seguridad vial en la ciudad y a la reducción de las víctimas fatales por accidentes de tránsito.

## Disposición del repositorio de GitHub
El repositorio de GitHub contiene los siguientes archivos:
### Readme.md: 
Este archivo, que proporciona una descripción general del proyecto.
### ETL:
Cuaderno Jupyter que contiene el código Python utilizado para el proceso de extracción, transformación y limpieza de los datos.
### EDA:
Cuaderno Jupyter que contiene el código Python utilizado para el análisis exploratorio de datos.
### Datasets: 
Los archivos CSV con los datos procesados.
### Dashboard: 
El archivo .pbix del dashboard de Power BI.

## Proceso de Extracción, Transformación y Carga de datos (ETL)
El proceso de ETL (Extracción, Transformación y Carga) constituyó un pilar fundamental en la preparación de los datos de siniestros viales de la Ciudad Autónoma de Buenos Aires (CABA) para su posterior análisis. A partir de las bases de datos suministradas, se extrajo la información básica sobre los incidentes. Posteriormente, se llevó a cabo un riguroso proceso de transformación de los datos, que incluyó la eliminación de variables redundantes, la corrección de inconsistencias (como la eliminación de guiones o la estandarización de formatos) y la normalización de los nombres de las variables para garantizar coherencia. Un aspecto distintivo de este proceso fue la creación de un conjunto de datos georreferenciados que permitió analizar la distribución espacial de los siniestros, cuantificando los eventos por dirección geográfica y ajustando las coordenadas geográficas. Finalmente, los datos transformados fueron almacenados en nuevos archivos CSV, listos para ser utilizados en análisis más profundos.
El proceso ETL permitió obtener un conjunto de datos limpio, consistente y estructurado, que facilitó la realización de análisis más sofisticados y la generación de visualizaciones informativas. La creación de nuevas variables, como el conteo de accidentes por ubicación, enriqueció el conjunto de datos y permitió explorar patrones espaciales y temporales.

## Proceso EDA
Inicialmente, se importaron los conjuntos de datos "victimaslimpio.csv" y "homicidioslimpio.csv", obtenidos tras un riguroso proceso de ETL, utilizando las librerías de Python pandas y matplotlib.
### Análisis Descriptivo Univariado y Bivariado
Se llevó a cabo un análisis descriptivo detallado de las variables individuales y sus relaciones. Mediante la utilización de estadísticas descriptivas, tablas de frecuencia y visualizaciones como histogramas y diagramas de caja, se caracterizó la distribución de variables como la edad de las víctimas, el tipo de vehículo involucrado y la hora del día en que ocurrieron los siniestros. Además, se exploraron las relaciones entre variables pareadas a través de tablas de contingencia y gráficos de dispersión, identificando posibles asociaciones entre factores como la ubicación geográfica y la gravedad del siniestro.
![image](https://github.com/user-attachments/assets/fdf55899-7000-4ce9-9580-d425c32f7cb6)
![image](https://github.com/user-attachments/assets/aed2222b-bca0-4ce6-a83d-853fe7c123e0)
![image](https://github.com/user-attachments/assets/34ae5a4b-3598-48ae-87a8-675517bd7b93)
### Análisis Temporal y Espacial
Con el objetivo de comprender la evolución de los siniestros en el tiempo y su distribución espacial, se realizaron análisis específicos. Se identificaron patrones estacionales y tendencias a largo plazo en la ocurrencia de siniestros, así como eventos puntuales que pudieron haber influido en su frecuencia. Asimismo, se emplearon mapas de calor y técnicas de geovisualización para visualizar la concentración de siniestros en determinadas zonas de la ciudad y explorar posibles factores geográficos asociados.
![image](https://github.com/user-attachments/assets/4ecb8352-7788-4758-9c22-19f1e4f0cee4)
![image](https://github.com/user-attachments/assets/c349c1bc-f52b-4a3c-8c4e-2e9e3df09ac6)
![image](https://github.com/user-attachments/assets/f3fb5581-d913-45da-84a5-d667ab06771b)
![image](https://github.com/user-attachments/assets/6f77678e-2d21-42ec-9f80-cd0a0de82511)
![image](https://github.com/user-attachments/assets/aecf9a82-58b0-4e13-b419-3fccdb6b202a)
![image](https://github.com/user-attachments/assets/1d049348-9aac-4f70-a770-53bf7d1a2961)
![image](https://github.com/user-attachments/assets/53ee90e7-459d-40a4-b876-65defd76f9a4)
![image](https://github.com/user-attachments/assets/91d94721-dd2d-46d6-bba3-a310ea46e56b)
### Cálculo de Indicadores Clave de Desempeño (KPIs)
Para cuantificar la magnitud del problema y evaluar el impacto de las medidas de seguridad vial implementadas, se calcularon diversos indicadores clave de desempeño (KPIs). Entre ellos se destacan la tasa de mortalidad por siniestros viales, la evolución de los accidentes de motociclistas y la paridad de género en las víctimas. Estos KPIs permitieron realizar un seguimiento de la situación y comparar los resultados obtenidos con los objetivos establecidos.
KPIs
Se definieron tres Key Performance Indicators (KPIs) para medir el progreso en la reducción de víctimas fatales por accidentes de tránsito:
#### 1.Reducir en un 10% la tasa de homicidios en siniestros viales de los últimos seis meses, en CABA, en comparación con la tasa de homicidios en siniestros viales del semestre anterior.
Se definió la tasa de homicidios en siniestros viales como el número de víctimas fatales en accidentes de tránsito por cada 100,000 habitantes en un área geográfica durante un período de tiempo específico. Su fórmula es:
 $\text{Tasa de homicidios en siniestros viales} = \frac{\text{Número de homicidios en siniestros viales}}{\text{Población total}}\times 100,000$
 
El análisis de la tasa de homicidios en siniestros viales reveló una tendencia general a la baja a lo largo del periodo estudiado, aunque con fluctuaciones semestrales. La mayor disminución se observó en el primer semestre de 2020, coincidiendo con las restricciones por la pandemia. En el segundo semestre de 2021, se superó ampliamente la meta establecida, logrando una reducción del 23% en comparación con el semestre anterior. Esto indica la efectividad de las medidas implementadas. A pesar de estos resultados positivos, es crucial mantener una vigilancia constante y ajustar las estrategias de seguridad vial para consolidar esta tendencia decreciente.
#### 2.Reducir en un 7% la cantidad de accidentes mortales de motociclistas en el último año, en CABA, respecto al año anterior.
Su fórmula es: 
 $\text{Cantidad de accidentes mortales de motociclistas} = -\frac{\text{Víctimas moto año anterior - Víctimas moto año actual}}{\text{Víctimas moto año anterior}}\times 100$

El análisis de los accidentes mortales de motociclistas revela una tendencia fluctuante a lo largo de los años. Si bien se observó una disminución significativa en 2017 y 2019, seguida de un aumento considerable en 2021, el año 2020 presentó una reducción excepcional que podría atribuirse a las restricciones por la pandemia de COVID-19. Estos datos sugieren la necesidad de implementar estrategias de seguridad vial más robustas y sostenibles para prevenir futuros incrementos en el número de accidentes mortales de motociclistas
#### 3.Reducir en un 10% la disparidad entre el número de hombres y mujeres fallecidos en accidentes de tránsito durante el próximo año.
 Su fórmula es: 
 $\text{KPI3} = IF([Totalvictimashombres] <= [Objetivoreducciondisparidad], "Objetivo alcanzado", "Objetivo no alcanzado")$
 
El análisis de la mortalidad masculina en accidentes de tránsito revela una tendencia positiva y sostenida a la baja en los últimos años. A pesar de algunas fluctuaciones semestrales, se observa un descenso continuo en el número de fallecimientos, superando incluso el objetivo establecido para el segundo semestre de 2021. Estos resultados evidencian la efectividad de las estrategias implementadas para mejorar la seguridad vial entre hombres. Sin embargo, es fundamental mantener un monitoreo constante y evaluar nuevas acciones para consolidar esta tendencia positiva y reducir aún más las muertes por accidentes de tránsito en este grupo poblacional.

## Conclusiones
La Ciudad de Buenos Aires experimentó entre 2016 y 2021 un preocupante número accidentes viales con víctimas fatales. Estos siniestros, concentrados principalmente en días laborales y horarios de alta circulación, revelan un perfil de víctima predominantemente masculino y joven. Motociclistas y peatones fueron los más afectados, y las avenidas, especialmente en sus intersecciones, los escenarios más comunes. A pesar de algunos avances, como la reducción de la tasa de homicidios en el último semestre de 2021, persisten desafíos en materia de seguridad vial, particularmente en lo que respecta a motociclistas y a la infraestructura vial.

## Recomendaciones
La seguridad vial requiere un enfoque integral que combine la vigilancia y el control con la educación. Es necesario fortalecer las campañas de concientización, especialmente dirigidas a motociclistas y hombres jóvenes, enfatizando los riesgos asociados a conductas imprudentes. Asimismo, se deben mejorar las condiciones viales, especialmente en avenidas y cruces, para reducir la probabilidad de accidentes.
