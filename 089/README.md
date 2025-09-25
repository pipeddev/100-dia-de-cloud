# ☁️ Día 89 — Observabilidad y supervisión en Google Cloud

Hoy comenzamos una nueva sección sobre la **observabilidad en la nube** y su papel en la confiabilidad de los sistemas. En entornos locales podíamos “ver” y revisar físicamente los servidores, pero en la nube la única forma de entender qué ocurre es mediante las herramientas de monitoreo y análisis que nos da la plataforma.

## 🌟 Puntos clave aprendidos

- La **supervisión** es la base de la confiabilidad: revela problemas urgentes, tendencias de uso y ayuda a planificar capacidad.
- Existen **cuatro indicadores clave** para medir el rendimiento y confiabilidad de un sistema:

  1. **Latencia** → tiempo que tarda un sistema en responder.
  2. **Tráfico** → cantidad de solicitudes que recibe el sistema.
  3. **Saturación** → qué tan llena está la capacidad del sistema (CPU, memoria, IOPS, etc.).
  4. **Errores** → fallos, respuestas incorrectas, códigos HTTP 4xx/5xx, excepciones.

- Estos indicadores permiten diagnosticar, anticipar y mejorar el rendimiento de aplicaciones y servicios.
- La **observabilidad** integra métricas, logs y trazas en un conjunto de herramientas como paneles, alertas y reportes automatizados.

## 🔧 Google Cloud Operations Suite

Google ofrece un conjunto de herramientas que permiten cubrir estas necesidades:

- **Cloud Monitoring** → métricas, paneles y alertas.
- **Cloud Logging** → recopilación y análisis de logs.
- **Error Reporting** → detección y análisis de fallas.
- **Cloud Trace** → seguimiento de latencia de solicitudes.
- **Cloud Profiler** → análisis de rendimiento de aplicaciones en producción.

## 🚀 Lo que aprendí

La observabilidad no solo ayuda a detectar errores, sino que es clave para **mejorar la experiencia del usuario, mantener la transparencia, y planificar la capacidad futura**.
Los cuatro indicadores (latencia, tráfico, saturación y errores) son la brújula para mantener sistemas sanos y confiables en la nube.
