# Despliegue.

## Configuración y Despliegue en GitHub.

### Paso 5: Crear un Repositorio en GitHub.

1- Ve a GitHub y crea un nuevo repositorio. Asegúrate de crearlo como un repositorio público para que la documentación sea accesible en *GitHub Pages*.

2- Inicializa Git en tu proyecto local:

`git init`

3- Crea un archivo `.gitignore` en el directorio raíz de tu proyecto con el siguiente contenido:

`venv/`

4- Realiza el primer *commit* y vincula tu repositorio remoto:

```bash
git add .
git commit -m "Primer commit"
git branch -M main
git remote add origin git@github.com:danielcarrascoortega/tarea_6_2.git
git push -u origin main
```

### Paso 6: Configurar GitHub Pages

1- Ve a la configuración de tu repositorio en **GitHub**.
2- Navega a la sección "*Pages*".
3- En "*Source*", selecciona *Deploy from a branch*, y elige *gh-pages* como rama.

No me aparece *gh-pages* como rama por lo que continúo con el proceso y continuaré más adelante con este paso.

4- Crea un nuevo archivo `.github/workflows/deploy.yml` en el directorio raíz de tu repositorio con el siguiente contenido:

```bash
name: Deploy MkDocs
 on:
  push:
    branches: [ main ]
 jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: actions/setup-python@v2
        with:
          python-version: '3.x'
      - run: pip install mkdocs-material
      - run: mkdocs gh-deploy --force
```

### Paso 7: Configurar Github actions.

1. Ve a la sección "*Actions*" de tu repositorio, y selecciona la sección *General*.

2. En la sección *Workflow Permissions*, selecciona "*Read and write access*" para permitir que el flujo de trabajo pueda hacer push a la rama *gh-pages*.

### Paso 8: Desplegar la Documentación.

1- Haz commit de los cambios en el archivo `.github/workflows/deploy.yml` y realiza un push a la rama main:

```bash
 git add .
 git commit -m "Configuración de GitHub Pages"
 git push origin main
```

2- Ve a la sección "*Actions*" de tu repositorio para ver el progreso del despliegue.

### Vuelvo al Paso 6.
1. Ve a la configuración de tu repositorio en GitHub. 
2. Navega a la sección "*Pages*" 
3. En "*Source*", selecciona *Deploy from a branch*, y elige *gh-pages* como rama.
4. Vuelvo a intentar el despliegue.

### Resultados

* Una vez completado, tu documentación estará disponible en: [Enlace a la documentación](https://danielcarrascoortega.github.io/tarea_6_2/)
* Enlace al repositorio en **GitHub**: [Enlace al repositorio](https://github.com/danielcarrascoortega/tarea_6_2)