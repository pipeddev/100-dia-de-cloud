# 📅 Día 011 – Almacenamiento en la nube

## 📌 Tema

Explorar los distintos tipos de almacenamiento en la nube, diferenciando entre datos estructurados, semiestructurados y no estructurados, y comprender el funcionamiento de **Cloud Storage** en Google Cloud.

---

## 📘 Descripción

Hoy estudié **Cloud Storage**, el servicio de almacenamiento de objetos de Google Cloud que permite a desarrolladores y organizaciones almacenar grandes volúmenes de datos de forma **duradera**, **segura** y con **alta disponibilidad**.

### 🔹 ¿Qué es el almacenamiento de objetos?

Es una arquitectura donde los datos se gestionan como **objetos individuales**, en lugar de estructuras jerárquicas como archivos y carpetas.  
Cada objeto incluye los datos, metadatos y un identificador único.  
Se utiliza comúnmente para almacenar:

- Videos
- Imágenes
- Archivos de audio
- Documentos u otros datos no estructurados

---

### 🗂️ Clases de almacenamiento en Cloud Storage

Google Cloud ofrece diferentes clases de almacenamiento según la **frecuencia de acceso** y el **costo asociado**:

| Clase                | Uso recomendado                                            | Frecuencia de acceso  | Costo    |
| -------------------- | ---------------------------------------------------------- | --------------------- | -------- |
| **Standard Storage** | Datos "activos" de acceso frecuente                        | Diaria                | Más alto |
| **Nearline Storage** | Datos accedidos 1 vez al mes o menos                       | Mensual               | Bajo     |
| **Coldline Storage** | Datos accedidos 1 vez cada 90 días                         | Trimestral            | Más bajo |
| **Archive Storage**  | Archivos históricos, backups y recuperación ante desastres | Menos de 1 vez al año | Mínimo   |

---

### 🔄 Función Autoclass

**Autoclass** permite automatizar el ciclo de vida de los objetos, trasladándolos dinámicamente a la clase de almacenamiento más adecuada según sus **patrones de acceso**.  
Esto reduce costos sin afectar la disponibilidad o integridad de los datos.

---

## 🛠️ Herramientas utilizadas

- Google Cloud Skills Boost

---

## ✅ Lo que aprendí

- Cómo funciona el **almacenamiento de objetos** en GCP.
- Diferencias entre los distintos **niveles de almacenamiento** según el acceso.
- Beneficios de usar **Autoclass** para optimizar costos de forma automática.

---

## 📚 Recursos útiles

- [Documentación oficial de Cloud Storage](https://cloud.google.com/storage/docs/introduction)

---

## 🎯 Resultado del día

Fortalecí mi comprensión sobre el almacenamiento en la nube, su clasificación según el acceso, y cómo Google Cloud maneja objetos de datos de manera eficiente y escalable.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)

---
