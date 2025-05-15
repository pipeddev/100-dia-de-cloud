# 📅 Día 003 – Asegurar la operación exitosa de una solución en la nube

## 📌 Tema

Exploración de conceptos clave en **Compute Engine** y **Google Kubernetes Engine (GKE)** para garantizar el correcto funcionamiento de una solución en la nube.  
Además, profundización en comandos esenciales de **Terraform** para gestionar infraestructura como código.

---

## 📘 Descripción

Hoy avancé en el módulo sobre cómo asegurar el éxito operativo de una solución en la nube.  
Estudié configuraciones importantes en **Compute Engine**, como el uso de instantáneas (snapshots) para respaldo de discos.  
En **GKE**, revisé conceptos como Pods, Deployments y Services, esenciales para la disponibilidad y escalabilidad.  
También avancé en mi curso de Terraform, aprendiendo más sobre su ciclo de vida y comandos clave.

---

## 🛠️ Herramientas utilizadas

- Cloud Skills Boost (Google Cloud)
- Curso de Terraform (Udemy)

---

## ✅ Lo que aprendí

### 🖥️ Compute Engine

- Una **instantánea (snapshot)** es una copia de seguridad incremental de un disco persistente.
- Las **instantáneas programadas** se crean automáticamente con políticas definidas.
- Los comandos `gcloud` siguen la estructura: **grupo → subgrupo → acción**.
  - Ejemplo: `gcloud compute snapshots list`

### ☸️ GKE – Kubernetes

![Diagrama de GKE](003/object-kubernetes.png)

- **Pod**: unidad más pequeña de ejecución, puede contener uno o más contenedores.
- **Deployment**: objeto que administra un conjunto de Pods idénticos (réplicas).
- **Service**: objeto que expone uno o varios Pods a través de un punto de red estable, utilizando selectores.

balanceo de carga en kubernetes.

![Balanceo de carga](003/balanceo-carga.png)

### 📦 Terraform

- `terraform init`: Inicializa el entorno y descarga los proveedores.
- `terraform plan`: Previsualiza los cambios que se aplicarán.
- `terraform apply`: Ejecuta los cambios descritos en el plan.
- `terraform destroy`: Elimina los recursos definidos en el archivo de configuración.

---

## 📚 Recursos útiles

- [Sitio oficial de 100DaysOfCloud](https://www.100daysofcloud.com/)
- [Repositorio base en GitHub](https://github.com/100DaysOfCloud/100DaysOfCloud)

---

## 🎯 Resultado del día

Consolidé conceptos esenciales de GKE y Compute Engine, y entendí cómo automatizar respaldos con snapshots.  
También profundicé en el ciclo de vida de Terraform y sus comandos básicos.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)

---
