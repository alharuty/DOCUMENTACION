# Configuración de GitHub Actions con `act` en local

## 1. Crear la carpeta `.github` dentro del repositorio
```sh
mkdir .github
```

## 2. Instalar `act` globalmente
```sh
pip install act
```

## 3. Abrir Docker  
Es necesario para ejecutar `act`.

## 4. Crear la carpeta `workflows` dentro de `.github`
```sh
mkdir -p .github/workflows
```

## 5. Crear un archivo de workflow (`demo.yaml`)
```sh
touch .github/workflows/demo.yaml
```

## 6. Agregar el siguiente contenido a `demo.yaml`
```yaml
name: GitHub Actions Demo
run-name: ${{ github.actor }} is testing out GitHub Actions 🚀
on: [push]
jobs:
  Explore-GitHub-Actions:
    runs-on: ubuntu-latest
    steps:
      - run: echo "🎉 Job triggered by ${{ github.event_name }} event."
      - run: echo "🐧 Running on a ${{ runner.os }} server hosted by GitHub."
      - run: echo "🔎 Branch: ${{ github.ref }} | Repo: ${{ github.repository }}"
      - name: Check out repository code
        uses: actions/checkout@v4
      - run: echo "💡 Repo cloned to runner."
      - run: echo "🖥️ Ready to test code."
      - name: List repository files
        run: ls ${{ github.workspace }}
      - run: echo "🍏 Job status: ${{ job.status }}"
```

## 7. Funcionalidad  
Esta acción se ejecuta cuando hacemos `push`. Permite verificar que todo funciona antes de subirlo a remoto.

## 8. Probar la acción en local con `act`
- **Listar las acciones disponibles**:
  ```sh
  act --list
  ```
- **Ejecutar el workflow y verificar que todo está bien**:
  ```sh
  act
  ```

## 9. Instalar la extensión **GitHub Actions** en Visual Studio Code *(opcional)*  
Facilita la gestión de workflows.

---

Este documento es una guía rápida para configurar GitHub Actions y probarlo en local con `act`. 
