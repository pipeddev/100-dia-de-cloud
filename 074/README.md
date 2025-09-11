# 🌥️ Día 74 – Introducción a Terraform e Infraestructura como Código en Google Cloud

## 📌 Tema

Infraestructura como Código (IaC) y el uso de **Terraform** en Google Cloud.

## 📝 Descripción

Hasta ahora, hemos creado recursos en Google Cloud usando la **Consola** y **Cloud Shell**:

- La consola es ideal cuando recién comienzas y prefieres una **interfaz gráfica**.
- Cloud Shell es útil cuando ya tienes experiencia y buscas **rapidez en la línea de comando**.

Pero **Terraform** va un paso más allá. Es una herramienta de **infraestructura como código (IaC)** que nos permite **definir, aprovisionar y eliminar infraestructura** de manera automatizada, repetible y declarativa.

### 🔹 ¿Qué es Infraestructura como Código (IaC)?

- Aprovisionamiento bajo demanda, eficiente y automatizado.
- Infraestructura replicable para entornos de **dev, test y prod**.
- Versionamiento de cambios en un único lugar (archivos de configuración).
- Integración en pipelines de **CI/CD** para habilitar **implementación continua**.

### 🔹 ¿Qué es Terraform?

- Herramienta **open source** compatible con **múltiples nubes** (pública y privada).
- Usa el **lenguaje HCL (HashiCorp Configuration Language)** para describir recursos con bloques, argumentos y expresiones.
- Permite implementar, modificar y eliminar infraestructura con **resultados consistentes**.
- Soporta recursos de Google Cloud como:

  - Compute Engine (VMs, plantillas, MIGs)
  - Redes VPC, reglas de firewall, Cloud Routers
  - Balanceadores de carga, VPNs y más.

## ⚙️ Flujo de trabajo con Terraform

1. ✍️ Definir la infraestructura deseada en archivos `.tf` (ejemplo: `main.tf`).
2. ▶️ Inicializar el proyecto con `terraform init` (descarga el proveedor de GCP).
3. 🔍 Revisar el plan con `terraform plan` (qué se va a crear/cambiar).
4. 🚀 Aplicar los cambios con `terraform apply`.
5. ❌ Eliminar los recursos cuando ya no sean necesarios con `terraform destroy`.

### Ejemplo simple (`main.tf`)

```hcl
provider "google" {
  project = "mi-proyecto"
  region  = "us-central1"
}

resource "google_compute_network" "vpc_network" {
  name                    = "mi-red"
  auto_create_subnetworks = true
  mtu                     = 1460
}

resource "google_compute_firewall" "default-allow-http" {
  name    = "allow-http"
  network = google_compute_network.vpc_network.name

  allow {
    protocol = "tcp"
    ports    = ["80", "8080"]
  }
}
```

## 🛠️ Herramientas utilizadas

- Google Cloud Console
- Cloud Shell
- Terraform (HCL)

## 🤓 Lo que aprendí

- **Terraform es declarativo**: describes el estado deseado y la herramienta se encarga de alcanzarlo.
- IaC permite **rapidez, replicabilidad y control** sobre entornos completos.
- Con Terraform puedo aprovisionar desde recursos básicos hasta arquitecturas completas en GCP.
- Los comandos `init`, `plan`, `apply` y `destroy` son el ciclo básico de trabajo.

## 🔗 Recursos útiles

- [Terraform en Google Cloud](https://cloud.google.com/docs/terraform)
- [Infraestructura como Código (IaC) en GCP](https://cloud.google.com/infrastructure-as-code)

## 🚀 Resultado del día

Hoy aprendí a usar **Terraform** como herramienta de **infraestructura como código** en Google Cloud, entendiendo cómo definir, aprovisionar y gestionar recursos de manera **automatizada y repetible**.
