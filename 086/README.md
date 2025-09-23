# 🌥️ Día 86 – Administración de objetos en Kubernetes

## 📌 Tema

Explorando la administración de **objetos en Kubernetes** mediante manifiestos YAML y controladores como Deployments.

## 📝 Descripción

En Kubernetes, todo gira en torno a **objetos**, que representan el estado deseado del sistema.

🔹 Cada objeto se identifica por:

- **Nombre único** (hasta 253 caracteres, letras/números, guiones o puntos).
- **UID** generado automáticamente.
- **Etiquetas (labels)** → pares clave-valor para organizar y seleccionar recursos.

### Archivos de manifiesto

- Los manifiestos en **YAML o JSON** declaran qué recursos Kubernetes debe crear y mantener.
- Campos básicos:

  - `apiVersion` → versión de la API.
  - `kind` → tipo de objeto (ej. Pod, Deployment).
  - `metadata` → nombre, UID y namespace.
  - `spec` → define el estado deseado (ej. imagen, número de réplicas).

- Buenas prácticas:

  - Usar **YAML** por legibilidad.
  - Agrupar objetos relacionados en un solo archivo.
  - Guardar manifiestos en **control de versiones** (ej. Cloud Source Repositories, GitHub).

### Pods y controladores

- Los **Pods** son las unidades básicas, pero son efímeros y no se reparan solos.
- Para asegurar disponibilidad, se usan **controladores** que mantienen el estado deseado:

  - **Deployment** → apps de larga duración (ej. servidores web).
  - **StatefulSet** → apps con estado persistente.
  - **DaemonSet** → un Pod por nodo.
  - **Job** → ejecución por lotes.

🔹 Ejemplo: en vez de declarar 3 Pods de nginx por separado, defines un **Deployment** con 3 réplicas.

- El Deployment crea un **ReplicaSet** que asegura que siempre haya 3 Pods ejecutándose.
- Si un Pod falla, ReplicaSet crea otro automáticamente.

## ⚙️ Flujo de trabajo simplificado

1. Escribir el manifiesto YAML (ej. un Deployment con 3 réplicas de nginx).
2. Aplicarlo con `kubectl apply -f archivo.yaml`.
3. Kubernetes compara estado deseado vs estado actual.
4. Controladores mantienen la cantidad y configuración de Pods.

## 🛠️ Herramientas utilizadas

- Kubernetes (kubectl, Pods, Deployments, ReplicaSets)
- YAML manifests
- Cloud Source Repositories / GitHub para versionado

## 🤓 Lo que aprendí

- Los objetos en Kubernetes se gestionan **declarativamente** con manifiestos YAML.
- Las etiquetas facilitan organizar y seleccionar recursos.
- Los Pods son efímeros, por lo que los controladores son esenciales para mantener disponibilidad.
- Deployments y ReplicaSets aseguran que siempre se cumpla el estado deseado.
- Guardar manifiestos en repositorios facilita trazabilidad y reproducibilidad.

## 🔗 Recursos útiles

- [Kubernetes Objects](https://kubernetes.io/docs/concepts/overview/working-with-objects/)
- [Deployments en Kubernetes](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/)

## 🚀 Resultado del día

Hoy aprendí cómo administrar **objetos en Kubernetes** mediante manifiestos declarativos y controladores, asegurando que las aplicaciones se ejecuten siempre en el estado deseado de forma automática y confiable.
