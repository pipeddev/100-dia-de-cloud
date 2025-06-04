# 📅 Día 022 – Precios en Google Cloud

## 📌 Tema

Comprender los costos asociados al tráfico de red y direcciones IP externas en Google Cloud Platform (GCP).

---

## 📘 Descripción

### 💸 Precios de red

- **Tráfico de entrada a GCP**: Sin costo, salvo que el tráfico pase por un recurso como un balanceador de carga.
- **Respuestas a solicitudes (tráfico de salida)**: Generan cargos.
- **Tráfico de salida dentro de la misma zona** (usando IP interna): **Sin costo**.
- **Tráfico de salida hacia productos de Google** (YouTube, Maps, Drive): **Sin costo**.
- **Tráfico hacia otro servicio de GCP en la misma región**: **Sin costo**.
- **Tráfico entre zonas dentro de la misma región**: **$0.01 USD/GB**.
- **Tráfico dentro de la misma zona usando IP externa**: **$0.01 USD/GB**.
- **Tráfico entre regiones dentro de EE. UU. y Canadá**: **$0.01 USD/GB**.
- **Tráfico entre regiones fuera de EE. UU. y Canadá**: **Precio variable según regiones involucradas**.

---

### 🌐 Precios de direcciones IP externas

| Tipo de IP externa                                                           | Precio por hora (USD) |
| ---------------------------------------------------------------------------- | --------------------- |
| Dirección IP estática asignada pero **no utilizada**                         | $0.010                |
| Dirección IP estática o efímera **en uso en instancias estándar**            | $0.004                |
| Dirección IP estática o efímera **en uso en instancias preemptibles**        | $0.002                |
| Dirección IP estática o efímera **adjunta a reglas de reenvío (forwarding)** | **Sin costo**         |

---

## ✅ Lo que aprendí

- Cuáles son los escenarios donde el tráfico de red genera cargos en GCP.
- La diferencia entre uso de IPs internas y externas a nivel de costos.
- Cómo se tarifan las direcciones IP externas según su uso.

---

## 📚 Recursos útiles

- [Documentación oficial de precios de red en GCP](https://cloud.google.com/vpc/network-pricing)
- [Precios de direcciones IP](https://cloud.google.com/compute/vpc/network-pricing#ipaddresspricing)

---

## 🎯 Resultado del día

Ahora comprendo mejor cómo calcular y optimizar los costos de red en mis proyectos de GCP, lo que me permite tomar decisiones más eficientes en términos de arquitectura y uso de recursos.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
