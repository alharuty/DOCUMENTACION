# Configuración y uso de Logging en Python

## ¿Qué es un sistema de logs?

Un **sistema de logs** es una herramienta que permite registrar eventos, errores y otros tipos de información en una aplicación. Por ejemplo cuando en un proyecto tenemos inputs y esperamos una salida, cuando el input es incorrecto sabemos que imprimimos algo en el terminal para que el usuario sepa que ha ingresado una opción incorrecta y le decimos que vuelva a intentarlo, pues en este caso podemos ingresar un log para que nos guarde dicho error en nuestro archivo de seguimiento de errores. Podemos ver dicho ejemplo más abajo.

Es útil para:
- Depurar errores.
- Monitorear el funcionamiento de la aplicación.
- Registrar información relevante durante la ejecución.

En Python, puedes usar la librería estándar `logging` para gestionar estos registros.

## Niveles de logging

Python proporciona varios niveles de severidad para los logs. Cada nivel tiene un propósito específico:

- **DEBUG**: Información detallada para diagnosticar problemas.
- **INFO**: Información general sobre el estado de la aplicación.
- **WARNING**: Mensajes que indican que algo inesperado ocurrió, pero no es un error grave.
- **ERROR**: Indica que ocurrió un error que afecta una operación.
- **CRITICAL**: Errores graves que podrían detener el programa.

## ¿Dónde poner la configuración de los logs?

### Opción 1: Configuración dentro del mismo archivo `proyecto.py`

En proyectos pequeños o cuando tienes solo un archivo, puedes configurar el logging directamente en el archivo principal.


- <font color="green">Ventajas:</font> Rápido y sencillo para proyectos pequeños
- <font color="red">Desventajas:</font> Puede vovlerse desordenado si el proyecto crece.

### Opción 2: Configuración en un archivo separado `logging_config.py`

Para proyectos más grandes, puedes separar la configuración de los logs en un archivo independiente `logging_config.py` e importarlo en cualquier parte de nuestro pryecto `proyecto.py`.

- <font color="green">Ventajas:</font> Centraliza la configuración de logging, lo que facilita el mantenimiento. Ideal para proyectos medianos o grandes.
- <font color="red">Desventajas:</font> Requiere más archivos y organización, lo que puede ser innecesario para proyectos pequeños.


Ver más informacion [en](https://atareao.es/pyldora/tus-logs-en-python-de-forma-eficiente/#:~:text=El%20logging%20en%20Python%20es,diagnosticar%20problemas%20en%20tiempo%20real)
