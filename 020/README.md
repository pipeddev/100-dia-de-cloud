# 📅 Día 020 – Redes y subredes

## 📌 Tema

Realizar un laboratorio práctico con Jenkins desde el Marketplace y comenzar el módulo de redes virtuales del curso de infraestructura esencial en Google Cloud.

---

## 📘 Descripción

### Proyectos, redes y subredes

#### Proyecto

Los proyectos organizan los recursos de la infraestructura de Google Cloud.  
Cada proyecto:

- Se asocia a una cuenta de facturación.
- Puede contener redes completas (hasta 15 por defecto, ampliable bajo solicitud).

#### Red

![Subred ejemplo](https://github.com/pipeddev/100-dia-de-cloud/blob/main/020/network-example.png)

Las redes pueden ser compartidas entre proyectos o intercambiar tráfico entre ellas.  
Características clave:

- No tienen rangos IP propios; funcionan como contenedores lógicos de recursos.
- Son **globales**, abarcando todas las regiones disponibles.
- Dentro de una red, se definen **subredes regionales**.

**Tipos de redes en GCP:**

- **Default (predeterminada)**:

  - Incluye subredes preconfiguradas en cada región con bloques CIDR únicos.
  - Reglas de firewall abiertas para ICMP, RDP y SSH desde cualquier origen.
  - Permite tráfico interno entre instancias por defecto.

- **Automatic (automática)**:

  - Crea subredes automáticamente en todas las regiones.
  - Utiliza rangos predefinidos /20 que pueden expandirse hasta /16.
  - Bloque CIDR: `10.128.0.0/9`.
  - Nuevas regiones generan nuevas subredes automáticamente.

- **Custom (personalizada)**:
  - No crea subredes automáticamente.
  - Permite control completo sobre las subredes y rangos IP.
  - No permite superposición entre subredes de la misma red.
  - Se puede convertir una red automática en personalizada (irreversible).

**IPv6 en GCP:**  
Disponible en redes VPC personalizadas mediante instancias de VM con **doble pila (dual-stack)** para usar IPv4 e IPv6.

> Si dos VMs están en la misma red, pueden comunicarse usando IP interna, incluso si están en distintas regiones.  
> Si están en redes diferentes, deben comunicarse mediante IP externa, incluso si están en la misma región.

La red de VPC permite la comunicación privada global entre instancias, incluyendo integración con redes locales a través de VPN Gateway.

---

### Subred

![Subred ejemplo](https://github.com/pipeddev/100-dia-de-cloud/blob/main/020/subnetwork-example.png)

- Las **subredes** son regionales pero pueden abarcar múltiples zonas.
- Representan un **rango de direcciones IP internas**.

**Direcciones reservadas en una subred:**

- `.0` – Red
- `.1` – Puerta de enlace de la subred
- Penúltima – Reservada
- Última – Dirección de broadcast
- `.2`, `.3`, etc. – Comienzan las direcciones asignables a VMs

**Ventajas:**

- VMs en distintas zonas dentro de una subred pueden comunicarse directamente.
- Reglas de firewall pueden aplicarse a toda la subred.

**Expansión de subredes sin recrear instancias:**

- El nuevo rango no debe superponerse con otros en la misma red.
- Los rangos deben ser CIDR válidos.
- Subredes automáticas pueden expandirse hasta `/16`.
- También pueden convertirse a modo personalizado para un control más granular.
- Evitar subredes demasiado grandes, ya que pueden generar conflictos CIDR al interactuar con otras redes, VPNs o conexiones on-premise.

---

### Direcciones IP

Cada VM puede tener:

1. **IP interna** (obligatoria)
2. **IP externa** (opcional)

#### IP Interna

- Asignada automáticamente vía DHCP interno.
- Resolución de nombres vía DNS interno (solo para hosts en la misma red).

#### IP Externa

- Útil para acceso desde fuera de GCP.
- Puede ser:
  - **Efímera**: se asigna de un pool dinámico.
  - **Estática**: se reserva explícitamente.
- IPs estáticas no asignadas a recursos generan costos adicionales.

---

## ✅ Lo que aprendí

- Cómo funcionan las redes, subredes y direcciones IP en GCP.
- Diferencias entre redes automáticas, predeterminadas y personalizadas.
- Consideraciones técnicas al diseñar subredes escalables y seguras.

---

## 📚 Recursos útiles

- [Documentación oficial sobre VPC en GCP](https://cloud.google.com/vpc/docs/overview)
- [Diferencias entre redes automáticas y personalizadas](https://cloud.google.com/vpc/docs/vpc#vpc_networks)

---

## 🎯 Resultado del día

Inicié formalmente el estudio del módulo de redes en GCP, reforzando los conceptos fundamentales de redes, subredes y direccionamiento IP. Comprendí cómo se estructuran los recursos a nivel de red y cómo escalar de manera segura utilizando las prácticas recomendadas de GCP.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
