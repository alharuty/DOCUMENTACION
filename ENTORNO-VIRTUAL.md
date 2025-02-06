# Uso de Entornos Virtuales en Python

Un **entorno virtual en Python** es una herramienta que te permite crear un espacio aislado para instalar paquetes y librerías sin afectar el sistema global de Python ni otros proyectos. Es especialmente útil en proyectos para garantizar que todas las dependencias sean consistentes.


> [!CAUTION]
> Hay que tener en cuenta que dichas dependencias están instaladas y se pueden usar SOLO en dicho entorno.<br>
> **Es decir, si estamos en un entorno virtual y descargamos un paquete o unas dependencias, éstas solo estarán disponibles dentro de dicho entorno, y cuando salgamos del entorno no las podremos usar porque no están en Global**


> [!IMPORTANT]
> Cada entorno virtual trabaja en la carpeta donde se ha creado inicialmente.<br>
> Imprescindible **ACTIVAR** el entorno virtual cada vez que vayamos a trabajar en un repositorio.<br>
> Incluir el repositorio **nombre_entorno/** en en archivo **.gitignore**


> [!NOTE]
> Es preferible como método de guía, llamar al entorno virtual igual que el proyecto o repositorio donde estamos trabajando.
> Es aconsejable **desactivarlo** cada vez que vayamos a dejar de trabajar en dicho repositorio o proyecto, aunque si apagamos el ordenador éste se desactivará por sí solo.

## **¿Por qué usar un entorno virtual?**
1. **Evita conflictos** entre dependencias de diferentes proyectos.
2. **Mantiene tu entorno limpio**, sin instalar paquetes innecesarios globalmente.
3. **Facilita la colaboración**, ya que otros desarrolladores pueden instalar exactamente las mismas versiones de las librerías usando un archivo `requirements.txt`.

---

## **Cómo crear y usar un entorno virtual en Python**
Como ya tienes tu código en marcha, **sí puedes activarlo ahora sin problemas**. Solo sigue estos pasos:

### **1️⃣ Crear el entorno virtual**
Abre la terminal en la carpeta de tu proyecto y ejecuta:

```sh
python -m venv venv
```
Esto crea una carpeta llamada `venv` que contendrá el entorno virtual.

---

### **2️⃣ Activar el entorno virtual**
Dependiendo del sistema operativo, usa uno de estos comandos:

- **Windows (CMD o PowerShell)**:
  ```sh
  venv\Scripts\activate
  ```
  (Si usas PowerShell y da error, ejecuta `Set-ExecutionPolicy Unrestricted -Scope Process` antes de activar.)

- **Mac/Linux**:
  ```sh
  source venv/bin/activate
  ```

Cuando el entorno esté activo, verás algo así en la terminal:

```
(venv) usuario@pc:~/mi_proyecto$
```

---

### **3️⃣ Instalar dependencias**
Si ya has usado paquetes en tu código sin el entorno virtual, puedes reinstalarlos dentro del entorno con:

```sh
pip install -r requirements.txt
```

Si no tienes un `requirements.txt`, genera uno con:

```sh
pip freeze > requirements.txt
```

---

### **4️⃣ Desactivar el entorno virtual**
Cuando termines de trabajar, puedes salir del entorno virtual con:

```sh
deactivate
```

---

### **5️⃣ Agregar `venv` a `.gitignore`**
Para evitar subir el entorno virtual a GitHub (no es necesario compartirlo), edita o crea un archivo `.gitignore` en la raíz del proyecto y agrega:

```
venv/
```

Con esto, puedes trabajar con un entorno virtual en tu proyecto sin afectar nada de lo que ya has hecho. 🚀

