# 📅 Día 093 – Cloud Trace y Cloud Profiler en Google Cloud

## 📌 Tema

Exploración de **Cloud Trace** y **Cloud Profiler**, servicios de Google Cloud para el análisis de latencia y rendimiento de aplicaciones en producción.

---

## 📘 Descripción

Hoy aprendí sobre dos herramientas clave de observabilidad dentro de Google Cloud’s operations suite:

- **Cloud Trace** → recopila y analiza datos de **latencia en aplicaciones distribuidas**, mostrando informes en tiempo casi real. Permite detectar degradaciones de rendimiento automáticamente y ofrece reportes detallados para identificar dónde se producen cuellos de botella.
- **Cloud Profiler** → analiza de forma continua el **uso de CPU y memoria** de una aplicación en ejecución, con un impacto mínimo en el rendimiento. Genera gráficos tipo llama (flame graphs) que ayudan a entender qué partes del código consumen más recursos.

Ambas herramientas se integran con aplicaciones desplegadas en **App Engine, Compute Engine y GKE**, además de admitir entornos locales o en otras nubes.

---

## 🛠️ Herramientas utilizadas

- Google Cloud Trace
- Google Cloud Profiler
- Google Cloud Console (visualización de métricas y gráficos)

---

## ✅ Lo que aprendí

- Cloud Trace **detecta automáticamente degradaciones** de latencia en aplicaciones distribuidas.
- Permite consultar estadísticas de rendimiento en **tiempo real**.
- Cloud Profiler se integra con múltiples lenguajes (Java, Go, Python, Node.js).
- El **gráfico tipo llama** ayuda a visualizar consumo de CPU/memoria por función.
- Ambas herramientas soportan cargas de trabajo en Google Cloud y fuera de ella, usando estándares abiertos como **Prometheus** y **OpenTelemetry**.

---

## 📚 Recursos útiles

- [Documentación oficial de Cloud Trace](https://cloud.google.com/trace/docs)
- [Documentación oficial de Cloud Profiler](https://cloud.google.com/profiler/docs)
- [Google Cloud Operations Suite](https://cloud.google.com/products/operations)

---

## 🎯 Resultado del día

Comprendí cómo **Cloud Trace** y **Cloud Profiler** permiten identificar problemas ocultos en latencia y consumo de recursos, ayudando a optimizar aplicaciones en producción sin afectar la experiencia del usuario.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
