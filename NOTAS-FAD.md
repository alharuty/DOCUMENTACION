# Notas que tomo en el curso de Fad Azure Fundamentals AI-900

**¿Qué es Azure?** Es un servicio de nube (plataforma Cloud) de Microsoft, donde podemos levantar máquinas, usar servicios como servidores, bases de datos, etc.

**Diferencia entre Big Data y Machine Learning:** Big data es la explotación de datos masivos, haciendo una media o cualquier otra operación que nos aclare sobre dichos datos repetitivos, y Machine Learning es cuando, la IA, toma muchos datos y mediante estos hace provisiones y estadísticas futuras. Por ejemplo, si tenemo un restaurante y tomamos datos durante un periodo largo y hacemos medias, podemos decir que durante x fecha se factura más, ó que tal plato se vende más. Pero con Machine Learning - IA, podemos tomar dichos datos y preveer que en tal fecha del año que viene se facturará una cifra estimada X.

**Principios de la IA responsable:**
1. Imparcialidad: el sesgo puede afectar a los resultados.
2. Confiabilidad y seguridad: los errores pueden causar daños.
3. Privacidad y protección: se podrían exponer datos privados.
4. Inlusión: es posible que las soluciones no funcionen para todos los usuarios.
5. Transparencia: los usuarios deben confiar en un sistema complejo, y que sus respuestas tengan un sentido y razón.
6. Responsabilidad: ¿quién es responsable de las decisiones en la IA? Los modelos fallan y pueden causar daños y no hay un responsable. Por ejemplo en detecciones de enfermedades mediante IA, pueden dar falsos positivos o falsos negativos y causar daño a la perosna.

<img width="618" alt="Captura de pantalla 2025-03-15 a las 8 44 43" src="https://github.com/user-attachments/assets/c08f6ac7-73f3-4c3f-a695-92b67d037e04" />

**¿Que es Estudio de Azure Machine Learning?** Es una plataforma basada en la nube para el aprendizaje automático con una interfaz de usuario para acceder a las funcionalidades y entrenar a máquinas sin código.

**Métricas de evaluación de regresión:** Estas son algunas métricas comunes que se usan par aevaluar un modelo de regresion:
1. Error medio absoluto (MAE)
2. Error cuadrático medio (MSE)
3. Raíz del error cuadrático medio (RMSE)
4. Coeficiente de determinación(R^2)
Tras múltiples iteraciones, se selecciona el modelo que da como resultado la mejor métrica de evaluación aceptable para el escenario específico.

**¿Qué es una matriz de confusión?**:El primer paso para calcular las métricas de evaluación para un modelo de clasificación binaria suele ser crear una matriz del número de predicciones correctas e incorrectas para cada etiqueta de clase posible:
<img width="250" alt="Captura de pantalla 2025-03-15 a las 13 24 38" src="https://github.com/user-attachments/assets/9903e52c-c947-4a51-a1d2-7b21a9a3dd54" />
Esta visualización se denomina matriz de confusión y muestra los totales de predicción donde:

ŷ=0 e y=0: Verdaderos negativos (TN por sus siglas en inglés)<br>
ŷ=1 e y=0: Falsos positivos (FP por sus siglas en inglés)<br>
ŷ=0 e y=1: Falsos negativos (FN por sus siglas en inglés)<br>
ŷ=1 e y=1: Verdaderos positivos (TP por sus siglas en inglés)<br>
La disposición de la matriz de confusión es tal que las predicciones correctas (verdaderas) se muestran en una línea diagonal de la parte superior izquierda a la derecha. A menudo, la intensidad del color se usa para indicar el número de predicciones en cada celda, por lo que un vistazo rápido a un modelo que predice bien debe revelar una tendencia diagonal profundamente sombreada.<br>

**¿Que es la coincidencia en las métricas?**: Coincidencia es una métrica que mide la proporción de casos positivos que el modelo identificó correctamente. Su fórmula es: TP ÷ (TP+FN)<br>
**¿Qué es la precisión en las métricas?**: Precisión es una métrica similar a la coincidencia, pero mide la proporción de casos positivos predichos en los que la etiqueta verdadera es realmente positiva. Su fórmula es: TP ÷ (TP+FP)<br>
**¿Qué es la puntuación F1?**: Puntuación F1 es una métrica global que combina coincidencia y precisión. La fórmula es: (2 x precisión x coincidencia) ÷ (precisión + coincidencia)<br>


**¿Qué ofrece Azure Machine Learning?**

1. Almacenamiento y gestión centralizada de datos para entrenar y evaluar modelos.
2. Recursos de procesamiento bajo demanda para ejecutar trabajos de aprendizaje automático.
3. AutoML, que automatiza la búsqueda del mejor modelo a través de múltiples algoritmos y parámetros.
4. Herramientas visuales para crear y orquestar canalizaciones de procesos como entrenamiento e inferencia.
5. Integración con marcos comunes de ML (como MLflow) para gestionar el ciclo de vida del modelo.
6. Soporte para evaluar métricas de IA responsable, como explicabilidad y equidad del modelo.

**¿Qué es OCR?:** Optical character recognition/ Reconocimiento óptico de caracteres, es la funcionalidad de Inteligencia Artificial de detectar y leer texto sobre una imágen. Se mezcla la visión artificial con el procesamiento del lenguaje natural.

<img width="470" alt="Captura de pantalla 2025-03-16 a las 12 26 07" src="https://github.com/user-attachments/assets/cf6a1f4c-4ec6-466d-ab99-6b3509248150" />

**SERVICIOS DE AZURE**
- Computer vision:
  1. Visión:
    1. Análisis de imágenes: Etiquetado de imágenes, descripciones, personalización de modelo...
    2. Reconocimiento óptico de carácteres: encontrar texto dentro de imágenes
    3. Análisis espacial: distancia entre objetos
  2. Face:
    1. Detección de caras
    2. Reconocimiento facial
- Procesamiento de lenguaje natural (NLP - PNL) :
  1. Lenguaje:
     1. Detección de idioma
     2. Extracción de frases clave
     3. Detección de entidad con nombre
     4. Análisis de opiniones y minería de opiniones
     5. Detección de información personal
     6. Resúmenes
     7. Respuesta a preguntas: chatbot
     8. Reconocimiento del lenguaje conversacional
     9. ...
  2. Voz:
     1. Texto a voz
     2. Voz a texto
     3. Traducción de voz
     4. Identificación del hablante
     5. Identificación del idioma
     6. ...
  3. Traductor:
     1. Traducción de texto
     2. Traducción de documentos
     3. Traducción personalizada
     4. ...
- Documento de inteligencia: Es la capacidad de extraer pares de texo, diseño y clave-valor de una imágen de documento. Cada uno de estos elementos tiene un nivel de confianza, lo que indica el nivel de precisión probable.
    
  
**¿Qué es CLU?**: Reconocimeitno del lenguaje conversacional en Azure, sirve para crear modelos de lenguaje que interpreten el significado de las frases en una configuración conversacional. Por ejemplo, entrenar al modelo para que pueda hacer una acción que se le diga por voz, como decir "Enciende las luces" y que ésta pueda interpretarlo y realizar la acción de endender la luz. Tiene en cuenta entidades e intenciones, en este caso la entidad sería 'luz' y la intención 'encender'. Para que el modelo funcione hay que darle las diferentes entidades e intenciones, y después entrenarlo para que entienda el lenguaje de la persona y asimilar que la misma intención se puede decir de diferentes maneras, como por ejemplo 'encender' == 'activar'.
