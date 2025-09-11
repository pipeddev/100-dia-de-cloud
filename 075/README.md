# 🌥️ Día 75 – Lab: Módulos de Terraform en Google Cloud

## 📌 Tema

Uso de **módulos en Terraform** para automatizar y reutilizar configuraciones en Google Cloud.

## 📝 Descripción general

En este laboratorio aprendí a crear una configuración de **Terraform con módulos**, lo que permite **reutilizar código**, abstraer recursos y facilitar la gestión de infraestructura en Google Cloud.

Terraform no solo permite definir recursos declarativos, sino que también puede generar **planes de ejecución incrementales**, aplicando cambios paso a paso conforme evoluciona la configuración.

El uso de un **módulo de instancias de VM** permitió definir una plantilla parametrizable con **variables de entrada**, de manera que la misma configuración puede replicarse para varios recursos sin duplicar código.

## 🎯 Objetivos del día

- Crear una configuración para una **red de modo automático**.
- Crear una configuración para una **regla de firewall**.
- Crear un **módulo de instancias de VM**.
- Implementar la configuración en Google Cloud.
- Verificar el despliegue de los recursos.

## ⚙️ Flujo de trabajo

1. 📄 Definir una configuración base (`main.tf`) para la red y firewall.
2. 📦 Crear un **módulo de instancias** con variables de entrada (nombre, zona, tipo de máquina, etc.).
3. 🛠️ Invocar el módulo desde la configuración principal para crear una o varias instancias.
4. 🚀 Ejecutar `terraform init`, `plan` y `apply` para desplegar la infraestructura.
5. ✅ Validar que la red, firewall y VMs se hayan creado correctamente.

## 🛠️ Herramientas utilizadas

- Terraform (HCL)
- Google Cloud VPC (modo automático)
- Firewall rules
- Compute Engine (instancias VM mediante módulo)

## 🤓 Lo que aprendí

- Los **módulos en Terraform** permiten estructurar la infraestructura en **componentes reutilizables**.
- Las **variables de entrada** hacen posible parametrizar los módulos y usarlos en diferentes entornos.
- Terraform puede generar **planes de ejecución incrementales**, lo que simplifica la evolución de la infraestructura.
- Este enfoque mejora la **modularidad y mantenibilidad** de la infraestructura como código.

## 🔗 Recursos útiles

- [Módulos de Terraform](https://developer.hashicorp.com/terraform/language/modules)
- [Terraform en Google Cloud](https://cloud.google.com/docs/terraform)

## 🚀 Resultado del día

Hoy implementé un **módulo en Terraform para instancias de VM**, junto con configuraciones de red y firewall.
Esto me permitió entender cómo **reutilizar configuraciones, parametrizar recursos y escalar implementaciones futuras** de forma más ordenada y eficiente.
