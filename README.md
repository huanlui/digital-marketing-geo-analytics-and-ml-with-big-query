# Business Analytics, Geo Analytics and Machine Learning with BigQuery 

Lo que se nos va a explicar lo podriamos aplicar ya mañana.

Vamos a usar Standard SQL (variante de SQL). Con ese lenguaje podremos hacer cosas como:
- Geo Analytics. 
- ML. 

Haremos un K-mins. Además, usaremos ?Google Labs?, peor que Tableau pero gratuito. 

Big Query ML. ES para realizar modelos de ML a través de SQL. Por ejemplo, ellos con Iberia predicen según el uso del navegador del usuario si va a comprar o no. 

Business Analytics puede usar Data Science pero puede no usarlo, y usar por ejemplo Business Intelligence. 


# Big Query

* Más barato por no tener ordenadores dedicados. 
* Columnar: que sea columanar lo hade más rápido. Si usas menos columnas es más barato por cómo está organizado. El coste está más en la columna que en la fila
* Es serverles.

En BigQuery, el almacenamiento es bastante barato, 2centimos giga y mes. Por lo que te cobran es por las consultas.

Por una consulta que devuelva un tera te cobran 5 dolares. 

Para hacer que cueste menos, tenemos una tabla resumida (con menos FILAS) para que la gente de la organización hagan sus pruebas.

Otra forma muy eficiente es particionar tablas por dias para sólo ejecutar las tablas por días. 

Las tablas se organizn por dataset. Un dataset tiene varias tablas, es como una especie de schema. 

Vamos a hacer varias consultas (ver diapositivas).  Vamos a usar los gratuitos, que los tenemos aquí:

https://cloud.google.com/bigquery/public-data/

Tiene funciones, como por ejemplo regexp_contains:

select origin from `chrome-ux-report.country_es.201907` where regexp_contains(origin,'bbva') order by origin desc limit 10

Nos permite hacer cast de datos:

select cast(fare as string) as castedfare from

Ver diapos para más funciones. 


... bla bla bla

## Ejercicio (Ver PDF del ejercicio)

* Frecuencia: cuantas veces ha comprado cada usuario.
* Monetización: cuánto se ha gastadio
* Recencia: ultima vez. que compro
* Compra media.
* Número medio de productos comprados. 
* Frecuencia media de compras (numero de compras por dias)

Ojo, que en las tablas hay devoluciones. 

DEspués, vamos a clusterizando usando el mismo BigQuery. Nos cobra por entrenar el modelo lo mismo que por la consulta. 

## Data Studio

Herramienta gratuita para visualización, Otras opciones: Tableau (mucho más potente) y PowerBi. 

A partir de una fuente de datos, generamos un datsource en DAta Studio, en el que podemos hacer pequeña transformaciones y 
después conectarse con el infore.

Hay muchos conectores con herramientas de Google. 

Proceso paera gastar menos dinero
- : subimos ficheros csv a un bucket.
- En big query lo cargamos desde ese bucket (mejor que hacer todo desde ahi por temas de dinero y porque BigQuery tiene limitación de tamanño)

El gasto siempre se te va en análisis en lugar de en almacenamiento. 

El fichero RAW  tiene datos de camapaña: tipo de camapaña, cliente, número de clicks, coste total asociado a los clicks que viene
en la moneda del cliente, impresiones, 
conversiones (numero de veces que he obtenido el objetivo, como comprar o que el usuario compre el prpducto.)


