## NOTAS QUE TOMO EN EL CURSO DE FUNDAMENTOS DE LA CIENCIA DE SATURDAYS.AI

La ciencia de datos es un campo que nos permite extraer información valiosa de los datos y sacar conclusiones.

<img width="363" alt="Captura de pantalla 2025-04-02 a las 19 42 35" src="https://github.com/user-attachments/assets/31492598-befb-4064-b240-8dc8f247bada" />

¿Cuáles son las diferencias entre Ciencia de Datos e Inteligencia Artificial?
- La ciencia de datos no necesariamente hace uso de la IA para la interpretación de sus datos.
- En cambio, el aprendizaje automático de la Inteligencia Artifical consiste en aprender e inferir un comportamiento a partir de un conjunto de datos.

Uno de los casos de éxito de uso de los datos viene desde el año 1854, cuando en Londres descubrieron mediante la recopilación manual de datos, de dónde procedía una de las enfermedades que se estaba expandiendo en el país.

**¿Cuáles son las 5 características del Big Data?** <br>
1. **Volumen:** Cantidad de datos recopilados.

2. **Velocidad:** Alta velocidad en la que se recogen y transmiten los datos.

3. **Veracidad:** Alta calidad de los datos.

4. **Variedad:** Campos semánticos variados.

5. **Valor:** Conocimiento del interés detrás de los datos.

> [!NOTE]
>
> Se estima que el 90% de los datos que tenemos actualmente se generaron en los últimos dos años

**EL CICLO DE VIDA DE LOS DATOS**
Tener un método de recopilar datos y mantenerlos, hará que ahorremos recursos y el estudio será más fácil.
<img width="423" alt="Captura de pantalla 2025-04-02 a las 19 55 08" src="https://github.com/user-attachments/assets/a8b918db-caf7-4be2-9076-09aaf7edef10" />
1. **Comprensión del negocio,** con preguntas claras y bien definidas. Comprender a qué problema nos enfrentamos y qué resultados necesitramos.
2. **Obtener los datos con los que trbajaremos**, es la fase de recopilación de datos.
3. **Limpiar los datos.**
4. **Emploración de datos**
5. **Ingeniería de características**
6. **Modelado predictivo**: utilizamos estadística, programación o modelos de IA para responder a las preguntas que nos hemos hecho a principio del estudio.
7. **Visualización de datos**

Nuestro objetivo como Data Scientist es resolver problemas de la empresa utilizando datos.

## Matemáticas para la ciencia de datos
Estas son algunas de las operaciones aritméticas necesarias para la limpieza y análisis de datos.

#### La tendencia central:
Es como la medida estimada del valor central de los datos ó valor que más se repite, por ejemplo la altura media a la que vuelan los aviones. Hay 2 métodos para determinar este punto medio, y debemos optar por uno u otro dependendiendo del caso y del tipo de datos que estemos utilizando. Hay que destacar que estos 2 valores a veces pueden coincidir pero no es seguro:
1. **La media**: Es la medida de tendencia central más conocida y se obtiene sumando todos los valores numéricos y dividiendo entre el total de los valores.

> [!NOTE]
>
> Los valores extremos pueden afectar a la media

2. **La mediana**: Es exactamente el valor central del conjunto de datos. Los datos se ordenan de menor a mayor y el conjunto se divide en dor partes con el mismo número de datos. Si la cantidad de elementos es impar, se elije como mediana el valor central que no corresponde a niguno de los conjuntos. Si la cantidad de elementos es par, se calcula el promedio de los dos elementos centrales limítrofes.

> [!NOTE]
>
> Los valores extremos no afectan a la media

#### La dispersión:
La dispersión mide la variación de los datos; su grado de agrupación (o no) con respecto a su tendencia central.

1. **Desviación estandar ó varianza**
2. **Rangos intercuartiles**
3. **Desviación media absoluta (DMA)**

> [!NOTE]
> **TERMINOLOGÍA DE CIENCIA DE DATOS**
> 1. **Exactitud**: mide la proximidad de las mediciones al valor real
> 2. **Precisión**: mide la dispersión de las mediciones
<img width="300" alt="Captura de pantalla 2025-04-03 a las 13 56 28" src="https://github.com/user-attachments/assets/b903993e-b1ae-4ab0-8e73-e7ac3cacfbc9" /><br>
Por ejemplo, una máquina mal calibrada podría ser precisa en sus mediciones, pero no exacta.
> 3. **Inducción**: consiste en extrapolar características generales de un evento o suceso particular
> 4. **Deducción**: consiste en definir las cualidades o propiedades que se presentarán a partir de características generales específicas


