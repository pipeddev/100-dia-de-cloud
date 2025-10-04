# 📅 Día 097 – MQL y PromQL en Cloud Monitoring

## 📌 Tema

Lenguajes de consulta para métricas en Cloud Monitoring: **MQL (Monitoring Query Language)** y **PromQL**.

---

## 📘 Descripción

Hoy aprendí cómo interactuar de manera más avanzada con métricas en Google Cloud utilizando lenguajes de consulta en lugar de interfaces gráficas.

🔹 **MQL** es un lenguaje expresivo y flexible que permite recuperar, filtrar, unir y manipular métricas de Cloud Monitoring en forma de series temporales. Con él, puedes aplicar operaciones matemáticas, lógicas, percentiles arbitrarios, expresiones regulares y crear gráficos y alertas personalizadas.

🔹 **PromQL** es el lenguaje de Prometheus que también está soportado por Cloud Monitoring, lo que permite consultar y graficar datos de servicios de Google Cloud (como GKE y Compute Engine), métricas definidas por el usuario y métricas desde Google Cloud Managed Service for Prometheus.

Ambos lenguajes pueden usarse desde el **Explorador de métricas** con la opción de “Código” y facilitan análisis más complejos que los que se pueden hacer con menús.

Un ejemplo práctico de MQL es calcular la proporción de solicitudes con error HTTP 500 sobre el total de solicitudes en un balanceador de carga. Esto ayuda a monitorear un **SLO crítico** como la tasa de errores de un servicio web distribuido.

---

## 🛠️ Herramientas utilizadas

- Cloud Monitoring
- MQL (Monitoring Query Language)
- PromQL
- Google Cloud Managed Service for Prometheus
- Grafana

---

## ✅ Lo que aprendí

- Que Cloud Monitoring no solo es dashboards: también soporta **lenguajes de consulta avanzados**.
- MQL permite encadenar operaciones al estilo _pipes_ de Linux (`|`) para consultas complejas.
- PromQL ofrece compatibilidad con workloads que ya usan **Prometheus**.
- Se pueden hacer comparaciones entre métricas en diferentes periodos (ej. semana a semana, año a año).
- Cómo usar consultas para detectar errores críticos y monitorear indicadores de SRE.

---

## 📚 Recursos útiles

- [Monitoring Query Language (MQL)](https://cloud.google.com/monitoring/mql)
- [PromQL en Cloud Monitoring](https://cloud.google.com/monitoring/promql)
- [Managed Service for Prometheus](https://cloud.google.com/stackdriver/docs/solutions/slo-monitoring)

---

## 🎯 Resultado del día

Exploré cómo **MQL y PromQL amplían la observabilidad** en Google Cloud al permitir consultas y cálculos avanzados sobre métricas, esenciales para monitoreo de SLOs y análisis profundo de sistemas distribuidos.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
