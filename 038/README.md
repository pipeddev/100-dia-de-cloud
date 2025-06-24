# 📅 Día 038 – Identidades, políticas y jerarquía en IAM

## 📌 Tema

Exploración profunda del sistema de Identity and Access Management (IAM) de Google Cloud: tipos de miembros, políticas, condiciones, jerarquía de recursos y buenas prácticas de seguridad.

---

## 📘 Descripción

Hoy estudié cómo gestionar el acceso seguro y granular en Google Cloud usando IAM. Aprendí cómo se combinan identidades (quién), roles (qué puede hacer) y recursos (dónde) para proteger el entorno de GCP. También profundicé en jerarquías, condiciones, políticas de denegación y sincronización con sistemas corporativos.

---

### 🧑‍💻 Tipos de miembros en IAM

1. **Cuenta de Google (User account)**

   - Representa a un desarrollador, administrador o usuario final. Puede usar direcciones `@gmail.com` o personalizadas.

2. **Cuenta de servicio (Service account)**

   - Representa aplicaciones o servicios que necesitan interactuar con recursos de GCP sin intervención humana.

3. **Grupo de Google (Google Group)**

   - Una colección de usuarios y/o cuentas de servicio que comparten la misma configuración de acceso.

4. **Dominio de Google Workspace**

   - Grupo virtual de todas las cuentas de una organización, como `@example.com`.

5. **Dominio de Cloud Identity**

   - Alternativa a Workspace para organizaciones sin G Suite, permite administración de usuarios sin apps colaborativas como Gmail.

---

### 🔐 Políticas IAM

Las políticas son conjuntos de **vinculaciones (bindings)** que asocian **miembros**, **roles** y condiciones opcionales.

📌 **Ejemplo de política:**

```json
{
  "bindings": [
    {
      "role": "roles/compute.admin",
      "members": [
        "user:juan@example.com",
        "serviceAccount:terraform-sa@project-id.iam.gserviceaccount.com"
      ]
    }
  ]
}
```

---

### 🧱 Jerarquía de recursos y herencia de políticas

IAM sigue la jerarquía de recursos de GCP:

1. **Organización** (ej: `example.com`)
2. **Carpetas** (Deptos o unidades de negocio)
3. **Proyectos** (contenedores de recursos)
4. **Recursos** (VMs, buckets, etc.)

Cada nivel hereda las políticas del superior. Por ejemplo, si se asigna un rol a nivel de organización, este se hereda por todas las carpetas, proyectos y recursos descendientes.

📸 Imagen de ejemplo:
![Jerarquía de recursos](https://github.com/pipeddev/100-dia-de-cloud/blob/main/038/hierarchy.png)

---

### 🎯 Tipos de roles

1. **Básicos**: Propietario, Editor, Visualizador. Son amplios y no recomendados para producción.
2. **Predefinidos**: Más específicos y alineados a servicios (ej. `roles/storage.objectViewer`).
3. **Personalizados**: Creados por el usuario para necesidades específicas.

---

### 🧩 Condiciones IAM

Permiten otorgar acceso bajo ciertas condiciones como:

- Rango de fechas
- Dirección IP
- Dispositivo
- Atributos personalizados

Útiles para control temporal de acceso o desde ubicaciones restringidas.

---

### 🚫 Políticas de denegación

Las políticas de denegación limitan el acceso incluso si hay una política que lo permite. Siempre tienen prioridad y son útiles para restringir permisos a identidades específicas.

---

### 🧠 Buenas prácticas

- Seguir el **principio de privilegio mínimo**.
- Usar grupos de Google para gestionar acceso.
- Usar roles predefinidos en vez de básicos.
- Aplicar condiciones siempre que sea posible.
- Revisar el uso con el recomendador de IAM.

---

## ✅ Lo que aprendí

- Cómo se estructuran identidades y permisos en Google Cloud IAM.
- Jerarquía de recursos y cómo influye en la herencia de permisos.
- Cómo usar condiciones y políticas de denegación para mayor control.

---

## 📚 Recursos útiles

- [Documentación oficial de IAM](https://cloud.google.com/iam/docs)
- [IAM Policy Troubleshooter](https://cloud.google.com/iam/docs/troubleshooting-access)

---

## 🌟 Resultado del día

¡Entendí la base para una gestión segura y escalable de accesos en GCP! Ideal para aplicar en proyectos reales con múltiples equipos y servicios.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/100-dia-de-cloud)
