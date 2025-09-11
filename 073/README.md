# 🌥️ Día 73 – Lab: Balanceo de cargas de aplicaciones (HTTP/HTTPS) en Google Cloud

## 📌 Tema

Configuración de un **balanceador de cargas HTTP(S) global** con escalado automático y soporte IPv4/IPv6.

## 📝 Descripción general

El **balanceo de cargas de aplicaciones (HTTP/HTTPS)** en Google Cloud se ejecuta en el **perímetro de la red de Google**, dentro de los **puntos de presencia (PoP)** distribuidos mundialmente.

🔹 El tráfico de usuario ingresa en el PoP más cercano y se enruta por la **red global de Google** hacia el backend con capacidad disponible más próxima.
🔹 Esto proporciona **baja latencia, alta disponibilidad y escalabilidad global automática**, sin necesidad de configurar hardware dedicado.

En este laboratorio, se implementó un **balanceador de cargas HTTP global**, verificando su funcionamiento con una **prueba de esfuerzo** para observar cómo distribuye la carga y escala automáticamente.

## 🎯 Objetivos del día

- Crear una **regla de firewall** para las verificaciones de estado.
- Configurar **Cloud NAT** y **Cloud Router** para el acceso de salida de las instancias.
- Construir una **imagen personalizada** de un servidor web.
- Crear una **plantilla de instancias** basada en dicha imagen.
- Desplegar **dos grupos de instancias administrados (MIGs)** en distintas regiones.
- Configurar un **balanceador de cargas HTTP global** con soporte **IPv4 e IPv6**.
- Ejecutar una **prueba de esfuerzo** para validar el balanceo y el escalado automático.

## ⚙️ Flujo de trabajo

1. 🚦 Configurar reglas de firewall para permitir las verificaciones de estado.
2. 🌐 Implementar Cloud NAT + Cloud Router para salida a internet.
3. 📀 Crear una imagen de servidor web.
4. 🛠️ Generar una plantilla de instancias a partir de la imagen.
5. 📊 Desplegar **MIGs multirregionales** para el backend.
6. 🌍 Configurar el balanceador HTTP(S) global con IPv4/IPv6.
7. 🔄 Someter el balanceador a una **prueba de esfuerzo** y validar el escalado.

## 🛠️ Herramientas utilizadas

- Google Cloud VPC
- Cloud NAT y Cloud Router
- Compute Engine (imágenes, plantillas y grupos administrados)
- HTTP(S) Load Balancing (global, capa 7)
- Firewall rules

## 🤓 Lo que aprendí

- Los balanceadores HTTP(S) de Google funcionan en los **PoPs globales**, optimizando la latencia para usuarios en cualquier parte del mundo.
- La **red global de Google** permite balanceo y escalado multirregional sin configuraciones complejas.
- Con IPv6 habilitado, es posible atender a clientes modernos sin modificar backends que usan IPv4.
- El **escalado automático** asegura la disponibilidad frente a cargas altas.
- Este enfoque reduce costos y complejidad al aprovechar la infraestructura administrada de Google.

## 🔗 Recursos útiles

- [HTTP(S) Load Balancing en Google Cloud](https://cloud.google.com/load-balancing/docs/https)
- [Cloud NAT con Cloud Router](https://cloud.google.com/nat/docs/overview)

## 🚀 Resultado del día

Hoy configuré un **balanceador de cargas HTTP(S) global** en GCP con soporte para IPv4/IPv6 y lo probé bajo condiciones de carga, comprobando el **escalado automático** y la distribución de tráfico a nivel mundial.
