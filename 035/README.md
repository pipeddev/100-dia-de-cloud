# 📅 Día 035 – Opciones de disco en Compute Engine

## 📌 Tema

Discos persistentes, SSD locales y discos en RAM en Google Cloud.

---

## 📘 Descripción

### 🔒 Persistent Disk

- Disco adjunto a la VM mediante interfaz de red, pero no físicamente unido.
- Sobrevive a la eliminación de la VM.
- Permite hacer snapshots (respaldos incrementales).
- Se puede redimensionar dinámicamente, incluso estando en uso.
- Se puede montar en múltiples VMs como solo lectura para compartir datos.
- Ofrece almacenamiento seguro y eficiente:
  - **Discos zonales:** almacenamiento en bloque seguro en una zona.
  - **Discos regionales:** replicación activa-activa entre dos zonas de una misma región (alta disponibilidad).

#### Tipos de Persistent Disks:

- `pd-standard`: disco HDD, ideal para cargas secuenciales y económicas.
- `pd-ssd`: SSD de alto rendimiento, ideal para bases de datos y apps empresariales.
- `pd-balanced`: equilibrio entre rendimiento y costo.
- `pd-extreme` (solo zonal): rendimiento consistente para bases de datos de nivel empresarial.

#### Seguridad:

- Todos los datos se encriptan en reposo por defecto.
- Puedes usar [Cloud KMS](https://cloud.google.com/kms) para manejar tus propias claves (CMEK).

---

### ⚡ SSD Locales

- Físicamente unidas a la VM.
- Muy alto rendimiento (IOPS).
- Tamaño de 375 GB (hasta 24 discos por instancia = 9 TB).
- Datos sobreviven reinicios, pero se pierden si la VM se detiene o elimina.
- No se pueden mover a otra VM.

---

### 🧠 Disco RAM (tmpfs)

- Almacena datos directamente en la memoria.
- Máximo rendimiento posible.
- Volátil: datos se pierden al reiniciar o apagar.

---

### 📌 Recomendaciones

- HDD si necesitas capacidad más que rendimiento.
- SSD si necesitas alto rendimiento.
- SSD local para tareas efímeras y alto IOPS.
- RAM si necesitas acceso ultrarrápido a datos temporales.

---

### 📊 Resumen de opciones de disco

| Tipo de Disco            | Persistencia | Rendimiento | Redundancia | Ideal para                            |
| ------------------------ | ------------ | ----------- | ----------- | ------------------------------------- |
| Persistent Disk HDD      | ✅           | Medio       | ✅          | Almacenamiento económico              |
| Persistent Disk SSD      | ✅           | Alto        | ✅          | Bases de datos, apps críticas         |
| Persistent Disk Balanced | ✅           | Medio/Alto  | ✅          | General purpose                       |
| Persistent Disk Extreme  | ✅           | Muy alto    | ✅          | Alta demanda, grandes bases de datos  |
| SSD Local                | ❌           | Muy alto    | ❌          | Cache, procesamiento intensivo        |
| RAM (tmpfs)              | ❌           | Máximo      | ❌          | Datos temporales, estructuras ligeras |

---

### 🧮 Máximo de discos persistentes por tipo de máquina

| Machine Type      | Límite de discos |
| ----------------- | ---------------- |
| Shared-core       | 16               |
| Standard          | 128              |
| High-memory       | -                |
| High-CPU          | -                |
| Memory-optimized  | -                |
| Compute-optimized | -                |

---

### 🔍 Diferencias entre Cloud Persistent Disk y Hardware Disk

| Característica              | Cloud Persistent Disk | Computer Hardware Disk |
| --------------------------- | --------------------- | ---------------------- |
| Sistema de archivos único   | ✅                    | ❌                     |
| Redimensionamiento          | ✅                    | ❌                     |
| Snapshots integrados        | ✅                    | ❌                     |
| Encriptación automática     | ✅                    | ❌                     |
| Particionado manual         | ❌                    | ✅                     |
| RAID / Gestión de volúmenes | ❌                    | ✅                     |
| Encriptación manual         | ❌                    | ✅                     |

---

## ✅ Lo que aprendí

- Tipos de discos disponibles en Compute Engine.
- Diferencias entre discos persistentes, SSD locales y discos en RAM.
- Cuándo usar cada tipo de disco según el caso de uso.
- Cómo gestionar la seguridad con claves administradas por el cliente.

---

## 📚 Recursos útiles

- [Persistent Disks – GCP Docs](https://cloud.google.com/compute/docs/disks)
- [Local SSDs – GCP Docs](https://cloud.google.com/compute/docs/disks/local-ssd)
- [Cloud KMS – Key Management Service](https://cloud.google.com/kms)

---

## 🌟 Resultado del día

Ahora tengo mayor claridad para elegir el tipo correcto de almacenamiento según el rendimiento, costo y persistencia que requiera una aplicación en Compute Engine.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
