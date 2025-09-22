# 🌥️ Día 85 – Modos de operación en GKE: Autopilot vs Standard

## 📌 Tema

Comparación entre los modos **Autopilot** y **Standard** en Google Kubernetes Engine (GKE).

## 📝 Descripción

GKE ofrece dos formas de operar clústeres de Kubernetes: **Autopilot** y **Standard**.
Cada uno tiene un enfoque distinto en cuanto a **administración, costos y control**.

### 🔹 GKE Autopilot

- **Totalmente administrado y optimizado por Google.**
- Diseñado para **producción** con prácticas recomendadas y endurecidas.
- **Menos opciones de configuración** (restricciones) → menos riesgo de errores.
- Google gestiona el **plano de control, los nodos y la seguridad**.
- Escalado automático según las cargas de trabajo.
- **Costos por Pods ejecutados** (no por nodos).
- Ventanas de actualización configurables con **mínima interrupción**.
- Restricciones:

  - Sin acceso a nodos vía SSH.
  - Sin elevación de privilegios.
  - Limitaciones en afinidad/antiafinidad de nodos.

- Todos los Pods tienen **QoS garantizada**.

### 🔹 GKE Standard

- **Mayor flexibilidad y control.**
- Tú administras la infraestructura: nodos, seguridad, escalado y optimización.
- Paga por toda la infraestructura aprovisionada, **se use o no**.
- Permite configuraciones avanzadas (ej. acceso a nodos, personalización total).
- Ideal si necesitas un control detallado del clúster.

## ⚙️ Comparación rápida

| Característica     | Autopilot 🟢              | Standard ⚙️                 |
| ------------------ | ------------------------- | --------------------------- |
| Gestión de clúster | Google                    | Usuario                     |
| Costos             | Por Pod                   | Por nodo                    |
| Seguridad          | Administrada por Google   | Personalizable por usuario  |
| Flexibilidad       | Baja                      | Alta                        |
| Uso recomendado    | Producción sin sobrecarga | Casos con control detallado |

## 🛠️ Herramientas utilizadas

- Google Kubernetes Engine (Autopilot / Standard)
- Kubernetes (clústeres, Pods, QoS)

## 🤓 Lo que aprendí

- **Autopilot** es ideal para enfocarse en aplicaciones sin preocuparse de la infraestructura.
- **Standard** da flexibilidad, pero requiere más administración y control operativo.
- Autopilot **reduce costos y errores de configuración** al eliminar tareas de gestión.
- Las restricciones de Autopilot están pensadas para aumentar seguridad y confiabilidad.
- Recomendación: usar **Autopilot** a menos que realmente se requiera control detallado.

## 🔗 Recursos útiles

- [GKE Autopilot Overview](https://cloud.google.com/kubernetes-engine/docs/concepts/autopilot-overview)
- [Choosing Autopilot or Standard](https://cloud.google.com/kubernetes-engine/docs/concepts/choose-autopilot)

## 🚀 Resultado del día

Hoy entendí las diferencias entre los modos **Autopilot y Standard en GKE**: uno prioriza simplicidad y eficiencia (Autopilot), mientras que el otro entrega control total (Standard). La elección depende del equilibrio entre **simplicidad vs flexibilidad** que requiera cada caso.
