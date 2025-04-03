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




