# ☁️ Día 57 - Cloud VPN: Clásica vs Alta Disponibilidad (HA) en Google Cloud

## 📌 Tema

Aprendizaje sobre los servicios de red privada virtual y conectividad segura en GCP mediante **Cloud VPN**, con foco en sus dos variantes: **VPN clásica** y **VPN con alta disponibilidad (HA)**.

---

## 📖 Descripción

Hoy profundicé en cómo conectar de forma **segura y cifrada** una red local o de otro proveedor de nube con Google Cloud, utilizando túneles **IPsec gestionados por Cloud VPN**.

---

### 🔐 Cloud VPN Clásica

- Crea un **túnel cifrado** (IPsec) entre tu red on-premise y una **red VPC** en GCP.
- Usa **rutas estáticas o dinámicas** (con Cloud Router).
- Requiere configurar **dos túneles** por conexión (bidireccional).
- Nivel de servicio (ANS): **99.9% de disponibilidad**.
- Ideal para **conexiones de bajo volumen**.
- No permite conexiones de clientes individuales (solo sitio a sitio).
- Soporta IKEv1 / IKEv2.

💡 **Importante**: la MTU no debe superar los **1460 bytes** por el overhead del cifrado.

---

### 🛡️ Cloud VPN con Alta Disponibilidad (HA)

- Conexión IPsec altamente disponible en una **única región**.
- Nivel de servicio: **99.99% de disponibilidad**.
- Usa **Cloud Router + BGP** para enrutamiento dinámico.
- Requiere **2 o 4 túneles** entre interfaces.
- GCP asigna automáticamente **2 IPs externas** (una por interfaz).
- Soporta configuraciones:

  - Con dispositivos físicos o virtuales (on-premise o AWS).
  - Entre redes VPC de GCP (VPN activa-activa o activa-pasiva).
  - Con ECMP (Equal-Cost Multi-Path) para balancear tráfico.

📌 **Redundancia**: al tener dos interfaces, tolera fallas, mantenimiento o actualizaciones sin perder conectividad.

---

### 🧠 Cloud Router + BGP

- Administra el **intercambio automático de rutas**.
- Permite que las **nuevas subredes** se anuncien entre redes sin modificar el túnel.
- Usa IPs locales dentro del rango **169.254.0.0/16** para la sesión BGP.

---

## 🛠️ Herramientas utilizadas

- Cloud VPN (Clásica y HA)
- Cloud Router
- Túneles IPsec
- BGP (Protocolo de puerta de enlace de frontera)

---

## 📚 Lo que aprendí

- Las **VPN clásicas** son útiles para conexiones básicas, pero tienen limitaciones.
- Las **VPN con HA** son ideales para entornos críticos, con necesidades de disponibilidad y redundancia.
- Cloud Router y BGP automatizan el enrutamiento, haciéndolo más flexible y mantenible.
- Entendí cómo diseñar arquitecturas híbridas que conectan múltiples regiones y plataformas (GCP, AWS, on-prem).

---

## 🔗 Recursos útiles

- [Documentación de Cloud VPN](https://cloud.google.com/network-connectivity/docs/vpn)
- [Cloud Router y BGP](https://cloud.google.com/network-connectivity/docs/router/concepts/overview)
- [Diseños de referencia para VPN HA](https://cloud.google.com/network-connectivity/docs/vpn/how-to/creating-ha-vpn)

---

## ✅ Resultado del día

Hoy aprendí cómo establecer **conectividad segura, cifrada y tolerante a fallos** entre redes, tanto en GCP como fuera de ella.
La **alta disponibilidad, redundancia y escalabilidad** son claves en arquitecturas modernas híbridas o multicloud, y GCP lo facilita con su suite de redes.
