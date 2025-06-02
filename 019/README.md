# 📅 Día 019 – Curso de Terraform y Redes Virtuales en GCP

## 📌 Tema

Realizar un laboratorio práctico con Jenkins desde el Marketplace y comenzar el módulo de redes virtuales del curso de infraestructura esencial en Google Cloud.

---

## 📘 Descripción

### 🧪 Lab: Implementación de Jenkins desde Marketplace

Se realizaron las siguientes tareas:

- Crear una instancia preconfigurada de Jenkins desde Google Cloud Marketplace (Bitnami).
- Verificar acceso a la IU de Jenkins.
- Acceder por SSH a la máquina virtual que ejecuta Jenkins.

**Parámetros configurados:** zona, tipo de máquina, cuenta de servicio.

El despliegue se realizó usando **Deployment Manager**, herramienta de infraestructura como código (IaC).

---

### 🌐 Redes virtuales (inicio de módulo)

#### Introducción

- GCP usa una red definida por software sobre infraestructura global de fibra óptica.
- Los **PoP (Points of Presence)** conectan la red de Google con otras redes e Internet.

#### Conceptos clave de VPC (Virtual Private Cloud)

- **VPC**: Red virtual donde se alojan los recursos de GCP.
- **Proyectos**: Contienen los servicios y recursos, incluidas las redes.
- **Redes**: Tipos disponibles: predeterminadas, automáticas y personalizadas.
- **Subredes**: Segmentan la red por región.
- **Regiones y zonas**: Representan los centros de datos físicos de Google.
- **Direcciones IP**: Internas, externas y rangos personalizados.
- **Instancias de VM**: Máquinas virtuales que se integran en la red.
- **Rutas**: Definen el enrutamiento del tráfico.
- **Firewalls**: Controlan el acceso al tráfico entrante y saliente.

---

## ✅ Lo que aprendí

- Cómo usar el Marketplace para implementar Jenkins rápidamente.
- Introducción al diseño de redes virtuales en GCP.
- Uso de Deployment Manager como herramienta de infraestructura como código.

---

## 📚 Recursos útiles

- [Documentación de Terraform Provisioners](https://developer.hashicorp.com/terraform/language/resources/provisioners/syntax)
- [Google Cloud CLI Docs](https://cloud.google.com/sdk/gcloud)
- [Google Cloud Marketplace](https://console.cloud.google.com/marketplace)
- [Documentación oficial de VPC](https://cloud.google.com/vpc/docs/overview)

---

## 🎯 Resultado del día

Implementé Jenkins como entorno CI/CD en minutos usando Marketplace. Además, comencé el módulo de redes virtuales, consolidando conceptos esenciales para el diseño de redes en GCP.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
