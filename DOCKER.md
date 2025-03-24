Comandos básicos de docker:

1. Ver las imágenes que tenemos:
```bash
docker ps
```
2. Desactivar una imagen:
```bash
docker stop nombre-imagen
```
3. Arrancar terminal bash del contenedor:
```bash
docker exec -it nombre-imagen bash
```
4. Crear un contenedor:
```bash
docker build -t usuario/nombre-que-queremos .
```
5. Correr el contenedor:
```bash
docker run -p 8000:8000 usuario/nombre-que-hemos-puesto
```
