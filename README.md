# Proyecto: Conteo de Palabras con Docker y MapReduce

##  Descripción

Este proyecto tiene como objetivo realizar un **conteo de palabras** utilizando la técnica de **MapReduce** sobre un archivo de texto `.txt` que contiene el libro completo de *Don Quijote de la Mancha*. Todo el proceso se ejecuta dentro de un **contenedor Docker**, garantizando la portabilidad y consistencia del entorno de trabajo.

##  Características

-  **Entrada**: Archivo de texto plano (`quijote.txt`).
-  **Procesamiento**: Técnica de **MapReduce** implementada para dividir el texto y contar las repeticiones de cada palabra.
-  **Entorno**: Ejecutado en un **contenedor Docker** con un entorno controlado.
-  **Salida**: Archivo `.txt` con el conteo de cada palabra del texto.
-  **Automatización**: Uso de `Dockerfile` para construir la imagen y correr el proceso automáticamente.

##  Tecnologías usadas

- Docker
- Bash
- Sistema de archivos local

## Cómo levantar un nodo de Hadoop con Docker

###  1. Clonar el repositorio

#### 1.1 Crea una carpeta en tus documentos con el nombre de docker-hadoop

Primero, se debe clonar el repositorio que contiene la configuración necesaria para levantar Hadoop en contenedores Docker:

```bash
git clone
```
[https://github.com/big-data-europe/docker-hadoop.git]


### 2. Acceder al directorio

Una vez clonado, entra al directorio del proyecto:
```bash
cd docker-hadoop
```
### 3. Iniciar los contenedores con Docker Compose

Ejecuta el siguiente comando para levantar los cinco contenedores necesarios de forma automática:



