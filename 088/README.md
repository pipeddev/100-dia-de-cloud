# 🌥️ Día 88 — Introspección y depuración con kubectl

Hoy aprendí a usar **kubectl** no solo para administrar, sino también para **depurar aplicaciones en Kubernetes** mediante un proceso llamado **introspección**. Esto consiste en recopilar información sobre Pods, contenedores, Services y otros recursos que se ejecutan en el clúster.

### 🔎 Comandos clave para depuración

- **get** → Proporciona una visión general (por ejemplo, el estado de los Pods).
- **describe** → Muestra detalles de Pods y contenedores (etiquetas, recursos, reinicios, puertos, etc.).
- **exec** → Permite ejecutar un comando dentro de un contenedor, o abrir una shell interactiva para inspección.
- **logs** → Muestra los registros de las aplicaciones dentro de los Pods, ideal para encontrar errores o mensajes de depuración.

### 📌 Estados comunes de un Pod

- **Pending** → Aceptado, pero aún sin programar en un nodo.
- **Running** → Contenedores activos en ejecución.
- **Succeeded (Sin errores)** → El contenedor finalizó sin problemas.
- **Failed (Con errores)** → Falló y no se reiniciará.
- **Unknown** → No se puede determinar el estado.
- **CrashLoopBackOff** → Contenedor falla repetidamente incluso después de reinicios.

### 💡 Buenas prácticas

- Evitar instalar software directamente en un contenedor en ejecución.
- Si detectas cambios necesarios, lo ideal es **actualizar la imagen del contenedor** y volver a desplegar.
- Usar la introspección para diagnosticar, pero resolver de forma definitiva en la configuración o en el Dockerfile.

---

## 🚀 Lo que aprendí

kubectl es mucho más que un comando de administración: también es una **herramienta de diagnóstico** que ayuda a entender qué está pasando dentro del clúster y permite reaccionar rápidamente ante problemas.
