# 📅 Día 043 – Servicios de almacenamiento y bases de datos en Google Cloud

## 📌 Tema

Exploración de los principales servicios de almacenamiento y bases de datos disponibles en Google Cloud Platform.

---

## 📘 Descripción

Hoy repasé los distintos servicios de almacenamiento de datos que ofrece Google Cloud y cómo elegir el adecuado según el tipo de datos, estructura, necesidades de análisis, latencia y escalabilidad.

Aprendí que todas las aplicaciones necesitan almacenar datos —ya sea información empresarial, contenido multimedia o datos de sensores— y que Google Cloud ofrece una variedad de soluciones adaptadas a cada caso de uso.

---

### 🗂️ Servicios destacados

- **Cloud Storage**: Almacenamiento de objetos, ideal para imágenes, backups, archivos multimedia. Soporta alta durabilidad y disponibilidad.
- **Filestore**: Sistema de archivos compartido, útil para aplicaciones que requieren almacenamiento POSIX.
- **Cloud SQL**: Base de datos relacional totalmente administrada compatible con MySQL, PostgreSQL y SQL Server. Ideal para aplicaciones tradicionales.
- **Cloud Spanner**: Base de datos relacional global y escalable, con características de consistencia fuerte y alta disponibilidad.
- **AlloyDB**: Base de datos relacional que combina procesamiento transaccional y analítico (HTAP), construida sobre PostgreSQL.
- **Firestore**: Base de datos de documentos NoSQL en tiempo real, pensada para aplicaciones móviles/web.
- **Cloud Bigtable**: Base de datos NoSQL de columnas anchas, optimizada para baja latencia y grandes volúmenes de datos.
- **Memorystore**: Servicio de caché en memoria completamente administrado compatible con Redis y Memcached.

### 🧠 Árbol de decisión para elegir el servicio correcto

1. ¿Tus datos están estructurados?

   - **No estructurados**:

     - ¿Necesitas un sistema de archivos compartido? ➡️ Usa **Filestore**
     - Si no ➡️ Usa **Cloud Storage**

   - **Estructurados**:

     - ¿Carga de trabajo enfocada en análisis?

       - Sí:

         - **BigQuery**: Optimizado para SQL y datos inmutables
         - **Bigtable**: Latencia baja, grandes volúmenes, casos como IoT o AdTech

       - No:

         - ¿Son relacionales?

           - No:

             - ¿Necesitas caché? ➡️ Usa **Memorystore**
             - Si no ➡️ Usa **Firestore**

           - Sí:

             - ¿Necesitas HTAP? ➡️ Usa **AlloyDB**
             - ¿Necesitas escalabilidad global? ➡️ Usa **Spanner**
             - Si no ➡️ Usa **Cloud SQL**

---

## ✅ Lo que aprendí

- A identificar cuándo usar Cloud SQL, Spanner, Firestore o Bigtable.
- A distinguir entre almacenamiento de objetos (Cloud Storage) y archivos compartidos (Filestore).
- A utilizar el árbol de decisión para seleccionar servicios basados en tipo de datos, análisis, escalabilidad y latencia.

---

## 📚 Recursos útiles

- [Google Cloud Storage Services Overview](https://cloud.google.com/products/storage)
- [Choosing the right database option](https://cloud.google.com/database-options)
- [Documentación oficial de cada servicio: SQL, Firestore, Spanner, BigQuery, etc.](https://cloud.google.com/docs)

---

## 🌟 Resultado del día

✔️ Consolidé el panorama general de los servicios de almacenamiento y bases de datos de GCP. Preparado para los labs prácticos de este módulo.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/100-dia-de-cloud)
