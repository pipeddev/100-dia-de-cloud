# 🌥️ Día 71 – Balanceo de cargas interno en Google Cloud

## 📌 Tema

Balanceo de cargas interno en Google Cloud (TCP/UDP y HTTPS).

## 📝 Descripción

El balanceador de cargas interno de Google Cloud es un servicio **regional y privado** diseñado para distribuir tráfico basado en **TCP, UDP y HTTPS** entre instancias dentro de una misma **VPC y región**.

A diferencia del balanceo externo, este servicio permite que el tráfico se mantenga **solo en la red interna de Google**, lo que mejora la **seguridad**, **reduce la latencia** y simplifica la configuración.

### 🔹 Puntos clave:

- Se accede únicamente mediante **direcciones IP internas**.
- El frontend del balanceador apunta a **instancias backend privadas**.
- Es una solución **distribuida y definida por software**, basada en **Andromeda** (la pila de virtualización de red de Google).
- El tráfico va **directamente del cliente al backend**, sin necesidad de dispositivos dedicados.

En el caso del **balanceo de cargas HTTPS interno**, este funciona a nivel **capa 7**, utilizando proxies de **Envoy** para ofrecer capacidades avanzadas de control de tráfico.

## ⚙️ Flujo de trabajo

Un ejemplo típico es un **arquitectura de 3 niveles**:

1. **Frontend web** → Balanceador HTTPS externo con IP global.
2. **Aplicación interna** → Balanceador interno (TCP/UDP o HTTPS) para comunicación entre servicios.
3. **Base de datos** → Nivel privado, solo accesible por la aplicación.

Este diseño evita exponer directamente niveles sensibles como aplicación o base de datos, lo que fortalece la **seguridad y aislamiento de la red**.

## 🛠️ Herramientas utilizadas

- Google Cloud VPC
- Internal TCP/UDP Load Balancer
- Internal HTTPS Load Balancer
- Andromeda (virtualización de red)
- Envoy (proxy de capa 7)

## 🤓 Lo que aprendí

- El balanceo interno es ideal para **microservicios y arquitecturas privadas** dentro de GCP.
- No se requieren **IPs públicas** para comunicación entre instancias internas.
- El modelo distribuido mejora la **eficiencia y escalabilidad**.
- El balanceo interno HTTPS habilita casos avanzados como **control de tráfico L7**.
- La arquitectura de **3 niveles** ayuda a proteger datos sensibles y reducir costos de red.

## 🔗 Recursos útiles

- [Documentación oficial: Load Balancing en GCP](https://cloud.google.com/load-balancing/docs)
- [Video sobre balanceo interno y Andromeda](https://cloud.google.com/andromeda)

## 🚀 Resultado del día

Hoy entendí cómo el balanceo de cargas interno de GCP permite crear arquitecturas seguras, privadas y escalables, especialmente en **entornos empresariales de múltiples niveles**.

---
