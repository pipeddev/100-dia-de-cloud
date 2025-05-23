# 📅 Día 012 – Almacenamiento en la nube

## 📌 Tema

Explorar los distintos servicios de almacenamiento en Google Cloud, comprendiendo sus diferencias, casos de uso y tipos de datos compatibles: estructurados, semiestructurados y no estructurados.

---

## 📘 Descripción

Hoy profundicé en los diferentes tipos de **almacenamiento gestionado** que ofrece Google Cloud, desde bases de datos relacionales hasta soluciones NoSQL, orientadas a alto rendimiento o grandes volúmenes de datos.

---

### 🗄️ Cloud SQL

- Servicio de **bases de datos relacionales** administradas para MySQL, PostgreSQL y SQL Server.
- No requiere instalación ni mantenimiento de software.
- Escala hasta **128 vCPUs, 864 GB de RAM** y **64 TB de almacenamiento**.
- Soporta **réplicas automáticas**, copias de seguridad administradas y cifrado en tránsito y en reposo.
- Incluye **firewalls de red** para controlar el acceso a las instancias.

---

### 🧩 Spanner

- Base de datos **relacional distribuida y escalable horizontalmente**.
- Ideal para aplicaciones globales que requieren alta disponibilidad, consistencia fuerte y procesamiento de transacciones.
- Compatible con SQL y permite trabajar con índices secundarios y uniones.

---

### 🔥 Firestore

- Base de datos **NoSQL, flexible y escalable** para apps web, móviles o de backend.
- Almacena los datos como **documentos** dentro de **colecciones**.
- Compatible con estructuras complejas, objetos anidados y subcolecciones.
- Ideal para aplicaciones que requieren sincronización en tiempo real y operaciones sin conexión.

---

### 📊 Bigtable

- Base de datos **NoSQL orientada a columnas**, usada por servicios como Gmail, Maps y Analytics.
- Optimizada para grandes volúmenes de datos con **alta capacidad de escritura/lectura** y baja latencia.
- No soporta SQL ni transacciones de varias filas.
- Casos ideales: IoT, AdTech, finanzas, análisis de usuarios.

---

### 📌 Comparativa de servicios de almacenamiento

| Servicio          | Tipo de datos           | Escala / Capacidad               | Ideal para                          |
| ----------------- | ----------------------- | -------------------------------- | ----------------------------------- |
| **Cloud Storage** | No estructurado (BLOBs) | Hasta 5 TB por objeto            | Imágenes, videos, backups           |
| **Cloud SQL**     | Relacional estructurado | Hasta 64 TB por instancia        | Aplicaciones web, credenciales      |
| **Spanner**       | Relacional distribuido  | Hasta petabytes                  | Apps globales con carga alta        |
| **Firestore**     | NoSQL estructurado      | Hasta TBs, 1 MB por entidad      | Apps móviles/web con sincronización |
| **Bigtable**      | NoSQL analítico         | Hasta petabytes, 100 MB por fila | IoT, analítica en tiempo real       |

---

## 🛠️ Herramientas utilizadas

- Google Cloud Skills Boost

---

## ✅ Lo que aprendí

- Características y diferencias entre servicios de almacenamiento en GCP.
- Qué tipo de almacenamiento usar según la estructura y volumen de datos.
- Comparativa de rendimiento, escalabilidad y casos de uso.
- Realicé el [cuestionario final del módulo](https://www.cloudskillsboost.google/course_templates/60/quizzes/530161).

---

## 📚 Recursos útiles

- [Cuestionario: Almacenamiento en la nube](https://www.cloudskillsboost.google/course_templates/60/quizzes/530161)

---

## 🎯 Resultado del día

Fortalecí mi comprensión sobre el ecosistema de almacenamiento en Google Cloud y aprendí a identificar la mejor opción según el tipo de datos, necesidad de escalabilidad y naturaleza de la aplicación.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)

---
