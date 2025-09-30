# 📅 Día 094 – Patrones comunes en la arquitectura de Cloud Monitoring

## 📌 Tema

Exploración de las capas y patrones comunes en la arquitectura de Cloud Monitoring, junto con las herramientas y servicios que la complementan.

---

## 📘 Descripción

Hoy profundicé en **Cloud Monitoring** y cómo se estructura su arquitectura típica, que se organiza en tres capas principales:

1. **Capa de recopilación de datos**

   - Reúne métricas, registros y seguimientos desde servicios como GKE, Compute Engine y App Engine.

2. **Capa de almacenamiento de datos**

   - Clasifica y organiza métricas a través de la **API de Cloud Monitoring**, para almacenarlas y analizarlas posteriormente.

3. **Capa de análisis y visualización de datos**

   - Permite identificar problemas y tendencias mediante paneles, verificaciones de tiempo de actividad, políticas de alertas y notificaciones.

Además, exploré cómo **Cloud Monitoring** se integra con diferentes enfoques y herramientas:

- **Supervisión de plataforma** (métricas predeterminadas y sin costo en más de 100 servicios de Google Cloud).
- **Prometheus** mediante **Google Cloud Managed Service for Prometheus (GMP)** para cargas en GKE.
- **Agente de operaciones** en Compute Engine, con más de 30 integraciones y soporte para OpenTelemetry.
- **Integraciones de socios** como Datadog, New Relic y Bindplane (Blue Medora) para ambientes híbridos o multicloud.

---

## 🛠️ Herramientas utilizadas

- Google Cloud Monitoring
- Google Kubernetes Engine (GKE)
- Google Compute Engine (GCE)
- Prometheus / Managed Service for Prometheus (GMP)
- Cloud Operations Agent
- Integraciones con terceros (Datadog, New Relic, Bindplane)

---

## ✅ Lo que aprendí

- La arquitectura de Cloud Monitoring se basa en **recopilación → almacenamiento → análisis/visualización**.
- **GMP** facilita usar Prometheus de manera administrada, con compatibilidad total con PromQL.
- El **Agente de operaciones** amplía la visibilidad en VMs y apps de terceros, apoyado en OpenTelemetry.
- **Bindplane** y otros socios permiten centralizar métricas en entornos **híbridos y multicloud**.
- Google ofrece más de **1,500 métricas predeterminadas sin costo**, lo que da una base sólida sin configuraciones iniciales.

---

## 📚 Recursos útiles

- [Cloud Monitoring Overview](https://cloud.google.com/monitoring/docs/overview)
- [Managed Service for Prometheus](https://cloud.google.com/stackdriver/docs/solutions/gke/prometheus)
- [Cloud Operations Agents](https://cloud.google.com/stackdriver/docs/solutions/agents/ops-agent/installation)

---

## 🎯 Resultado del día

Entendí cómo **Cloud Monitoring** estructura su arquitectura y cómo se adapta a distintos entornos (nativo de GCP, GKE, Compute Engine y multicloud), garantizando observabilidad unificada.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
