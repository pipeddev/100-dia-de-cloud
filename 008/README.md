# 📅 Día 008 – Recursos y acceso en la nube

## 📌 Tema

Explorar la jerarquía de recursos en Google Cloud, comprender el funcionamiento de IAM (Identity and Access Management), cuentas de servicio y Cloud Identity.

---

## 📘 Descripción

Hoy estudié cómo se organiza la infraestructura en Google Cloud a través de una jerarquía de recursos que permite aplicar políticas de acceso de manera escalable y segura.

### Jerarquía de recursos en GCP (de menor a mayor):

1. **Recursos individuales** (VMs, buckets de Cloud Storage, datasets de BigQuery, etc.)
2. **Proyecto** (unidad lógica que agrupa recursos y configura permisos, facturación y APIs)
3. **Carpetas** (agrupan proyectos bajo un mismo contexto organizacional)
4. **Organización** (nivel raíz de la jerarquía; representa la empresa o dominio)

Cada proyecto tiene tres identificadores:

- **Project ID**: identificador único, inmutable y global.
- **Project Name**: nombre asignado por el usuario; puede cambiarse y no necesita ser único.
- **Project Number**: identificador numérico único asignado por Google.

Las políticas de acceso pueden aplicarse a cualquier nivel de la jerarquía, y **los recursos heredan las políticas desde niveles superiores**.

---

### 🔐 IAM (Identity and Access Management)

Con IAM puedes definir **quién puede hacer qué sobre qué recurso**:

- **Quién**: puede ser una Cuenta de Google, Grupo de Google, cuenta de servicio o un dominio de Cloud Identity.
- **Qué puede hacer**: se determina mediante **roles**.

Tipos de roles:

- **Básicos**: propietario, editor, visualizador.
- **Predefinidos**: roles específicos con permisos limitados por servicio.
- **Personalizados**: creados por el usuario con permisos específicos según sus necesidades.

---

### 🤖 Cuentas de servicio

Las **cuentas de servicio** permiten que las aplicaciones o recursos (como VMs) se autentiquen con otros servicios de GCP sin intervención humana. Son esenciales para flujos de trabajo automatizados y seguros.

---

## 🛠️ Herramientas utilizadas

- Google Cloud Skills Boost

---

## ✅ Lo que aprendí

- Existen **cuatro niveles jerárquicos** en la estructura de recursos de GCP.
- Cómo aplicar políticas de IAM desde niveles superiores y cómo se heredan.
- Diferencias entre roles básicos, predefinidos y personalizados.
- Cómo funcionan las cuentas de servicio y su rol en automatización y seguridad.
- Realicé mi primer **laboratorio práctico**:  
  👉 [Crear una máquina virtual con LAMP en GCP](https://www.cloudskillsboost.google/course_templates/60/labs/530141)

---

## 📚 Recursos útiles

- [Google Cloud Training – Skill Boost](https://www.cloudskillsboost.google/)
- [IAM Overview](https://cloud.google.com/iam/docs/overview)

---

## 🎯 Resultado del día

Comprendí cómo se estructuran y protegen los recursos en GCP mediante jerarquías y políticas de acceso con IAM.  
Además, realicé un laboratorio práctico desplegando una VM con Apache, MySQL y PHP.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)

---
