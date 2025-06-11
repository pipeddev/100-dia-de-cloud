# 🗓️ Día 028 – Terraform locals y precio por computo

## 📌 Tema

Uso de `locals` en Terraform y modelo de precios de Compute Engine en Google Cloud Platform.

---

## 📘 Descripción

### 📊 Terraform locals

`locals` es un bloque que permite definir variables locales dentro de un módulo. Estas no pueden sobrescribirse desde fuera del módulo y ayudan a evitar repeticiones, mejorar la legibilidad y calcular valores derivados.

#### Ejemplo:

```hcl
locals {
  suffix = "${var.tags.project}-${var.tags.env}-${var.tags.region}" # recurso-cerberus-prod-region
}

resource "random_string" "sufijo_s3" {
  length  = 8
  special = false
  upper   = false
}

locals {
  s3_suffix = "${var.tags.project}-${random_string.sufijo_s3.id}"
}

resource "aws_s3_bucket" "cerberus_bucket" {
  bucket = local.s3_suffix
}

tags = {
  Name = "vpc_virginia-${local.suffix}"
}
```

#### Cuándo usar `locals`:

- Para calcular valores derivados de otras variables.
- Para evitar repeticiones (principio DRY).
- Para definir valores intermedios o constantes internas.

---

### 💸 Precio por computo

Google ofrece modelos de precios optimizados para reducir costos en Compute Engine:

- Se cobra un mínimo de **1 minuto** por vCPU, GPU y memoria. Luego del primer minuto, se factura por **segundos**.
- El modelo de precios es **por recurso**, no por tipo de máquina. La facturación separa vCPU y RAM.

#### Tipos de descuentos:

- **Sustained Use Discount (SUD)**: Descuento automático por uso continuo de más del 25% del mes.
- **Committed Use Discount (CUD)**: Contrato a 1 o 3 años con descuento mayor.
- **Preemptible VMs**: Máquinas temporales con un costo mucho menor.

#### Recomendaciones de Compute Engine:

- Sugerencias automáticas para redimensionar VMs.
- Aparecen luego de 24 horas de creación de la instancia.

#### Límites gratuitos:

- Compute Engine ofrece un pequeño límite gratuito por mes (consultar documentación actualizada).

#### Ejemplo de descuento por uso sostenido:

![Ejemplo de descuento sostenido](https://github.com/pipeddev/100-dia-de-cloud/blob/main/028/discount.png)

Dos instancias en `us-central1`:

- **Primera mitad del mes**: N1-standard-4 (4 vCPU, 15 GB RAM).
- **Segunda mitad del mes**: N1-standard-16 (16 vCPU, 60 GB RAM).

Compute Engine reorganiza:

- 4 vCPU + 15 GB RAM por **un mes completo** (descuento máximo).
- 12 vCPU + 45 GB RAM por **medio mes**.

---

## ✅ Lo que aprendí

- Uso de `locals` en Terraform para mejorar modularidad.
- Modelo de precios de Compute Engine basado en recursos individuales.
- Aplicación de descuentos automáticos por uso sostenido.
- Recomendaciones de redimensionamiento en GCP.

---

## 📚 Recursos útiles

- [Terraform locals](https://developer.hashicorp.com/terraform/language/values/locals)
- [Compute Engine Pricing](https://cloud.google.com/compute/pricing)
- [Descuentos por uso sostenido](https://cloud.google.com/compute/docs/sustained-use-discounts)

---

## 🌟 Resultado del día

Aprendí a simplificar configuraciones con `locals` en Terraform y comprendí el impacto financiero del uso eficiente de recursos en Compute Engine aplicando descuentos automáticos y recomendaciones de optimización.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
