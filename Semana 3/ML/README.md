# <h1 align="center"> Modelo de Machine Learning  </h1>

## Tabla de contenidos
* [Introducción](#Introducción)
* [Objetivos](#Objetivos)
* [Modelización](#Modelización)

## Introducción
Hemos desarrollado un sistema avanzado de análisis de datos que puede predecir con precisión las futuras tasas de desempleo y las tendencias de migración neta en varios países. Aprovechando el poder del aprendizaje automático, hemos creado un modelo que puede proporcionar información valiosa para la toma de decisiones y la planificación. Nuestro objetivo es poner esta compleja tecnología al alcance de personas como tú, aunque no tengas conocimientos de informática.

## Objetivos 
+ **_Predicciones fáciles de entender:_**
Nuestro modelo tiene en cuenta datos históricos y diversos indicadores para predecir tendencias futuras. Por ejemplo, tiene en cuenta factores como el crecimiento económico, la dinámica de la población y las tasas de empleo. Analizando estos patrones, nuestro modelo puede ofrecer una imagen clara de lo que nos depara el futuro en términos de tasas de desempleo y migración neta.
+ **_Interfaz fácil de usar:_**
Para garantizar la facilidad de uso de nuestra tecnología, hemos desarrollado una interfaz sencilla e intuitiva que permite interactuar con las predicciones. Nuestro sistema está desplegado en Streamlit, una plataforma fácil de usar que presenta la información en un formato fácilmente comprensible. Podrá visualizar las predicciones a través de gráficos claros y visualmente atractivos, lo que le permitirá comprender sin esfuerzo las perspectivas que le ofrece nuestro modelo de aprendizaje automático.
+ **_Ventajas para la toma de decisiones:_**
Al utilizar nuestro sistema, tendrá acceso a predicciones fiables sobre futuras tasas de desempleo y tendencias migratorias netas. Esta información puede ser de gran ayuda a la hora de tomar decisiones informadas y formular estrategias eficaces. Tanto si es usted un director general, un responsable político o alguien que busca información sobre estos importantes aspectos, nuestro modelo de aprendizaje automático le proporcionará los conocimientos que necesita.
+ **_Experiencia en la que puede confiar:_**
Nuestro equipo está formado por científicos de datos altamente cualificados especializados en aprendizaje automático y análisis predictivo. Con sus conocimientos y experiencia, hemos desarrollado un modelo robusto y preciso que ha sido ampliamente probado. Tenemos un historial probado de predicciones fiables y conocimientos prácticos para nuestros clientes.

## Modelización de las futuras tasas de desempleo y migración neta mediante aprendizaje automático
Empleamos varios modelos de aprendizaje automático, centrándonos en el análisis de series temporales y la previsión. Los modelos que utilizamos en el enfoque de series temporales fueron el regresor XGBoost, la regresión lineal (adaptada a series temporales) y el modelo ARIMA (incluidos sus derivados SARIMA y SARIMAX). Además, para el análisis de regresión, empleamos modelos como XGBoost para la regresión multivariante.

### Selección del modelo
Tras evaluar el rendimiento de los distintos modelos, determinamos que el modelo ARIMA superaba a los demás en términos de rendimiento global. Por lo tanto, seleccionamos el modelo ARIMA como nuestra opción principal para el análisis posterior. A continuación, buscamos conjuntos de datos adecuados entre las opciones disponibles y aplicamos regresión y medias móviles. Como la mayoría de los conjuntos de datos eran no estacionarios, aplicamos la diferenciación de primer orden para lograr la estacionariedad. Posteriormente, empleamos el modelo ARIMA, considerando la mayoría de conjuntos de datos con diferenciación de primer orden o no estacionarios. El modelo ARIMA arrojó unos resultados impresionantes, con unas puntuaciones R-cuadrado que oscilaban entre el 56% y el 93%. Estos resultados son muy prometedores para el análisis de series temporales.

### Optimización y despliegue
Tras la selección y el análisis del modelo, procedimos a automatizar el proceso y lo aplicamos a los nueve conjuntos de datos optimizados para analizar los indicadores de migración neta en los nueve países. Además, optimizamos nueve conjuntos de datos para analizar los indicadores de la tasa de desempleo en estos mismos países. Para automatizar la optimización de los parámetros, utilizamos la biblioteca pmdarima y su módulo autoarima. Este enfoque nos permitió identificar de forma autónoma los mejores parámetros (p, d, q) para los modelos y conjuntos de datos.

Además, aplanamos los 18 modelos utilizando la biblioteca pickle y los cargamos junto con los respectivos archivos CSV que contenían los indicadores de migración neta y tasa de desempleo de los nueve países. Con el fin de proporcionar una interfaz fácil de usar para acceder a los datos y visualizarlos, desplegamos los modelos en Streamlit, donde los usuarios pueden explorar los resultados a través de representaciones gráficas personalizadas creadas con Matplotlib.

En resumen, nuestro modelo de aprendizaje automático le proporciona predicciones accesibles y precisas sobre las futuras tasas de desempleo y las tendencias migratorias netas. A través de nuestra interfaz de fácil uso, podrá navegar y comprender fácilmente los datos proporcionados. Aprovechando nuestra experiencia en ciencia de datos, puede tomar decisiones informadas y mantenerse a la vanguardia.
