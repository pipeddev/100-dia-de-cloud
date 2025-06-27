# 📅 Día 041 – Restricciones para organizaciones en Google Cloud

## 📌 Tema

Control de acceso a recursos de GCP mediante restricciones organizacionales y uso de proxies de salida en dispositivos administrados.

---

## 📘 Descripción

![Jerarquía de recursos](https://github.com/pipeddev/100-dia-de-cloud/blob/main/041/organization-restriction.png)

Hoy aprendí sobre las **restricciones para organizaciones** en Google Cloud, una función clave para reforzar la seguridad y prevenir fugas de datos o accesos no autorizados desde dispositivos o usuarios con malas intenciones.

Esta función permite restringir el acceso a los recursos de Google Cloud para que solo se pueda acceder a organizaciones específicas autorizadas por tu empresa.

---

### 🔒 ¿Qué son las restricciones para organizaciones?

- Permiten limitar el acceso a recursos **únicamente** a organizaciones de Google Cloud autorizadas por el administrador.
- Se utiliza principalmente para prevenir el robo de datos mediante phishing o accesos desde usuarios con información privilegiada.
- Se aplica sobre **dispositivos administrados** y se refuerza mediante el uso de un **proxy de salida corporativo**.

---

### 🛡️ Funcionamiento general

1. **Política empresarial** administra los dispositivos.
2. Los empleados acceden a los recursos de la organización desde dispositivos administrados.
3. El **proxy de salida** añade encabezados especiales de restricción a cada solicitud.
4. Google Cloud inspecciona los encabezados para permitir o denegar acceso a los recursos.

---

### 🧩 Ejemplos de uso

- Permitir acceso únicamente a recursos de tu organización y bloquear otras organizaciones.
- Permitir acceso de lectura a buckets de Cloud Storage **solo dentro de tu organización**.
- Autorizar acceso tanto a tu organización como a una de tus proveedoras confiables de GCP.

---

## ✅ Lo que aprendí

- Cómo las restricciones organizacionales fortalecen el principio de acceso mínimo.
- La colaboración necesaria entre administradores de GCP y de red para implementar esta función.
- Casos de uso prácticos para proteger entornos empresariales en la nube.

---

## 📚 Recursos útiles

- [Restricciones para organizaciones – Documentación oficial](https://cloud.google.com/resource-manager/docs/organization-policy/org-policy-constraints)

---

## 🌟 Resultado del día

Mejor comprensión de cómo limitar el alcance de los accesos a recursos en GCP mediante políticas organizacionales.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/100-dia-de-cloud)
