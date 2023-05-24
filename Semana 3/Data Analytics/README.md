# <h1 align="center">:mag: Informe de análisis de datos :bar_chart: </h1>

## Tabla de contenidos
* [Introducción](#Introducción)
* [Proceso preliminar](#Proceso-preliminar)
* [Dashboard](#Dashboard)

## Introducción
El siguiente análisis de los flujos migratorios en Latinoamérica y Estados Unidos es el resultado del trabajo de las semanas anteriores donde se recopilaron y transformaron datos de gran valor para poder mostrarlos en una visualización sobre los flujos migratorios en Latinoamérica y Estados Unidos, junto con el análisis de las posibles razones que motivan a las personas a migrar, y cómo influyen en esta decisión los factores económicos y la calidad de vida de las personas en su país de origen.

En este análisis trabajaremos los siguientes Indicadores clave de Rendimiento (**KPIs**):
1. Variación de la tasa de migración neta en Estados Unidos por año
2. Variación anual de la Migración neta por país
3. Relación del PIB entre países de Latinoamérica y Estados Unidos, por año
4. Diferencia porcentual entre las Remesas y el PIB per cápita por país y año
5. Variación del % de Desempleo entre países de Latinoamérica y Estados Unidos, por año
6. Variación del índice de felicidad entre países y Estados Unidos en el año 2021

Con el presente dashboard nuestra intensión es disponibilizar la información trabajada en este proyecto a nuestros clientes, gobiernos y toda persona que tenga la intención de migrar en Latinoamérica y Estados Unidos.

## Proceso preliminar
Una vez los datos fueron procesados y cargados AWS S3 los conectamos con Power Bi para usar las tablas. Se aplico cierta limpieza a cada tabla para normalizarlas y que su uso fuera más eficiente, quedando los datos divididos en los tablas:
+ datos de migración (datos_migración)
+ datos de calidad de vida (datos_felicidad)

## Dashboard
Para la creación del Dashboard se utilizó el software PowerBI, donde se creó una portada, una página informativa sobre los KPIs abordados en el dashboard y 4 páginas interactivas, enfocadas en los datos de migración, los posibles factores decisivos a la hora de migrar, datos sobre la economía y la calidad de vida.

**_Dashboard Migración:_**
Esta dashboard interactivo muestra la Migración neta (Inmigración - Emigración) en los países estudiados, se puede filtrar la información por país y año; y se muestran los KPIs 1 y 2 que nos ayudan a comprender la variación en la migración de Estados Unidos y de cada país de Latinoamérica.
Los Kpis tanto 1 como el 2, nos son de gran importancia porque  partir de un análisis con esos datos nos ayudaría a entender y poder establecer una tendencia de cada país, y que mejor si se lo puede comparar de manera porcentual con el país que adoptamos como  base a nuestro estudio, que en este caso es Estados Unidos
<p align="center">
   <img width="800" height="450" src="img/dashboard_migracion.png">
   </p>

**_Dashboard Factor decisivo:_**
Esta dashboard resume las principales factores que pueden motivar la migración de un país de origen, como son: _la percepción de la corrupción, la libertad de tomar decisiones vitales y el PIB per cápita_ de cada país.
En este tablero es uno de los más importantes para poder entender el origen de la migración, ya que para empezar a relacionar los datos en sus respectivas gráficas, primero se necesita conocer los datos y que representan para luego recién poder interpretar el valor de las comparaciones. También es para destacar que con la infomación proporcionada en este tablero se puede sacar algunas conclusiones en respecto del origen de la decisión de los migrante, para ello tenesmos que comparar con las teorías de Charles Henry Dow en su teoría de tendencia y la  teoría de  Vilfredo Pareto con su ley del 70 - 30, e nos cuenta que aproximadamente el 70% de los resultados se deben al 30% de las causas.
<p align="center">
   <img width="800" height="450" src="img/dashboard_factor decisivo.png">
   </p>

**_Dashboard Economía:_**
Este dashboard resume la relevancia queda más notoria luego de poder explicar el tablero anterior podemos destacar a la parte económica como la razón más importante para migrar, y aunque estemos todos de acuerdo que no es la única, si es importante destacar que en gran medida las decisiones pasan  por ese lado.
<p align="center">
   <img width="800" height="450" src="img/dashboard_economia.png">
   </p>

**_Dashboard Calidad de Vida:_**
Este dashboard expresa la relevancia que posee temas que no están vinculados a la parte económica y que si condiciona el origen de la migración de una manera decisiva. Lo cierto es que podemos tratar de entender las cosas así, como en economía nos hablaban del Ceteris Paribus que se utiliza para analizar algo de manera independiente, dejando todo lo demás constante, y aunque esto puede ser muy útil a la hora de aprender sobre un tema, a la hora de tomar decisiones al partir de eso sería un error muy grande, ya que si se cambia un valor una formula todo lo demás se cambia. 
<p align="center">
   <img width="800" height="450" src="img/dashboard_calidad de vida.png">
   </p>
