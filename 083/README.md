# 🌥️ Día 83 – Google Kubernetes Engine (GKE)

## 📌 Tema

Introducción a **Google Kubernetes Engine (GKE)**, el servicio administrado de Kubernetes en Google Cloud.

## 📝 Descripción

**Kubernetes** es muy potente, pero administrarlo de forma manual puede ser complejo y demandante.
Aquí es donde entra **Google Kubernetes Engine (GKE)**: un servicio administrado que implementa, administra y escala clústeres de Kubernetes sobre la infraestructura de Google Cloud.

🔹 GKE elimina la necesidad de **aprovisionar y mantener la infraestructura subyacente**.
🔹 Usa un **sistema operativo optimizado para contenedores**, con huella mínima y capacidad de escalar rápidamente.
🔹 Ofrece dos modos de operación:

- **Estándar:** control total sobre los nodos y configuración.
- **Autopilot:** GKE administra de manera automática nodos, escalado, seguridad y configuración.

## ⚙️ Características principales

- 🔄 **Actualizaciones automáticas:** mantiene los clústeres en la última versión estable de Kubernetes.
- 🛠️ **Autoreparación de nodos:** detecta nodos dañados, los drena y los reemplaza automáticamente.
- 📈 **Escalado automático:** tanto de cargas de trabajo como del propio clúster.
- 🔗 **Integraciones nativas con GCP:**

  - **Artifact Registry:** almacenamiento seguro de imágenes.
  - **Cloud Build:** automatización de despliegues.
  - **IAM:** control de acceso basado en roles.
  - **Cloud Monitoring:** métricas y observabilidad de aplicaciones.
  - **VPCs y Load Balancing:** redes seguras y balanceadores de carga integrados.

- 📊 **Consola de Google Cloud:** panel centralizado para ver, revisar y gestionar recursos de clústeres.

## 🛠️ Herramientas utilizadas

- Google Kubernetes Engine (GKE)
- Cloud Build
- Artifact Registry
- Cloud IAM
- Cloud Monitoring
- VPC & Load Balancing

## 🤓 Lo que aprendí

- **GKE simplifica la gestión de Kubernetes**, liberando a los equipos de la complejidad de la infraestructura.
- El modo **Autopilot** es ideal para quienes buscan enfocarse en las aplicaciones sin administrar nodos.
- La **autoreparación y actualización automática** hacen que los clústeres sean más resilientes.
- Con las integraciones nativas de GCP, se obtiene un ecosistema completo para construir, desplegar y monitorear apps en contenedores.
- GKE convierte Kubernetes en una plataforma lista para producción con menos fricción.

## 🔗 Recursos útiles

- [Google Kubernetes Engine Overview](https://cloud.google.com/kubernetes-engine/docs/concepts)
- [Autopilot vs Standard modes](https://cloud.google.com/kubernetes-engine/docs/concepts/autopilot-overview)

## 🚀 Resultado del día

Hoy aprendí cómo **Google Kubernetes Engine (GKE)** lleva la potencia de Kubernetes a un nivel administrado, ofreciendo escalabilidad, seguridad y resiliencia con integraciones nativas en Google Cloud.
