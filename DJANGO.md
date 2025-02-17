`python -m venv django` : crear entorno virtual

`source django/bin/activate` : activarlo

`pip install django` : instalar django

`django-admin --version` : ver la version de django

`django-admin startproject my_django` : crear el proyecto django

`cd my_django` : entrar en el proyecto

`python manage.py runserver` : correr el servidor

`python manage.py migrate`: migrar dependencias si hace falta

`django-admin startapp nombre_app` : crear la aplicación

`python3 manage.py makemigrations` : crear las migraciones

`python3 manage.py createsuperuser` : crear el superusuario, rellenar los datos de usuario

`python3 manage.py runserver` : correr el servidor, nos abrirá en internet el proyecto

en navegador: 127.0.0.1:8000/admin : acceder al admin

En settings.py > INSTALLED_APPS > añadir en un string el nombre de nuestra app