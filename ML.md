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
* Por ejemplo, para detectar fraude: record y precioon.
* Para detectar caracteristicas anómalas, usaríamos recall en lugar de precission, como vimos antes.
