# 📅 Día 040 – Service Account

## 📌 Tema

Profundización en las cuentas de servicio en Google Cloud: tipos, usos, autorización, roles y gestión segura de credenciales.

---

## 📘 Descripción

Hoy exploré en profundidad las **cuentas de servicio** en Google Cloud Platform. Este tipo de identidad no está asociada a un usuario, sino que representa a una aplicación o servicio que interactúa con otros servicios de Google Cloud.

### 🔐 ¿Qué es una Service Account?

Una **cuenta de servicio** es una identidad usada por aplicaciones o componentes de infraestructura para realizar acciones en nombre de un servicio, sin necesidad de autenticar con credenciales de usuario.

**Ejemplo:** una aplicación que interactúa con Cloud Storage debe autenticarse para acceder a la API (XML o JSON), lo cual se puede lograr mediante una cuenta de servicio.

---

### 🧱 Tipos de cuentas de servicio

1. **Creadas por el usuario (personalizadas):** creadas manualmente por administradores, permiten control total sobre permisos y uso.
2. **Integradas:** creadas automáticamente por Google Cloud para servicios específicos.
3. **De las APIs de Google:** como `project-number@cloudservices.gserviceaccount.com`, usadas internamente por Google para operar recursos en tu nombre.

---

### 📧 Formato de identificación

Las cuentas de servicio se identifican mediante correos como:

- `project-number-compute@developer.gserviceaccount.com`
- `project-number@cloudservices.gserviceaccount.com`

---

### ⚙️ Autenticación y autorización

- **Autenticación:** Proceso que asegura que la identidad es válida (ej. cuenta de servicio).
- **Autorización:** Determina los permisos que dicha identidad tiene sobre recursos.

Google Cloud otorga **tokens de acceso** a las cuentas de servicio, los cuales definen sus permisos (ej. lectura, escritura en buckets de Cloud Storage).

Puedes crear y asignar estas cuentas al iniciar una instancia VM. Si usas `gcloud`, por defecto se asigna la cuenta `Compute Engine default service account`, con rol `Editor`.

---

### 🔄 Roles de IAM y acceso

- Las cuentas de servicio pueden recibir roles de IAM, como `roles/compute.instanceAdmin`.
- Puedes otorgar a usuarios el rol `Service Account User` para que puedan “actuar como” dicha cuenta.

**Ejemplo práctico:**

- `App A` accede al bucket con permisos de solo lectura.
- `App B` accede con permisos de lectura/escritura.

Esto permite segmentar accesos por componente, aplicación o microservicio.

---

### 🔐 Gestión de claves

Las cuentas de servicio pueden autenticarse mediante:

#### ✅ Claves administradas por Google

- Usadas dentro de servicios como Compute Engine o Cloud Functions.
- Google maneja rotación, almacenamiento y acceso.

#### ⚠️ Claves administradas por el usuario (externas)

- Usadas para aplicaciones fuera de Google Cloud.
- Tú gestionas la clave privada.
- Hasta 10 claves por cuenta.

🔁 Usa estas claves como **último recurso**. Prefiere tokens temporales o credenciales de corta duración.

Puedes usar `gcloud iam service-accounts keys list` para listar las claves activas.

---

## ✅ Lo que aprendí

- Qué es una cuenta de servicio y cómo funciona.
- Diferencias entre cuentas predeterminadas, integradas y personalizadas.
- Cómo autenticar servicios sin usar claves de usuario.
- Gestión de permisos mediante IAM.
- Buenas prácticas de rotación y seguridad de claves.

---

## 📚 Recursos útiles

- [Documentación oficial de IAM](https://cloud.google.com/iam/docs)
- [Guía sobre Service Accounts](https://cloud.google.com/iam/docs/service-accounts)
- [IAM Roles](https://cloud.google.com/iam/docs/understanding-roles)

---

## 🌟 Resultado del día

Consolidé mi entendimiento sobre el uso seguro de cuentas de servicio y aprendí a distribuir permisos precisos para cada aplicación y microservicio en GCP.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/100-dia-de-cloud)
