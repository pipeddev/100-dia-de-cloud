# 🗓 Día 62 – Managed Instance Groups (MIG) en Google Cloud

## 📌 Tema

**Compute Engine – Grupos de instancias administrados (Managed Instance Groups - MIG)**

---

## 🧠 Descripción

Hoy aprendí sobre los **grupos de instancias administrados** en Google Cloud, un recurso esencial para construir aplicaciones **escalables**, **tolerantes a fallos** y **fáciles de mantener**.

Un MIG gestiona un conjunto de instancias **idénticas** creadas a partir de una plantilla, y puede:

- 📈 **Escalar automáticamente** según la demanda del sistema.
- 🛠 **Recrear instancias con fallas** sin intervención manual (autohealing).
- 🌐 **Repartir tráfico** entre instancias con balanceo de carga.
- 🔁 **Aplicar actualizaciones progresivas** de forma controlada.
- 🧩 Ejecutarse en **una zona** o **regionalmente** para lograr alta disponibilidad.

---

## ⚙️ Flujo de trabajo

Aquí te muestro los **6 pasos clave** para crear un MIG desde la consola, basados en la imagen:

### ✅ Paso 1: Tipo de grupo

Seleccioné **New managed instance group (stateless)** para cargas sin estado.
📌 Soporta: autoscaling, autohealing, multi-zona y balanceo de carga.
👉 _Imagen referencia: `01`_

---

### ✅ Paso 2: Nombre del grupo

Asigné un nombre permanente para el grupo, por ejemplo: `instance-group-1`.
👉 _Imagen referencia: `02`_

---

### ✅ Paso 3: Ubicación

Elegí si el grupo sería:

- 🔵 **Single zone** (zonas específicas)
- 🌐 **Multiple zones** (mayor disponibilidad)

En este caso seleccioné `us-central1` y zona `us-central1-a`.
👉 _Imagen referencia: `03`_

---

### ✅ Paso 4: Plantilla de instancia

Usé una plantilla de instancia (`instance-template-1`) ya creada, con la configuración base de las VMs.
👉 _Imagen referencia: `04`_

---

### ✅ Paso 5: Autoscaling

Activé el **modo autoscale** con una política basada en uso de CPU ≥ 60%.
También puedes agregar otras métricas según la carga.
👉 _Imagen referencia: `05`_

---

### ✅ Paso 6: Autohealing

Configuré la verificación de estado (**health check**) para detectar instancias no saludables y que el grupo pueda recrearlas automáticamente.
👉 _Imagen referencia: `06`_

📸 Imagen de ejemplo:
![Jerarquía de recursos](https://github.com/pipeddev/100-dia-de-cloud/blob/main/062/mig.png)

---

## 🛠 Herramientas utilizadas

- Compute Engine
- Instance Templates
- Managed Instance Groups
- Load Balancing (opcional)
- Cloud Monitoring (para métricas)

---

## 🚀 Lo que aprendí

- Cómo definir reglas avanzadas para escalar instancias automáticamente.
- La diferencia entre un MIG zonal y regional.
- La importancia de la verificación de estado para la recuperación automática.
- Cómo automatizar la operación y mantenimiento de infraestructura compute.

---

## 🔗 Recursos útiles

- [Documentación de MIGs](https://cloud.google.com/compute/docs/instance-groups/)
- [Autohealing y health checks](https://cloud.google.com/load-balancing/docs/health-check-concepts)
- [Instance templates](https://cloud.google.com/compute/docs/instance-templates)
