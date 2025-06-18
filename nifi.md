# [nifi](https://nifi.apache.org/) con Daniel Torbellino en F5

Es una interfaz de ingesta y administración de datos, de principio hasta la nube.

1. [Descargar](https://www.youtube.com/watch?v=x9BVUJxp3ss)
2. Para saber en qué browser funciona, ir a README y buscar algo como `https://localhost:8443/nifi/`
3. Ver estado de nifi: `bin/nifi.sh status`
4. Añadir JAVA_HOME si no lo tiene: `export JAVA_HOME=/opt/homebrew/opt/openjdk@21/libexec/openjdk.jdk/Contents/Home`
5. Buscar clave y usuario: ir a logs/nifi-app.log y buscar la palabra `generated` y encontrar el usuario y clave.
6. Arrancar nifi: `bin/nifi.sh start`
7. Ir al navegador a la ruta correcta: `https://localhost:8443/nifi/`
8. Loggearse con el usuario y clave que encontramos en logs/nifi-app.log


<img width="1325" alt="Captura de pantalla 2025-06-18 a las 12 04 27" src="https://github.com/user-attachments/assets/4619263e-c2de-4d0e-a021-2be11661c4bb" />
/
