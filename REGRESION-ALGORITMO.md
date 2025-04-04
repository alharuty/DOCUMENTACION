## NOTAS PARA LA CIENCIA DE DATOS

### ¿Qué es el algoritmo de regresion?
El algoritmo de regresión es una ecuación matemática que nos ayuda a predecir valores numéricos a partir de datos de entrada. Además, son un subcampo del aprendizaje automático supervisado. Se utiliza para analizar y predecir resultadsos. 

**TIPOS DE ALGORITMOS DE REGRESIÓN:**
1. **Regresión lineal:** Calcula una relación lineal entre variables<img width="200" alt="Captura de pantalla 2025-04-04 a las 14 14 44" src="https://github.com/user-attachments/assets/b5c0b954-d6cd-42fb-9dd7-b95d3c1d923b" /><br>
  - **Regresión lineal simple:** Modela la relación entre una variable dependiente y una
  única variable independiente asumiendo una relación lineal entre ambas.
  - **Regresión lineal múltiple:** Extiende la regresión lineal simple al considerar múltiples
  variables independientes para predecir la variable dependiente.
  - **Regresión polinómica:** Utiliza una relación polinómica para modelar la relación
  entre las variables, permitiendo capturar relaciones no lineales.

2. **Regresión logística:** Determina la contribución de varios factores a un par de resultados<br>
<img width="200" alt="Captura de pantalla 2025-04-04 a las 14 15 55" src="https://github.com/user-attachments/assets/f4851023-eb67-4ded-bb5c-8e598979a978" /><br>
4. **Regresión por vectores de soporte:**<br>
<img width="200" alt="Captura de pantalla 2025-04-04 a las 14 17 47" src="https://github.com/user-attachments/assets/87f9b7fe-7785-4c3e-b710-2ce3d79d4d4a" /><br>


#### Vamos a profundizar en REGRESIÓN LINEAL
La regresión lineal es un modelo estadístico que busca predecir una variable dependiente (y) a partir de una o más variables independientes (x) ajustando una línea recta. Su objetivo es encontrar la relación lineal entre las variables. 
Es simple, rápido y se usa como base para modelos más complejos.
- **Variables independientes**: Son los valores que usamos para predecir un valor dependiente, por ejemplo, numero de habitaciones de una casa para poder calcular su precio.
- **Variables dependientes**: Es el resultado predecido mediante el uso de variables independientes, el valor de la venta de casa según el número de habitaciones

  y = mx + b
<img width="250" alt="Captura de pantalla 2025-04-04 a las 14 32 08" src="https://github.com/user-attachments/assets/ca6d3913-a1bd-4a5e-9396-e933eacb1043" />

En nuestro ejemplo de los precios de la casa podríamos tener una base de datos donde vemos la diferencia de precios de la casa según crece el número de habitaciones:

| Habitaciones (x) | Precio (y) |
|------------------|------------|
| 1                | 150        |
| 2                | 200        |
| 3                | 250        |

La tabla se vería así:

<img width="250" alt="Captura de pantalla 2025-04-04 a las 14 39 38" src="https://github.com/user-attachments/assets/3eafadb4-3136-4835-a0f8-4dc65c06c53b" />

Ahora, partiendo de nuestra base de datos sabemos que la ecuación se vería algo así como:

  y = 50x + 100
  
Donde 50 es la cifra que sube por cada habitación, y 100 es el precio base. Es decir, 100 es la intersección con el eje y, y 50 es la pendiente de la línea.
Nuestra regresión lineal haría algo como:

  4*50 + 100 = 300
  5*50 + 100 = 350, etc
  
**Método de mínimos cuadrados**: Sirve para encontrar el error/diferencia entre los valores reales y los predichos.

  Error = y(real) - y(predicho)

<img width="150" alt="Captura de pantalla 2025-04-04 a las 14 47 05" src="https://github.com/user-attachments/assets/9097c1b7-b404-42a0-af5f-2227c536eed7" />

**Método de mínimos cuadrados**: Al elevar al cuadrado el error evita que los errores negativos y positivos se cancelen
entre sí y da más peso a los errores grandes (los puntos más alejados de la recta).

Error cuadrático = (calor real - predicción)^2

**Error cuadrático medio (MSE)**:Esta fórmula mide el promedio de los errores cuadrados, y penaliza los errores con
mayor severidad gracias a la elevación al cuadrado. Con este cálculo evitamos
grandes diferencias entre el valor real y el predicho.

<img width="238" alt="Captura de pantalla 2025-04-04 a las 14 49 34" src="https://github.com/user-attachments/assets/8f710176-909d-43d2-bd58-81e64691b35b" />

