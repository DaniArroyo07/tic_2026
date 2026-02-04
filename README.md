# CICD de APPScript
Para trabajar de forma eficiente en la nube, seguimos estos pasos para dejar el entorno listo para desarrollo:
## Configuración del repositorio y codespace
Para comenzar, debemos establecer una base en nuestro entorno de desarrollo. Para ello deberemos:
 - <b>Configurar el entorno: </b>Al iniciar nuestro proyecto en Codespace, deberemos preparar la zona de desarrollo, es decir, comprobar que tenemos el repositorio clonado y vinculado a GitHub.
 - <b>Instalaciones necesarias: </b> La instalación necesaria es la de clasp, para que la terminal reconozca los comandos.
 - <b>Habilitar la Google Apps Script API:</b> Sin la activación de esta, las herramientas externas no podrán interactuar con nuestros proyectos.
    [Enlace a Google Apps Script API](script.google.com/home/settings)

## Autenticación de Clasp
Una vez preparado la zona de trabajo, deberemos decir quien está modificando el código, donde, mediante el login, se genera un archivo que contiene los tokens de acceso necesarios.

## Estructura del proyecto
Mantener un orden de archivos es clave para que el pipeline de CI/CD funcione correctamente y el código sea mantenible.

 - <b>Estructura del proyecto:</b> Definiremos una jerarquía u orden donde los archivos de configuración residan en la raíz, mientras que la lógica se organiza en carpetas dedicadas

 - <b>Módulo de generación de documentos:</b> En este archivo se centraliza la programación principal. Aquí es donde desarrollamos las funciones encargadas de interactuar con el entorno de Google 

 ## Pipeline de CI/CD
 La parte final consiste en automatizar todo el proceso para que no tengamos que subir los cambios manualmente. Para ello, deberemos configurar un archivo que se encargue de:

 1. Detectecambios en el código
 2. Instale las herramientas automáticamente
 3. Utilizar las credenciales guardadas en GitHub
 4. Desplegar la última versión del código