#### La probabilidad incondicionada:
Es el estudio de las frecuencias o la aparición de eventos o efectos de forma directa, es decir, sin considerar su dependencia de otros eventos. Se calcula mediante la simple división denominada regla de Laplace, que calcula la probabilidad como se mencionó anteriormente.<br>
<img width="266" alt="Captura de pantalla 2025-04-03 a las 15 15 12" src="https://github.com/user-attachments/assets/aafec852-38ba-446a-ba6b-185095774d6f" />
El resultado siempre suele ser un número entre 0 y 1, pero en ocasiones puede darse en formate porcentaje.<br>
Por ejemplo, tenemos una bolsa con 8 bolas azules y 16 bolas amarillas.
- Probabilidad de sacar una bola azul = 8/24 bolas en total = 0,33 = 33,3 % 
- Probabilidad de sacar una bola amarilla 16/24 bolas en total = 0,66 = 66,6%
- Probabilidad de sacar una bola roja = 0/24 bolas en total = 0 = 0%

#### Tipos de datos
<img width="300" alt="Captura de pantalla 2025-04-04 a las 18 20 38" src="https://github.com/user-attachments/assets/18b57ca7-076b-4cfc-813f-33a7e39a3f0d" />

**¿Cuáles son los errores con los que tendremos que lidiar para hacer limpieza de datos?**
  - Errores de formato => fecha: Abril/34/2025
  - Errores de coherencia => fecha: Abril/34/2025
  - Valores faltantes
  - Valores atípicos => edad: -4
**Vamos a analizarlos**

1. **Valores faltantes**: Es una de las características más típicas en los conjuntos de datos. Pero, cómo gestionamos estos valores faltantes? Pues depende del caso.
   - Eliminarlos
   - Ignorarlos
   - Rellenarlos con null
   - Rellenarlos con media o mediana

<img width="500" alt="Captura de pantalla 2025-04-04 a las 17 58 15" src="https://github.com/user-attachments/assets/9f7b9977-b3f9-4c43-ad29-3918f3608ee9" />

2. **Valores atípicos**: Son valores numericamente alejados del resto de valores que tiene dicha columna, y si los tenemos en cuenta a la hora de estudiar y sacar conclusiones sobre los datos, nos pueden llevar a errores o cifras que están alejados de la "realidad". Por ejemplo un valor atípico sería que una persona mida 175 metros.
En un diagrama de caja, se puede ver los outliers como valores atípicos ya que se alejan de la distribución en una variable. 
<img width="725" alt="Captura de pantalla 2025-04-04 a las 18 02 32" src="https://github.com/user-attachments/assets/fd90fd53-4a5f-4c6d-9dfc-a9c6057695ff" />
También suele ocurrir, que 2 tipos de variables por sí solos no sean atípicos, pero juntos sí, porejemplo una persona que mida 1.85cm y que pese 45kg, son valores que no concuerdan, este tipo de valores son más difíciles de identificar. ¿Qué podemos hacer con ellos?
  - Si se puede corregir, por ejemplo en el caso de la persona que su alutra son 175 m, podemos entender que es en cenímetros, y podemos cambiar de 175m a 1,75m.
  - Si no hay posibilidad de corregir, podemos eliminarlos o reemplazarlos.
Los outliers son valores atípicos que estan lejos de la realidad.
<img width="500" alt="Captura de pantalla 2025-04-04 a las 18 07 28" src="https://github.com/user-attachments/assets/5f3760d9-4b95-42ec-9681-c961f0e4a54b" />

En resumen, podemos decir que los valores atípicos son valores extraños o atípicos. Cuando provienen de errores, deben corregirse y, si no es posible, eliminarse. Por otro lado, si son valores legítimos, debemos conservarlos a menos que el contexto o el modelo que vayamos a utilizar nos aconsejen eliminarlos o modificarlos de alguna manera.

**¿Qué son las distribuciones de probabilidad?**


Podemos decir que hay 2 tipos de distribuciones:
  - **Distribución discreta**: cuando los valores son exactas, no puede ser 1,25 o 1,75. Son valores exactos y entre uno y otro siempre hay la misma diferencia. Por ejemplo las potencias de fuego de una vitrocerámica, puede ser 1, 2, 3, 4, 5, 6. Y nunca un número con decimales ni que se pueda modificar.
  - **Distribución continua**: es lo contrario a discreta y se puede cojer el rango que se quiera, por ejemplo en una cocina de gas, la potencia del fuego puede cambiar desde el mínimo hasta el máximo.

Si queremos pasar de discreta a continua, se llama interpolación.
Si queremos pasar de continua a discreta, se llama discretización o modulación

<img width="400" alt="Captura de pantalla 2025-04-04 a las 18 34 57" src="https://github.com/user-attachments/assets/88e070a6-59bf-4a9c-bf35-d10baea4d490" />

**¿Cuáles son los métodos de muestreo?**

