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

Se debe clonar el repositorio que contiene la configuración necesaria para levantar Hadoop en contenedores Docker:


[https://github.com/big-data-europe/docker-hadoop.git]


#### 1.2 Descomprime el archivo descargado en la carpeta que ya creaste con el nombre de: docker-hadoop


### 2. Acceder al directorio

Una vez clonado, entra al directorio del proyecto:
```bash
cd docker-hadoop
```
### 3. Iniciar los contenedores con Docker Compose

Ejecuta el siguiente comando para levantar los cinco contenedores necesarios de forma automática:

```bash
docker-compose up -d
```
#### Si es la primera vez que ejecutas este comando, Docker descargará las imágenes necesarias. Esto puede tardar algunos minutos.

#### ¿Qué hace docker-compose?

docker-compose es una herramienta que permite definir y ejecutar aplicaciones Docker multicontenedor a partir de un solo archivo de configuración (docker-compose.yml). Este archivo contiene todas las instrucciones necesarias para construir y levantar los servicios requeridos.

### 4. Verificar que los contenedores están corriendo

Puedes comprobar que los contenedores están en ejecución de dos formas:
Desde la terminal:

```bash
docker ps
```
Desde Docker Desktop:

Abre Docker Desktop y verifica que los cinco contenedores del proyecto docker-hadoop estén activos.

Este entorno permite levantar un clúster Hadoop completamente funcional en tu máquina local, ideal para pruebas, desarrollo y aprendizaje en temas de Big Data.


## Estructura General

### Entrar al nodo maestro namenode 

Ejecutar

```bash
    docker exec -it namenode bash
```

### Accedemos a nuestro contenedor namenode, es el nodo maestro de nuestro clúster Hadoop. 
### Crear una estructura de carpetas para archivos de entrada

Enumerar todos los archivos en nuestro sistema HDFS : 

```bash
    hdfs dfs -ls / 
```

Tenemos que crear la caperta /user/root/, ya que hadoop trabaja con esta estructura definida, para lo anterior ejecutamos

```bash
    hdfs dfs -mkdir -p /user/root/ 
```

Podemos verificar si se creó correctamente: 

```bash
    hdfs dfs -ls /user/
```






