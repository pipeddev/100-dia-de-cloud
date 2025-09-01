## ☁️ Día 64 – Balanceo de Cargas HTTP(S) en Google Cloud

📅 **#100DíasDeCloud – Google Cloud Platform**

---

### 🧠 Tema

Balanceo de cargas HTTP(S) global en la capa 7 (aplicación) del modelo OSI, para distribuir solicitudes entrantes hacia múltiples instancias de backend.

---

### 🧠 Descripción

Hoy aprendí cómo funciona el **balanceador de cargas HTTP(S)** en Google Cloud, una herramienta esencial para distribuir tráfico a través de múltiples instancias o regiones, mejorar la disponibilidad y escalar automáticamente nuestras aplicaciones.

Este balanceador opera en la **capa 7 del modelo OSI (HTTP/HTTPS)** y permite:

- Enrutamiento inteligente basado en URL.
- Distribución del tráfico entre backends en múltiples regiones.
- Escalado global con una sola dirección IP Anycast.
- Compatibilidad con IPv4 e IPv6.
- Balanceo de carga sin necesidad de precalentamiento.

---

### ⚙️ Flujo de trabajo

1. **Regla de reenvío global:** Dirige tráfico entrante a un proxy HTTP(S) de destino.
2. **Proxy HTTP(S):** Evalúa la URL entrante y enruta la solicitud al servicio de backend adecuado.
3. **Servicio de backend:**

   - Aplica lógica de verificación de estado.
   - Evalúa afinidad de sesión (si está configurada).
   - Considera el tiempo de espera para respuestas backend.

4. **Backends (grupos de instancias):**

   - Administrados o no administrados.
   - Pueden escalar automáticamente según demanda.
   - Su modo de balanceo puede ser por CPU o RPS (requests per second).

5. **Reglas de escalamiento y balanceo:**

   - El modo de balanceo define cuándo una instancia está al máximo.
   - El parámetro de capacidad controla cuánto del recurso se usa.

---

### 🔎 Conceptos clave

- **URL Map:** Permite enrutar por patrones (e.g., `/audio`, `/video`) a diferentes backends.
- **Anycast IP:** Proporciona una IP global que enruta al backend más cercano disponible.
- **Affinity (afinidad de sesión):** Mantiene la conexión entre un cliente y la misma instancia.
- **Timeout fijo:** Define cuánto esperar por respuesta del backend (por defecto 30s).
- **Verificación de estado:** Solo las instancias saludables reciben tráfico.

---

### 🛠️ Herramientas utilizadas

- Google Cloud Load Balancing (HTTP(S))
- Compute Engine – Managed Instance Groups
- Cloud Monitoring
- URL Maps
- Health checks

---

### 📚 Recursos útiles

- [Documentación Balanceador HTTP(S)](https://cloud.google.com/load-balancing/docs/https)
- [Diseño de balanceadores en GCP](https://cloud.google.com/load-balancing/docs/)

---

### ✅ Resultado del día

Comprendí cómo funciona el balanceador HTTP(S), desde la solicitud entrante hasta la elección del backend. Este conocimiento será clave para diseñar arquitecturas escalables, tolerantes a fallos y globales en futuras aplicaciones cloud.
