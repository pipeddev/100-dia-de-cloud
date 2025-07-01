# 📅 Día 042 – IAM: Otorgar y revocar roles, y uso de Service Account User

## 📌 Tema

Control de acceso en Google Cloud con IAM: uso del rol **Usuario de cuenta de servicio**, asignación y revocación de roles, y configuración de permisos específicos sobre recursos como Cloud Storage y Compute Engine.

---

## 📘 Descripción

En este laboratorio interactivo exploré cómo otorgar y revocar roles a usuarios y cuentas de servicio, además de configurar permisos específicos a nivel de proyecto y recurso. A través de una serie de pasos prácticos, experimenté con la administración del rol **`Service Account User`** para otorgar permisos mínimos necesarios y permitir el acceso controlado a buckets de Cloud Storage desde una VM con identidad de cuenta de servicio.

---

## 🎯 Objetivos alcanzados

- Usar IAM para implementar el control de acceso basado en roles.
- Restringir el acceso a funciones o recursos específicos.
- Configurar y usar el rol **Usuario de cuenta de servicio**.
- Delegar accesos mínimos necesarios mediante políticas de IAM.
- Crear cuentas de servicio con permisos específicos.
- Asociar cuentas de servicio a VMs y observar su comportamiento.

---

## 🧪 Actividades realizadas

1. **Creación de dos usuarios temporales (Username 1 y Username 2)** para gestionar el acceso desde distintos perfiles.
2. **Exploración de roles desde IAM**: Visualización de permisos desde ambas cuentas.
3. **Creación de un bucket de Cloud Storage**, subida de un archivo y prueba de acceso con un usuario con rol limitado.
4. **Revocación de acceso a Username 2** y verificación de la pérdida de visibilidad del recurso.
5. **Asignación del rol `Storage Object Viewer`** a Username 2 y validación desde la terminal con Cloud Shell.
6. **Creación de una cuenta de servicio personalizada** llamada `read-bucket-objects`, con permisos de lectura sobre Storage.
7. **Asignación del rol `Service Account User` al dominio `altostrat.com`** para simular acceso a través de una VM.
8. **Creación de una instancia de VM** con dicha cuenta de servicio asignada y pruebas vía SSH:

   - Lectura de objetos desde Cloud Storage (✅ éxito).
   - Intento de escritura fallido (❌ `403 AccessDenied`).

9. **Actualización de permisos** de la cuenta de servicio a `Storage Object Creator` y nuevo intento exitoso de escritura (✅ éxito).

---

## ✅ Lo que aprendí

- La importancia del principio de privilegios mínimos (Least Privilege).
- Cómo usar cuentas de servicio para representar componentes de una aplicación.
- Cómo otorgar acceso granular a recursos desde una VM mediante identidades de servicio.
- Que una instancia hereda el contexto de IAM de su cuenta de servicio.
- Que los roles pueden otorgarse por recurso, proyecto, o jerárquicamente.

---

## 📚 Recursos útiles

- [Documentación oficial sobre Service Accounts](https://cloud.google.com/iam/docs/understanding-service-accounts)
- [Políticas de IAM](https://cloud.google.com/iam/docs/policies)
- [Guía práctica: Rol de Service Account User](https://cloud.google.com/iam/docs/impersonating-service-accounts)

---

## 🌟 Resultado del día

- Automatización del acceso a recursos con cuentas de servicio.
- Validación práctica del control de permisos a través de roles IAM.
- Aislamiento de permisos por identidad y recurso.
- Simulación de usuarios para validar configuraciones IAM.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/100-dia-de-cloud)
