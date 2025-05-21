# 📅 Día 010 – Máquinas virtuales y redes en la nube

## 📌 Tema

Realización de un laboratorio práctico para explorar redes, subredes, rutas y reglas de firewall en Google Cloud utilizando instancias de Compute Engine.

---

## 📘 Descripción

Hoy completé un laboratorio centrado en comprender cómo funcionan las **redes (VPC)**, **subredes**, **rutas** y **reglas de firewall** en Google Cloud Platform, y cómo afectan a la comunicación entre recursos.

### Actividades realizadas:

1. **Eliminé la VPC por defecto** y sus reglas de firewall para entender qué sucede en su ausencia.
   - Resultado: no se pueden crear VMs sin una VPC válida.
2. Intenté crear una máquina virtual sin una red configurada → **Fallo esperado**.
3. Creé una **VPC personalizada**, con subredes y reglas de firewall específicas.
4. Desplegué **dos instancias de VM** dentro de la nueva red y realicé pruebas de conectividad:

   - Comunicación mediante IP **externa** usando `ping`.
   - Comunicación mediante IP **interna**.
   - Acceso remoto vía **SSH**.

5. **Eliminé reglas de firewall clave** para observar cómo afectan a la conectividad:
   - `allow-icmp`: sin esta regla no es posible hacer ping entre máquinas (ICMP bloqueado).
   - `allow-custom`: necesaria para el tráfico interno entre VMs (IP privada).
   - `allow-ssh`: sin esta regla, no se puede acceder por SSH a las instancias desde el exterior.

Estas pruebas me permitieron visualizar de forma práctica cómo funcionan los componentes de red y seguridad en GCP y por qué es fundamental definir adecuadamente las reglas de acceso.

---

## 🛠️ Herramientas utilizadas

- Google Cloud Skills Boost Labs

---

## ✅ Lo que aprendí

- Una **VPC es esencial** para desplegar recursos; sin ella, no es posible crear VMs.
- Las **reglas de firewall** determinan si es posible la comunicación entre instancias o desde/hacia Internet.
- Las **subredes** permiten segmentar la red por región y aislar recursos.
- La **comunicación entre VMs** depende de las IPs internas y externas, y requiere reglas explícitas para cada tipo de tráfico.
- Eliminando y restaurando reglas se puede verificar el impacto de cada una, lo que ayuda a entender la configuración mínima necesaria para entornos funcionales y seguros.

---

## 📚 Recursos útiles

- [Lab – Networking Basics in GCP](https://www.cloudskillsboost.google/course_templates/60/labs/530150)

---

## 🎯 Resultado del día

Aprendí de forma práctica cómo funcionan las **VPCs**, **subredes**, **rutas** y **reglas de firewall**, y cómo se configuran para permitir o restringir tráfico en Google Cloud.  
Además, finalicé el submódulo **"Máquinas virtuales y redes en la nube"** del curso.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)

---
