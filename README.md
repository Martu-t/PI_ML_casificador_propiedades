![HenryLogo](https://d31uz8lwfmyn8g.cloudfront.net/Assets/logo-henry-white-lg.png)
​
# Proyecto individual 2
​
Este proyecto es parte de la Datathon para los alumnos de Data Science de Henry.
​
## Marco de trabajo: Mercado inmobiliario
​
Dentro de la sociedad globalizada e industrializada, es sabido que los precios de los inmuebles han presentado un constante cambio, por lo que quienes deseen invertir o vender una propiedad se enfrentan al fenómeno especulativo existente en la valorización de éstos. Esto, debido a la constante tendencia de las ciudades a crecer demográfica y comercialmente, llegando a un punto en donde no se tiene certeza de la valorización real dentro del sector en donde se desee invertir. 
​
Pese a que el precio depende, en cierta medida, de las tendencias que esté teniendo el mercado inmobiliario en un determinado tiempo, poder estimar adecuadamente el valor de una propiedad es una referencia clave para entender si es una buena oportunidad, ya sea de compra o de venta.
​
## Descripción del problema
​
Una empresa inmobiliaria en Colombia necesita un módelo de clasificación que permita clasificar el precio de las propiedades en venta, utilizando los datos que se han puesto a su disposición correspondientes al año 2020.
​
Para esto, específicamente, elegimos predecir la **categorización** de las propiedades entre baratas o caras, considerando como criterio el valor promedio de los precios (la media).  

Esto servirá para una base de clasificación de propiedades, para más adelante tomar acciones teniendo en cuenta esta clasificación inicial.
​

## Que encontrarás en este repositorio
​
1) Se encuentra un .zip con los archivos utilizados que se pueden descargar. Los originales han sido ignorados por el tamaño que tiene.
Se proveen los archivos dentro del archivo comprimido 'properties_colombia.zip'

2) main.ipynb donde se realiza todo el proceso desde carga de datos hasta predicción. Sus secciones se dividen en:

    1) Análisis EDA (exploración y análisi de los datos)
    - Cómo se compone el dataset, relación 
    - Conclusiones pre-eliminares 

    2) Preprocesamiento de datos
    - Tratamiento de datos faltantes: Imputación o eliminación
    - Elección de features más importantes
    - Normalización y escalamiento de datos
    - Codificación de variables categóricas

    3) Módelo clasificador
    - Instanciar un módelo y ver sus métricas: Se ha utilizado el módelo de regresión logística. La razón: es un módelo simple y ayuda en las problematicas binarias (caro o barato en este caso). 
    Se pueden ver las métricas obtenidas en el Notebook

    4)Predicción
    - Se hace una predicción en base al archivo ´properties_colombia_test.csv´ y se genera autómaticamente un archivo llamado Martu-t.csv 

​
## Métricas
​
Ya que es muy importante para nosotros intentar predecir cuando una propiedad es cara, utilizaremos cómo primera métrica objetivo el recall y en complemento el Accuracy.
​
Esto se tuvo en cuenta a la hora del elegir el peso de cada variable en nuestro módelo.
​
## Glosario
- id - Identificador del aviso. No es único: si el aviso es actualizado por la inmobiliaria (nueva versión del aviso) se crea un nuevo registro con la misma id pero distintas fechas: de alta y de baja.
- ad_type - Tipo de aviso (Propiedad, Desarrollo/Proyecto).
- start_date - Fecha de alta del aviso.
- end_date - Fecha de baja del aviso.
- created_on - Fecha de alta de la primera versión del aviso.
- lat - Latitud.
- lon - Longitud.
- l1 - Nivel administrativo 1: país.
- l2 - Nivel administrativo 2: usualmente provincia.
- l3 - Nivel administrativo 3: usualmente ciudad.
- l4 - Nivel administrativo 4: usualmente barrio.
- l5 - Nivel administrativo 5.
- l6 - Nivel administrativo 6.
- rooms - Cantidad de ambientes.
- bedrooms - Cantidad de dormitorios (útil en el resto de los países).
- bathrooms - Cantidad de baños.
- surface_total - Superficie total en m².
- surface_covered - Superficie cubierta en m².
- price - Precio publicado en el anuncio.
- currency - Moneda del precio publicado.
- price_period - Periodo del precio (Diario, Semanal, Mensual)
- title - Título del anuncio.
- description - Descripción del anuncio.
- property_type - Tipo de propiedad (Casa, Departamento, PH).
- operation_type - Tipo de operación (Venta).
- geometry - Puntos geométricos formados por las coordenadas latitud y longitud. 
​
