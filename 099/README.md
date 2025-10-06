# 📅 Día 099 – Entendiendo SLI, SLO y ANS en la Observabilidad

## 📌 Tema

Indicadores y acuerdos de nivel de servicio: SLI, SLO y ANS.

---

## 📘 Descripción

Hoy me adentré en tres conceptos clave para la **observabilidad y confiabilidad de sistemas en la nube**:
los **SLI (Service Level Indicator)**, **SLO (Service Level Objective)** y **ANS (Acuerdo de Nivel de Servicio o SLA)**.

Estas métricas y acuerdos son la base para definir, medir y mantener la calidad del servicio ofrecido, tanto internamente como frente a los usuarios finales.

---

## 🧩 Conceptos clave

### 🟢 **SLI – Service Level Indicator**

Son **métricas cuidadosamente elegidas** que miden un aspecto crítico de la confiabilidad de un servicio.
Ejemplo:

> Proporción entre solicitudes exitosas y solicitudes totales.

**Propósito:** reflejar la **experiencia real del usuario** con datos medibles y objetivos.

---

### 🟠 **SLO – Service Level Objective**

Es el **objetivo asociado al SLI**, expresado como un porcentaje de cumplimiento.
Ejemplo:

> “El 99.9% de las solicitudes deben responder en menos de 100 ms.”

**Características de un buen SLO:**

- Específico 📏
- Medible 📊
- Alcanzable 🎯
- Relevante 💡
- Limitado en el tiempo ⏱️

---

### 🔵 **ANS – Acuerdo de Nivel de Servicio (SLA)**

Define el **nivel mínimo de servicio garantizado** al cliente y las **acciones de compensación** en caso de incumplimiento.
Ejemplo:

> “Si el servicio tiene una tasa de error superior al 0.3%, se otorgarán créditos al cliente.”

**Diferencia principal:**
El **SLA** está enfocado en el cliente y tiene implicaciones comerciales,
mientras que los **SLO y SLI** se usan internamente para medir y mejorar la confiabilidad.

---

## 🧠 Lo que aprendí

- Cómo los **SLI, SLO y ANS** trabajan juntos para mantener la confiabilidad de un sistema.
- Que los **umbrales de alerta** deben configurarse **por encima del SLA** para reaccionar antes de que impacte al cliente.
- La importancia de establecer **SLOs alcanzables y relevantes** para evitar falsas expectativas.
- Cómo estas métricas guían las decisiones técnicas y de negocio en **equipos SRE y DevOps**.

---

## 📊 Esquema visual

```mermaid
graph TD
    A[📡 Monitoreo de servicio] --> B[📈 SLI<br>Indicador medible de confiabilidad]
    B --> C[🎯 SLO<br>Objetivo cuantificable basado en el SLI]
    C --> D[📜 ANS (SLA)<br>Promesa formal al cliente]
    D --> E[💰 Compensación o crédito si no se cumple]
    C --> F[🚨 Umbral de alerta<br>más estricto que el ANS]
```

---

## 📚 Recursos útiles

- [Site Reliability Engineering Book – Google](https://sre.google/sre-book/service-level-objectives/)
- [Definición de SLIs y SLOs en Google Cloud](https://cloud.google.com/stackdriver/docs/solutions/slo-monitoring)
- [SLA Management Best Practices](https://cloud.google.com/terms/sla)

---

## 🎯 Resultado del día

Comprendí cómo los SLI, SLO y ANS definen el marco de confiabilidad de un servicio y cómo se integran con las **alertas proactivas** para mantener la experiencia del usuario.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
