# 🌥️ Día 76 – Introducción a BigQuery en Google Cloud

## 📌 Tema

BigQuery como **almacén de datos en la nube** sin servidores.

## 📝 Descripción

**BigQuery** es el **data warehouse serverless, escalable y rentable** de Google Cloud.
Permite realizar **consultas de nivel petabyte** de manera rápida, gracias a la potencia de la infraestructura de Google.

🔹 Al ser un servicio totalmente administrado, **no necesitas servidores ni administradores de bases de datos**.
🔹 Solo te enfocas en obtener información valiosa mediante **SQL estándar**, sin preocuparte por la infraestructura.
🔹 Es ampliamente utilizado por empresas de todos los tamaños para **análisis de datos, BI y machine learning**.

## ⚙️ Acceso a BigQuery

Puedes interactuar con BigQuery de diferentes formas:

- 🌐 **Consola de Cloud** (interfaz gráfica).
- 💻 **Herramienta de línea de comandos** (`bq`).
- 📡 **API REST de BigQuery** con bibliotecas cliente (Java, .NET, Python, etc.).
- 📊 Herramientas externas para **visualización, carga y análisis de datos** (ej. Looker, Data Studio, Tableau).

## 🔹 Ejemplo de consulta SQL

Supongamos que tenemos una tabla llamada `groceries`.
Una consulta básica en BigQuery podría verse así:

```sql
SELECT
  g.*
FROM
  `project_id.dataset.groceries` AS g;
```

Este ejemplo retorna todas las columnas de la tabla `groceries` usando un alias (`g`).

## 🛠️ Herramientas utilizadas

- BigQuery Console
- BigQuery CLI (`bq`)
- BigQuery API (REST + client libraries)

## 🤓 Lo que aprendí

- BigQuery permite **consultas rápidas a escala de petabytes** sin tener que administrar infraestructura.
- Es posible trabajar con SQL estándar, lo que facilita la adopción para equipos ya familiarizados con SQL.
- Puedo conectarlo con **APIs, bibliotecas cliente y herramientas de visualización externas**.
- Es un servicio fundamental para proyectos de **analítica, BI y machine learning** en la nube.

## 🔗 Recursos útiles

- [BigQuery Overview](https://cloud.google.com/bigquery/docs/introduction)
- [BigQuery SQL Reference](https://cloud.google.com/bigquery/docs/reference/standard-sql/query-syntax)

## 🚀 Resultado del día

Hoy entendí cómo **BigQuery simplifica el análisis de datos a gran escala** sin necesidad de administrar servidores, permitiendo enfocarme en la **información y no en la infraestructura**.
