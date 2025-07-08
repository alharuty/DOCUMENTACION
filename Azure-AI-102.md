# Azure AI-102

**¿Qué es IoT en programación?:** IoT (Internet de las Cosas) se refiere a la práctica de programar dispositivos conectados a internet para que puedan recopilar, enviar y recibir datos, interactuando entre sí y con los usuarios a través de redes.

**¿Qué es SDK de Azure?:** Software Development Kit, es un conjunto de herramientas y bibliotecas que facilita a los desarrolladores la interacción con los servicios de Azure desde sus aplicaciones. Permite la gestión y manipulación de recursos de Azure de manera programática, utilizando el lenguaje de programación preferido por el desarrollador.

## Módulo 1: Introducción a Servicios de Azure AI

### 1.1. Planeamiento y preparación para desarrollar soluciones de inteligencia artificial
**Azure AI Foundry** es una plataforma completa para el desarrollo de inteligencia artificial en Microsoft Azure.
La inteligencia artificial replica el comportamiento y las funcionalidades más comunes son:
- **IA Generativa:** Capacidad de generar respuestas originales en lenguaje natural.
- **Agentes:** Aplicaciones de IA generativas que sirven para realizar tareas y alcanzar objetivos en nombre de un usuario o de otro sistema. Por ejemplo un agente que recuerde la hora de una reunión.
- **Visión por computadora:** Es la capacidad de aceptar, interpretar y procesar entradas visuales de imágenes, videos y secuencias de cámara en directo. Por ejemplo conteo de personas que entran a una tienda mediante las cámaras de videovigilancia.
- **Discurso:** La capacidad de reconocer y sintetizar la voz humana. Por ejemplo un asistente digital como Alexa o Siri.
- **Procesamiento de lenguaje natural:** La capacidad de procesar lenguaje natural en formato escrito o hablado, analizarlo, identificar puntos clave y generar resúmenes o categorizaciones.
- **Extracción de información:** La capacidad de usar computer vision, voz y procesamiento de lenguaje natural para extraer información clave de documentos, formularios, imágenes, grabaciones y otros tipos de contenido. Por ejemplo la herramienta de gastos previstos de un banco en línea.
- **Soporte de decisiones:** La capacidad de usar datos históricos y correlaciones aprendidas para realizar predicciones que admitan la toma de decisiones empresariales.

- **LLM**: Large Language Model
- **SLM**: Small Language Model

**Los servicios de Azure AI más comunes son:**

| Servicio                                     | Descripción resumida |
|---------------------------------------------|-----------------------|
| **Azure OpenAI**                             | Acceso a modelos generativos de OpenAI (GPT, DALL·E) en la nube de Azure. |
| **Visión de Azure AI**                       | API para análisis de imágenes: objetos, texto, etiquetas y descripciones. |
| **Voz de Azure AI**                          | Convierte voz a texto y texto a voz; incluye traducción y reconocimiento de locutores. |
| **Lenguaje de Azure AI**                     | Análisis de texto natural: entidades, sentimiento, resumen y lenguaje conversacional. |
| **Seguridad del contenido de Azure AI Foundry** | Detecta y marca contenido ofensivo o riesgoso en texto e imágenes. |
| **Traductor de Azure AI**                    | Traducción automática de texto entre múltiples idiomas. |
| **Azure AI Face**                            | Detección y análisis facial con restricciones por privacidad. |
| **Azure AI Custom Vision**                   | Entrena modelos personalizados de clasificación y detección en imágenes. |
| **Inteligencia de Documentos de Azure AI**   | Extrae información estructurada de documentos como facturas y formularios. |
| **Descripción del contenido de Azure AI**    | Analiza contenido multimodal: documentos, imágenes, videos y audio. |
| **Azure AI Search**                          | Motor de búsqueda potenciado por IA que crea índices a partir de contenido. |



**Hay 2 tipos de proyectos en Azure AI Foundry:**

