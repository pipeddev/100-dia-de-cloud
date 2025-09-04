# ☁️ Día 67 – Acelerando el contenido con **Cloud CDN**

## 🧠 Tema

Cloud CDN: cómo aprovechar la red global de Google para entregar contenido más rápido y eficiente desde el perímetro.

## 🧠 Descripción

Hoy aprendí cómo Cloud CDN puede mejorar drásticamente el rendimiento de nuestras aplicaciones web al reducir la latencia y el uso de recursos backend. Cloud CDN aprovecha más de 90 puntos de presencia distribuidos en el mundo para entregar contenido estático o dinámico cercano al usuario.

### ✅ Beneficios Clave:

- Cacheo de contenido en nodos perimetrales de Google.
- Reducción del tiempo de ida y vuelta (RTT).
- Disminución de la carga en los servicios backend.
- Mejora en los tiempos de carga y experiencia del usuario.
- Reducción de costos por menor tráfico al origen.

## ⚙️ Flujo de trabajo

1. Un usuario realiza una solicitud HTTP(S) que pasa por el balanceador de cargas.
2. Cloud CDN revisa si tiene ese contenido cacheado:

   - **Si es un acierto de caché (cache hit)** ➜ el contenido se entrega desde el nodo cercano.
   - **Si es un fallo de caché (cache miss)** ➜ el contenido se obtiene del backend (grupo de instancias o Cloud Storage) y se guarda para futuras solicitudes.

3. El contenido cacheado se sirve automáticamente a otros usuarios cercanos.

## 💡 Modos de almacenamiento en caché:

- `USE_ORIGIN_HEADERS`: Respeta las directivas del backend (por ejemplo, `Cache-Control`).
- `CACHE_ALL_STATIC`: Almacena recursos estáticos sin directivas como `no-store`, `private`, `no-cache`.
- `FORCE_CACHE_ALL`: Fuerza el cacheo incluso sin encabezados; **precaución** con datos dinámicos o privados.

📸 Imagen de ejemplo:
![caching with CDN](https://github.com/pipeddev/100-dia-de-cloud/blob/main/067/cloud-cdn.png)

## 🛠️ Herramientas utilizadas

- Cloud CDN
- HTTPS Load Balancing
- Compute Engine (MIGs)
- Cloud Storage
- Monitoring and Logging

## 📚 Recursos útiles

- [Documentación oficial de Cloud CDN](https://cloud.google.com/cdn/docs)
- [Buenas prácticas de caché en GCP](https://cloud.google.com/cdn/docs/caching-content)
- [Tipos de contenido aptos para cacheo](https://cloud.google.com/cdn/docs/cacheable-content)

## 📝 Resultado del día

Aprendí cómo aprovechar Cloud CDN para mejorar la entrega de contenido web globalmente. Comprendí los modos de almacenamiento en caché y cómo aplicarlos de manera segura, especialmente al trabajar con contenido mixto (estático y dinámico).
