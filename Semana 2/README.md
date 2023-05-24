<h1 align="center"> Data engineering </h1>

# Tabla de contenidos
* [Introducción](#Introducción)
* [Tecnologías a usar](#Tecnologías-a-usar)
* [Flujo de trabajo](#Flujo-de-trabajo)
* [Modelo ER](#Modelo-ER)

# Introducción
Esta semana trabajaremos las áreas que involucran al data engineering, tenemos el desafío de crear un Data Warehouse completamente funcional que sea accesible tanto para el área de Analitycs como para el área de Machine Learning. Además, debemos tener nuestra base de datos en AWS S3 e implementar transformaciones a nuestros datos para la consulta de ellos.

# Tecnologías a usar  
+ **_AWS S3:_** es una plataforma en la nube que ofrece una variedad de servicios,tales como los recursos para poder almacenar la información y encargarse de proporcionar la capacidad de cómputo necesaria para brindar un servicio constante a la base de datos y al orquestador de datos, Airflow.
+ **_Python_** y **_pandas:_** mediante scripts se encargan de construir la estructura y aplicar los cambios necesarios para la extracción, limpieza y carga de los datos. 
+ **_Power BI:_**
+ **_Docker:_**
+ **_Airflow:_** se encarga de la automatización del proceso de ETL que mediante el uso de DAGs, se utiliza para automatizar tareas repetitivas y programar tareas en un horario específico.

# Flujo de trabajo
<p align="center">
   <img width="800" height="375" src="img/workflow.png">
   </p>

Nuestro flujo de trabajos consistió en:
*	Carga de datos: el código utilizado para la tarea de cargar datos presenta el siguiente orden de ejecución:
    -	Importar librerías necesarias para las tareas de carga y transformación de datos  
    -	Extracción de datos desde archivos CSV mediante la librería pandas. Utilizando funciones como ‘read_csv()’ para leer los archivos y convertirlos en dataframes.
*	Extracción de datos: El origen de los datos proviene de 8 archivos CSV, los que han sido extraídos previamente de sitios web de datos mundiales (Banco Mundial, World Happiness Record).
*	Ingesta de datos: utilizando la librería Boto3 de Python, los datos extraídos se carga en el servicio de almacenamiento AWS S3. Esta interfaz nos permite interactuar con el servicio de AWS, permitiéndonos cargar datos en S3 de forma programática.
*	Proceso de Transformación: durante la etapa de transformación se aplicaron diversas acciones para preparar los datos para su uso, las que incluyeron:
    -	Revisar y manejar los valores nulos y duplicados 
    -	Filtrar columnas por nombre de país y años de interés (2000-2021).
    -	Eliminación de columnas que no contengan valores relevantes para el análisis
    -	Filtrar filas por nombre de países de interés (Estados Unidos, México, Guatemala, Honduras, El Salvador, Colombia, Chile, Argentina, Brasil, Uruguay)
*	Carga de datos transformados: una vez los datos han sido transformados según el paso anterior, se exportan a un archivo CSV para su posterior carga en AWS S3 para su almacenamiento en el bucket de consulta.

Esta arquitectura de datos implica la carga de datos desde archivos CSV, su transformación mediante operaciones de limpieza y filtrado, para finalizar en una carga de los datos transformados a AWS S3. 

## *Video demostrativo*
En el siguiente [link](https://drive.google.com/) se explica el flujo de datos con más detalle.

# Modelo ER
 <p align="center">
   <img width="600" height="465" src="img/modelo1.png">
   </p>

Nuestro modelo entidad relación es en forma de estrella, el cual se organiza en torno a una tabla central de hechos con los campos de Country Name (nombre del país) y Años comprendidos entre 2000 y 2021. Esta tabla de hechos se relaciona con las tablas dimensionales mediante la clave foránea. En este caso nuestra Primary Key (PK) seleccionada es el Nombre del país. 

Cada tabla dimensional del modelo contiene medidas numéricas de los indicadores sobre:
-	Migración (Migración neta)
-	Indicadores Económicos (Crecimiento del Producto Interno Bruto (% anual y % anual percápita, Porcentaje de Desempleo, Remesas e Índice de Gini)
-	Indicador de la Calidad de Vida (Índice de Felicidad)

Esta estructura de diseño de base de datos nos proporciona un enfoque simple, eficiente y comprensible para el análisis de datos.

## Diagrama Entidad Relación
 <p align="center">
   <img width="800" height="575" src="img/modelo2.png">
   </p>