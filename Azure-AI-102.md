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















