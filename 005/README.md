# 📅 Día 005 – Configura el acceso y la seguridad

## 📌 Tema

Revisión del contenido del módulo **"Configura el acceso y la seguridad"** del curso de preparación para la certificación **Associate Cloud Engineer**.  
Además, práctica de comandos básicos con `kubectl` para interactuar con clústeres de Kubernetes.

---

## 📘 Descripción

Hoy revisé conceptos clave sobre **cuentas de servicio**, **usuarios**, **grupos** y **dominios** en Google Cloud, además del ciclo de vida de los objetos en **Cloud Storage**.  
También exploré varios comandos de `kubectl` para administrar recursos dentro de un clúster Kubernetes.

---

## 🛠️ Herramientas utilizadas

- Visual Studio Code
- Google Cloud Skills Boost

---

## ✅ Lo que aprendí

### 🔐 Gestión de acceso en Google Cloud

- **Cuenta de Google**: representa a una persona que interactúa con GCP; puede estar asociada a cualquier dirección de correo electrónico.
- **Cuenta de servicio**: permite que aplicaciones y recursos se autentiquen y accedan a otros servicios en GCP usando claves, en lugar de credenciales interactivas.
- **Grupos de Google**: colecciones de usuarios o cuentas de servicio que pueden recibir permisos a través de políticas compartidas.
- **Dominios de Google Workspace y Cloud Identity**: permiten administrar usuarios a nivel organizacional, controlando el acceso centralizadamente.

### 🧱 Ciclo de vida de Cloud Storage

![Diagrama de ciclo de vida](https://github.com/pipeddev/100-dia-de-cloud/blob/main/005/lifecycle-storage.png)

- Gestión automática de objetos basada en reglas como antigüedad, tipo de almacenamiento, o versiones.

### ☸️ Comandos básicos de `kubectl`

| Comando                          | Descripción                                                              |
| -------------------------------- | ------------------------------------------------------------------------ |
| `kubectl run`                    | Crea un nuevo objeto Deployment con configuración por defecto.           |
| `kubectl create -f archivo.yaml` | Crea un recurso a partir de un archivo de configuración.                 |
| `kubectl get pods`               | Lista los pods activos en el clúster.                                    |
| `kubectl expose`                 | Crea un Service que expone tráfico a los Pods con etiquetas específicas. |

---

## 📚 Recursos útiles

- [Resumen diagnóstico: Asegura la operación exitosa](https://www.cloudskillsboost.google/paths/11/course_templates/77/documents/530319)
- [Resumen diagnóstico: Configura el acceso y seguridad](https://www.cloudskillsboost.google/paths/11/course_templates/77/documents/530326)

---

## 🎯 Resultado del día

Profundicé en la configuración de permisos y autenticación en Google Cloud, entendiendo cómo interactúan los distintos tipos de identidades y cómo se aplican políticas de acceso.  
También practiqué comandos esenciales de `kubectl` y repasé el ciclo de vida de los objetos en Cloud Storage.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)

---
