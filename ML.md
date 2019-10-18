# ML for Analyst with Google.

Vamos a hacer tood el proceso de ML.

## División del conjunto de datos

El conjunto de daatos lo dividismos en:
- Entrenamiento.
- Validación: usando las métricas, vemos si el modelo está bien o no, 
- Test: como en validación estamos reentrenando, podemos tener el problema de nuevo de overtfiting. 
Por eso tenemos este subconjunto para comprobar que bien.

## Métricas

Es inmportante saber c
Accuracy = porcentaje de aciertos. 
Precission = del total de positivos, en cuantos ha acertado. 
Recall = del total de positiv os, 

![](https://www.digital-mr.com/media/cache/5e/b4/5eb4dbc50024c306e5f707736fd79c1e.png)

Ejemplo de cuándo tener en cuenta métricas.

* El accuracy del 99% no tiene por qué ser bueno. Por ejepmplo, si pongo un modelo que diga que siempre la gente 
no tiene albinismo, acertaré en el 99.999 % de las veces y mi modelo es una mierda.
* Por ejemplo, para detectar fraude: record y precioon. Si el fraude es una anomalía: recall.
* Para detectar caracteristicas anómalas, usaríamos recall en lugar de precission, como vimos antes.
* PAra decidir si metemos a uno en la cárcel o no, usaríamos mejor la precisión, para no meter a gente en la cárcel que no debemos. 

El AUC de la ROC es otr forma . La ROC nos permite ver el comprimiso entre Recall y falsos positivos. Cuanto mejor recall tenemos , también tenemos más falsos positivos. 

Otra opción sería hacer una matriz de coste beneficios. Asignamos un beneficio para las true positivos y otro para los true negatives. Y ponemos coste para false negative y false positivo. Y así podemos decidir. 

# Bg Query ML
Modelos facilitos y muy fáciles de poner en marcha. 

Para estos casos de uso:

* Cuando hay una oprtunidad de negocio en ML, en lugar de ponernos a usar un proyecto conmplicado, podemos usar esta herramienta para hacer una prueba de concepto. 
* Si vemos que el negocio no es muy grande, podemos quedarnos a usar este modelo simple y explotartlo así. 
* Para analistas que no saben mucho de programación.

Esta herramienta es importante, porque las revoluciones digitales aparecen cuando ponemos al alcance de un usuario normal las cosas. 
