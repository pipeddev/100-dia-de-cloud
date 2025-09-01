# ☁️ Día 65 – HTTP Load Balancer en Acción

📅 **#100DíasDeCloud – Google Cloud Platform**

---

## 🧠 Tema

Funcionamiento práctico de un balanceador de cargas HTTP(S) con instancias distribuidas regionalmente en GCP.

---

## 🧠 Descripción

Hoy exploré cómo opera un balanceador de cargas HTTP(S) global en un escenario real, con usuarios en múltiples regiones (NA y EMEA) accediendo a una misma aplicación distribuida 🌍.

### 🔁 Flujo general del balanceo de cargas:

1. **Regla de reenvío global**: Redirige las solicitudes entrantes al proxy HTTP.
2. **Proxy HTTP**: Evalúa la **URL Map** para determinar el backend adecuado.
3. **Servicio de backend**: Encargado de recibir y procesar las solicitudes, contiene múltiples configuraciones backend.
4. **Backends distribuidos**: Uno en `us-central1-a` y otro en `europe-west1-d`, cada uno con su **MIG**.
5. **Verificación de estado**: Asegura que solo las instancias saludables reciban tráfico.
6. **Enrutamiento inteligente**:

   - Si hay capacidad, se enruta al grupo más cercano.
   - Si no hay capacidad o fallan los health checks, se aplica **balanceo interregional**.
   - Si se usa **URL-based routing**, se puede enrutar a servicios distintos según el path (`/video`, `/web`, etc.).

> Todo esto se logra con una única dirección IP **Anycast global**, lo que simplifica el enrutamiento y mejora la disponibilidad y latencia.

---

## ⚙️ Flujo de trabajo

🔸 Implementar:

- Regla de reenvío global (`guestbook-forward`)
- Proxy de destino (`guestbook-target-proxy`)
- Mapeo de URLs (`guestbook-map`)
- Servicios de backend con configuraciones por región
- Health checks

🔸 Configurar:

- Grupos de instancias administrados en diferentes regiones
- Políticas de balanceo basadas en CPU o requests por segundo
- Afinidad de sesión si es necesario

---

## 🛠️ Herramientas utilizadas

- Google Compute Engine
- Managed Instance Groups
- Global HTTP(S) Load Balancer
- Health Checks
- Backend Services
- URL Maps
- Global Forwarding Rules

---

## 📚 Recursos útiles

- [Balanceo de cargas HTTP(S) – Documentación oficial](https://cloud.google.com/load-balancing/docs/https)
- [Health Checks en Google Cloud](https://cloud.google.com/load-balancing/docs/health-checks)

---

## ✅ Resultado del día

Aprendí cómo enruta tráfico de forma inteligente, evalúa el estado de las instancias y asegura alta disponibilidad para usuarios distribuidos por el mundo. Una herramienta esencial para arquitecturas modernas y resilientes.
