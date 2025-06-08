# ¿QUÉ SON LOS ALGORITMOS DE CLASIFICACIÓN Y CUALES SON LOS MÁS COMUNES?

| Algoritmo                   | Características Principales                                         | Ejemplo de Uso                         |
|----------------------------|----------------------------------------------------------------------|----------------------------------------|
| Regresión Logística        | Clasificación binaria, modelo lineal, fácil de interpretar           | Clasificación de correos como spam     |
| K-Nearest Neighbors (KNN)  | Basado en vecinos más cercanos, sin entrenamiento explícito          | Clasificación de especies de flores    |
| SVM (Máquinas de Soporte)  | Encuentra el hiperplano óptimo, útil en alta dimensión                | Reconocimiento de dígitos manuscritos  |
| Árboles de Decisión        | Reglas tipo if-else, fácil de visualizar                             | Otorgamiento de crédito                |
| Random Forest              | Conjunto de árboles, reduce sobreajuste                              | Diagnóstico médico                     |
| Naive Bayes                | Basado en probabilidad, rápido y eficiente con texto                 | Clasificación de sentimientos          |
| Redes Neuronales           | Aprende patrones complejos, útil para datos no lineales              | Reconocimiento facial                  |
| Gradient Boosting (XGBoost, etc.) | Ensambles secuenciales, alta precisión, ganador en muchas competencias | Predicción de abandono de clientes     |


Estos algoritmos de clasificación son métodos de aprendizaje **supervisado** para predecir una etiqueta o categoría a partir de datos de entrada. Vamos a explicarlos un poco más a fondo.

## Regresión Logística
Es un modelo de clasificación, no de regresión (a pesar del nombre). Su objetivo es predecir la probabilidad de pertenencia a una clase, es decir su output es un porcentaje entre 0 y 1, lo cual se puede traducir a Sí y No, dándoles un umbral específico. Si es > 0.5 se predice clase 1, si es ≤ 0.5 se predice clase 0.

También puede extenderse a clasificación multiclase, llamándose Regresión Logística Multinomial.


### Métricas comunes:

- **Accuracy:** Proporción de prediccioines correctas sobre el total. Devuelve un valor entre 0 y 1 (o porcentaje) donde 1 es todo bien clasificado. Es útil cuando las clases están bien balanceadas, pero poco fiablre si las clases están desbalanceadas.
- **Precisión:** De todas las veces que se predijo "positivo", ¿cuántas eran realmente positivas? Es un valor entre 0 y 1, y cuanto más alto es el valor mejores resultados es que tiene. 
- **Recall:** De todos los positivos reales, ¿cuántos detectó el modelo? Valor entre 0 y 1, y cuanto más alto es el valor, pocos faltos snegativos tiene. 
- **F1 Score:** Media armónica entre precisión y recall. F1 = 2*((Precisión*Recall)/(Precisión+Recall)). Valor entre 0 y 1. Equilibra precisión y recall. 
- **Curva de ROC / AUC**
- **Matriz de confusión:** Una tabla que muestra las predicciones frente a los valores reales. 
- **L1 (Lasso):** Se usa cuando hay muchas variables y quieremos un modelo más simple o interpretable.
- **L2 (Ridge):** Se usa cuando hay multicolinealidad o se busca prevenir sobreajuste suavemente.


## K-Nearest Neighbors


  
