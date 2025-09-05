# ☁️ Día 68 – Balanceo de cargas con Proxy TCP/SSL en Google Cloud

🧠 **Tema**
Balanceo de cargas con **Proxy SSL y TCP**, servicios globales para tráfico encriptado y no HTTP.

🧠 **Descripción**
Hoy aprendí cómo Google Cloud permite distribuir tráfico seguro (no HTTP) de manera eficiente y global a través de los balanceadores de cargas **SSL Proxy** y **TCP Proxy**.

🔐 **Balanceador de cargas SSL Proxy**

- Diseñado para tráfico SSL no-HTTP.
- Finaliza la conexión SSL en el balanceador (TLS termination).
- Reenvía el tráfico en SSL o TCP a backends regionales.
- Ideal para servicios como correo seguro, aplicaciones personalizadas con sockets seguros, etc.

🔌 **Ventajas del SSL Proxy Load Balancer**

- Global y escalable.
- Soporte para IPv4 e IPv6.
- Enrutamiento inteligente hacia backends con capacidad.
- Administración centralizada de certificados.
- Parches automáticos ante vulnerabilidades en TLS/SSL.
- Reducción de carga en las VMs usando certificados autofirmados.

🧭 **Ejemplo de arquitectura**

- Un usuario desde Boston o Iowa se conecta mediante SSL a una IP global.
- La conexión es terminada en el balanceador de cargas.
- Se enruta hacia la región más cercana y con capacidad: `us-east1` o `us-central1`.

⚙️ **Flujo de trabajo**

1. Crear backends (VMs en múltiples regiones).
2. Configurar certificados SSL.
3. Configurar el servicio backend y políticas de SSL.
4. Crear el proxy SSL.
5. Configurar regla de reenvío global (global forwarding rule).
6. Asociar la IP externa global.

🛠️ **Herramientas utilizadas**

- Compute Engine
- Google Cloud Load Balancing
- SSL Certificates
- Global Forwarding Rules

📚 **Recursos útiles**

- [SSL Proxy Load Balancing](https://cloud.google.com/load-balancing/docs/ssl/)
- [TCP Proxy Load Balancing](https://cloud.google.com/load-balancing/docs/tcp/)
- [Best practices](https://cloud.google.com/load-balancing/docs/ssl/best-practices)

✅ **Resultado del día**
Hoy comprendí el flujo completo de tráfico cifrado en un entorno multi-región utilizando los balanceadores **SSL Proxy** y **TCP Proxy** de GCP. No realicé laboratorio práctico, pero afianzé la teoría de balanceo global seguro para aplicaciones que no usan HTTP.
