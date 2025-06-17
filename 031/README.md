# 🗓️ Día 031 – Terraform Cloud

## 📌 Tema

Introducción a Terraform Cloud y su uso para gestionar el `terraform.tfstate` de manera remota.

---

## 📘 Descripción

### ¿Qué es Terraform Cloud?

Terraform Cloud es un servicio SaaS proporcionado por HashiCorp que permite almacenar el **state remoto** y colaborar en infraestructura como código de forma centralizada. Aunque puedes seguir ejecutando `plan` y `apply` de forma local, Terraform Cloud añade una capa de gestión y seguridad muy útil.

Cuenta con una **capa gratuita**, ideal para comenzar.

### Funcionalidades principales

- 🌐 Almacenamiento remoto y seguro del Terraform state.
- 🤝 Colaboración entre equipos.
- 💻 Entornos consistentes y confiables.
- 🎛️ Interfaz web intuitiva.
- 🔐 Gestión de equipos y control de permisos.
- 📦 Registro privado de módulos.
- 🛡️ Integración de políticas con Sentinel.

### Pasos para usar Terraform Cloud

1. **Registro** en la plataforma:

   - 👉 https://app.terraform.io/

2. **Crear un Workspace**:

   - Asociarlo a tu repositorio (GitHub, GitLab, Bitbucket, etc.).

3. **Configurar la versión de Terraform**:

   - Asegúrate de que coincida con la versión en tu entorno local.

4. **Agregar variables sensibles**:

   - `access_key` y `secret_key` de tu proveedor en el menú de Variables.

5. **Ejecutar un run**:

   - Tipos de ejecución disponibles:
     - `Plan and apply` (estándar).
     - `Plan only`.
     - `Refresh state`.
     - `Allow empty apply`.

6. **Eliminar recursos**:
   - Ve a: `Settings` → `Destruction and Deletion` → `Queue destroy plan`.

### Ejemplo de proyecto

📁 Repositorio: [cloud-terraform-example](https://github.com/pipeddev/cloud-terraform-example)

📸 Dashboard:

![Dashboard proyecto de terraform cloud](https://github.com/pipeddev/100-dia-de-cloud/blob/main/031/page-terraform-cloud.png)

---

## ✅ Lo que aprendí

- Qué es Terraform Cloud y cómo utilizarlo para almacenar el estado remoto.
- Cómo integrar Terraform Cloud con GitHub y automatizar workflows.
- Las distintas opciones de ejecución y destrucción de infraestructura desde la consola web.

---

## 📚 Recursos útiles

- [Terraform Cloud – Documentación oficial](https://developer.hashicorp.com/terraform/cloud-docs)
- [Terraform CLI vs Terraform Cloud](https://developer.hashicorp.com/terraform/cli/cloud)

---

## 🌟 Resultado del día

Implementé Terraform Cloud para almacenar el `terraform.tfstate` remoto, conecté un repositorio desde GitHub y realicé operaciones de infraestructura directamente desde la consola web. Un paso clave hacia la colaboración y automatización segura en proyectos de infraestructura.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
