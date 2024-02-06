# Modelo de Predicción Estadístico para Temperatura y Precipitación con el algoritmo Random Forest en lenguaje R 
## Introducción a modelamiento con el proceso Random Forest
El modelamiento con el proceso Random Forest es una técnica poderosa y versátil en el ámbito del aprendizaje automático. Se trata de un algoritmo de conjunto que combina múltiples árboles de decisión para realizar predicciones más precisas y robustas. Este enfoque se destaca por su capacidad para manejar conjuntos de datos complejos, lidiar con problemas de sobreajuste y ofrecer una mayor generalización.

El Random Forest opera construyendo una colección (o "bosque") de árboles de decisión independientes y no correlacionados. Cada árbol se entrena en una muestra aleatoria del conjunto de datos, utilizando un subconjunto aleatorio de características en cada nodo de decisión. Esta aleatoriedad durante la construcción del modelo ayuda a evitar la sobreajuste y mejora la diversidad entre los árboles.

El proceso de predicción en un Random Forest implica que cada árbol en el bosque emita su propia predicción, y luego se realiza una votación (en el caso de problemas de clasificación) o se toma el promedio (en problemas de regresión) para obtener la predicción final del modelo.

## ¿Como se construye un modelo Random Forest?
Cada arbol de contruye de la siguiente manera: 

1.- En el caso de que el número total de casos en el conjunto de entrenamiento sea N, se selecciona aleatoriamente una muestra de esos N casos, permitiendo la repetición (con reemplazo). Esta muestra se utiliza como conjunto de entrenamiento para construir el árbol i.

2.- Cuando se cuentan con M variables de entrada, se especifica un número m<M de manera que, en cada nodo, se seleccionan aleatoriamente m variables de las M disponibles. La mejor división entre estas m características se utiliza para ramificar el árbol. Este valor m permanece constante durante la creación de todo el bosque.

3.- Cada árbol crece hasta alcanzar su máxima extensión posible, sin realizar ningún proceso de poda.

4.- Las nuevas instancias se predicen mediante la agregación de las predicciones de los x árboles, utilizando el criterio de mayoría de votos en caso de clasificación, o el promedio en caso de regresión.

![image](https://github.com/Jncruz1726/informatica/assets/158979734/a121b7fc-a01d-4f11-a616-2066ddfa7126)

### Ventajas de Random Forest
1.- Normalmente tiene mucho mejor desmpeño que arboles de decisión sensillos o bagging.

2.- El set de validación incorporado no equiere altos sacrificios de los datos de entrenamiento.

3.- Preprocesamiento no es del todo requerido.

4.- Es eficaz en el procesamiento de conjuntos de datos grandes y complejos, gracias a su capacidad para manejar múltiples variables y observaciones sin comprometer el rendimiento.

5.- Random Forest tiende a proporcionar predicciones precisas debido a la combinación de múltiples árboles de decisión, reduciendo así el riesgo de sobreajuste.








