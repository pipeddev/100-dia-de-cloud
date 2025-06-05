# 📅 Día 023 – Redes

## 📌 Tema

Alta disponibilidad, diseño global de red y acceso seguro a servicios en Google Cloud Platform.

---

## 📘 Descripción

### 🟢 Aumentar disponibilidad con múltiples zonas

![Múltiples zonas en una región](https://github.com/pipeddev/100-dia-de-cloud/blob/main/023/network-same-region-diff-zone.png)

- Si tu aplicación requiere alta disponibilidad, puedes desplegar instancias en **múltiples zonas dentro de una misma región**.
- Ambas VMs pueden estar en la misma subred (por ejemplo, `10.2.0.0/16`), lo que facilita las configuraciones de red y reglas de firewall.
- Este enfoque permite:
  - Redundancia ante fallas zonales.
  - Comunicación interna eficiente usando IPs privadas.
- Un **grupo de instancias administrado regional** (regional MIG) puede distribuir instancias automáticamente entre zonas, mejorando la disponibilidad del servicio.

---

### 🌍 Globalización con múltiples regiones

![Diseño global de red](https://github.com/pipeddev/100-dia-de-cloud/blob/main/023/globalization-network.png)

- Distribuir recursos en múltiples regiones ofrece:
  - Mayor tolerancia a fallos.
  - Menor latencia para los usuarios.
  - Reducción de costos de salida si se combina con un balanceador de cargas global.
- Con **Cloud Load Balancing (HTTP/S)** puedes enrutar tráfico automáticamente a la región más cercana al usuario.

---

### 🌐 Cloud NAT: acceso controlado a internet desde instancias privadas

![Cloud NAT](https://github.com/pipeddev/100-dia-de-cloud/blob/main/023/cloud-nat.png)

- **Cloud NAT** permite que las instancias **sin IP pública** puedan acceder a internet de forma segura (por ejemplo, para actualizaciones de software).
- Es un servicio administrado y escalable de Google Cloud que traduce direcciones privadas a públicas (solo salida).
- Importante:
  - No permite conexiones entrantes desde internet a las instancias privadas.
  - Refuerza la seguridad y el aislamiento de tus redes internas.

---

### 🔐 Acceso privado a servicios de Google (Private Google Access)

![Acceso privado a APIs de Google](https://github.com/pipeddev/100-dia-de-cloud/blob/main/023/private-google-access.png)

- **Private Google Access** permite a las VMs con **solo IP interna** acceder a APIs y servicios públicos de Google (como Cloud Storage).
- Se habilita por **subred**.
- Ejemplo del diagrama:
  - **VM A1** (sin IP pública, subred con acceso privado habilitado) → ✅ acceso permitido.
  - **VM B1** (sin IP pública, subred sin acceso privado) → ❌ acceso denegado.
  - VMs con IP pública pueden acceder sin importar la configuración del acceso privado.

---

## ✅ Lo que aprendí

- Cómo mejorar la disponibilidad mediante distribución zonal y regional.
- Beneficios de usar Cloud NAT para mantener seguridad y acceso a internet.
- Cómo configurar acceso privado a servicios de Google desde instancias sin IP pública.
- La importancia de las decisiones de diseño en redes para escalabilidad, rendimiento y seguridad.

---

## 📚 Recursos útiles

- [Cloud NAT - Documentación oficial](https://cloud.google.com/nat/docs/overview)
- [Private Google Access](https://cloud.google.com/vpc/docs/private-google-access)
- [Cloud Load Balancing](https://cloud.google.com/load-balancing)
- [Managed Instance Groups (MIGs)](https://cloud.google.com/compute/docs/instance-groups/creating-groups-of-managed-instances)

---

## 🎯 Resultado del día

Consolidé conocimientos clave sobre diseño de red distribuida, acceso seguro a internet y a servicios de Google, aplicando buenas prácticas de arquitectura en GCP para disponibilidad y seguridad.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
