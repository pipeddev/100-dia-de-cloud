# 📅 Día 048 – Introducción a Cloud Spanner

## 📌 Tema

Exploración de Cloud Spanner, el servicio de base de datos relacional distribuida de Google Cloud, diseñado para escalabilidad horizontal sin sacrificar la coherencia transaccional.

---

## 📘 Descripción

Hoy aprendí sobre **Cloud Spanner**, el servicio administrado que combina lo mejor del mundo relacional y no relacional: esquema SQL, coherencia fuerte y replicación automática con escalabilidad horizontal y alta disponibilidad global.

Es ideal para aplicaciones críticas como sistemas financieros, gestión de inventarios, y otras soluciones empresariales que requieren disponibilidad, rendimiento y consistencia de datos en múltiples regiones.

---

## 🔍 Características Clave

- ✅ **SQL relacional + NoSQL escalable**
- 🌍 **Escalabilidad horizontal global**
- 🔐 **Coherencia transaccional fuerte**
- 💡 **Replicación automática síncrona**
- ⏱️ **Relojes atómicos para precisión y coherencia temporal**
- 📦 **Esquema relacional definido en SQL estándar**
- ⚙️ **Configuración multirregional o regional con diferentes SLA**

---

## 🧠 Casos de uso recomendados

- Aplicaciones financieras o bancarias con gran volumen de operaciones
- Gestión de inventario en retailers con alta concurrencia
- Sistemas transaccionales globales
- Consolidación de múltiples bases de datos fragmentadas

---

## 🧭 ¿Cuándo usar Cloud Spanner?

Puedes considerar Cloud Spanner si:

- Las bases de datos tradicionales no escalan lo suficiente
- Necesitas mantener **coherencia transaccional** en una arquitectura distribuida
- Requieres replicación y alta disponibilidad a escala global
- Buscas evitar la fragmentación (sharding) de tu base de datos manualmente

De lo contrario, si no necesitas capacidades relacionales o globales, podrías optar por servicios **NoSQL** como **Firestore**.

---

## 📚 Recursos útiles

- [Documentación oficial de Cloud Spanner](https://cloud.google.com/spanner/docs)
- [Comparativa entre Spanner, Cloud SQL y Firestore](https://cloud.google.com/docs/databases)
- [Migración desde MySQL a Spanner](https://cloud.google.com/spanner/docs/migration/mysql)

---

## ✅ Resultado del día

✔️ Comprendí en profundidad cuándo y por qué elegir Cloud Spanner sobre otras opciones como Cloud SQL, especialmente cuando se busca **escalabilidad horizontal con coherencia transaccional**.

🔗 [Repositorio del reto #100DiasDeCloud](https://github.com/pipeddev/100-dia-de-cloud)
