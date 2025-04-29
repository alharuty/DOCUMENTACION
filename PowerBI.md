# ¿Qué es Power BI?



Métricas útiles:
  - Promedio: Es la suma de todos los valores dividido entre el número total de valores. Por ejemplo si tenemos los valores 3, 7, 5, 9 y 11, el promedio sería (3+7+5+9+11)/5 = 7.
  - Mediana: Es la medida central de un conjunto de números, se ordena en orden asendente y se elije el número que está en la mitad. Si el conjunto de número es impar, se escoje el número central, si el conjunto es par, se escojen los 2 números centrales y se divive entre 2. Por ejemplo, si tenemos 5, 1 y 9, la mediana es 5. Si tenemos 5, 1, 9, 7, la mediana sería (5+7)/2 = 6.
  - Percentil: es una medida que indica el valor bajo el cual se encuentra un cierto porcentaje de observaciones en un conjunto de datos. Por ejemplo, si un estudiante está en el percentil 90 en una prueba, significa que ha superado al 90% de los otros estudiantes que tomaron la prueba.
  - Correlacion: mide la relación entre dos variables y cómo una variable puede poredecir la otra. La correlacion varía entre -1 y 1. Un valor de 1 indica una correlaciónpositiva pefecta, mientras que -1 indica una correlación negativa perfecta. Un valor de 0 indica que no hay una relación.

Ejercicio de gráficos con PowerBi. 
![Captura de pantalla 2025-04-21 220440](https://github.com/user-attachments/assets/61ae71f7-36ff-4f72-b756-2dbeef174d51)


**Box&Whiskers:**

<img src="https://github.com/user-attachments/assets/eb7827e3-8350-44e8-9c10-8ae5ced1fbd8" width="300px">

Un Box&Whiskers (también llamado boxplot) es un gráfico que resume visualmente la distribución de un conjunto de datos. Muestra la mediana, los cuartiles y los valores extremos (mínimo y máximo).

Los cuartiles dividen el conjunto de datos ordenados en 4 partes iguales, cada una con el 25% de los valores.
- **Q1 (Primer Cuartil, 25%)**: Es el valor que deja por debajo el 25% de los datos. Es decir, 1 de cada 4 valores es menor o igual que Q1. (Parte inferior de la caja)
- **Q2 (Segundo Cuartil o Mediana, 50%):** Es el valor del medio. Deja el 50% de los datos por debajo y 50% por encima. (Línea dentro de la caja)
- **Q3 (Tercer Cuartil, 75%):** Es el valor que deja por debajo el 75% de los datos.(Parte superior de la caja)

- Ejercicios prácticos que he realizado:
<img src="https://github.com/user-attachments/assets/5b6afd7a-158a-46d8-810f-bb0cae036509" width="300px">
<img src="https://github.com/user-attachments/assets/7bc4f7fe-dea0-4dae-be43-bbba1fbddee3" width="300px">
<img src="https://github.com/user-attachments/assets/ccdeec7a-943c-4f99-8405-ced748406e78" width="300px">
<img src="https://github.com/user-attachments/assets/5684e41d-153a-46d5-8e24-85ad328c80d7" width="300px">

**forecasting/previsiones:** Permiten a los analistas anticipar comportamientos futuros basándose en datos históricos, lo que facilita la toma de decisiones estratégicas. Existen diferentes modelos de series termporales que nos ayudan a identificar patrones y tendencias, uno de los más comunes es:
- **Descomposición aditiva** que separa la serie temporal en componentes de tendencia, estacionalidad y ruido.

<img src="https://github.com/user-attachments/assets/cb4e760b-06c4-4ba1-862b-5b364246254b" width="300px">

Para realizar previsiones en PowerBi, lo que debemos hacer es:
1. Seleccionar un conjunto de datos
2. Agregar la visualización
3. Seleccionar una variable dependiente en el eje Y
4. Campo como fecha en el eje X
5. Hacer click en la visualización de línea
6. Ir al panel de análisis (icono de lupa) en la parte derecha
7. Seleccionar la sección de 'Forectast' y activar la opción
8. Configurar parámetros: ejemplo: período de predicción(36 meses) y confianza(95%)

Una vez configurado, veremos la línea de resultados, el color azul es los datos reales, y el color gris cómo se espera que sean los datos en los siguientes meses. Este tipo de gráfico puede servirnos porejemplo para provisionar una tienda con los productos necesarios deacuerdo a los datos pasados.

¿Cómo mejorar y optimizar el modelo de previsión?
1. Aumentar el periodo de histórico: Usar un dataset con datos de un tiempo más prolongado
2. Ajustar la granulidad: analizar si es mejor trabajar con datos diarios, semanales o mensuales
3. Evaluar el modelo: utilizar medidas de precisión como el Error Absoluto Medio (MAE) o el Error Cuadrático Medio (MSE) para evaluar y ajustar el modelo.

**Crear visuals automáticamente con IA y NLP en PowerBI**
Este mecanismo de PowerBI llamado Q&A, nos permite realizar preguntas en lenguaje natural como "Muéstrame el gráfico de barras de ingresos por región" y el sistema se encarga de interpetar esta consulta, realizar operaciones y devolver la correspondiente información de forma rápida, automática y visual. Esta función nos ahorra tiempo y permite que personas con poca experiencia en PowerBi puedan obtener buenos y valiosos resultados.

<img src="https://github.com/user-attachments/assets/576939fe-4dd5-43ef-95a6-dfa00c22b8ea" width="300px">

**Detección de anomalías**
Es como una forma de detectar posibles "errores" o ouliers a lo largo del tiempo. Es decir, analiza todos los datos y por ejemplo si en una tienda online, en un mes ve que hay unas cifras muy diferentes a otros años, nos saltará una desviación y proporcionará explcaciones potenciales basadas en los datos anteriores. Es una herramienta muy poderosa que permite a los analistas identificar y abordar irregularidades en los datos de manera eficaz.

Se puede ajustar esto haciendo click encima de alguna gráfica > Visualizaciones > Lupa > Buscar anomalías
<img src="https://github.com/user-attachments/assets/97f6cbdb-60c7-4e92-a850-d4831c3ec9b5" width="300px">

**Key influencers (elementos influyentes)**
Es una herramienta que mediante IA permite identificar los factores que más influyen en un resultado específico.

<img src="https://github.com/user-attachments/assets/b1d25b43-2fd5-4000-84ad-7de686bb8bcd" width="300px">

**Esquema jerárquico**
Es una forma fácil y rápida de entender cuáles son las mejores variables que tenemos. Es decir, si tenemos una tienda (online y tienda presencial) en varios países con diferentes métodos de envío. Podemos usar el esquema jerárquico, insertamos en "Analizar" nuestra columna "ventas finales" y en "Explicar por" todas las variables que queramos tener en cuenta. 

<img src="https://github.com/user-attachments/assets/a33ecadf-1f57-4793-89cd-26253bda76d2" width="300px">

<img src="https://github.com/user-attachments/assets/d2f4cc9a-4ffd-49d0-bd18-748ef57e7a54" width="300px">

Ahora que lo tenemos configurado, nos devolverá un esquema:

<img src="https://github.com/user-attachments/assets/3240f116-2b22-412b-ac38-1e5b7340732f" width="300px">

Este esquema nos dice que, del total de nuestras ventas, elmétodo de envío más utilizado es "Standard Class" y se envía al Estado de "California" y más específicamente a la ciudad de "Los Ángeles". Lo que nos da una muestra clara de donde podemos invertir más nuestros esfuerzos para generar más. 



