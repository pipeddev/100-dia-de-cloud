# 📅 Día 037 – Roles en Cloud IAM

## 📌 Tema

Entendiendo los tipos de roles en Google Cloud IAM: básicos, predefinidos y personalizados.

---

## 📜 Descripción

En este día exploramos los distintos **tipos de roles** que nos ofrece Cloud IAM y su aplicación para controlar el acceso a recursos de Google Cloud de manera segura y granular.

### Tipos de roles en IAM

1. **Roles básicos** (amplios y de propósito general):

   - 📦 **Propietario**: acceso total, incluyendo administración de miembros y eliminación de proyectos.
   - ✍️ **Editor**: modificar, implementar y configurar recursos.
   - 👁️ **Visualizador**: acceso solo lectura.
   - 💳 **Administrador de facturación**: gestión de facturación, sin acceso a los recursos del proyecto.

> ⚠️ Estos roles se aplican a todos los recursos del proyecto, por lo tanto, su uso debe ser limitado.

---

2. **Roles predefinidos** (más específicos y seguros):

   - Son conjuntos de permisos diseñados para servicios específicos (Compute Engine, Cloud Storage, etc.).
   - Ejemplo: `roles/compute.instanceAdmin` permite iniciar, detener y administrar instancias de VM.

   Algunos roles predefinidos comunes en Compute Engine:

   - 🔧 `Administrador de Compute`: control completo sobre recursos de Compute Engine.
   - 🌐 `Administrador de Red`: gestionar redes, pero solo lectura en reglas de firewall.
   - 💾 `Administrador de Almacenamiento`: crear/modificar/borrar discos, imágenes, snapshots.

---

3. **Roles personalizados** (máxima granularidad):

   - Te permiten definir roles específicos a tus necesidades.
   - Útiles para aplicar el principio de **menor privilegio**.
   - Ejemplo: Crear un rol `Operador de Instancia` que solo permite iniciar y detener VMs, sin poder reconfigurarlas.

---

## ✅ Lo que aprendí

- Los tipos de roles en IAM y cuándo usarlos.
- Cómo los roles predefinidos ayudan a limitar el acceso a recursos específicos.
- La utilidad de los roles personalizados para aplicar seguridad granular.
- Importancia del modelo de **privilegio mínimo**.

---

## 📚 Recursos útiles

- [Tipos de roles en Cloud IAM](https://cloud.google.com/iam/docs/understanding-roles)
- [Lista de roles predefinidos en Compute Engine](https://cloud.google.com/compute/docs/access/iam)

---

## 🌟 Resultado del día

Ahora comprendo cómo asignar correctamente los distintos roles según el nivel de acceso requerido. Esto me ayudará a configurar IAM de forma más segura y ordenada en futuros proyectos.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub – 100 Días de Cloud](https://github.com/pipeddev/100-dia-de-cloud)
