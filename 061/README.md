# ☁️ Día 61 - Redes multiproyecto: VPC Compartidas e Intercambio de Tráfico entre VPC

## 📌 Tema

Exploración de las dos principales estrategias para compartir redes y permitir comunicaciones privadas entre proyectos o incluso entre organizaciones en Google Cloud:

- 🔗 **VPC compartida**
- 🔄 **Intercambio de tráfico entre redes de VPC (VPC peering)**

---

## 📖 Descripción

En entornos organizacionales complejos, es común tener múltiples proyectos que deben **compartir infraestructura de red**. Hoy aprendí cómo lograrlo de forma segura y escalable utilizando:

---

### 🔗 VPC Compartida (Shared VPC)

Permite que **varios proyectos dentro de una misma organización** compartan una única red VPC centralizada.

✅ Características:

- Un **proyecto host** contiene la red VPC compartida.
- Los **proyectos de servicio** usan subredes de esa red para desplegar recursos.
- Los administradores de red mantienen el control centralizado de rutas, subredes y firewalls.
- Delegación de tareas: los equipos pueden administrar sus recursos sin comprometer la gobernanza central.

📌 Uso ideal:

- Entornos con múltiples equipos o productos en la misma organización.
- Modelo de administración **centralizado**.

---

### 🔄 Intercambio de tráfico entre redes de VPC (VPC Peering)

Conecta de manera **privada y bidireccional** dos redes de VPC para que las instancias se comuniquen a través de sus IPs internas (RFC 1918).

✅ Características:

- Funciona entre proyectos distintos, y **también entre organizaciones diferentes**.
- Las redes de VPC pueden mantener su propio control de seguridad y enrutamiento.
- Comunicación eficiente sin necesidad de IPs externas ni VPN.
- Menor latencia y mejor seguridad que soluciones anteriores.

📌 Uso ideal:

- Integración de soluciones cross-org o cross-proyecto.
- Modelo de administración **descentralizado**.

---

### 🧠 Comparación

| Característica              | VPC Compartida                           | Intercambio de tráfico VPC                      |
| --------------------------- | ---------------------------------------- | ----------------------------------------------- |
| Ámbito                      | Misma organización                       | Misma o distinta organización                   |
| Modelo de gestión           | Centralizado                             | Descentralizado                                 |
| Nivel de comunicación       | Entre proyectos                          | Entre redes (misma org o distinta)              |
| Control de firewall y rutas | En el proyecto host                      | En cada red participante                        |
| Caso de uso típico          | Unidades colaborando en una organización | Equipos o empresas independientes que colaboran |

---

## 🛠️ Herramientas utilizadas

- Google Cloud VPC
- Shared VPC (proyecto host y de servicio)
- VPC Peering
- Reglas de firewall y tablas de rutas

---

## 📚 Lo que aprendí

- La **VPC compartida** es ideal cuando se necesita una **política de red centralizada**, simplificando gobernanza en organizaciones grandes.
- El **intercambio de tráfico entre redes VPC** (peering) permite una **conectividad privada y segura** incluso entre distintas organizaciones, con menor acoplamiento.
- Ambas soluciones reemplazan el uso de IPs públicas o VPNs para comunicación interna, mejorando **seguridad, latencia y costos**.

---

## 🔗 Recursos útiles

- [VPC Compartida](https://cloud.google.com/vpc/docs/shared-vpc)
- [VPC Peering](https://cloud.google.com/vpc/docs/vpc-peering)

---

## ✅ Resultado del día

Hoy aprendí a **diseñar topologías de red multiproyecto** en Google Cloud, eligiendo entre **modelos centralizados (Shared VPC)** o **descentralizados (VPC Peering)** según los requerimientos de gobernanza, seguridad y colaboración entre equipos u organizaciones.
