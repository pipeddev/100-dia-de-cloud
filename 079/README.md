# 🌥️ Día 79 – Introducción a Cloud Dataproc en Google Cloud

## 📌 Tema

Procesamiento de datos con **Cloud Dataproc**: clústeres administrados de **Apache Spark y Hadoop**.

## 📝 Descripción

**Cloud Dataproc** es un servicio **completamente administrado, rápido y rentable** que facilita la creación y gestión de **clústeres de Apache Spark y Hadoop** en Google Cloud.

🔹 Los clústeres inician, escalan y se apagan en **90 segundos o menos**, mucho más rápido que en entornos locales o IaaS tradicionales.
🔹 La facturación es por segundo y se puede optimizar aún más usando **instancias interrumpibles**.
🔹 Se integra con el ecosistema de GCP, como **BigQuery, Cloud Storage, Bigtable, Logging y Monitoring**, ofreciendo una plataforma de datos completa.

## ⚙️ Características principales

- 🚀 **Velocidad**: creación de clústeres en minutos.
- 💰 **Costo eficiente**: pagas solo por lo que usas, con soporte para instancias interrumpibles.
- 🔄 **Integración nativa** con servicios de Google Cloud para almacenamiento, análisis y monitoreo.
- 🔧 **Compatibilidad total** con **Spark, Hadoop, Pig y Hive** → no necesitas aprender nuevas APIs.
- 🎯 **Flexibilidad**: permite mover cargas de trabajo existentes al cloud sin rediseñarlas.

## 🔹 Dataproc vs Dataflow

Ambos servicios procesan datos en lotes y en streaming, pero la elección depende de tu contexto:

- ✅ Usa **Cloud Dataproc** si:

  - Tienes dependencias en **Spark, Hadoop o el ecosistema Apache**.
  - Prefieres un enfoque **práctico / DevOps** con control de clústeres.

- ✅ Usa **Cloud Dataflow** si:

  - Buscas un enfoque **serverless y sin intervención**.
  - Quieres pipelines declarativos basados en Apache Beam.

## 🛠️ Herramientas utilizadas

- Cloud Dataproc (Spark / Hadoop)
- BigQuery
- Cloud Storage
- Cloud Bigtable
- Cloud Logging & Monitoring

## 🤓 Lo que aprendí

- Con Dataproc puedo **crear y administrar clústeres Spark/Hadoop rápidamente**, sin la complejidad de hacerlo manualmente.
- La facturación por segundo y las instancias interrumpibles lo hacen **muy rentable**.
- Permite **migrar cargas de trabajo existentes** sin cambios en código o herramientas.
- Entendí cómo elegir entre **Dataproc y Dataflow** según las necesidades: más control (Dataproc) o más simplicidad serverless (Dataflow).

## 🔗 Recursos útiles

- [Cloud Dataproc Overview](https://cloud.google.com/dataproc/docs/overview)
- [Comparación Dataproc vs Dataflow](https://cloud.google.com/solutions/big-data/data-processing-overview)

## 🚀 Resultado del día

Hoy aprendí a usar **Cloud Dataproc** para ejecutar clústeres administrados de Spark y Hadoop, entendiendo cómo integrarlo con el ecosistema de Google Cloud y cómo compararlo frente a **Cloud Dataflow** para elegir la mejor opción de procesamiento.
