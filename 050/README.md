# ☁️ Día 50 - Cloud Firestore en Google Cloud

## 📌 Tema

Introducción a **Cloud Firestore**, la base de datos NoSQL moderna, escalable y totalmente administrada de Google Cloud.

## 📖 Descripción

Hoy exploré **Cloud Firestore**, un servicio de base de datos de documentos que combina lo mejor de la flexibilidad NoSQL con características avanzadas como transacciones ACID y replicación multirregional.

Algunos aspectos destacados:

- 🔥 Firestore es **nativo en la nube**, sin servidores que administrar.
- 📲 Ideal para apps web, móviles, IoT y más.
- 📡 Soporta **sincronización en tiempo real** y uso **offline**.
- 🔐 Se integra con Firebase y ofrece potentes reglas de seguridad.
- 🔁 Compatible con Datastore (modo retrocompatible).

Además, aprendí que Firestore se puede usar en dos **modos operativos**:

- **Modo Nativo**: Recomendado para nuevas apps web y móviles.
- **Modo Datastore**: Recomendado para proyectos de backend nuevos o migraciones desde Cloud Datastore.

También destaca por:

- Consultas sofisticadas sin afectar el rendimiento.
- Consistencia fuerte (ya no eventual como en Datastore).
- Transacciones con menos limitaciones.
- Escalabilidad automática a nivel global.

## 🔁 Flujo de trabajo

1. Identificar si Firestore es adecuado según el tipo de app.
2. Elegir entre modo nativo o modo datastore.
3. Configurar base de datos desde Firebase Console o GCP.
4. Integrar cliente (Web, Android, iOS o Admin SDK).
5. Aplicar reglas de seguridad y realizar pruebas de lectura/escritura.

## 🛠️ Herramientas utilizadas

- Google Cloud Platform (GCP)
- Firebase Console
- Cloud Firestore
- Firebase Admin SDK

## 📚 Lo que aprendí

- Cloud Firestore es una evolución natural de Cloud Datastore.
- El modelo de datos basado en **colecciones y documentos** ofrece gran flexibilidad.
- Las **transacciones ACID** en Firestore permiten operaciones seguras incluso en entornos NoSQL.
- Firestore es una excelente opción para **proyectos serverless**.

## 🔗 Recursos útiles

- [Documentación oficial de Cloud Firestore](https://cloud.google.com/firestore)
- [Diferencias entre Firestore en modo nativo y modo Datastore](https://cloud.google.com/datastore/docs/firestore-or-datastore)
- [Comparativa entre Firestore y otras bases de datos NoSQL en GCP](https://cloud.google.com/products/databases)

## ✅ Resultado del día

Hoy aprendí cuándo y por qué utilizar Cloud Firestore. Si buscas una base de datos NoSQL **altamente escalable**, **con sincronización en tiempo real** y que pueda adaptarse a apps modernas sin complicaciones, Firestore es una gran opción.
