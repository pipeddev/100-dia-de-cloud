## ☁️ Día 70 – Balanceo de Cargas de Red (Network Load Balancing)

🧠 **Tema**

Balanceo de cargas de red (NLB) en Google Cloud Platform, un servicio **regional sin proxies** para distribuir tráfico TCP y UDP.

---

🧠 **Descripción**

Hoy aprendí sobre el **Network Load Balancer (NLB)** de Google Cloud, una opción regional que no utiliza proxy. Esto significa que el tráfico llega directamente a tus instancias backend, con **baja latencia** y sin terminación de sesión intermedia.

A diferencia de los balanceadores globales como HTTP(S), TCP Proxy o SSL Proxy, este balanceador solo distribuye tráfico entre instancias dentro de **una misma región**.

### 🔍 Características clave:

- 🔁 **Balanceo de carga sin proxy:** tráfico directo a las instancias.
- 🌍 **Regional:** tráfico distribuido solo dentro de una región.
- ⚡ **Baja latencia y alto rendimiento.**
- 🔌 **Soporte para tráfico TCP, UDP y SSL en puertos no admitidos por proxies.**
- 🔄 **Hash IP para selección de instancias** (source/destination IP + puerto).
- 🔧 **Dos arquitecturas posibles:**

  - Basado en **servicios de backend**
  - Basado en **grupos de destino (Target Pools)**

---

⚙️ **Comparativa de arquitecturas**

| Tipo                           | Características                                                                                                                                       |
| ------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Grupos de destino (legacy)** | - Hasta 50 por proyecto <br> - Una sola verificación de estado <br> - Solo tráfico TCP/UDP <br> - Todas las instancias deben estar en la misma región |
| **Servicios de backend**       | - Soporte para escalado automático, múltiples protocolos (TCP/SSL/HTTP/2) <br> - Vaciado de conexiones <br> - Conmutación por error configurable      |

---

🔧 **Casos de uso recomendados**

- Juegos online (tráfico UDP)
- Servidores VoIP
- Servicios que no usan puertos estándar
- Sistemas que exigen baja latencia y sin overhead de proxy

---

🛠️ **Herramientas utilizadas**

- Network Load Balancer
- Grupos de instancias
- Reglas de reenvío
- Verificaciones de estado
- Servicios de backend

---

📚 **Recursos útiles**

- [Network Load Balancing – Documentación oficial](https://cloud.google.com/load-balancing/docs/network)
- [Migrar de grupos de destino a servicios de backend](https://cloud.google.com/load-balancing/docs/network/backend-service)

---

📌 **Resultado del día**

Hoy comprendí cómo aprovechar el balanceo de cargas regional sin proxy, ideal para aplicaciones que necesitan velocidad, simplicidad y compatibilidad con múltiples protocolos.
