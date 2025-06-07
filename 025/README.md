# 📅 Día 025 – Iniciar el módulo de máquinas virtuales

## 📌 Tema

Introducción a Compute Engine y el ciclo de vida de las máquinas virtuales en Google Cloud.

---

## 📘 Descripción

### Compute Engine

Google Compute Engine (GCE) es un servicio de infraestructura como servicio (IaaS) que permite crear y ejecutar máquinas virtuales (VMs) en la infraestructura de Google Cloud. Ofrece gran flexibilidad, ya que puedes elegir el sistema operativo, lenguaje de programación y configuración de red, almacenamiento y escalamiento.

- Permite escalar automáticamente según las reglas definidas.
- Ideal para cargas de trabajo generales, como aplicaciones empresariales.

#### ¿Qué es Compute Engine?

- Son servidores físicos en la infraestructura de Google Cloud, configurables en tipos predefinidos o personalizados.
- Puedes seleccionar la cantidad exacta de CPU y memoria que necesitas.
- Opciones de almacenamiento:
  - Disco persistente zonal o regional (HDD o SSD)
  - SSD local (de alto rendimiento y baja latencia)
  - Cloud Storage (para almacenamiento de objetos)
- Soporta múltiples sistemas operativos: Linux y Windows.
- Permite definir redes, balanceo de carga, reglas de firewall, etc.

---

### Limitaciones de hardware

- **CPU**: Unidad de procesamiento central.
- **GPU**: Unidad de procesamiento gráfico.
- **TPU**: Unidad de procesamiento de tensores.
  - Son ASICs (circuitos integrados de aplicación específica) desarrollados por Google.
  - Diseñados para acelerar cargas de trabajo de machine learning.
  - Optimizados para operaciones como multiplicación de matrices, clave en el aprendizaje automático.

---

### Almacenamiento

- **Disco estándar**: Mayor capacidad, menor rendimiento.
- **SSD persistente**: Mayor IOPS por dólar.
- **SSD local**:
  - Mayor rendimiento y menor latencia.
  - Conectadas directamente al hardware físico.
  - Datos no persistentes: se borran al detener o eliminar la instancia.
- Hasta **257 TB por instancia** en discos persistentes.

---

### Networking

Compute Engine proporciona características robustas de red:

- Redes automáticas o personalizadas.
- Reglas de firewall (entrantes/salientes) basadas en:
  - Dirección IP
  - Etiquetas de instancia o grupo
- Balanceo de carga HTTPS regional.
- Balanceo de carga de red sin necesidad de prewarming.
- Subredes globales y multirregionales.

---

### Accesos y ciclo de vida de las VM

#### Acceso

- **Linux**: SSH desde la consola o terminal.
- **Windows**: RDP usando usuario/contraseña generada desde la consola.

#### Estados del ciclo de vida

1. **Provisioning**: Se reservan recursos (CPU, memoria, disco).
2. **Staging**: Se asignan IPs, se inicia el sistema operativo.
3. **Running**: La VM está activa y accesible (SSH o RDP habilitado).
4. **Stopping**: Se ejecutan comandos de apagado.
5. **Terminated**: Se puede reiniciar (retorna a provisioning) o eliminar.
6. **Repairing**: La VM es inaccesible temporalmente por mantenimiento o fallos.
7. **Suspending**: Estado intermedio que permite reanudar o borrar la VM.

---

## ✅ Lo que aprendí

- Conceptos clave de Compute Engine como IaaS en Google Cloud.
- Tipos de almacenamiento disponibles para VMs.
- Diferencias entre CPU, GPU y TPU.
- Accesos y ciclo de vida completo de una máquina virtual.
- Funcionalidades avanzadas de red y balanceo de carga.

---

## 📚 Recursos útiles

- [Documentación oficial de Compute Engine](https://cloud.google.com/compute/docs/overview)
- [Tipos de discos en GCP](https://cloud.google.com/compute/docs/disks)
- [TPU en Google Cloud](https://cloud.google.com/tpu/docs/)

---

## 🎯 Resultado del día

Exploré Compute Engine, comprendiendo sus características fundamentales, ventajas frente a otros servicios de infraestructura, y aprendí a evaluar configuraciones de red, almacenamiento y procesamiento.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
