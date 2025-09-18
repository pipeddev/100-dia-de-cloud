# 🌥️ Día 81 – Imágenes y contenedores en Google Cloud

## 📌 Tema

Diferencia entre **imagen** y **contenedor**, y cómo se construyen y ejecutan con tecnologías como **Docker** y **Cloud Build**.

## 📝 Descripción

- Una **imagen** es una aplicación empaquetada con todas sus dependencias.
- Un **contenedor** es una instancia en ejecución de una imagen.

Los desarrolladores crean imágenes de contenedor para **empaquetar y distribuir aplicaciones** sin preocuparse del sistema donde se ejecutarán.
Para compilar y ejecutar imágenes, se usan herramientas como **Docker** o **Cloud Build** en Google Cloud.

### Tecnologías clave en Linux que hacen posible los contenedores

- 🧠 **Procesos de Linux:** cada proceso tiene su propio espacio de memoria virtual.
- 👓 **Namespaces:** definen qué puede “ver” una app (procesos, direcciones IP, directorios, etc.).
- ⚖️ **cgroups:** limitan lo que una app puede usar (CPU, memoria, I/O).
- 📂 **Sistemas de archivos en capas:** empaquetan apps y dependencias en capas reutilizables.

### Imágenes y Dockerfiles

- Una **imagen de contenedor** se estructura en capas de solo lectura.
- El archivo **Dockerfile** define cómo construir esas capas (ej. `FROM`, `COPY`, `RUN`, `CMD`).
- Cuando un contenedor se ejecuta, se agrega una capa superior **efímera y de escritura**.
- Los datos persistentes deben almacenarse fuera del contenedor (ej. volúmenes, bases de datos).

### Buenas prácticas

- Usar **compilación en múltiples etapas**: un contenedor construye la app y otro ejecuta solo lo necesario.
- Colocar las capas menos cambiantes al inicio del Dockerfile, y las que más cambian al final.
- Aprovechar la **reutilización de capas** → solo se descargan/copias las diferencias en cada actualización.

### Repositorios y construcción de imágenes

- 📦 **Artifact Registry (pkg.dev)**: repositorio seguro integrado con IAM para imágenes privadas y públicas.
- 🌍 Repositorios externos: Docker Hub, GitLab Registry.
- ⚙️ **Cloud Build**: servicio administrado que compila contenedores, ejecuta pruebas e integra con repositorios (GitHub, Bitbucket, Cloud Source Repositories).

## ⚙️ Flujo de trabajo típico

1. Escribir un **Dockerfile** para definir la imagen.
2. Usar **Cloud Build** para compilar la imagen.
3. Almacenar la imagen en **Artifact Registry** o en un registro externo.
4. Implementar la imagen en entornos como **GKE, App Engine o Cloud Functions**.

## 🛠️ Herramientas utilizadas

- Docker / Dockerfile
- Linux (processes, namespaces, cgroups)
- Artifact Registry
- Cloud Build
- Google Kubernetes Engine (GKE), App Engine, Cloud Functions

## 🤓 Lo que aprendí

- Una **imagen** es el blueprint de una app, y un **contenedor** es su ejecución real.
- Los contenedores aprovechan tecnologías de Linux para ser ligeros y aislados.
- Las imágenes en capas optimizan actualizaciones y despliegues.
- Cloud Build permite **automatizar la construcción y distribución de imágenes**.
- Es esencial separar datos persistentes del contenedor para evitar pérdidas.

## 🔗 Recursos útiles

- [Cloud Build Overview](https://cloud.google.com/build/docs/overview)
- [Artifact Registry](https://cloud.google.com/artifact-registry)
- [Dockerfile reference](https://docs.docker.com/engine/reference/builder/)

## 🚀 Resultado del día

Hoy entendí cómo funcionan las **imágenes y contenedores**, desde sus bases en Linux hasta la construcción en **Cloud Build** y su despliegue en servicios de Google Cloud, reforzando el concepto de empaquetar aplicaciones de forma **portátil, ligera y eficiente**.
