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

