# Instalación.

### Paso 1: Configuración del Entorno 1. 

1. Crea un nuevo directorio para tu proyecto. 

```bash
mkdir mi-documentacion 
cd mi-documentacion
```

2. Crea un entorno virtual de Python: 

`python -m venv venv`

3. Activa el entorno virtual. 

En Windows: `venv\Scripts\activate`

Como me da error en la utilización de scripts, sigo los siguientes pasos:
* Ejecuto el comando `Get-ExecutionPolicy -List` y veo que no está definida la política de ejecución de scripts.
* Ejecuto el comando `Set-ExecutionPolicy RemoteSigned -Scope CurrentUser `
* Ejecuto de nuevo `venv\Scripts\activate`

4. Instala MkDocs y el tema Material. 

`pip install mkdocs mkdocs-material`