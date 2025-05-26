# 📅 Día 014 – Contenedores en la nube

## 📌 Tema

Explorar los conceptos fundamentales de los contenedores, el uso de Kubernetes como orquestador y su implementación en Google Cloud mediante Google Kubernetes Engine (GKE).

---

## 📘 Descripción

Hoy estudié el funcionamiento de los **contenedores** en la nube y cómo se gestionan usando **Kubernetes**. También aprendí cómo utilizar **Google Kubernetes Engine (GKE)**, el servicio administrado de Kubernetes de Google Cloud.

### 🧱 Contenedores

- En IaaS, los recursos de hardware se virtualizan mediante VMs, donde cada desarrollador puede instalar su propio SO.
- Los contenedores brindan una capa de abstracción sobre el sistema operativo y el hardware, lo que facilita la portabilidad, el aislamiento y la eficiencia.
- Permiten empaquetar todo un entorno de ejecución: servidor web, base de datos, configuración y dependencias.

### ☸️ Kubernetes

- Plataforma de código abierto para administrar contenedores a gran escala.
- Organiza contenedores en **Pods**, la unidad mínima de ejecución.
- Usa **Deployments** para mantener la disponibilidad de Pods replicados.
- Expone los Pods mediante **Services**, proporcionando una IP estable dentro del clúster.

#### 📌 Comandos útiles

```bash
kubectl get pods      # Lista los Pods activos
kubectl get services  # Lista los Services disponibles
```

### 🚀 Google Kubernetes Engine (GKE)

**GKE** es el servicio administrado de Kubernetes en Google Cloud que permite desplegar clústeres sin necesidad de gestionar la infraestructura directamente.

- Los clústeres están formados por **instancias de Compute Engine** agrupadas.

#### Modos disponibles:

🔹 **Autopilot**

- Google administra la infraestructura subyacente.
- Incluye seguridad reforzada, escalado automático y actualizaciones.
- Ideal para entornos de producción y eficiencia operativa.

🔹 **Standard**

- El usuario tiene control total sobre la configuración y operación del clúster.
- Requiere gestionar nodos, escalado y actualizaciones manualmente.

---

### 🧪 Implementación

Puedes crear clústeres de GKE a través de:

- La **consola de Google Cloud**
- El comando `gcloud` desde la CLI

---

## 🛠️ Herramientas utilizadas

- Google Cloud Skills Boost
- Kubernetes
- GKE
- `kubectl`

---

## ✅ Lo que aprendí

- Qué son los contenedores y cómo se diferencian de las máquinas virtuales.
- Componentes clave de Kubernetes: plano de control, nodos, Pods, Deployments y Services.
- Comandos básicos para consultar recursos usando `kubectl`.
- Diferencias entre los modos Autopilot y Standard en GKE.
- Cómo desplegar y administrar contenedores de forma escalable en Google Cloud.

---

## 📚 Recursos útiles

- [Cuestionario – Contenedores en la nube](https://www.cloudskillsboost.google/course_templates/60/quizzes/530165)

---

## 🎯 Resultado del día

Aprendí los conceptos clave sobre contenedores y orquestación con Kubernetes, así como su aplicación práctica mediante GKE.  
Ahora tengo una base sólida para trabajar con microservicios y cargas distribuidas en Google Cloud.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