- **Proyectos de fundición foundry:** Este tipo de proyecto permite una configuración sencilla, acceso a agentes y modelos líderes del sector desde OpenAI, Mistral, Meta, etc.
- **Proyectos basados en centros hub:** Si su empresa tiene un equipo administrativo que creó una plataforma para usted, puede crear un proyecto a partir de esa plataforma. Si está trabajando por su cuenta, puede crear un proyecto y se creará automáticamente un centro predeterminado.

<img width="300" alt="Captura de pantalla 2025-06-30 a las 11 51 24" src="https://github.com/user-attachments/assets/6a1c7e4b-134e-42e8-98e6-97c337f4f335" />

**Principios de la IA**:

- Imparcialidad: Sin sesgos de género, etnicidad u otros factores que pueden dar lugar a una ventaja o desventaja desleal a grupos.
- Confiabilidad y seguridad: Deben funcionar de forma confiable y segura. Por ejemplo que un vehículo autónomo sea seguro y confiable.ç
- Privacidad y seguridad: Deben ser seguros y respetar la privacidad, manteniendo los datos privados.
- Inclusión: Una manera de optimizar la inclusión es asegurarse de que el diseño, el desarrollo y las pruebas de la aplicación incluya la entrada de grupos de personas con discapacidad física, etc.
- Transparencia: Deben ser comprensibles, los usuarios deben tener en cuenta plenamente el propósito del sistema, cómo funciona y qué limitaciones se pueden esperar.
- Responsabilidad: Los usuarios y desarrolladores deben entender que la IA debe funcionar en un marco de gobernanza y principios que garanticen los estándares responsables y legales.


### 1.2. Creación y consumo de los [servicios de Azure AI](https://learn.microsoft.com/es-es/azure/ai-services/what-are-ai-services#available-azure-ai-services)

Para aprovisionar los servicios de Azure, se necesita definir un punto de conexión a través del cual una aplicacion puede consumir dicho servicio y se requiere la siguiente información:

- URI del punto de conexión: Esta es la dirección HTTP a la que se puede acceder a la interfaz REST del servicio.
- Una clave de suscripción: Las aplicaciones cliente deben proporcionar una clave válida para consumir el servicio.
- Ubicación del recurso: Al aprovisionar un recurso en Azure, normalmente se le asigna a una ubicación, que determina el centro de datos de Azure en el que se define el recurso.

### 1.3. Protección de los servicios de Azure AI

Los servicios de Azure AI proporcionan varias capas de seguridad que podemos implementar para estar siempre protegidos:

