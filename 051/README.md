# ☁️ Día 51 - Cloud Bigtable en Google Cloud

## 📌 Tema

Exploración de **Cloud Bigtable**, una base de datos NoSQL altamente escalable, ideal para cargas de trabajo de lectura/escritura intensivas con baja latencia.

## 📖 Descripción

Hoy me adentré en el mundo de **Cloud Bigtable**, el motor de almacenamiento utilizado por productos de Google como Búsqueda, Maps, Gmail y Analytics.

Cloud Bigtable destaca por:

- 🚀 **Escala a nivel de petabytes**.
- ⚡ **Baja latencia (<10ms)** para lectura y escritura.
- 🧠 Aprende patrones de acceso para balancear carga.
- 🔄 Compatible con la API de **HBase**.
- 🧩 Integra fácilmente con **Dataflow**, **Dataproc**, **Hadoop**, y otras herramientas de Big Data.
- 🧱 Almacena datos en formato **clave-valor** ordenado (tablas dispersas).

📊 Su modelo está basado en:

- **Filas indexadas por clave única**.
- **Familias de columnas** que agrupan datos relacionados.
- **Celdas versionadas por timestamp**, ideales para mantener histórico.

🔧 Arquitectura:

- Separa el **almacenamiento** (Colossus) del **procesamiento**.
- Los datos se almacenan como SSTables (archivos inmutables y ordenados).
- Fragmentación en tablets permite escalabilidad horizontal.

## 🔁 Flujo de trabajo

1. Crear una instancia de Bigtable con un mínimo de 3 nodos.
2. Definir tablas, filas y familias de columnas.
3. Integrar tu aplicación mediante API HBase o cliente nativo.
4. Monitorear el rendimiento y escalar nodos si es necesario.

## 🛠️ Herramientas utilizadas

- Google Cloud Platform (GCP)
- Cloud Bigtable
- HBase API
- Cloud Dataflow / Dataproc (integraciones)

## 📚 Lo que aprendí

- Bigtable es ideal para cargas operativas **altamente escalables** y para soluciones **analíticas en tiempo real**.
- Su rendimiento escala **linealmente** al agregar nodos.
- **Pagas por nodo activo**, por lo tanto no es una solución económica para cargas intermitentes o de bajo volumen.
- Aunque es NoSQL, requiere un **diseño cuidadoso** de claves de fila para evitar hotspots.

## 🔗 Recursos útiles

- [Documentación oficial de Cloud Bigtable](https://cloud.google.com/bigtable/docs)
- [Diferencias entre Bigtable y Firestore](https://cloud.google.com/databases/docs/compare/firestore-vs-bigtable)
- [Introducción a Bigtable (YouTube)](https://www.youtube.com/watch?v=KZ-lPVWnVAw)

## ✅ Resultado del día

Hoy entendí cuándo usar Cloud Bigtable:
✔️ Necesito almacenar **más de 1TB**
✔️ Mi aplicación requiere **lectura/escritura con latencia <10ms**
✔️ Necesito **alta escalabilidad** y **consistencia fuerte**
✔️ Integro con herramientas de Big Data o uso la **API de HBase**
