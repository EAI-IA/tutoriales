### Paso 1: Crear un nuevo repositorio en GitHub

1. **Inicia sesión en GitHub.**
2. **Haz clic en el botón "New"** (Nuevo) en la esquina superior derecha o ve a [Crear un nuevo repositorio](https://github.com/new).
3. **Completa los campos:**
    - **Repository name**: Elige un nombre único para tu repositorio.
    - **Description**: (Opcional) Describe brevemente el repositorio.
    - **Visibility**: Selecciona si deseas que sea público o privado.
    - **Initialize this repository with**:
        - Puedes marcar "Add a README file" para crear un archivo README inicial.
        - Selecciona un template para `.gitignore` si es necesario.
        - Escoge una licencia si lo deseas.
4. **Haz clic en "Create repository"**.

### Paso 2: Clonar el repositorio

Una vez creado, clona el nuevo repositorio a tu máquina local:

```bash
git clone <https://github.com/tu_usuario/nombre_del_repositorio.git>

```

Reemplaza `tu_usuario` y `nombre_del_repositorio` con los valores correspondientes.

### Paso 3: Navegar al directorio del repositorio

Cambia al directorio del nuevo repositorio:

```bash
cd nombre_del_repositorio

```

### Paso 4: Agregar y modificar archivos

1. **Crea la estructura de carpetas** y archivos que necesites.
2. **Agrega contenido** a los archivos.

### Paso 5: Realizar commits

Cada vez que realices cambios, agrega y comitea esos cambios:

```bash
git add .
git commit -m "Descripción de los cambios realizados"

```

### Paso 6: Hacer push a GitHub

Cuando estés listo para subir tus cambios al repositorio remoto, ejecuta:

```bash
git push origin main

```

### Paso 7: Mantener el repositorio actualizado

1. **Para actualizar el repositorio**:
    - Realiza cambios en tus archivos y repite los pasos 4 a 6.
2. **Si trabajas en un entorno colaborativo**, asegúrate de hacer `git pull` antes de hacer un push para integrar cualquier cambio que otros hayan realizado.

### Otras consideraciones

- Si tu proyecto crece, considera crear ramas para nuevas características o cambios significativos.
- Mantén tu archivo README y otros documentos actualizados.

Si necesitas ayuda en algún paso específico o más detalles, ¡avísame!

Si vas a agregar un “repositorio embebido” tienes que hacer lo siguiente.

```python
git submodule add <url_del_repositorio> <lab4-5/automate-youtube-with-crewai>
# URL DEL REPOSITO   ------  NOMBRE DEL REPOSITORIO DESDE LA UBICACION DEL REPOSTORIO PRINCIPAL
```

- Luego borrar la referencia del indice
    
    ```python
    git rm --cached lab4-5/automate-youtube-with-crewai
    ```
    

### Paso 8: Actualización

**Realiza un nuevo commit:**
Una vez que hayas eliminado las claves, guarda los cambios y haz un nuevo commit:

```
git add config.py test/gs_slct_input.py intro/lab1.py
git commit -m "Eliminar claves sensibles"
```

**Haz un `push` de nuevo: A**hora puedes intentar hacer el `push` de nuevo:

```
git push origin main
```

Token - setting develp

email: ervin.academic@gmail.com

Usernamer: EAI-IA

Pass: ghp_xxxxxxx

## Solución a trabajar con **repositorio** **Privados**

Pasos para Generar un Token de Acceso Personal (PAT)

1. **Ir a GitHub**:
    - Accede a tu cuenta en [GitHub](https://github.com/).
2. **Ir a Configuración**:
    - Haz clic en tu avatar en la esquina superior derecha.
    - Selecciona "Settings".
3. **Desarrollador**:
    - En el menú de la izquierda, selecciona "Developer settings".
4. **Tokens**:
    - Selecciona "Personal access tokens".
    - Haz clic en "Tokens (classic)".
5. **Generar nuevo token**:
    - Haz clic en "Generate new token" (Generar nuevo token).
    - Asigna un nombre al token.
    - Selecciona los permisos necesarios (por ejemplo, "repo" para acceso a repositorios).
6. **Generar y copiar el token**:
    - Haz clic en "Generate token".
    - **Copia el token** y guárdalo en un lugar seguro (no podrás volver a verlo).
