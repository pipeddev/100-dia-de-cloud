# 🗓️ Día 030 – Terraform Módulos práctico

## 📌 Tema

Uso práctico de módulos en Terraform y gestión del estado remoto con S3 y DynamoDB.

---

## 📘 Descripción

### Módulos en Terraform

- Podemos crear módulos en Terraform para mantener ordenado nuestro proyecto y reutilizar componentes.

![Ejemplo de estructura de carpetas](https://github.com/pipeddev/100-dia-de-cloud/blob/main/030/structure_folder.png)

- Podemos usar el módulo `tfstate-backend` con el objetivo de mantener el `terraform.tfstate` en un solo lugar, de modo que solo una persona pueda modificarlo, utilizando un bucket S3 y una tabla en DynamoDB para el control de bloqueo.

#### Pasos destacados:

- Se crea un archivo `backend.tf` con la información del bucket y la tabla DynamoDB.
- Luego de tener el archivo sincronizado, puedes eliminar el archivo `terraform.tfstate` local y usar el almacenado en la nube.
- Si deseas usar el state localmente nuevamente:
  - Ejecuta:
    ```bash
    terraform state pull > terraform.tfstate
    ```
  - O comenta el contenido de `backend.tf` y ejecuta:
    ```bash
    terraform init -migrate-state
    ```

### Ejemplo del módulo para manejar `terraform.tfstate`

```hcl
module "terraform_state_backend_aws_example" {
  source  = "cloudposse/tfstate-backend/aws"
  version = "1.5.0"

  namespace = "example_test"
  stage     = "prod"
  name      = "terraform"
  attributes = ["state"]

  terraform_backend_config_file_path = "."
  terraform_backend_config_file_name = "backend.tf"
  force_destroy = false
}
```

### Contenido generado en `backend.tf` al ejecutar `apply`

```hcl
terraform {
  required_version = ">= 1.0.0"

  backend "s3" {
    region         = "us-east-1"
    bucket         = "exampletest-prod-terraform-state"
    key            = "terraform.tfstate"
    profile        = ""
    encrypt        = "true"
    dynamodb_table = "exampletest-prod-terraform-state-lock"
  }
}
```

---

## ✅ Lo que aprendí

- Cómo organizar infraestructura como código usando módulos reutilizables.
- Configurar y utilizar almacenamiento remoto del estado (`terraform.tfstate`) en AWS.
- Uso del módulo `tfstate-backend` de Cloud Posse para automatizar esta configuración.
- Estrategias para migrar entre almacenamiento local y remoto de manera segura.

---

## 📚 Recursos útiles

- [Módulos Terraform Registry](https://registry.terraform.io/browse/modules)
- [Cloud Posse tfstate-backend module](https://github.com/cloudposse/terraform-aws-tfstate-backend)
- [Documentación oficial sobre Remote State](https://developer.hashicorp.com/terraform/language/state/remote)

---

## 🌟 Resultado del día

Consolidé el uso de módulos en Terraform y configuré el backend remoto con S3 y DynamoDB, mejorando la colaboración y evitando conflictos de estado en entornos multiusuario.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
