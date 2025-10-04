# 📅 Día 096 – Modelo de datos en Cloud Monitoring y visualización en paneles

## 📌 Tema

Modelo de datos en Monitoring y cómo visualizar métricas en gráficos y paneles personalizados.

---

## 📘 Descripción

Hoy avancé en el reto de #100DaysOfCloud explorando el **modelo de datos de Cloud Monitoring** y cómo se estructuran las métricas para luego analizarlas en paneles.

Las métricas en Cloud Monitoring se registran en **series temporales**, que incluyen:

- **Metric** → define el tipo de métrica y sus etiquetas.
- **Resource** → especifica el recurso supervisado y sus etiquetas.
- **MetricKind** → indica cómo se interpretan los valores:

  - _GAUGE_: mide un instante específico (ej: uso de CPU).
  - _DELTA_: mide el cambio en un intervalo (ej: solicitudes por segundo).
  - _CUMULATIVE_: valores que aumentan en el tiempo (ej: bytes enviados).

- **ValueType** → tipo de dato (BOOL, INT64, DOUBLE, STRING, DISTRIBUTION).

Una vez recopiladas, estas métricas pueden visualizarse en **gráficos y paneles**:

- Paneles creados automáticamente según los recursos (Compute Engine, GKE, etc.).
- **Explorador de métricas** para crear gráficos ad-hoc, aplicar filtros, agrupar y alinear series temporales.
- Opciones avanzadas como alias de leyenda, comparación con valores pasados, umbrales y modos de análisis (estándar, estadísticas, rayos X).

Esto permite pasar de datos crudos a **visualizaciones claras y accionables**, mejorando la observabilidad y la toma de decisiones.

---

## 🛠️ Herramientas utilizadas

- Google Cloud Monitoring
- Explorador de métricas
- Paneles personalizados
- Cloud Console

---

## ✅ Lo que aprendí

- Cómo se estructura el modelo de datos en series temporales.
- Diferencias entre métricas _GAUGE_, _DELTA_ y _CUMULATIVE_.
- Uso del Explorador de métricas para filtrar, agrupar y alinear datos.
- Opciones avanzadas de visualización: alias de leyenda, comparaciones históricas y umbrales.

---

## 📚 Recursos útiles

- [Documentación de Cloud Monitoring – Métricas](https://cloud.google.com/monitoring/api/v3/metrics)
- [Explorador de métricas en Google Cloud](https://cloud.google.com/monitoring/charts/metrics-explorer)

---

## 🎯 Resultado del día

Pude comprender cómo Cloud Monitoring transforma datos en **gráficos útiles y paneles personalizados**, optimizando la observabilidad de sistemas en GCP.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
