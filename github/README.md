# 📘 Resumen de lo aprendido en GitHub

## 🔹 1. Configuración inicial en tu PC

* Instalar Git y configurar identidad:

  ```bash
  git config --global user.name "EAI-IA"
  git config --global user.email "ervin.academic@gmail.com"
  ```
* Autenticación SSH configurada con GitHub → subir/cargar sin usuario/contraseña.

---

## 🔹 2. Creación y sincronización de repositorios

Cada curso tiene su propio repositorio (privado). Pasos típicos:

### Paso 1: Inicializar el repositorio local

```bash
cd /ruta/del/curso
mkdir NOMBRE_REPO
cd NOMBRE_REPO

git init
```

### Paso 2: Crear `.gitignore`

Para evitar subir archivos innecesarios:

```bash
echo "__pycache__/
.ipynb_checkpoints/
*.pyc
*.pyo
*.pyd
*.so
*.log
*.DS_Store
.vscode/" > .gitignore
```

### Paso 3: Conectar con GitHub

```bash
git branch -M main
git remote add origin git@github.com:EAI-IA/NOMBRE_REPO.git
```

### Paso 4: Primer commit y push

```bash
git add .
git commit -m "Primer commit - curso X"
git push -u origin main
```

---

## 🔹 3. Flujo de trabajo diario (actualizaciones)

#### * ¿Dónde entra el comando git clone?
    Ese paso va antes de cualquier modificación, y solo lo usas cuando no tienes ya el repositorio local.
    Es decir:
    - Si es la primera vez en una máquina nueva → clonas.
    - Si ya tienes la carpeta local → solo haces git pull para actualizar.

* Clonar el repositorio (solo la primera vez en una máquina nueva):
  ```bash
  git clone git@github.com:EAI-IA/NOMBRE_REPO.git
  cd NOMBRE_REPO
  ```

* Actualizar a la última versión (cuando ya tienes el repo local):
  ```bash
  git pull
  ```

* Hacer cambios

* Guardar cambios:

  ```bash
  git add .
  git commit -m "Descripción del cambio"
  ```
* Subir a GitHub:

  ```bash
  git push
  ```
* Ver cambios:

  ```bash
  git status
  ```
---

## 🔹 4. Manejo de errores comunes

* **Repositorios embebidos** (`projetomachado`): Git los trata como submódulos.

  * Solución: borrar `.git/` interno o usar `git submodule add`.
* **Nombres inválidos** (`Programação`): GitHub no acepta acentos ni caracteres especiales.

  * Solución: usar `OOP_Programacao`.
* **Archivos grandes >50 MB** (.pth, datasets): GitHub recomienda **Git LFS** o excluirlos.

  * Solo se suben scripts y configuraciones, no modelos enormes.

---

## 🔹 5. Environments de Conda

No subir el environment completo (muy pesado). Guardar la receta del entorno:

* Con Conda:

  ```bash
  conda env export > environment.yml
  conda env create -f environment.yml
  ```

* Con pip:

  ```bash
  pip freeze > requirements.txt
  pip install -r requirements.txt
  ```

---

## 🔹 6. Buenas prácticas

* Mantener repositorios **privados** para cursos personales.
* Cada curso en su propio repo → más organizado.
* Incluir `README.md` explicando el curso y uso.
* Incluir `environment.yml` o `requirements.txt` para reproducir entornos.

---

# 🚀 En conclusión

Aprendí a:

* Configurar Git y conectarlo con GitHub vía SSH.
* Crear y subir repositorios privados (uno por curso).
* Sincronizar cambios (push/pull).
* Resolver problemas comunes (submódulos, nombres inválidos, archivos grandes).
* Mantener limpio el repo con `.gitignore`.
* Exportar y versionar environments con `environment.yml` o `requirements.txt`.
