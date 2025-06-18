# 📅 Día 033 – Ejercicio práctico

## 📌 Tema

Creación de una máquina virtual en GCP y AWS utilizando Terraform.

---

## 📘 Descripción

Hoy realicé un ejercicio práctico que consiste en **crear una máquina virtual en Google Cloud y otra en AWS utilizando Terraform**. El objetivo fue preparar un workshop demostrando cómo desplegar infraestructura en múltiples proveedores desde un mismo proyecto.

### 🛠️ Proceso:

1. **Archivo `provider.tf`**

   - Declarar la versión de Terraform a utilizar.
   - Definir `required_providers` con `google` y `aws`.
   - Configurar los bloques `provider` para ambos entornos.

2. **Archivo `main.tf`**

   - Añadir los recursos `google_compute_instance` y `aws_instance` con su configuración respectiva.

3. **Archivo `variables.tf`**

   - Declarar las variables necesarias para ambas instancias.

4. **Archivo `terraform.tfvars`**

   - Asignar valores a las variables definidas.

5. **Archivo `output.tf`**
   - Declarar los `output` para mostrar la IP pública de cada instancia.

### 💡 Tips:

- Habilitar la API de Compute Engine en GCP.
- Crear un **Service Account** en GCP con rol de **Compute Admin**.
- Configurar las credenciales en Terraform con el archivo `.json` del Service Account.
- En AWS, crear una llave `.pem` y configurar las credenciales `access_key` y `secret_key`.

---

## ✅ Lo que aprendí

- Cómo estructurar un proyecto multicloud con Terraform.
- Diferencias básicas entre `google_compute_instance` y `aws_instance`.
- Configuración de proveedores y autenticación para GCP y AWS.
- Cómo utilizar archivos `.tfvars` para manejar variables de forma ordenada.

---

## 📚 Recursos útiles

- [Terraform AWS Provider Docs](https://registry.terraform.io/providers/hashicorp/aws/latest/docs)
- [Terraform Google Provider Docs](https://registry.terraform.io/providers/hashicorp/google/latest/docs)
- [Autenticación con Service Account en GCP](https://cloud.google.com/docs/authentication/getting-started)

---

## 🎯 Resultado del día

Ejecuté satisfactoriamente la creación de una VM en AWS y otra en GCP con una misma configuración de Terraform, imprimiendo sus IP públicas. Este ejercicio refuerza el uso práctico de Terraform en entornos multicloud y será útil para compartir en futuros workshops.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
