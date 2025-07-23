# ☁️ Día 53 - Cuotas, Etiquetas y Facturación en Google Cloud

## 📌 Tema

Administración de recursos y costos en GCP mediante **cuotas**, **etiquetas** y **presupuestos de facturación**.

## 📖 Descripción

Hoy aprendí tres conceptos clave para **gestionar de forma eficiente los recursos y costos** en Google Cloud:

---

### 🔐 1. Cuotas

Las **cuotas** son límites predefinidos que GCP impone sobre el uso de recursos por proyecto. Existen para:

- Evitar consumo excesivo (por errores o ataques).
- Controlar el ritmo de solicitudes a APIs.
- Administrar la disponibilidad regional.

📌 Tipos de cuotas:

- **Por recurso**: ej. 15 redes VPC por proyecto.
- **Por frecuencia**: ej. 5 ops/seg en API de Spanner.
- **Regional**: ej. 24 vCPU por región.

🛠 Puedes **solicitar aumentos** desde la consola si tu uso lo requiere, pero tener cuota ≠ disponibilidad garantizada.

---

### 🏷️ 2. Etiquetas de recursos

Las **etiquetas** (key-value) ayudan a organizar, buscar y agrupar recursos como VMs, discos, imágenes o snapshots.

📌 Casos de uso:

- `entorno:producción` o `entorno:testing`
- `equipo:marketing`, `componente:frontend`
- `estado:enuso`, `propietario:juan`

Beneficios:

- 🔍 Búsqueda rápida de recursos.
- 💰 Análisis de costos por etiqueta.
- 🤖 Automatización de tareas y limpieza.
- 📊 Segmentación de presupuestos y reportes.

> ❗ No confundir con etiquetas de instancia (solo útiles para reglas de red).

---

### 💸 3. Facturación y presupuestos

La **facturación** en GCP se agrupa por cuenta y proyecto. Para evitar sorpresas:

✅ Crea **presupuestos** y activa **alertas** por porcentaje o valor gastado.
✅ Usa **Cloud Pub/Sub + Cloud Functions** para acciones automáticas (ej. apagar recursos).
✅ Exporta los datos de facturación a **BigQuery** y visualízalos en **Looker Studio (Data Studio)** para análisis más avanzado.

💡 Consejo: combina etiquetas + exportación a BigQuery para tener visibilidad total del gasto por equipo, entorno, región o componente.

---

## 🛠️ Herramientas utilizadas

- Google Cloud Console
- Cloud Billing
- Cloud Pub/Sub
- BigQuery
- Looker Studio (ex Data Studio)

## 📚 Lo que aprendí

- Las cuotas protegen tanto tu proyecto como tu presupuesto.
- Etiquetar recursos es clave para el orden, la automatización y el análisis de costos.
- Con herramientas como presupuestos, alertas, Pub/Sub y BigQuery puedes **tomar el control de tu gasto en la nube**.

## 🔗 Recursos útiles

- [Página de cuotas](https://console.cloud.google.com/iam-admin/quotas)
- [Etiquetas de recursos](https://cloud.google.com/resource-manager/docs/tags/tags-overview)
- [Presupuestos de facturación](https://cloud.google.com/billing/docs/how-to/budgets)

## ✅ Resultado del día

Hoy aprendí a **gobernar los recursos en GCP** desde tres frentes: límites operativos, organización con etiquetas y control de costos con presupuestos.
¡Todo lo necesario para escalar sin perder el control! 💡💸
