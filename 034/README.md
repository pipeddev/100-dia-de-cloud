# 📅 Día 034 – Imágenes en Compute Engine

## 📌 Tema

Imágenes públicas y personalizadas en Compute Engine

---

## 📘 Descripción

Cuando creas una máquina virtual (VM) en Google Cloud, debes elegir una **imagen de disco de arranque**. Esta imagen incluye:

- El **bootloader**.
- El **sistema operativo**.
- La **estructura del sistema de archivos**.
- Todo el **software preconfigurado** y otras personalizaciones necesarias.

### Tipos de imágenes

#### 🏛️ Imágenes públicas

- Google Cloud ofrece imágenes de **Linux y Windows**.
- Algunas son **premium** (se indica con una “(p)”):
  - Se cobran **por segundo** después del primer minuto.
  - Las imágenes de **SQL Server** se cobran **por minuto** con un mínimo de 10 minutos.
  - El precio depende del tipo de máquina, pero **no cambia según la región o zona**.

#### 🛠️ Imágenes personalizadas

- Puedes crear tu propia imagen personalizada con software aprobado por tu organización.
- También es posible **importar imágenes locales** desde otra estación de trabajo o incluso desde otro proveedor de nube.
  - Este proceso es **gratuito** y se recomienda instalar un agente para facilitarlo.

### 🖼️ Imágenes de máquina

Un recurso especial en Compute Engine que almacena:

- Configuración
- Metadatos
- Permisos
- Datos de uno o más discos

Son ideales para:

- Mantenimiento del sistema
- Recuperación
- Creación de copias de seguridad
- Clonación de instancias

---

## ✅ Lo que aprendí

- Las diferencias entre imágenes públicas, premium y personalizadas.
- Cómo se tarifican las imágenes premium según el sistema operativo y la duración.
- Qué es una imagen de máquina y cómo facilita tareas de respaldo y replicación en Compute Engine.

---

## 📚 Recursos útiles

- [Documentación oficial sobre imágenes en GCP](https://cloud.google.com/compute/docs/images)
- [Precios de imágenes premium](https://cloud.google.com/compute/vm-instance-pricing#os-pricing)

---

## 🌟 Resultado del día

Ahora puedo elegir con mayor criterio las imágenes para mis VMs, ya sea por optimización de costos, personalización o tareas de backup.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