[**Autenticación**:](https://learn.microsoft.com/es-es/training/modules/secure-ai-services/2-authentication)

- Regenerar las claves periodicamente.
- Uso de Azure Key Vaut para almacenar claves de forma segura.
- Autenticación basada en tokens con validez de 10 minutos.
- Autenticación de Microsoft Entra ID: Hay diferentes maneras de autenticarse en los servicios de Azure AI mediante el identificador de Microsoft Entra, entre las que se incluyen:
  1. Autenticación mediante entidades de servicio
  2. Autenticación mediante entidades administradas

[**Implementación de la seguridad de red**:](https://learn.microsoft.com/es-es/training/modules/secure-ai-services/3-implement-network-security)

- Restricciones de acceso de red.
- Cambio de la acción predeterminada.
- Configuración de restricciones de acceso de red (todas las redes, redes seleccionadas, deshabilitado)
- Configuración de reglas de acceso para redes virtuales y direcciones IP
- Configuración de reglas de acceso para conexiones de punto de conexión privado
- Excepciones para servicios de confianza


### 1.4. Supervisión de los servicios de Azure AI
Los pasos para una supervisión de servicios son los siguientes:

- Supervisión de costos de servicios constante y cálculo de costo previo a la implementación de servicios.
- [Creación de alertas](https://learn.microsoft.com/es-es/training/modules/monitor-ai-services/3-create-alerts) mediante reglas de alertas, que mandan notificaciónes en función de eventos o umbrales de métricas establecidos.
- [Visualización de métricas mediante Azure Monitor](https://learn.microsoft.com/es-es/training/modules/monitor-ai-services/4-view-metrics)
- [Administración de registros de diagnóstico](https://learn.microsoft.com/es-es/training/modules/monitor-ai-services/5-manage-diagnostic-logging) que permiten capturar datos operativos muy completos
- [Azure Los Analytics](https://learn.microsoft.com/es-es/training/modules/monitor-ai-services/5-manage-diagnostic-logging) 

### 1.5. Implementar servicios de Azure AI en contenedores

Se pueden usar contenedores que estén en la nube, en una red privada o en e equipo local. Por ejemplo:

- Un servidor Docker
- Una instancia de Azure Container (ACI)
- Un clúser de Azure Kubernetes Service (AKS)

### 1.6. Uso responsable de la inteligencia artificial con la seguridad del contenido de Azure AI Foundry

Se puede usar **Foundry Content Safety** Para garantizar la seguridad y moderar el contenido que se incorpora a los servicios de IA. Este servicio funciona con texto e imágenes, y contenido generado por IA.

<img width="300" alt="Captura de pantalla 2025-06-30 a las 14 13 07" src="https://github.com/user-attachments/assets/eb8f5e53-e837-4f33-a95c-1347d2546222" />

Lo que hace es definir un nivel de gravedad para cada categoría para determinar si el contenido debe bloquearse, enviarse a un moderador o aprobarse automáticamente. Hay que tener claro que es posible que no siempre detecte los contenidos dañinos, por lo que hay que comparar su rendimiento con las métricas de accuracy con VP, FP, VN, FN.


## Módulo 2: Desarrollo de soluciones de Computer Vision de Azure

Con el servicio de Vision de Azure Ai, podemos usar modelos ya entrenados para analizar imágenes y extraer información de ellas. La visión artifical es cuando el software interpresa la información visual, como imágenes o videos. Podemos usar Azure AI Vision para implementar Computer Vision con las siguientes opciones:

- Análisis de imágenes
- Reconocimiento óptico de caracteres (OCR)
- Detección y análisis de caras
- Análisis de videos

### 2.1. Análisis de imágenes

Para conectar al punto de conexión del recurso, debemos ir a Azure Portal o Azure AI Foundry, y buscar una dirección URL similar al siguiente: https://<resource_name>.cognitiveservices.azure.com/ y autenticar la aplicación cliente para poder usar la conexión.
Se puede conectar mediante **Autenticación basada en claves o Autenticación de Microsoft Entra ID.**

```python
from azure.ai.vision.imageanalysis import ImageAnalysisClient
from azure.ai.vision.imageanalysis.models import VisualFeatures
from azure.core.credentials import AzureKeyCredential

client = ImageAnalysisClient(
    endpoint="<YOUR_RESOURCE_ENDPOINT>",
    credential=AzureKeyCredential("<YOUR_AUTHORIZATION_KEY>")
)

result = client.analyze(
    image_data=<IMAGE_DATA_BYTES>, # Binary data from your image file
    visual_features=[VisualFeatures.CAPTION, VisualFeatures.TAGS],
    gender_neutral_caption=True,
)
```

Las características visuales disponibles en VisualFeatures son: **TAGS, OBJECTS, CAPTION, DENSE_CAPTIONS, PEOPLE, SMART_CROPS, READ** y este método devuelve un JSON con toda la información solicitada.

### 2.2. Leer texto en imágenes

Azure AI Vision Image Analysis service usa algoritmos para procesar imágenes y devolver información. En este módulo se explica cómo usar la API de análisis de imágenes para el reconocimiento óptico de caracteres (OCR). Hay varios servicios que extraen texto de imágenes:

- **Azure AI Visión:**
  - Ubicación de texto y extracción de documentos escaneados: leer texto en etiquetas, menús, tarjetas de presentación...
  - Buscar y leer texto en fotografía: señales de tráfico, nombres de calles...
  - Administración de recursos digitales (DAM): descrpción o categorización de un aimagen, catalogar indexar o analizar grandes volúmenes de imágenes...

- **Inteligencia de documentos de Azure AI:** extrae información de documentos digitales complejos. Extrae texto, pares clave-valor, tablas, procesamiento de formularios, modelos precompilados, modelos personalizados...

- **Descriptión del contenido de Azure AI:** (Azure AI Content Understanding) se ocupa de la extracción de contenidos multimodales y escenarios de análisis de contenido personalizados...

### 2.3. Detección, análisis y reconocimiento de caras (Azure AI Face)

Es la capacitdad de las aplicaciones para detectar caras humanas, analizar rasgos faciales y emociones e identificar individuos en imágenes:
- Detección de caras
- Análisis de atributos faciales:
  - Posición de la cabeza
  - Gafas
  - Máscara
  - Desenfoque
  - Ruido visual
  - Objetos que ocultan la cara
  - Accesorios como gafas, gorros, etc
  - QualityForRecognition (bajo, medio, alto)
- Ubicación de punto de referencia facial,
- Comparación de caras
- Reconocimiento facial
- Vivacidad facial, para detectar videos o imágenes falsas

Consideraciones de inteligencia artificial responsable para soluciones basadas en caras:

- Privacidad y seguridad de los datos
- Transparencia
- Equidad e inlusión

  
### 2.4. Clasificación de imágenes

La clasificación de imágenes se usa para determinar el asunto principal de una imagen. Por ejemplo, un sistema de pago automático en una tienda de comestibles podría usar una cámara para escanear cada artículo que un cliente agrega a su carrito y usar la clasificación de imágenes para identificar el producto en la imagen.

el servicio Custom Vision de Azure AI nos permite crear nuestros propios modelos de Computer Visión y para ello necesitramos 2 servicios:

- Custom Visión de Azure AI de entrenamiento
- Custom Vision de Azure AI para generar predicciones

Además podemos usar el [Portal de Custom Vision](https://www.customvision.ai/) para entrenar, publicar y probar modelos.

La clasificación de imágenes es una técnica de Computer Vision en la que se entrena un modelo para predecir una etiqueta de clase para una imagen en función de su contenido, por ejemplo pasándole imágenes de frutas que el modelo sepa predecir de qué fruta se trata. 
<img width="400" alt="Captura de pantalla 2025-07-07 a las 13 31 12" src="https://github.com/user-attachments/assets/f47e5d59-3ccf-453e-86d9-e54a2e5f0b37" />

Normalmente, la etiqueta de clase se relaciona con el asunto principal de la imagen. Para poder usar el portal de Custom visión se puede seguir estos pasos:
- Cree un proyecto de clasificación de imágenes para el modelo y asócielo a un recurso de entrenamiento.
- Cargue imágenes y asigne etiquetas de clase a ellas.
- Revise y edite imágenes etiquetadas.
- Entrenar y evaluar un modelo de clasificación.
- Pruebe un modelo entrenado.
- Publique un modelo entrenado en un recurso de predicción.
- Usar el SDK de Azure AI Custom Vision para desarrollar una aplicación cliente que envíe nuevas imágenes que se van a clasificar.

Para conectarse a Custom Visión de Azure AI desde una aplicación cliente necesitaremos: El punto de conexión y la clave del recurso de predicción de Custom Vision, el identificador del proyecto de clasificación de imágenes y el nombre del modelo implementado.

### 2.5. Detección de objetos en imágenes

La detección de objetos se usa para ubicar e identificar objetos en las imágenes. Por ejemplo, un sistema automatizado de caja en una tienda de comestibles podría usar una cámara para supervisar una cinta transportadora en la que puede haber varios artículos diferentes en todo momento. El sistema podría utilizar la detección de objetos para identificar qué elementos están en la cinta y dónde aparecen en la imagen.

<img width="400" alt="Captura de pantalla 2025-07-07 a las 13 32 54" src="https://github.com/user-attachments/assets/a5a87a7c-4f69-403a-ae88-fcb73f72dee5" />

<img width="400" alt="Captura de pantalla 2025-07-07 a las 13 41 35" src="https://github.com/user-attachments/assets/f452a028-2cc6-4312-855f-63217dfd737a" />

**¿Cuál es la diferencia entre clasificación de imágenes y detección de objetos en imágenes?:** La clasificación de imágenes identifica qué objeto hay en una imagen completa, mientras que la detección de objetos localiza y clasifica múltiples objetos dentro de la imagen usando cajas delimitadoras.

### 2.6. Analizar vídeos

Azure Video Indexer es un servicio para:

- Reconocimiento facial: detección de la presencia de personas individuales en la imagen. Se requiere la aprobación de acceso limitado .
- Reconocimiento óptico de caracteres: lectura de texto en el vídeo.
- Transcripción del discurso: creación de una transcripción de texto del diálogo hablado en el vídeo.
- Temas : identificación de temas clave tratados en el vídeo.
- Opinión : análisis de cómo son los segmentos positivos o negativos del vídeo.
- Etiquetas : etiquetas que identifican temas o objetos clave en todo el vídeo.
- Moderación de contenido : detección de temas adultos o violentos en el vídeo.
- Segmentación de escena: desglose del vídeo en sus escenas constituyentes.

**¿Que son Widgets de Azure Video Indexer?**: Podemos usarlos para reproducir, analizar y editar videos en nuestras propias interfaces HTML personalizadas.

### 2.7. Desarrollo de una aplicación de IA generativa habilitada para la visión
Es la mezcla entre Computer Visión, IA generativa y NLP, llamada interligencia artificial generativa multimodal, que admita no solo datos textuales, sino también datos de imágenes (y, en algunos casos, de audio), por lo que para utilizarlo el usuario debe enviar varias partes; contenido de texto y contenido de imágen.

Se puede pasar la url de una imágen o como dato binario.

### 2.8. Generación de imágenes con IA

Los modelos de generación de imágenes son un modelo de IA generativo que puede crear datos gráficos a partir de la entrada de lenguaje natural. En pocas palabras, puede proporcionar al modelo una descripción y puede generar una imagen adecuada.

Los parámetros de generación de imágenes son:
- prompt: descripción de la imagen que se va a generar.
- n: número de imágenes que se van a generar. DALL-E 3 solo admite n=1.
- size: la resolución de las imágenes que se van a generar (1024x1024, 1792x1024 o 1024x1792 para DALL-E 3)
- calidadOpcional: la calidad de la imagen (estándar o hd). El valor predeterminado es estándar.
- styleOpcional: el estilo visual de la imagen (natural o vívido). El valor predeterminado es vívido.


## Módulo 3: Desarrollo de soluciones de lenguaje natural en Azure

### 3.1. Análisis de texto con Lenguaje de Azure AI

Este servicio nos permite crear aplicaciones y servicios inteligenctes que extraen información semántica de textos y se puede usar para tareas como:
- **Detección de idioma:** devuelve en formato JSON el lenguaje previsto y un valor que indica el nivel de confianza de la predicción. En textos con varios idiomas, devolverá el idioma predominante. Cuando el contenido es ambiguo devolverá un 0.
- **Extracción de frases y palabras clave:** funciona mejor con documentos grandes pero máximo 5120 caracteres. Devuelve una lista JSON con las diferentes frases clave detectadas con indexación.
- **Análisis de sentimiento o opiniones:** Se utiliza para evaluar cómo de positivo o negativo es un texto. Devuelve una clasificación positivo, negativo y neutro entre 0 y 1 para cada clasificación.
- **Reconocimiento de entidades con nombre como entidades, personas, ubicaciones, fehca, hora, organizaciones, dirección, correo electrónico, URL:** devuelve un array JSON con todas las entidades que encuentre
- **Vinculación de entidades:** La vinculación de entidades se puede usar para desambiguar entidades del mismo nombre haciendo referencia a un artículo de una base de conocimiento mediante Wikipedia, por ejemplo dar contexto en una instancia de la palabra "Venus" que puede hacer referencia al planeta o a la diosa de la mitología. Por ejemplo, "Vi Venus brillando en el cielo" está asociado con el vínculo https://en.wikipedia.org/wiki/Venus; mientras que "Venus, la diosa de la belleza" está asociada con https://en.wikipedia.org/wiki/Venus_(mythology)





