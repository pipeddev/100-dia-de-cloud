# 📅 Día 004 – Práctica con Terraform: Entendiendo el Estado

## 📌 Tema

Comprender el funcionamiento del archivo de estado de Terraform y su importancia dentro del ciclo de infraestructura como código.

---

## 📘 Descripción

Hoy profundicé en el concepto de **estado en Terraform**, aprendiendo cómo y cuándo se generan los archivos `terraform.tfstate` y `terraform.tfstate.backup`.  
Además, exploré por qué **no deben incluirse en control de versiones** y cómo gestionar estos archivos de manera segura mediante un backend remoto.

También practiqué comandos clave para consultar, visualizar y manipular el estado de Terraform.

---

## 🛠️ Herramientas utilizadas

- Visual Studio Code
- Curso de Terraform (Udemy)

---

## ✅ Lo que aprendí

### 📄 Archivos de estado

- `terraform.tfstate`: almacena el **estado actual** de la infraestructura.
- `terraform.tfstate.backup`: respaldo generado automáticamente tras cada cambio de estado.
- Ambos archivos pueden contener **datos sensibles**, como claves, IPs o tokens.

### ⚠️ Por qué no subir `.tfstate` a GitHub/GitLab

- Exposición de información confidencial.
- Riesgo de corrupción del estado en equipos colaborativos.
- Conflictos en versionado manual.

### ✅ Recomendación

Usar un backend remoto para manejar el estado de forma segura:

- Google Cloud Storage (GCS)
- Amazon S3 + DynamoDB
- Azure Blob Storage
- Terraform Cloud

Agregar al `.gitignore`:

```gitignore
*.tfstate
*.tfstate.backup
.terraform/
terraform.tfvars
```

| Comando                                    | Descripción                                                              |
| ------------------------------------------ | ------------------------------------------------------------------------ |
| `terraform show -json`                     | Muestra detalles del estado (opcional: `-json`).                         |
| `terraform providers`                      | Lista proveedores usados y restricciones.                                |
| `terraform refresh`                        | Sincroniza el `.tfstate` con el estado real de la infraestructura.       |
| `terraform graph`                          | Muestra el grafo de dependencias.                                        |
| `terraform graph \| dot -Tsvg > graph.svg` | Genera un gráfico visual de dependencias.                                |
| `terraform state list`                     | Lista todos los recursos gestionados.                                    |
| `terraform state show <recurso>`           | Muestra el detalle completo de un recurso específico.                    |
| `terraform state mv`                       | Mueve recursos dentro del archivo de estado.                             |
| `terraform state rm`                       | Elimina un recurso del archivo `.tfstate`, sin eliminarlo del proveedor. |

---

## 📚 Recursos útiles

[Tutorial oficial de Terraform – Estado](https://developer.hashicorp.com/terraform/tutorials/certification-003)

---

## 🎯 Resultado del día

Comprendí a fondo cómo funciona el archivo de estado en Terraform, su importancia, riesgos y mejores prácticas.
Además, incorporé comandos clave que me permitirán administrar recursos de forma más precisa y segura.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)

---
