## ☁️ Día 63 – Autoscaling y Verificaciones de Estado en MIG

📅 #100DíasDeCloud – Google Cloud Platform

---

### 🧠 Tema

**Ajuste de escala automático (autoscaling) y verificaciones de estado (health checks)** en grupos de instancias administrados (MIG).

---

### 🧠 Descripción

Hoy profundicé en cómo los MIG pueden escalar automáticamente según la carga y cómo detectar instancias en mal estado para mantener la disponibilidad de nuestras aplicaciones.

✅ **Ajuste de escala automático (autoscaling):**
Los grupos agregan o eliminan instancias automáticamente basándose en políticas como:

- Uso de CPU (ej. mantenerlo bajo un 75%)
- Capacidad del balanceador de carga
- Métricas de Cloud Monitoring
- Mensajes en colas como Pub/Sub
- Programación por horarios

✅ **Verificaciones de estado (health checks):**
Permiten saber si una instancia está operativa. Si falla una cierta cantidad de veces en un intervalo, es reemplazada automáticamente.
Parámetros configurables:

- Protocolo (HTTP, TCP)
- Puerto
- Tiempo de espera
- Umbrales de fallos y éxitos consecutivos

Estas funcionalidades permiten tener una infraestructura autosuficiente, escalable y resiliente ante fallos 🛠️.

---

### ⚙️ Flujo de trabajo

1. Crear un MIG con plantilla de instancia.
2. Activar autoscaling seleccionando:

   - Métrica objetivo (ej. uso de CPU)
   - Valor de objetivo (ej. 75%)

3. Configurar una verificación de estado:

   - Protocolo y puerto
   - Intervalo y timeout
   - Umbral de éxito/fallo

4. Supervisar métricas desde el gráfico de uso (CPU, red, disco).
5. Ajustar políticas con base en observaciones reales desde Cloud Monitoring.

---

### 🛠️ Herramientas utilizadas

- Compute Engine (Managed Instance Groups)
- Cloud Monitoring
- Autoscaler
- Health checks
- Stackdriver Alerts

---

### 📚 Recursos útiles

- [Autoscaler – Documentación oficial](https://cloud.google.com/compute/docs/autoscaler)
- [Health Checks – Documentación oficial](https://cloud.google.com/load-balancing/docs/health-check-concepts)

---

### ✅ Resultado del día

Aprender sobre escalamiento automático y mecanismos de detección de fallos con MIGs.
Me quedó más clara la importancia de automatizar la respuesta a la demanda y cómo mantener la salud del sistema sin intervención manual.
