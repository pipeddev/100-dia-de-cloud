## 🌥️ Día 046 - Filestore en Google Cloud

### 📌 Tema

Exploración de **Filestore**, el servicio de almacenamiento de archivos administrado de Google Cloud.

---

### 📄 Descripción

Filestore es un sistema de archivos compartido administrado por Google Cloud que proporciona una interfaz de sistema de archivos basada en **NFS v3**, ideal para aplicaciones que necesitan acceso simultáneo a los mismos datos desde múltiples instancias. Es ampliamente utilizado en cargas de trabajo empresariales que requieren alto rendimiento, baja latencia y escalabilidad.

---

### 🔁 Flujo de trabajo

- Introducción a Filestore y su arquitectura.
- Casos de uso comunes (EDA, renderización, análisis genómico, hosting, etc.).
- Comprensión de sus características clave:

  - Escalabilidad independiente de capacidad y rendimiento.
  - Integración nativa con Compute Engine y GKE.
  - Bloqueo de archivos sin software adicional.
  - Compatibilidad con cargas de trabajo heredadas.

---

### 🛠️ Herramientas utilizadas

- [Google Cloud Console](https://console.cloud.google.com/)
- [Filestore (Documentación)](https://cloud.google.com/filestore)

---

### 📚 Lo que aprendí

- Filestore permite una experiencia nativa con sistemas de archivos en la nube.
- Se ajusta automáticamente para escalar según necesidad, separando rendimiento y capacidad.
- Compatible con entornos de desarrollo y producción que demandan almacenamiento compartido de alto rendimiento.
- Casos reales donde Filestore es clave:

  - Renderizado colaborativo (e.g. efectos visuales)
  - Diseño electrónico asistido (EDA)
  - Análisis financiero/científico
  - Hosting y CMS como WordPress

---

### 🔗 Recursos útiles

- [Filestore Overview](https://cloud.google.com/filestore/docs/overview)
- [Filestore vs Cloud Storage](https://cloud.google.com/filestore/docs/choosing-storage-option)
- [GKE + Filestore Integration](https://cloud.google.com/kubernetes-engine/docs/how-to/persistent-volumes/filestore-csi-driver)

---

### ✅ Resultado del día

✔️ Comprensión completa del uso, casos aplicables y ventajas de Filestore para entornos que requieren almacenamiento compartido en Google Cloud.

📌 Repositorio del reto:
[https://github.com/pipeddev/100-dia-de-cloud](https://github.com/pipeddev/100-dia-de-cloud)
