# 📅 Día 095 – Supervisión de varios proyectos con un solo permiso de métricas

## 📌 Tema

Supervisión centralizada en **Google Cloud Monitoring** utilizando permisos de métricas para gestionar múltiples proyectos desde un único punto.

---

## 📘 Descripción

Hoy aprendí cómo funciona la supervisión de proyectos en Google Cloud y las distintas estrategias para centralizar métricas y configuraciones:

🔹 Cada proyecto en Google Cloud crea su propio **permiso de métricas**, el cual almacena paneles, alertas y verificaciones de estado.
🔹 Se puede optar por mantener la supervisión **de manera local en cada proyecto** o bien usar un **proyecto centralizado** para supervisar múltiples proyectos.

Existen dos enfoques principales:

1. **Supervisión local por proyecto**

   - ✅ Ventajas: separación clara, acceso controlado para equipos específicos, fácil automatización.
   - ❌ Desventajas: visibilidad limitada si la aplicación abarca varios proyectos.

2. **Supervisión centralizada con un solo permiso de métricas**

   - ✅ Ventajas: panel único de visibilidad, facilidad para comparar entornos (producción vs pruebas), configuración unificada.
   - ❌ Desventajas: menos separación de responsabilidades, ya que los roles de IAM se aplican a todos los proyectos supervisados.

El enfoque recomendado para entornos de producción es **crear un proyecto exclusivo para la supervisión**, y desde ahí configurar métricas y paneles para todos los demás proyectos.

---

## 🛠️ Herramientas utilizadas

- **Google Cloud Monitoring**
- **IAM Roles** (para control de acceso)

---

## ✅ Lo que aprendí

- Cómo se crean y almacenan los permisos de métricas en proyectos de Google Cloud.
- Diferencias entre la supervisión local vs supervisión centralizada.
- La importancia de separar proyectos de monitoreo de proyectos de recursos para mayor estabilidad y visibilidad.

---

## 📚 Recursos útiles

- [Cloud Monitoring – Documentation](https://cloud.google.com/monitoring/docs)
- [Roles y permisos en Cloud Monitoring](https://cloud.google.com/monitoring/access-control)

---

## 🎯 Resultado del día

Ahora puedo diseñar una estrategia de monitoreo más organizada para múltiples proyectos en Google Cloud, eligiendo entre aislamiento por proyecto o centralización según el caso de uso.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
