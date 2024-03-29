### Análisis cluster locales en planta baja destinados a actividad económica de la ciudad de Barcelona

El dataset incluye información del censo de locales en planta baja de la ciudad de Barcelona destinados a actividad económica y que se encuentran en activo o
pendientes de actividad. 

El **propósito** de este proyecto es aplicar el algoritmo de K-means clustering para segmentar los locales. 

### Las variables que se han tenido en consideración son las siguientes

*Codi_Principal_Activitat*, identificador global único.

*Nom_Principal_Activitat*, descripción de codigo sobre el uso principal de l'activitat.

*Codi_Sector_Activitat*, identificador del sector de la actividad.

*Nom_Sector_Activitat*, nombre del sector de la actividad. 

*Codi_Grup_Activitat*, código grupo de la actividad. 

*Nom_Grup_Activitat*, nombre del grupo de la actividad. 

*Nom_Activitat*, actividad del local. 

*Nom_Local*, nombre del local. 

*SN_Oci_Nocturn*, si se dedica al ocio nocturno (sí/ no). 

*SN_Coworking*, si se dedica al coworking (sí/ no). 

*SN_Servei_Degustacio*, si tiene servicio de degustación (sí/ no). 

*SN_Obert24h*, está abierto 24/7 (sí/ no). 

*SN_Mixtura*, tiene más de una actividad (sí/ no). 

*SN_Carrer*, si el local se encuentra a pie de calle (sí/ no). 

*SN_Mercat*, si el local está dentro de un mercado (sí/ no). 

*SN_Galeria*, si el local se encuentra dentro de una galería (sí/ no). 

*SN_CComercial*, si está dentro de un centro comercial (sí/ no). 

*SN_Eix*, si forma parte de un eje comercial (sí/ no). 

*Latitud*, la latitud a la que se encuentra. 

*Longitud*, la longitud a la que se encuentra. 

*Codi_Via*, el código de la vía.  

*Codi_Barri*, el código del barrio.

*Codi_Districte*, el código del distrito. 


### Procesamiento de Datos

En este proyecto, se aplicaron varias técnicas de preprocesamiento de datos antes de aplicar el algoritmo de K-means clustering. A continuación se describen los pasos específicos que se siguieron:

One-hot Encoding

Se utilizó la técnica de One-hot encoding para manejar variables categóricas en el conjunto de datos de locales. Esto implicó convertir cada variable categórica en una representación numérica binaria, lo que nos permitió utilizarla en el algoritmo de clustering.

Standard Scalar

Antes de aplicar el algoritmo de K-means clustering, se estandarizaron las características numéricas utilizando StandardScaler de scikit-learn. Esto aseguró que todas las características tuvieran una media de 0 y una desviación estándar de 1, lo que ayudó a mejorar la convergencia del algoritmo.

K-means Clustering

Se aplicó el algoritmo de K-means clustering para segmentar a los locales de grupos homogéneos. Se utilizó la implementación de K-means de scikit-learn, especificando el número de clusters deseado.

Elbow Method
Se utilizó el método del codo (Elbow Method) para determinar el número óptimo de clusters para el conjunto de datos. Se iteró sobre un rango de posibles valores de clusters y se calculó la suma de los errores cuadráticos (SSE) para cada valor. Se seleccionó el punto en el que la curva de SSE tuvo un cambio significativo, lo que indicó el número óptimo de clusters (5).



