# 📅 Día 027 – Terraform estructura condicional y opciones de cómputo

## 📌 Tema

Uso de estructuras condicionales en Terraform y exploración de las opciones de cómputo en Google Cloud.

---

## 📘 Descripción

### 🎛️ Terraform: estructura condicional

En Terraform, es posible condicionar la creación de recursos usando la propiedad `count` junto con operadores lógicos. Esto permite desplegar recursos solo si se cumple cierta condición.

```hcl
variable "enable_monitoring" {
  description = "Habilita el despliegue de un servicio de monitoreo"
  type        = number # También puede ser bool
  default     = 0
}
```

Definiendo el valor:

`enable_monitoring = 0`

El recurso se creará solo si enable_monitoring == 1:

```
resource "aws_instance" "monitoring_instance" {
  count         = var.enable_monitoring == 1 ? 1 : 0
  ami           = var.ec2_specs.ami
  instance_type = var.ec2_specs.instance_type
  subnet_id     = aws_subnet.public_subnet.id
  key_name      = data.aws_key_pair.key.key_name
  vpc_security_group_ids = [aws_security_group.sg_public_instance.id]
  user_data     = file("scripts/userdata.sh")

  tags = {
    Name = "Monitoreo"
  }
}
```

💡 Al ejecutar terraform plan, se muestra si el recurso será creado o no.

### 🖥️ Opciones para crear máquinas virtuales

Google Cloud permite crear VMs de tres maneras:

1. Consola de Google Cloud
2. Línea de comandos (gcloud)
3. API REST

Para configuraciones complejas y automatización, se recomienda el uso de la API REST. Puedes usar la consola primero y luego obtener el equivalente en REST o CLI.

#### 🧮 Familias de máquinas en Compute Engine

Las _machine families_ agrupan configuraciones optimizadas según el tipo de carga de trabajo:

---

## 1. 🔧 General Purpose

Relación equilibrada entre precio y rendimiento.

- **E2**: Bajo costo. Ideal para microservicios, entornos de desarrollo y aplicaciones ligeras.
- **N2 / N2D / N1**: Balance entre costo y rendimiento. Adecuadas para bases de datos medianas, aplicaciones web exigentes y cargas de trabajo generales.
- **Tau T2D / T2A**: Excelente rendimiento por costo. Óptimas para cargas escalables como microservicios en contenedores, transcodificación de medios y aplicaciones Java a gran escala.

---

## 2. ⚙️ Compute Optimized

Diseñadas para tareas de procesamiento intensivo.

- **C2**: Ideales para videojuegos AAA, simulaciones, automatización de diseño electrónico (EDA) y cómputo de alto rendimiento (HPC).
- **C2D**: VMs más grandes con excelente rendimiento por núcleo, enfocadas en HPC.
- **H3**: Hasta 88 vCPUs, memoria DDR5. Basadas en CPU Intel Sapphire Rapids y hardware personalizado de Google.

---

## 3. 🧠 Memory Optimized

Altas capacidades de RAM para bases de datos en memoria y análisis intensivo.

- **M1 / M2 / M3**: Diseñadas para cargas que requieren gran memoria como SAP HANA, SQL Server, análisis en memoria y modelado genómico.
- **M3**: Hasta 128 vCPUs y más de 3.8 TB de RAM por VM.

---

## 4. 🚀 Accelerator Optimized

Equipadas con GPUs, ideales para aprendizaje automático (ML), inteligencia artificial (IA) y cómputo masivamente paralelo.

- **A2**: Con GPUs NVIDIA A100, hasta 16 GPUs por VM. Perfectas para entrenamiento intensivo de modelos.
- **G2**: De 4 a 96 vCPUs y hasta 432 GB de memoria. Ideales para inferencia de ML, transcodificación de video y estaciones de trabajo de visualización remota.

---

## 🛠️ Configuración adicional

Dentro de cada familia, puedes definir:

- **Machine Series**: subcategorías que definen las características del procesador y memoria.
- **Machine Type**: configuración específica de vCPU y memoria dentro de una serie.

> 🧠 Elegir correctamente la familia y tipo de máquina es clave para optimizar rendimiento y costos en tus proyectos de GCP.

---

## ✅ Lo que aprendí

- Cómo utilizar estructuras condicionales en Terraform con `count`.
- Opciones para crear VMs en Google Cloud: consola, CLI y REST.
- Tipos de máquinas disponibles en Compute Engine y sus usos.
- Identificar la familia de máquina adecuada para cada carga de trabajo.

---

## 📚 Recursos útiles

- [Condicionales en Terraform](https://developer.hashicorp.com/terraform/language/meta-arguments/count)
- [Compute Engine machine families](https://cloud.google.com/compute/docs/machine-resource)
- [REST API Compute Engine](https://cloud.google.com/compute/docs/reference/rest/v1/)

---

## 🎯 Resultado del día

Apliqué condicionales en Terraform para controlar la creación de recursos y comprendí las diferencias clave entre las distintas familias de máquinas en Compute Engine, lo que me permite elegir mejor según los requerimientos de cada aplicación.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
