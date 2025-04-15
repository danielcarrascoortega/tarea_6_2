# Configuración.

## Creación y Configuración de MKDocs.

### Paso 2: Crear el Proyecto MkDocs.

1- Inicializa un nuevo proyecto **MkDocs** en el directorio actual:

`mkdocs new .`

2- Esto creará dos archivos importantes:

- `mkdocs.yml` : El archivo de configuración
- `docs/index.md` : Tu página principal

### Paso 3: Configurar MkDocs.

1- Abre el archivo `mkdocs.yml` y configura el tema **Material**:

 `site_name: Mi Documentación`  
 `theme:`  
 `name: material`  
 `features:`  
  `- navigation.tabs`  
  `- navigation.sections`  
  `- navigation.expand`  
  `- content.code.cop`  
 
### Paso 4: Crear la Estructura de Documentación.

1- En la carpeta docs , crea la siguiente estructura:

 docs/  
 ├── index.md  
 ├── guia/  
 │  ├── instalacion.md  
 │  ├── configuracion.md  
 │  └── despliegue.md  
 └── ejemplos/  
    └── ejemplo1.md

2- Edita el archivo `docs/index.md`  


 \# Bienvenido a Mi Documentación

 Esta es la página principal de mi documentación.

 \## Contenido

 \- \[Guía de Instalación](guia/instalacion.md)  
 \- \[Configuración](guia/configuracion.md)  
 \- \[Despliegue](guia/despliegue.md)  