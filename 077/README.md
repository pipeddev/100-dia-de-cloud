# 🌥️ Día 77 – Introducción a Cloud Dataflow en Google Cloud

## 📌 Tema

Procesamiento de datos en lotes y en tiempo real con **Cloud Dataflow**.

## 📝 Descripción

**Cloud Dataflow** es un servicio completamente administrado de Google Cloud para ejecutar **canalizaciones de procesamiento de datos**.

🔹 Permite transformar y enriquecer datos en **modos de transmisión (streaming) y por lotes (batch)** con la misma confiabilidad.
🔹 Escala automáticamente para manejar desde pequeños flujos hasta **millones de eventos por segundo**.
🔹 Elimina la complejidad de instalar, configurar y mantener infraestructura.

Cloud Dataflow se basa en **Apache Beam**, lo que brinda APIs expresivas en **SQL, Java y Python**, además de funciones avanzadas como:

- **Ventanas de tiempo** (windowing) para procesar datos en streaming.
- **Análisis de sesiones**.
- **Conectores a múltiples fuentes y destinos**.

## ⚙️ Integraciones y monitoreo

- 🔗 Se integra con servicios de GCP como **Pub/Sub, Datastore, BigQuery y Bigtable**.
- 🌐 También soporta fuentes externas como **Apache Kafka** y **Apache Avro**.
- 📊 Se conecta con **Stackdriver (Cloud Monitoring & Logging)** para alertas y métricas de canalizaciones.
- 📈 Con **Data Studio**, puedes crear **dashboards en tiempo real** ideales para IoT y analítica de streaming.

## 🔹 Casos de uso de Cloud Dataflow

- Procesamiento en tiempo real de datos de sensores IoT.
- ETL (extracción, transformación y carga) de grandes volúmenes de datos.
- Integración con **BigQuery** para análisis avanzado.
- Limpieza y enriquecimiento de datos antes de entrenamiento de modelos en **AI Platform**.

## 🛠️ Herramientas utilizadas

- Cloud Dataflow
- Apache Beam SDK (SQL, Java, Python)
- Cloud Pub/Sub
- BigQuery / Bigtable
- Data Studio
- Stackdriver (Monitoring & Logging)

## 🤓 Lo que aprendí

- **Cloud Dataflow** combina lo mejor del **procesamiento batch y streaming** en un único servicio administrado.
- No es necesario administrar clústeres ni servidores: el servicio escala automáticamente.
- Su **ecosistema de integraciones** lo convierte en el centro de muchos flujos de datos en GCP.
- Gracias a Apache Beam, puedo desarrollar canalizaciones con un mismo código y ejecutarlas en diferentes entornos.
- Es ideal para escenarios de **ETL en tiempo real** y analítica avanzada en la nube.

## 🔗 Recursos útiles

- [Introducción a Cloud Dataflow](https://cloud.google.com/dataflow/docs/overview)
- [Apache Beam SDK](https://beam.apache.org/documentation/)

## 🚀 Resultado del día

Hoy aprendí cómo **Cloud Dataflow simplifica el procesamiento de datos por lotes y en streaming**, permitiendo construir canalizaciones escalables e integradas con el ecosistema de GCP, desde **Pub/Sub hasta BigQuery y Data Studio**.
