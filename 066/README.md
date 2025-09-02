# ☁️ Día 66 – Balanceador de Cargas HTTPS y NEG en Google Cloud

---

## 🧠 Tema

Balanceador de cargas HTTPS, certificados SSL, buckets de backend y grupos de extremos de red (NEG).

---

## 🧠 Descripción

Hoy aprendí cómo funciona el balanceador de cargas HTTPS en GCP, sus diferencias frente al HTTP, cómo manejar tráfico con buckets de backend y cómo utilizar grupos de extremos de red (Network Endpoint Groups – NEG) para mayor flexibilidad.

### ✅ Características clave del Balanceador de Cargas HTTPS:

* Utiliza un **proxy HTTPS** en lugar de HTTP.
* Finaliza la sesión SSL directamente en el balanceador.
* Requiere uno o más **certificados SSL**.
* Soporta **QUIC**, un protocolo que mejora el rendimiento del transporte.

### ✅ Certificados SSL:

* Puedes agregar hasta **15 certificados** por proxy HTTPS.
* Cada certificado debe definirse como un recurso de certificado SSL.
* Utilizados exclusivamente con proxies de balanceo de cargas (HTTPS o SSL).

### ✅ Buckets de backend:

* Permiten enrutar tráfico a **Cloud Storage buckets** como destino final.
* Casos comunes:

  * `/static` → bucket con imágenes.
  * `/api` → servicio backend.

### ✅ NEG (Network Endpoint Group):

* Definen **grupos de extremos** para mayor granularidad.
* Tipos comunes:

  * **Zonales**: VMs o servicios dentro de GCP.
  * **De Internet**: endpoints fuera de GCP (por FQDN o IP).
  * **Sin servidor**: Cloud Run, App Engine o Cloud Functions.
  * **Híbridos**: tráfico hacia servicios externos usando Traffic Director.

---

## ⚙️ Flujo de trabajo

1. Crear balanceador de cargas HTTPS con certificado SSL.
2. Configurar **URL Map** para enrutar tráfico dinámico y estático.
3. Definir servicios backend y buckets como destinos.
4. Asociar **NEG** zonales, sin servidor o de Internet según necesidad.
5. Probar rutas como `/love-to-fetch` para validar asignaciones.

---

## 🛠️ Herramientas utilizadas

* **HTTPS Load Balancer**
* **Cloud Storage (Buckets)**
* **SSL Certificates**
* **NEG (Network Endpoint Group)**
* **URL Maps**

---

## 📚 Recursos útiles

* [Balanceo de cargas HTTPS – GCP Docs](https://cloud.google.com/load-balancing/docs/https/)
* [NEG – GCP Docs](https://cloud.google.com/load-balancing/docs/negs/)

---

## ✅ Resultado del día

Comprendí cómo extender la funcionalidad de los balanceadores de cargas mediante certificados SSL, buckets de almacenamiento y NEGs, habilitando una distribución de tráfico inteligente, segura y eficiente para apps modernas y sin servidor.
