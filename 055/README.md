# ☁️ Día 55 - Google Cloud’s Operations Suite y Cloud Monitoring

## 📌 Tema

Supervisión centralizada, métricas, alertas y buenas prácticas operativas con **Google Cloud’s Operations Suite** (antes Stackdriver).

## 📖 Descripción

Hoy estudié cómo **monitorear y operar eficientemente** recursos en GCP y AWS usando **Cloud Monitoring**, parte de la suite de operaciones integrada de Google Cloud.

---

### 🧰 Google Cloud’s Operations Suite

Es un conjunto de herramientas integradas para:

- 🔍 Supervisión (Monitoring)
- 📜 Registro (Logging)
- ❗ Reporte de errores
- 🧵 Seguimiento de fallas (Tracing)

Beneficios clave:

- Descubrimiento automático de recursos en GCP y AWS.
- Interfaz unificada para **ver métricas, alertas y registros**.
- Integración con socios tecnológicos para expandir funciones de seguridad y cumplimiento.
- Modelo **pay-as-you-go** con cuota gratuita.

---

### 📊 Cloud Monitoring

Herramienta principal para **observar el estado y rendimiento de los recursos**, desde instancias hasta servicios.

📌 Funcionalidades principales:

- Paneles personalizados con **gráficos de métricas** (CPU, red, etc).
- **Verificaciones de tiempo de actividad** (HTTP, HTTPS, TCP).
- **Políticas de alertas** automáticas.
- Supervisión cruzada entre proyectos y cuentas AWS usando **permisos de métricas**.

🔎 **Métricas**:

- Se pueden visualizar desde GCP o exportar.
- Posibilidad de crear **métricas personalizadas**, por ejemplo: usuarios activos en un juego online.

⚙️ **Agente de operaciones**:

- Recolecta datos desde dentro de VMs (uso de memoria, aplicaciones como MySQL, NGINX, SAP HANA, etc).
- Compatible con sistemas Linux y Windows.

📢 **Alertas recomendadas**:

- Basadas en síntomas, no solo en causas.
- Múltiples canales (correo, SMS, Pub/Sub).
- Personalizadas por público y criticidad.
- Evitar ruido y falsos positivos.

---

## 🛠️ Herramientas utilizadas

- Cloud Monitoring
- Cloud Logging
- Cloud Pub/Sub (para notificaciones)
- Agente de operaciones
- AWS connector (para monitoreo multi-cloud)

## 📚 Lo que aprendí

- GCP permite visibilidad completa de sistemas distribuidos con paneles y alertas en tiempo real.
- Las métricas personalizadas permiten escalar según necesidades del negocio, no solo de la infraestructura.
- Las prácticas de SRE (Site Reliability Engineering) están embebidas en Cloud Monitoring.
- Las alertas deben ser accionables, claras y evitar el “alert fatigue”.

## 🔗 Recursos útiles

- [Operations Suite (documentación oficial)](https://cloud.google.com/products/operations)
- [Cloud Monitoring](https://cloud.google.com/monitoring)
- [Agente de operaciones](https://cloud.google.com/monitoring/agent)

## ✅ Resultado del día

Hoy aprendí cómo usar **Cloud Monitoring** para asegurar que mis aplicaciones sean **confiables, observables y escalables**.
Con una sola herramienta puedo monitorear VMs, servicios, aplicaciones personalizadas y recibir alertas proactivas para tomar decisiones a tiempo.
