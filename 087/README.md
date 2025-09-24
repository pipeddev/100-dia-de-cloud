# 🌥️ Día 87 – El comando kubectl en Kubernetes

## 📌 Tema

Introducción a **kubectl**, la herramienta de línea de comandos para interactuar con Kubernetes.

## 📝 Descripción

**kubectl** es la utilidad principal que permite a los administradores y usuarios **controlar clústeres de Kubernetes**.
Se comunica con el **kube-apiserver** en el plano de control, convirtiendo los comandos de línea en **llamadas API HTTPS** que consultan o modifican el estado del clúster.

### Configuración

- **kubectl** necesita conocer:

  - La **ubicación del clúster**.
  - Las **credenciales de acceso**.

- La configuración se guarda en:

  - Carpeta oculta `~/.kube/config`.
  - Contiene lista de clústeres, usuarios y contextos.

- En GKE, las credenciales se obtienen con:

  ```bash
  gcloud container clusters get-credentials CLUSTER_NAME --zone ZONE
  ```

- Esto actualiza automáticamente `~/.kube/config`.

### Sintaxis general de kubectl

```bash
kubectl [comando] [tipo] [nombre] [opciones]
```

- **comando** → acción (ej. `get`, `describe`, `logs`, `exec`).
- **tipo** → recurso (ej. `pods`, `deployments`, `nodes`).
- **nombre** → nombre del objeto (opcional).
- **opciones** → banderas adicionales (`-o yaml`, `-o wide`, etc.).

### Ejemplos

- Ver todos los Pods:

  ```bash
  kubectl get pods
  ```

- Ver un Pod específico:

  ```bash
  kubectl get pod my-test-app
  ```

- Describir un Pod:

  ```bash
  kubectl describe pod my-test-app
  ```

- Exportar la definición YAML de un Pod:

  ```bash
  kubectl get pod my-test-app -o=yaml
  ```

### Relación con gcloud

- **kubectl**: administra objetos dentro de un clúster ya existente.
- **gcloud**: administra la infraestructura (crear/eliminar clústeres, obtener credenciales, etc.).

## ⚙️ Herramientas utilizadas

- kubectl
- gcloud CLI
- kube-apiserver

## 🤓 Lo que aprendí

- **kubectl** es el puente entre el usuario y el plano de control de Kubernetes.
- Necesita credenciales y contexto para conectarse a un clúster.
- Los manifiestos YAML y kubectl son las dos piezas clave para administrar Kubernetes declarativamente.
- `kubectl get`, `describe` y `logs` son comandos esenciales para la administración diaria.
- En GKE, la integración con `gcloud` simplifica la autenticación y conexión.

## 🔗 Recursos útiles

- [Documentación oficial de kubectl](https://kubernetes.io/docs/reference/kubectl/)
- [kubectl Cheat Sheet](https://kubernetes.io/docs/reference/kubectl/cheatsheet/)

## 🚀 Resultado del día

Hoy entendí la importancia de **kubectl** como herramienta esencial para administrar clústeres de Kubernetes: desde consultar Pods hasta aplicar manifiestos YAML, siempre en comunicación directa con el **kube-apiserver**.
