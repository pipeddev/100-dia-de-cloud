# 📅 Día 032 – Tipos de VM en Compute Engine

## 📌 Tema

Tipos avanzados de máquinas virtuales en Google Cloud: Spot, interrumpibles, protegidas, confidenciales y nodos dedicados.

---

## 📘 Descripción

### ☁️ VMs Interrumpibles

- Las **VMs interrumpibles** son instancias temporales que pueden ser interrumpidas en cualquier momento.
- Tienen un descuento del **60% al 91%** frente a las VMs estándar.
- Si se interrumpe dentro del primer minuto, **no se cobra**.
- Se ejecutan como máximo por **24 horas**.
- Google envía una notificación **30 segundos antes** de ser interrumpidas.
- No admiten **migraciones en vivo ni reinicios automáticos**.
- Pueden ser reemplazadas por balanceadores de carga o mecanismos externos.

📌 **Caso de uso**: Procesamiento en lote, donde una interrupción solo retrasa el proceso, sin interrumpir completamente la operación.

---

### 💡 VMs Spot

- Son la evolución de las VMs interrumpibles.
- **No tienen límite de tiempo** de ejecución (a diferencia de las interrumpibles).
- Usan el mismo modelo de precios que las interrumpibles.
- Pueden ser interrumpidas si Google necesita recuperar los recursos.
- Su disponibilidad varía según la demanda y zona.
- No admiten migración en vivo ni reinicios automáticos.

📌 **Consejo**: Es más fácil obtener capacidad Spot con máquinas pequeñas.

---

### 🔒 Nodos dedicados (User-only Nodes)

- Servidores físicos dedicados a un solo proyecto.
- Garantizan **aislamiento físico** para cargas de trabajo con requisitos de cumplimiento o seguridad.
- Permiten agrupar múltiples VMs del mismo proyecto en un mismo host.
- Admite tipos de máquina personalizados y licencias existentes.
- Se puede usar **reinicio in situ** para optimizar recursos.

---

### 🛡️ VMs Protegidas (Shielded VMs)

- Proporcionan **integridad verificable** frente a rootkits o malware de bajo nivel.
- Son parte de la iniciativa **Shielded Cloud**.
- Usan funciones como **vTPM** para proteger los datos y el arranque seguro.
- Para utilizarlas, debes seleccionar una **imagen protegida** al crear la VM.

---

### 🔐 VMs Confidenciales

- Encriptan **datos en uso**, no solo en reposo o en tránsito.
- Usan procesadores **AMD EPYC 2da generación (Rome)** con tecnología **SEV**.
- No requieren cambios en el código de tus aplicaciones.
- Ofrecen **rendimiento optimizado** para cargas de memoria alta.
- Google **no tiene acceso** a las claves de cifrado.
- Puedes seleccionarlas desde la consola, API o CLI.

---

## ✅ Lo que aprendí

- Diferencias clave entre VMs estándar, interrumpibles, Spot, protegidas y confidenciales.
- Casos de uso y ventajas para cada tipo de instancia.
- Cómo seleccionar el tipo correcto según necesidades de seguridad, disponibilidad y costos.
- Qué es un nodo de usuario único y cómo ayuda al cumplimiento normativo.

---

## 📚 Recursos útiles

- [Spot VMs](https://cloud.google.com/compute/docs/instances/spot)
- [Shielded VMs](https://cloud.google.com/compute/shielded-vm/)
- [Confidential VMs](https://cloud.google.com/confidential-computing)
- [User-only Nodes](https://cloud.google.com/compute/docs/nodes/sole-tenant-nodes)

---

## 🎯 Resultado del día

Exploré opciones avanzadas de instancias en Google Cloud, entendiendo sus beneficios en términos de costo, seguridad y rendimiento. Ahora puedo tomar mejores decisiones al elegir el tipo de VM ideal para cada proyecto.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