**Error absoluto máximo (M)**: Esta métrica busca encontrar el error absoluto máximo entre los valores reales y los valores predichos por el modelo, nos indica así cuál ha sido el error de mayor peso que se ha cometido en el entrenamiento, por lo que si tenemos errores que van arrojando: 2, 4, 2, 7, 7 ; el valor que se tomará como error máximo es el 7.

<img width="275" alt="Captura de pantalla 2025-04-04 a las 14 50 45" src="https://github.com/user-attachments/assets/89023b53-65cc-4705-a21f-e6e45c9546c2" />

**Error absoluto medio (MAE)**: en este caso seguimos utillizando la diferencia entre el valor real y el valor obtenido por predicción como parámetro de evaluación, sin embargo no penaliza demasiado a los errores mayores, por ello es mejor ante datos atípicos. Saca el promedio de la suma de todos los residos.

<img width="204" alt="Captura de pantalla 2025-04-04 a las 14 52 12" src="https://github.com/user-attachments/assets/abbc3150-6735-42a5-8a51-bd8e2565bc6d" />

**Error cuadrático medio (MSE)**: Es una métrica utilizada para medir la precisión de un modelo de predicción. Específicamente, mide la diferencia promedio entre los valores reales (observados) y los valores predichos por el modelo, elevado al cuadrado esas diferencias para penalizar más los errores grandes.

<img width="143" alt="Captura de pantalla 2025-04-04 a las 14 53 40" src="https://github.com/user-attachments/assets/dbbaf623-0877-4b81-bbfa-2d946534cbfb" />

**Raíz cuadrada del Error Cuadrático Medio (RMSE):** La raíz cuadrada del MSE (conocida como RMSE) se usa para mantener la penalización de errores grandes, pero al tomar la raíz cuadrada se vuelve a la unidad original (como dólares), haciendo que el resultado sea más interpretable.

<img width="193" alt="Captura de pantalla 2025-04-04 a las 14 55 02" src="https://github.com/user-attachments/assets/52264a49-deb3-4c85-a8db-50a5abffd11d" />

**Suma de los Cuadrados de los Residuos (RSS):** Esta métrica es la suma de los errores al cuadrado para todas las observaciones en el conjunto de datos. Esto ayuda a cuantificar la cantidad de variación en los datos que el modelo no puede explicar.

<img width="161" alt="Captura de pantalla 2025-04-04 a las 14 55 53" src="https://github.com/user-attachments/assets/73f62ab4-37cd-4e8d-ba33-41ae83b02959" />

**Coeficiente de determinación (R2 o R-squared):** R² (coeficiente de determinación) indica qué tanto las variables del modelo explican la variación en la variable dependiente. Un valor cercano a 1 significa buen ajuste. Sin embargo, puede sobrevalorar modelos al agregar variables irrelevantes y no es fiable en modelos no lineales.

<img width="179" alt="Captura de pantalla 2025-04-04 a las 14 56 49" src="https://github.com/user-attachments/assets/314bf765-d9c5-4f20-a802-234980c1f23e" />

**R2 Ajustado:** Es una versión ajustada del R2 que penaliza la adición de variables independientes al modelo, lo cual nos puede ser útil con el overfitting.

<img width="238" alt="Captura de pantalla 2025-04-04 a las 14 57 30" src="https://github.com/user-attachments/assets/9653fa7f-e5e9-4dc2-9385-0cdf7005c665" />
  
  n = número de observaciones (número de filas o datos)
  k = numero de predictores (variables independientes)

**Error Absoluto Medio Porcentual (MAPE):** Esta métrica se presenta como un porcentaje, facilitando la comparación entre modelos. Su ventaja es que es independiente de la escala y fácil de interpretar. Obtenemos su porcentaje de error y luego sacamos la media de todos esos valores.

<img width="238" alt="Captura de pantalla 2025-04-04 a las 14 58 28" src="https://github.com/user-attachments/assets/c12b5694-e85f-4c4d-a9bd-0240e0db206e" />

**Error Cuadrático Medio Logarítmico (MSLE):** Su función es crear un balance entre los puntos de datos con orden de diferencia de magnitud durante el entrenamiento. A diferencia de otras métricas esta reduce el impacto de los valores de error mayores, y penaliza más los errores relativos cuando los valores reales son pequeños, por ejemplo: un error de 1 en un valor real de 2 representa un error del 50%

<img width="254" alt="Captura de pantalla 2025-04-04 a las 14 59 49" src="https://github.com/user-attachments/assets/ef4e38cd-56be-4a88-988c-ea065ea34fdd" />















