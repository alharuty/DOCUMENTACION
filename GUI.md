# GUI (Interfaz Gráfica de Usuario) en Python

## 🔍 ¿Qué es una GUI en Python?
Una **GUI (Graphical User Interface)** o **Interfaz Gráfica de Usuario** en Python permite interactuar con programas mediante elementos visuales como ventanas, botones, menús y cuadros de texto, en lugar de usar solo la línea de comandos.

## 📚 Librerías populares para crear GUIs en Python
Python ofrece varias librerías para desarrollar interfaces gráficas, entre las más usadas están:

1. **Tkinter** (Integrada en Python, fácil de usar)
2. **PyQt** (Basada en Qt, más avanzada y personalizable)
3. **PySide** (Versión oficial de Qt para Python)
4. **Kivy** (Para aplicaciones móviles y multitouch)
5. **PyGTK** (Basada en GTK para interfaces modernas en Linux)
6. **WxPython** (Alternativa ligera y multiplataforma)

Aprender más:
[Guía 1:](https://www.youtube.com/watch?v=hTUJC8HsC2I)
[Guía 2:](https://www.youtube.com/watch?v=M80CzDC1Crc)
[Guía 3:](https://youtu.be/Nf4-gvf-tNg?si=aOPaouruBGPfNkjV)

## 📝 Ejemplo básico con Tkinter

```python
import tkinter as tk

# Crear ventana principal
ventana = tk.Tk()
ventana.title("Mi primera GUI")

# Agregar etiqueta
etiqueta = tk.Label(ventana, text="¡Hola, mundo!")
etiqueta.pack()

# Ejecutar la aplicación
ventana.mainloop()
```


Podemos usar la librería tkinter de forma fácil y rápida porque está integrada en python y en principio no es necesario instalar nada más.

Para usarlo primero debemos importarlo con el script `from tkinter import *` y crear nuestro *programa base* usando `my_program = Tk()` que es como que estamos inicializando el programa base donde iremos creando cada boton y frame. Y ahora ya está listo para ser usado.

| Código                          | Descripción                                                                 |
|----------------------------------|-----------------------------------------------------------------------------|
| `.title`                         | Cambiar el título del programa.                                             |
| `.Label(frame_usado, text="Texto")` | Crear un campo donde se vea el texto "Texto" dentro del frame especificado. |
| `.pack()`                          | Usar este atributo para que un frame funcione correctamente.                |
| `.mainloop()`                    | Usar al final del programa para que entre en un bucle infinito y el programa funcione de forma continua. |
| `.configure(argumentos)`         | Dentro de `configure` se definen los estilos que se deseen aplicar, como colores, tamaños, etc. |
| `.Button(frame_usado, text="Aceptar")`               | Creamos un boton con el texto Aceptar. |
| `.pack_forget()`               | Dejar de visualizar algún frame, boton, label, etc. |


Especificaciones dentro de `.configure`:
| Código                  | Descripción                                |
|-------------------------|--------------------------------------------|
| `bg="black"`            | Cambiar el color de fondo a negro.         |
| `font=("Arial", 16, "bold")` | Cambiar la fuente a Arial, tamaño 16 y en negrita. |
| `padx=20`               | Aplicar un padding de 20px a los lados.    |
| `pady=20`               | Aplicar un padding de 20px arriba y abajo. |
| `fg`               | Color del texto. |
