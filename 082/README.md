# 🌥️ Día 82 – Introducción a Kubernetes

## 📌 Tema

¿Qué es **Kubernetes** y cómo ayuda a administrar aplicaciones en contenedores?

## 📝 Descripción

Cuando una organización adopta contenedores, la cantidad de instancias puede crecer rápidamente, mucho más de lo que antes ocurría con máquinas virtuales.
En ese escenario, surge la necesidad de **orquestar** y administrar esos contenedores: aquí entra **Kubernetes**.

**Kubernetes** es una **plataforma de código abierto** para administrar cargas de trabajo y servicios en contenedores.

🔹 Permite organizar contenedores en múltiples hosts, escalar aplicaciones como microservicios, implementar nuevas versiones y aplicar reversiones.
🔹 Proporciona un **conjunto de APIs** para describir cómo deben ejecutarse y relacionarse las aplicaciones dentro de un **clúster**.
🔹 Está compuesto por:

- **Plano de control (control plane):** administra el estado del clúster.
- **Nodos:** instancias de cómputo (VMs en GCP) que ejecutan los contenedores.

### Declarativo vs Imperativo

- **Declarativo:** describes el estado deseado, Kubernetes lo mantiene incluso ante fallos.
- **Imperativo:** emites comandos puntuales para modificar el sistema.
  👉 Lo recomendado es **declarativo** (infraestructura como código), mientras que el modo imperativo se usa para ajustes temporales.

## ⚙️ Funciones principales de Kubernetes

- Soporte para **cargas sin estado** (ej. Nginx, Apache) y **con estado** (apps que requieren persistencia de datos).
- Admite **trabajos por lotes** y **daemons**.
- Escalado automático en función del uso de recursos.
- Definición de **requests y limits** de CPU, memoria, etc., para optimizar rendimiento.
- Extensibilidad mediante **Custom Resource Definitions (CRDs)** y un amplio ecosistema de complementos.
- Portabilidad: al ser de código abierto, puede ejecutarse en **local, nubes públicas o híbridas**.

## 🛠️ Herramientas utilizadas

- Kubernetes (clúster, plano de control, nodos)
- Google Kubernetes Engine (en GCP, nodos = VMs de Compute Engine)
- Declarative Configs (YAML/JSON)

## 🤓 Lo que aprendí

- Kubernetes **orquesta contenedores** y asegura que las aplicaciones se mantengan en el estado deseado.
- El enfoque declarativo reduce errores y facilita la automatización.
- Permite **escalar, actualizar y revertir despliegues** con facilidad.
- Se adapta a diferentes tipos de cargas de trabajo: **stateless, stateful, batch y daemon**.
- Es **portátil y extensible**, lo que lo convierte en un estándar de la industria.

## 🔗 Recursos útiles

- [Kubernetes.io – Documentación oficial](https://kubernetes.io/docs/home/)
- [Google Kubernetes Engine (GKE)](https://cloud.google.com/kubernetes-engine)

## 🚀 Resultado del día

Hoy aprendí cómo **Kubernetes resuelve la complejidad de administrar contenedores a gran escala**, asegurando que las aplicaciones se ejecuten en el estado deseado, con escalabilidad, resiliencia y portabilidad.
