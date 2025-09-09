# 🌥️ Día 72 – Elegir el balanceador de cargas adecuado en Google Cloud

## 📌 Tema

Criterios y guía para seleccionar el balanceador de cargas correcto en Google Cloud.

## 📝 Descripción

Ahora que revisamos los diferentes servicios de **Cloud Load Balancing**, es momento de entender **cómo elegir la opción más adecuada** según el tipo de tráfico, el alcance de la aplicación y los requerimientos técnicos.

### 🔹 Compatibilidad con IPv6

- No todos los balanceadores soportan IPv6.
- Solo los balanceadores **HTTPS, de proxy SSL y de TCP** son compatibles con clientes IPv6.
- La **finalización IPv6** permite recibir solicitudes en IPv6 y conectarlas mediante proxy IPv4 a los backends.
- De esta forma, los usuarios pueden acceder con IPv4 o IPv6, pero tus backends internos siguen funcionando con IPv4.

Ejemplo:
Un sitio web `www.example.com` puede resolverse en **IPv4** y **IPv6** mediante Cloud DNS.

- Usuario en Nueva York → conexión IPv4.
- Usuario en Iowa → conexión IPv6.
  Ambos llegan al balanceador, que traduce y reenvía la solicitud a backends IPv4.

### 🔹 Tipos de balanceadores recomendados

La selección depende del **tipo de tráfico y necesidades**:

- **Balanceador de aplicaciones (HTTP/HTTPS)**
  👉 Ideal para tráfico HTTPS con funciones avanzadas (control de tráfico en capa 7).

- **Balanceador de red de proxy (TCP/SSL Proxy)**
  👉 Recomendado cuando se necesita **delegación de TLS, proxies TCP o balanceo externo hacia backends multi-región**.

- **Balanceador de red de transferencia (Network TCP/UDP passthrough)**
  👉 Útil si quieres **evitar la sobrecarga de proxies, exponer direcciones IP de clientes, o usar protocolos como UDP, ICMP y ESP**.

### 🔹 Consideraciones clave

- ¿El tráfico será **interno o externo**?
- ¿Necesitas backends **globales o regionales**?
- ¿Requieres un servicio **administrado** (frontal de Google o proxy Envoy) o una configuración más directa?

## ⚙️ Flujo de trabajo

1. Identificar el **tipo de tráfico** (HTTP/HTTPS, TCP, UDP, etc.).
2. Determinar si la aplicación es **externa o interna**.
3. Verificar si se requiere compatibilidad con **IPv6**.
4. Elegir entre balanceadores **administrados** o **no administrados**.
5. Seleccionar el esquema de balanceo según los requisitos de red.

## 🛠️ Herramientas utilizadas

- Cloud Load Balancing (HTTP(S), TCP/UDP, SSL Proxy)
- Cloud DNS (para resolución IPv4/IPv6)
- Google Frontend (GFE)
- Envoy Proxy (para balanceo L7 administrado)

## 🤓 Lo que aprendí

- No todos los balanceadores soportan clientes IPv6, y es clave considerar esto en arquitecturas modernas.
- La **finalización de IPv6** es transparente para los backends, que pueden seguir usando IPv4.
- La decisión de qué balanceador usar depende de: **tipo de tráfico, alcance (interno/externo) y protocolos**.
- Los **balanceadores administrados** simplifican la operación, mientras que los de transferencia son útiles para **protocolos adicionales y menor sobrecarga**.

## 🔗 Recursos útiles

- [Guía de selección de balanceadores de cargas en GCP](https://cloud.google.com/load-balancing/docs)
- [Niveles de servicio de red en Google Cloud](https://cloud.google.com/network-tiers/docs/overview)

## 🚀 Resultado del día

Hoy aprendí cómo **definir el balanceador correcto** en Google Cloud según el tipo de tráfico, la compatibilidad con IPv6 y el alcance de la aplicación, lo que permite construir arquitecturas **más seguras, escalables y eficientes**.
