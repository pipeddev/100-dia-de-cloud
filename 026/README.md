# 📅 Día 026 – Funciones en Terraform y Compute Engine

## 📌 Tema

Explorar funciones integradas en Terraform y comprender el ciclo de vida de máquinas virtuales en Google Cloud con Compute Engine.

---

## 📘 Descripción

### 🧪 Terraform Console y funciones comunes

El comando `terraform console` permite evaluar expresiones para depuración y aprendizaje. A continuación, se listan ejemplos útiles para listas, cadenas y mapas:

---

#### Funciones con listas

```hcl
toset(var.instancias)
// Convierte una lista en un conjunto (elimina duplicados)
// Ej: ["mysql", "jumpserver", "mysql"] → {"mysql", "jumpserver"}

length(var.instancias)
// Retorna el número de elementos en la lista

max(1, -1, 500, 200)
// Devuelve el número más alto → 500

min(1, -1, 500, 200)
// Devuelve el número más bajo → -1

ceil(12.4)   // Resultado: 13
floor(12.8)  // Resultado: 12
```

---

#### Funciones con cadenas

```
variable "cadena" {
  type    = string
  default = "ami-123,AMI-AAV,ami12f"
}

split(",", var.cadena)
// → ["ami-123", "AMI-AAV", "ami12f"]

lower(var.cadena)
// → "ami-123,ami-aav,ami12f"

upper(var.cadena)
// → "AMI-123,AMI-AAV,AMI12F"

substr(var.cadena, 0, 7)
// → "ami-123"

substr(var.cadena, 2, 7)
// → "i-123,A"
```

---

#### Funciones con listas de palabras

```
variable "palabras" {
  type    = list(string)
  default = ["hola", "como", "estas"]
}

join("-", var.palabras)
// → "hola-como-estas"

index(var.palabras, "como")
// → 1

contains(var.palabras, "test")
// → false
```

---

#### Funciones con mapas

```
variable "entornos" {
  type = map(string)
  default = {
    "dev"  = "172.16.0.0/16",
    "prod" = "10.10.0.0/16",
  }
}

lookup(var.entornos, "prod")
// → "10.10.0.0/16"

lookup(var.entornos, "test", "no existe")
// → "no existe"
```

### ☁️ Compute Engine – Lab de VMs

En el laboratorio práctico se realizaron las siguientes acciones:

- Crear VMs estándar y personalizadas.
- Probar VMs con diferentes sistemas operativos (Linux y Windows).
- Eliminar instancias creadas para limpieza del entorno.
- Aplicar prácticas comunes de administración de recursos en Compute Engine.

---

## ✅ Lo que aprendí

- Evaluación de funciones en Terraform para listas, cadenas y mapas.
- Uso práctico de terraform console como herramienta de depuración.
- Configuración y despliegue de máquinas virtuales estándar y personalizadas.
- Comparación entre tipos de VMs y sistemas operativos en Google Cloud.

---

## 📚 Recursos útiles

- Funciones en Terraform (HashiCorp)

---

## 🎯 Resultado del día

Dominé el uso de funciones clave en Terraform y realicé un despliegue efectivo de máquinas virtuales en Google Cloud. Este conocimiento refuerza habilidades tanto en automatización como en operación manual de infraestructura.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