1. **Muestreo aleatorio simple**: todos los individuos de la población tienen la misma probabilidad de ser seleccionados para formar parte de la muestra.
2. **Muestreo sistemático:** Se elige un individuo cada cierto número de pasos. Es fácil de aplicar, pero puede generar sesgos si hay patrones en la población.
3. **Muestreo estratificado:** Se divide la población en subgrupos homogéneos y se toma una muestra de cada uno. Permite representar bien la población, pero requiere conocer previamente los subgrupos.

**Cómo evitar los sesgos?**
  - Definir reglas de muestreo pobres y flexibles
  - Omitir individuos pertenecientes a grupos de dificil acceso
  - Incorporar datos históricos antigos al estudio

**¿Qué son Normalización VS Estandarización?**
Son técnicas de escalado de características.
  - **Normalización:** Su objetivo principal es reescalar cada característica para que su rango esté entre 0 (valor mínimo) y 1 (valor máximo).
    
<img width="300" alt="Captura de pantalla 2025-04-04 a las 18 51 28" src="https://github.com/user-attachments/assets/fefdd39d-9a1d-4367-a407-df238d03d001" />

  - **Estandarización**: Los datos se centrarán en el valor 0 y tendrán una desviación estándar unitaria.

<img width="167" alt="Captura de pantalla 2025-04-04 a las 18 52 35" src="https://github.com/user-attachments/assets/cf01c524-e0a8-46f5-a7b6-26d0fe921580" />

**¿Cómo saber quñe técnica usar**

- La normalización es útil cuando se sabe que la distribución de los datos no sigue una distribución gaussiana. Esto puede ser útil en algoritmos que no asumen ninguna distribución de los datos.

- La estandarización, por otro lado, puede ser útil en casos donde los datos siguen una distribución gaussiana. Sin embargo, esto no tiene por qué ser necesariamente cierto. Además, a diferencia de la normalización, la estandarización no tiene un rango límite. Por lo tanto, incluso si hay valores atípicos en los datos, estos no se verán afectados por la estandarización.


**¿QUÉ ES NORMALIDAD?**
Es la forma en que se distribuyen los datos numéricos. La distribución normal es una distribución de probabilidad que se caracteriza por ser simétrica alrededor de una media. Si el valor p es menor que el nivel de significancia (generalmente α=0,05), se rechaza la hipótesis nula y se concluye que los datos no siguen una distribución normal. Por el contrario, si el valor p es mayor que α, se concluye que no se puede rechazar la hipótesis nula y se asume que los datos siguen una distribución normal.
Las pruebas más comunes son:
- Kolmogorov-Smirnov
- Shapiro-Wilk: es uno de los más eficaces para contrastar la normalidad

**¿QUÉ ES HOMOCEDASTIICIDAD?**
Es la igualdad de varianzas entre los grupos a comparar. la hipótesis nula supone la igualdad de varianzas en los diferentes grupos de datos. Por lo tanto, valores p por debajo del nivel de significancia indicarán heterocedasticidad.
Las pruebas más comunes son:
- Levene
- Flinger-Killeen

**MAPAS DE CORRELACIÓN**
Una forma muy útil y práctica de buscar correlación es el diagrama de dispersión o gráfico de burbujas. Se trata de un tipo de diagrama matemático que utiliza coordenadas cartesianas para mostrar los valores de dos variables de un conjunto de datos.
 
<img width="600" alt="Captura de pantalla 2025-04-08 a las 13 58 03" src="https://github.com/user-attachments/assets/8441df63-56bf-46d5-ab8a-257e248aaa44" />

En un mapa de correlación puede tener valores entre -1 y 1:
- Los extremos indican una correlación perfecta (Pearson)
- 0 indica una ausencia de correlación
- El signo es negativo cuando valores altos de una variable se asocian con valores bajos de la otra
- El signo es positivo cuando ambas variables tienden a aumentar o disminuir simultáneamente


**FUNDAMENTOS DE REGRESIÓN LINEAL**
Sirve para determinar si existe alguna relación entre 2 ó más variables.
<img width="600" alt="Captura de pantalla 2025-04-08 a las 14 11 51" src="https://github.com/user-attachments/assets/5c23360f-b4bf-4ef9-a275-973538934b81" />
Tiene 2 tipos de variables:
- y : variable explicada, dependiente o endógena
- x : variable explicativa, independiente o exógea

Las relaciones entre dos variables pueden ser de dos tipos:
1) Funcional (o determinista): cuando existe una fórmula matemática que permite calcular los valores de una de las variables a partir de los valores que toma la otra.
2) Estadística (o estocástica): cuando no existe una expresión matemática que las relacione exactamente.

**¿POR QUÉ ES IMPORTANTE LA VISUALIZACIÓN DE DATOS?**
Aprovechamos la capacidad de la percepción visual humana para trnasmitir conocimiento. Centramos la atención del usuario en lo relevante e importante, para que genere más comprensión.




