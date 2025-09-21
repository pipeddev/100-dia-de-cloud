# 🌥️ Día 84 – El plano de control de Kubernetes

## 📌 Tema

Entendiendo el **plano de control de Kubernetes**, sus componentes principales y cómo GKE simplifica su gestión.

## 📝 Descripción

El **plano de control** es el conjunto de procesos que mantiene un clúster de Kubernetes funcionando y alineado con el estado deseado.
Su función es coordinar, supervisar y administrar los **nodos** y **Pods** dentro del clúster.

En un clúster de Kubernetes, los roles se dividen en:

- **Plano de control:** administra el estado del clúster.
- **Nodos:** ejecutan los Pods (contenedores).

### Componentes principales del plano de control

- **kube-apiserver** 🛠️

  - Punto de entrada para interactuar con Kubernetes.
  - Recibe comandos (kubectl, API) y valida autenticación, autorización y admisión.

- **etcd** 🗄️

  - Base de datos distribuida que almacena el **estado del clúster**.
  - Guarda configuración, nodos activos, Pods y su ubicación.

- **kube-scheduler** 📅

  - Decide en qué nodo ejecutar un Pod.
  - Evalúa recursos disponibles, afinidad/antiafinidad, políticas y restricciones de hardware/software.

- **kube-controller-manager** 🔄

  - Supervisa continuamente que el estado actual coincida con el deseado.
  - Usa controladores como:

    - **Deployment:** mantiene Pods replicados y escalados.
    - **Node Controller:** responde a nodos caídos.
    - **Cloud Controller Manager:** integra con recursos del proveedor cloud (balanceadores, volúmenes, etc.).

### Componentes en los nodos

- **kubelet** 👷

  - Agente que ejecuta en cada nodo.
  - Recibe instrucciones del kube-apiserver para iniciar Pods y reporta su estado.

- **Container Runtime (ej. containerd)** 📦

  - Lanza contenedores a partir de imágenes.

- **kube-proxy** 🌐

  - Maneja la red entre Pods y servicios.
  - Usa iptables del kernel de Linux para enrutar tráfico.

## ⚙️ Kubernetes vs GKE

En Kubernetes puro, el usuario debe administrar y asegurar cada componente del plano de control.
Con **Google Kubernetes Engine (GKE)**:

- Google aprovisiona y mantiene el plano de control.
- El usuario interactúa con la API de Kubernetes mediante una IP expuesta.
- El nivel de administración depende del modo:

  - **Autopilot:** GKE gestiona todo (nodos, escalado, seguridad, redes).
  - **Standard:** el usuario administra la configuración de los nodos.

## 🛠️ Herramientas utilizadas

- Kubernetes (kube-apiserver, etcd, scheduler, controller-manager, kubelet, kube-proxy)
- Google Kubernetes Engine (Autopilot y Standard)
- containerd (runtime de contenedores)

## 🤓 Lo que aprendí

- El plano de control es el **cerebro de Kubernetes**, orquestando todos los componentes.
- kube-apiserver es el punto central de comunicación entre usuarios y el clúster.
- etcd garantiza consistencia y persistencia del estado del clúster.
- Con GKE, gran parte de esta complejidad se abstrae, especialmente en modo Autopilot.
- La diferencia clave: en Kubernetes puro, tú gestionas el plano de control; en GKE, Google lo hace por ti.

## 🔗 Recursos útiles

- [Kubernetes Control Plane](https://kubernetes.io/docs/concepts/overview/components/)
- [Control plane en GKE](https://cloud.google.com/kubernetes-engine/docs/concepts/control-plane)

## 🚀 Resultado del día

Hoy aprendí cómo funciona el **plano de control de Kubernetes**, qué rol cumple cada componente y cómo **GKE simplifica esta gestión**, liberando al usuario de la complejidad de mantener el cerebro del clúster.
