# ☁️ Día 58 - Cloud Interconnect y Servicios de Intercambio de Tráfico en Google Cloud

## 📌 Tema

Exploración de las opciones de **conectividad física y lógica** que Google Cloud ofrece para integrar tu infraestructura local con su red global.

---

## 📖 Descripción

Hoy estudié los distintos tipos de **servicios de interconexión e intercambio de tráfico** que permiten conectar una red local, un data center o una red de otro proveedor con la infraestructura de Google Cloud, con **alto rendimiento**, **baja latencia** y **seguridad**.

---

### 🔗 Tipos de conexión disponibles

Google Cloud clasifica sus servicios de conectividad en:

#### 1. **Cloud Interconnect**:

Conexiones privadas y dedicadas hacia la red de Google. Ofrece:

- 🚪 **Dedicated Interconnect**:

  - Conexión **física dedicada** a la red de Google.
  - Alta capacidad (hasta 100 Gbps por circuito).
  - Usada por grandes empresas o entornos críticos.
  - **Conexión de capa 2** (conectividad directa a IPs internas).

- 🤝 **Partner Interconnect**:

  - Conexión compartida a través de un **socio proveedor (partner)** autorizado.
  - Más flexible, menos costosa.
  - Soporta **capas 2 y 3**.

---

#### 2. **Servicios de Intercambio de Tráfico (Peering)**:

- 🔄 **Direct Peering**:

  - Conexión directa entre la red de tu empresa y la red de Google.
  - Acceso a servicios públicos como **APIs, Google Workspace, YouTube**.

- 🌐 **Carrier Peering (Intercambio por proveedor)**:

  - Similar a Direct Peering pero a través de un proveedor/carrier.
  - Acceso a servicios públicos de Google, pero a través de rutas IP públicas.

---

### 🌉 Comparación con Cloud VPN

- **Cloud VPN**:

  - Usa **Internet público** para la conexión.
  - Trafico **encriptado**.
  - Acceso a **IPs internas (RFC 1918)**.
  - Buena opción para comenzar o complementar otras conexiones.

---

## 🛠️ Herramientas utilizadas

- Cloud Interconnect (Dedicated y Partner)
- Direct Peering
- Carrier Peering
- Cloud VPN

---

## 📚 Lo que aprendí

- Existen múltiples **niveles de conexión según la necesidad** de seguridad, rendimiento y disponibilidad.
- Las **conexiones dedicadas** ofrecen más control y velocidad, mientras que las compartidas son más flexibles y fáciles de implementar.
- Es importante entender la **capa de red (2 o 3)** para seleccionar la opción adecuada.
- **Cloud VPN** es una solución fácil de implementar y útil como complemento de otras opciones de interconexión.

---

## 🔗 Recursos útiles

- [Cloud Interconnect Overview](https://cloud.google.com/network-connectivity/docs/interconnect)
- [Peering Options](https://cloud.google.com/network-connectivity/docs/overview#peering)
- [Comparación entre VPN, Interconnect y Peering](https://cloud.google.com/network-connectivity/docs/choosing-product)

---

## ✅ Resultado del día

Hoy aprendí a **diseñar la conectividad física y lógica** entre mi red local y Google Cloud, entendiendo las **diferencias clave entre VPN, Interconnect y Peering**, y cuándo usar cada opción según disponibilidad, seguridad y rendimiento.
