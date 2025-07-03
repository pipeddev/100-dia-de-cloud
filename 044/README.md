# 📅 Día 044 – Cloud Storage en Google Cloud

## 📌 Tema

Almacenamiento de objetos con Cloud Storage: clases, ubicaciones, control de acceso y administración.

---

## 📘 Descripción

### ¿Qué es Cloud Storage?

Google Cloud Storage es el servicio de almacenamiento de objetos de Google Cloud que permite almacenar y recuperar datos desde cualquier parte del mundo, en cualquier momento. Está diseñado para escalar a niveles de exabytes, ofreciendo alta disponibilidad y baja latencia, incluso para grandes volúmenes de datos.

### Usos comunes

- Distribución de contenido web
- Almacenamiento de backups y archivos para recuperación ante desastres
- Almacenamiento y descarga directa de grandes volúmenes de datos

---

### Características clave

- **Alta escalabilidad**: hasta exabytes de datos.
- **Latencia baja**: respuesta en milisegundos.
- **Alta disponibilidad** en todas las clases.
- **Una sola API** para todas las operaciones.

### Estructura

- **Buckets**: no anidables y con nombres únicos a nivel global.
- **Objetos**: archivos almacenados dentro de buckets.

---

## 🧱 Clases de almacenamiento

| Clase    | Ideal para                      | Mínimo almacenamiento | Costos acceso |
| -------- | ------------------------------- | --------------------- | ------------- |
| Standard | Acceso frecuente, datos activos | Ninguno               | Bajo          |
| Nearline | Acceso mensual, backups         | 30 días               | Medio         |
| Coldline | Acceso trimestral, archivado    | 90 días               | Alto          |
| Archive  | Acceso anual, archivado crítico | 365 días              | Muy alto      |

### Tipos de ubicación

- **Multirregión**: redundancia global (ej. EEUU)
- **Región doble**: dos regiones específicas (ej. Finlandia + Países Bajos)
- **Región**: ubicación única (ej. Londres)

---

## 🔐 Control de acceso

- **IAM**: define roles a nivel de proyecto/bucket/objeto.
- **ACL (Access Control Lists)**: control granular de acceso a nivel de objeto o bucket.
- **URL firmadas**: permite acceso temporal a recursos específicos con una clave privada.

---

## 🔄 Administración del ciclo de vida

- Permite configurar reglas automáticas para cambiar la clase de almacenamiento de los objetos con base en el tiempo o condiciones.
- Ejemplo: mover archivos a Archive después de 365 días.

---

## ✅ Lo que aprendí

- Cómo elegir la clase de almacenamiento adecuada según frecuencia y duración del acceso.
- Diferencias clave entre IAM, ACLs y URLs firmadas.
- Arquitectura interna de Cloud Storage basada en buckets y objetos.
- Concepto de "11 nueves" de durabilidad: protección contra pérdida de datos, no disponibilidad.

---

## 📚 Recursos útiles

- [Documentación oficial de Cloud Storage](https://cloud.google.com/storage/docs)
- [Comparación de clases de almacenamiento](https://cloud.google.com/storage/docs/storage-classes)

---

## 🌟 Resultado del día

Exploré profundamente Cloud Storage, comprendí las diferencias entre sus clases, sus ubicaciones y configuré controles de acceso con IAM y URL firmadas.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub – Desafío 100 Días de Cloud](https://github.com/pipeddev/100-dia-de-cloud)
