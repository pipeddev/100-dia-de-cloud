# ☁️ Día 59 - Cloud Interconnect, Partner Interconnect y Cross-Cloud Interconnect

## 📌 Tema

Conectividad de nivel empresarial entre tu infraestructura local (o de otro proveedor cloud) y Google Cloud, mediante **opciones de interconexión física dedicada o compartida**.

---

## 📖 Descripción

Hoy aprendí sobre los tres tipos principales de interconexión de alto rendimiento en Google Cloud:

- 🔌 **Dedicated Interconnect**
- 🤝 **Partner Interconnect**
- 🌐 **Cross-Cloud Interconnect**

Estas soluciones permiten establecer conexiones privadas, de alta capacidad y baja latencia con la red de Google, superando las limitaciones de Cloud VPN y de la red pública.

---

### 🔐 1. Dedicated Interconnect

Conexión **física directa** entre tu red y la de Google, en un centro de datos de colocación.

✅ Características:

- Hasta **100 Gbps** por enlace.
- Mínimo de **10 Gbps** por vínculo.
- ANS de **99.9% o 99.99%** (dependiendo de redundancia).
- Requiere instalación física en ubicaciones específicas.
- Usa **Cloud Router + BGP** para el intercambio de rutas.

📍 [Ubicaciones disponibles](https://cloud.google.com/interconnect/docs/concepts/colocation-facilities)

---

### 🤝 2. Partner Interconnect

Conexión compartida a través de un **proveedor de servicios autorizado**, útil si no tienes acceso directo a un centro de colocación.

✅ Características:

- Capacidad desde **50 Mbps hasta 50 Gbps**.
- También usa **Cloud Router + BGP**.
- ANS de hasta **99.99%** (entre Google y el partner).
- Más flexible, menos costosa y más accesible geográficamente.

📍 [Lista de proveedores compatibles](https://cloud.google.com/interconnect/docs/concepts/service-providers)

---

### 🌐 3. Cross-Cloud Interconnect

Conexión dedicada entre **Google Cloud y otros proveedores cloud**, como:

- AWS
- Azure
- Oracle Cloud
- Alibaba Cloud

✅ Características:

- Conexión dedicada entre redes VPC de Google y otro proveedor cloud.
- Capacidad de **10 Gbps o 100 Gbps**.
- Requiere configuración redundante en ambos extremos.
- **Google no garantiza la disponibilidad del otro proveedor**.

Ideal para **estrategias multicloud**, reducción de complejidad, menor latencia y mayor seguridad.

---

### 📊 Comparación general

| Solución                 | Capacidad             | Conexión física directa | Requiere partner   | Uso típico                        |
| ------------------------ | --------------------- | ----------------------- | ------------------ | --------------------------------- |
| Cloud VPN                | 1.5 – 3 Gbps/túnel    | ❌ (por Internet)       | ❌                 | Pruebas, bajo volumen, bajo costo |
| Dedicated Interconnect   | 10 – 100 Gbps/vínculo | ✅                      | ❌                 | Alto rendimiento, misión crítica  |
| Partner Interconnect     | 50 Mbps – 50 Gbps     | ✅ (vía proveedor)      | ✅                 | Flexible y accesible              |
| Cross-Cloud Interconnect | 10 – 100 Gbps         | ✅                      | ❌ (pero otro CSP) | Multicloud empresarial            |

---

## 🛠️ Herramientas utilizadas

- Cloud Interconnect
- Cloud Router
- BGP
- Partner Interconnect
- Cross-Cloud Interconnect

---

## 📚 Lo que aprendí

- **Dedicated Interconnect** es la mejor opción para empresas que requieren alto rendimiento y están ubicadas cerca de un centro de colocación.
- **Partner Interconnect** democratiza ese acceso para ubicaciones más remotas.
- **Cross-Cloud Interconnect** facilita la conectividad privada entre GCP y otros proveedores, ideal para estrategias multicloud.
- La capacidad, el costo y la ubicación física son factores clave al elegir la opción correcta.

---

## 🔗 Recursos útiles

- [Dedicated Interconnect Overview](https://cloud.google.com/interconnect/docs/concepts/dedicated-overview)
- [Partner Interconnect Overview](https://cloud.google.com/interconnect/docs/concepts/partner-overview)
- [Cross-Cloud Interconnect](https://cloud.google.com/network-connectivity/docs/cross-cloud)

---

## ✅ Resultado del día

Hoy aprendí cómo diseñar una conectividad empresarial de alta capacidad entre Google Cloud, redes locales y otros proveedores cloud.
Estas opciones de interconexión permiten crear arquitecturas **híbridas, multicloud y seguras**, con **rendimiento consistente y latencias mínimas**.
