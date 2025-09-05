## ☁️ Día 69 – Balanceo de Cargas Global con TCP Proxy en Google Cloud

### 🧠 Tema

**Balanceo de cargas global de tráfico TCP no encriptado (no-HTTP)** usando **TCP Proxy Load Balancer** en GCP.

### 🧠 Descripción

Hoy aprendí cómo GCP permite balancear tráfico TCP de manera global sin necesidad de usar HTTPS o HTTP. Este enfoque es ideal para servicios que utilizan TCP puro (como bases de datos, juegos en línea o sistemas legados) y que requieren alta disponibilidad y baja latencia.

✅ **Características del TCP Proxy Load Balancer:**

- Termina sesiones TCP en la capa de balanceo y redirige el tráfico hacia tus instancias.
- Balanceo automático entre regiones según la **capacidad disponible más cercana**.
- Admite **clientes IPv4 e IPv6**.
- Incluye **enrutamiento inteligente**, **parcheo automático** ante vulnerabilidades TCP.
- Tráfico entre proxy y backends puede ser **TCP o SSL** (recomendado: SSL para mayor seguridad).
- Similar en funcionamiento al **SSL Proxy Load Balancer**, pero sin necesidad de manejar certificados para el tráfico entrante.

🔁 **Flujo resumido:**

1. El usuario se conecta desde una ubicación remota (ej. Iowa o Boston).
2. El tráfico se enruta primero al proxy TCP global.
3. El balanceador establece una nueva conexión con el backend más cercano con capacidad.
4. El backend responde y completa la comunicación.

### ⚙️ Flujo de trabajo

1. Crear un TCP Proxy Load Balancer desde el panel de GCP.
2. Definir la regla de reenvío global para el puerto TCP deseado.
3. Asignar un proxy TCP de destino.
4. Crear y asociar servicios de backend (grupos de instancias en distintas regiones).
5. Verificar enrutamiento y latencia desde múltiples ubicaciones.
6. (Opcional) Configurar SSL en el tramo backend para tráfico seguro.

### 🛠️ Herramientas utilizadas

- Google Cloud Load Balancing
- TCP Proxy Load Balancer
- Compute Engine (VMs distribuidas regionalmente)
- Cloud Monitoring

### 📚 Recursos útiles

- [TCP Proxy Load Balancing – GCP Docs](https://cloud.google.com/load-balancing/docs/tcp)
- [Tipos de balanceadores en GCP](https://cloud.google.com/load-balancing/docs)

### ✅ Resultado del día

Hoy comprendí cómo balancear tráfico TCP no encriptado a nivel global, utilizando el proxy TCP de GCP. Aunque no realicé laboratorios prácticos, el flujo de red quedó muy claro para futuras implementaciones de servicios que no usan HTTP pero necesitan alta disponibilidad.
