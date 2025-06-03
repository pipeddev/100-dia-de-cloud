# 📅 Día 021 – Resolución de DNS, Rutas y Reglas de Firewall en GCP

## 📌 Tema

Profundizar en los conceptos de resolución de DNS interna y externa, alias IP, rutas y reglas de firewall en Google Cloud Platform.

---

## 📘 Descripción

### 🧭 DNS para direcciones internas

Google Cloud ofrece dos tipos de resolución DNS interna:

- **Zonal**: Más confiable, aísla fallas a zonas específicas.
- **Global**: Menos recomendable si se necesita alta disponibilidad por zona.

Cada instancia:

- Tiene un nombre de host que se resuelve a una IP interna.
- El FQDN sigue un formato estandarizado.

🔁 **Importante**: Si una instancia es eliminada y recreada, su IP interna puede cambiar, pero su nombre DNS se mantiene apuntando a la instancia actual.

📡 Las consultas DNS dentro de la red son resueltas por el servidor de metadatos. Este servidor también enruta las consultas externas a los DNS públicos.

---

### 🌐 DNS para direcciones externas

Instancias con IP externa permiten conexiones desde el exterior:

- Puedes conectarte directamente con la IP externa.
- Los registros DNS públicos no se crean automáticamente.
- Puedes usar **Cloud DNS** para publicarlos.

#### Cloud DNS

- Sistema DNS administrado, confiable y escalable.
- Utiliza infraestructura global de Google (Anycast).
- SLA del 100% para zonas DNS gestionadas.
- Soporta administración vía UI, CLI o API.

---

### 🎭 Alias IP

Permite asignar múltiples IP internas a una única interfaz de red en una VM:

- Ideal para alojar varios servicios o contenedores en una misma instancia.
- No requiere múltiples interfaces de red.

---

### 🛣️ Rutas y Reglas de Firewall

#### Cloud Routes

- Permiten enviar tráfico entre instancias, incluso entre subredes.
- Todas las redes incluyen una ruta predeterminada para salida hacia Internet.

#### Mapeo de tráfico

- Las rutas determinan el destino en función de la IP.
- Las reglas de firewall deben permitir el tráfico.

#### Tablas de rutas en instancias

- Una ruta se aplica a una instancia si:

  - La red coincide.
  - Las etiquetas coinciden (si están definidas).

- Si no hay etiquetas de instancia, la ruta se aplica a todas.

---

### 🔥 Reglas de Firewall

Las reglas de firewall protegen a las VMs de tráfico no autorizado:

- Se aplican a nivel de red, pero se ejecutan en cada VM.
- GCP tiene reglas implícitas por defecto:

  - **Ingress**: Deny all.
  - **Egress**: Allow all.

#### Reglas de salida

- Controlan el tráfico saliente desde las VMs.
- Puedes definir reglas para permitir o denegar tráfico según:

  - IPs destino.
  - Protocolos.
  - Puertos.

---

## ✅ Lo que aprendí

- Cómo funciona la resolución DNS interna y externa en GCP.
- Uso de alias IP para alojar múltiples servicios en una VM.
- La importancia de configurar rutas y reglas de firewall personalizadas.

---

## 📚 Recursos útiles

- [Cloud DNS Overview](https://cloud.google.com/dns/docs/overview)
- [VPC Firewall Rules](https://cloud.google.com/vpc/docs/firewalls)
- [Alias IP ranges](https://cloud.google.com/vpc/docs/alias-ip)

---

## 🎯 Resultado del día

Consolidé conocimientos esenciales sobre la configuración de redes, protección de instancias y resolución de nombres en Google Cloud.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
