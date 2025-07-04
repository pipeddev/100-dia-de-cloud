# 📅 Día 045 – Funciones avanzadas de Cloud Storage

## 📌 Tema

Exploración de funciones avanzadas de **Cloud Storage** en Google Cloud: control de versiones, administración del ciclo de vida, sincronización, notificaciones, autoclass, transferencia masiva y coherencia global.

---

## 📘 Descripción

Hoy profundicé en las capacidades adicionales que ofrece Cloud Storage, más allá del almacenamiento de objetos. Aprendí cómo se puede administrar de forma eficiente el ciclo de vida de los objetos, mantener múltiples versiones, sincronizar datos entre entornos y realizar cargas masivas utilizando diferentes servicios. Además, comprendí el funcionamiento de la coherencia global que garantiza la consistencia inmediata de las operaciones.

---

### 🚀 Funcionalidades destacadas

- **Control de versiones de objetos**
  Permite mantener varias versiones de un mismo objeto en un bucket. Se pueden listar versiones, restaurar o eliminar versiones específicas.

  > 💡 Se identifican mediante números de generación.

- **Administración del ciclo de vida de objetos**
  Permite aplicar reglas automáticas para archivar, cambiar la clase de almacenamiento o eliminar objetos según criterios como fecha, edad o cantidad de versiones.

  > ⏳ Cambios pueden tardar hasta 24 horas en aplicarse.

- **Sincronización de directorios**
  Posibilidad de sincronizar carpetas locales (como de una VM) con un bucket de Cloud Storage.

- **Notificaciones con Pub/Sub**
  Se pueden configurar notificaciones de cambios en objetos para integraciones con otros servicios o flujos automatizados.

- **Autoclass**
  Automatiza la asignación de clases de almacenamiento a los objetos según su uso y patrones de acceso.

---

### 🧪 Inmutabilidad y consistencia

- Los objetos en Cloud Storage son **inmutables**. No pueden modificarse, solo reemplazarse.
- Se garantiza **coherencia fuerte global** en:

  - Subidas
  - Reemplazos
  - Eliminaciones
  - Listado de buckets y objetos

---

### 🚚 Servicios de transferencia de datos

1. **Transfer Appliance**
   Dispositivo físico para migraciones grandes (hasta 1PB) sin interrupciones.

2. **Storage Transfer Service**
   Permite importar datos desde buckets de Cloud Storage, S3 o URLs.

3. **Importación de medios sin conexión**
   Proveedor externo sube datos desde dispositivos físicos como discos, cintas o USBs.

---

## 🔐 Seguridad

- **Claves de encriptación del cliente** (CSEK)
  Alternativa a las claves administradas por Google para una mayor seguridad personalizada.

---

## ✅ Lo que aprendí

- Cómo aplicar y gestionar reglas de ciclo de vida para optimizar costos.
- Importancia del control de versiones para recuperación de datos.
- Usos adecuados de servicios de transferencia para cargas masivas.
- El funcionamiento de la coherencia fuerte en operaciones sobre objetos.

---

## 🧩 Resultado del día

✔️ Comprendí cómo habilitar y gestionar el control de versiones de objetos.
✔️ Revisé casos prácticos para aplicar reglas del ciclo de vida.
✔️ Analicé las diferencias entre las opciones de transferencia de datos a gran escala.
✔️ Entendí cómo funciona la coherencia global en Cloud Storage y su importancia para sistemas distribuidos.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub – Desafío 100 Días de Cloud](https://github.com/pipeddev/100-dia-de-cloud)
