# ☁️ Día 60 - Servicios de Intercambio de Tráfico en Google Cloud: Directo y por Proveedores

## 📌 Tema

Exploración de las opciones de **intercambio de tráfico público** en Google Cloud, que permiten acceder a los servicios públicos de Google (como APIs, Google Workspace, YouTube, etc.) a través de conexiones optimizadas de red.

---

## 📖 Descripción

Hoy aprendí sobre dos formas de **intercambiar tráfico de forma eficiente entre mi red y la red pública de Google**, sin usar internet tradicional:

- 🔄 **Intercambio de tráfico directo (Direct Peering)**
- 🌐 **Intercambio por proveedores (Carrier Peering)**

Estas opciones no dan acceso a IPs internas, pero permiten mejorar la conectividad hacia los **servicios públicos de Google** mediante rutas más estables y de menor latencia.

---

### 🔄 1. Intercambio de tráfico directo (Direct Peering)

Conexión directa entre **tu red** y la **red perimetral de Google**, en un **PoP (Point of Presence)** compartido.

✅ Características:

- Acceso optimizado a todos los servicios públicos de Google.
- Usa **BGP** para intercambio de rutas.
- No ofrece **SLA** (Acuerdo de Nivel de Servicio).
- Capacidad: **10 Gbps por vínculo**.
- Requiere estar presente en una ubicación física con presencia perimetral de Google.

📍 Ver ubicaciones disponibles en [PeeringDB](https://www.peeringdb.com/net/4335).

---

### 🌐 2. Intercambio de tráfico por proveedores (Carrier Peering)

Conexión a Google a través de un **proveedor de servicios de red autorizado** (carrier).

✅ Características:

- Ideal si no estás cerca de un PoP de Google o no cumples con los requisitos de Direct Peering.
- Capacidad y requisitos dependen del **proveedor**.
- No ofrece **SLA**.
- Acceso a **servicios públicos de Google** mediante rutas optimizadas.

📍 Lista de proveedores disponible en la [documentación oficial](https://cloud.google.com/network-connectivity/docs/overview#peering).

---

### 📊 Comparación rápida

| Característica              | Direct Peering | Carrier Peering            |
| --------------------------- | -------------- | -------------------------- |
| Acceso a servicios públicos | ✅             | ✅                         |
| Requiere PoP de Google      | ✅ Sí          | ❌ No                      |
| A través de un proveedor    | ❌ No          | ✅ Sí                      |
| SLA                         | ❌ No          | ❌ No                      |
| Capacidad estimada          | 10 Gbps        | Variable (según proveedor) |
| Requiere BGP                | ✅             | ✅                         |

---

## 🛠️ Herramientas utilizadas

- Direct Peering
- Carrier Peering
- BGP (Border Gateway Protocol)

---

## 📚 Lo que aprendí

- Ambas opciones son útiles para **optimizar el acceso a servicios públicos de Google** desde redes corporativas.
- **No proporcionan acceso a IPs internas** como Cloud VPN o Interconnect.
- Elegir entre directo o por proveedor depende de:

  - Tu ubicación física respecto a los PoP de Google.
  - Tu relación con proveedores/carriers autorizados.
  - La capacidad que necesitas y la facilidad de implementación.

---

## 🔗 Recursos útiles

- [Google Cloud Peering Overview](https://cloud.google.com/network-connectivity/docs/overview#peering)
- [PeeringDB - Google](https://www.peeringdb.com/net/4335)
- [Carrier Peering Providers](https://cloud.google.com/network-connectivity/docs/overview#carrier-peering)

---

## ✅ Resultado del día

Hoy completé el ciclo de opciones de conectividad en Google Cloud. Aprendí a diferenciar **interconexiones privadas** (Interconnect) de **intercambios de tráfico público** (Peering), entendiendo que cada una tiene su propósito en función del **tipo de tráfico**, **latencia requerida**, y **disponibilidad geográfica**.
