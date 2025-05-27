# 📅 Día 015 – Aplicaciones en la nube

## 📌 Tema

Explorar las opciones y beneficios de usar VMs, almacenamiento y contenedores en la nube, y desarrollar un laboratorio práctico con Cloud Run.

---

## 📘 Cloud Run

**Cloud Run** es una plataforma serverless completamente administrada que permite ejecutar contenedores sin estado en respuesta a solicitudes HTTP o eventos de Pub/Sub.

### Características principales:

- Basada en **Knative**, compatible con Kubernetes.
- Sin gestión de infraestructura: solo enfócate en tu código.
- Escala automática desde cero en milisegundos.
- Modelo de facturación por uso: en incrementos de 100 ms.
- Ejecuta cualquier contenedor compilado para Linux de 64 bits.

### Lenguajes compatibles:

- Populares: Java, Python, Node.js, PHP, Go, C++
- También soporta otros como: COBOL, Haskell, Perl

---

## 🔁 Flujo de trabajo en Cloud Run

1. Escribir tu aplicación con tu lenguaje favorito.
2. Empaquetarla como una imagen de contenedor.
3. Subir la imagen a Artifact Registry y desplegarla en Cloud Run.

Una vez desplegado, Cloud Run te asigna una URL HTTPS única. Los contenedores se inician automáticamente en respuesta a solicitudes entrantes.

---

## ⚙️ Cloud Run Functions

**Cloud Run Functions** es una solución ligera, asincrónica y basada en eventos.

- Crea funciones pequeñas que reaccionan a eventos (Cloud Storage, Pub/Sub, etc).
- No se requiere administrar servidores ni entornos.
- Soporta: Node.js, Python, Go, Java, .NET Core, Ruby y PHP.
- Facturación precisa por 100 ms de ejecución.

---

## 🔬 Lab realizado

**Objetivo**: Desplegar una app Node.js en Cloud Run

### Pasos realizados:

1. **Habilitar API de Cloud Run**
   ```bash
   gcloud services enable run.googleapis.com
   ```
2. **Establecer región y variables**
   ```bash
   gcloud config set compute/region us-east1
   export LOCATION="us-east1"
   ```
3. **Compilar contenedor con Cloud Build**
   ```bash
   gcloud builds submit --tag gcr.io/$GOOGLE_CLOUD_PROJECT/helloworld
   ```
4. **Listar imágenes del proyecto**
   ```bash
   gcloud container images list
   ```
5. **Configurar autenticación de Docker**
   ```bash
   gcloud auth configure-docker
   ```
6. **Desplegar contenedor en Cloud Run**

   ```bash
   gcloud run deploy --image gcr.io/$GOOGLE_CLOUD_PROJECT/helloworld \
   --allow-unauthenticated --region=$LOCATION
   ```

7. **Borrar imagen y servicio al finalizar**
   ```bash
   gcloud container images delete gcr.io/$GOOGLE_CLOUD_PROJECT/helloworld
   gcloud run services delete helloworld --region=us-east1
   ```

---

## 🛠️ Herramientas utilizadas

- Google Cloud Skills Boost
- Cloud Run
- Artifact Registry
- Cloud Build
- gcloud CLI

---

## ✅ Lo que aprendí

- Cómo crear, compilar y desplegar contenedores en Cloud Run.
- Cómo funciona el modelo serverless y la escalabilidad automática.
- Cómo conectar los servicios: Cloud Build + Artifact Registry + Cloud Run.
- Flujo completo de despliegue sin administrar infraestructura.
- Usar gcloud para automatizar tareas de desarrollo y limpieza.

---

## 📚 Recursos útiles

- [Documentación oficial de Cloud Run](https://cloud.google.com/run/docs)

---

## 🎯 Resultado del día

Aprendí a implementar aplicaciones sin servidor usando contenedores y servicios completamente gestionados por Google Cloud.
Este flujo me da flexibilidad, escalabilidad y eficiencia sin preocuparme por la infraestructura.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
