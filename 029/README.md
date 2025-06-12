# 🗓️ Día 029 – Terraform dynamic blocks

## 📌 Tema

Uso de bloques dinámicos en Terraform y conceptos teóricos sobre módulos.

---

## 📘 Descripción

### 🔁 Dynamic blocks

Nos permite tener un código más prolijo y entendible cuando hay varias repeticiones del mismo tipo de estructura.  
Un ejemplo clásico es la configuración de múltiples reglas de `ingress` en un `security group`.

**📦 Declarar variable**  
Archivo: `variables.tf`

```
variable "ingress_port_list" {
  description = "Lista de puertos de ingreso"
  type        = list(number)
}
```

**⚙️ Asignar valor a variable**  
Archivo: `terraform.tfvars`

```
ingress_port_list = [22, 80, 443]
```

**🛡️ Uso de dynamic block**

```
resource "aws_security_group" "sg_public_instance" {
  name        = "Public Instance SG"
  description = "Allow SSH traffic and ALL egress traffic"
  vpc_id      = aws_vpc.vpc_virginia.id

  dynamic "ingress" {
    for_each = var.ingress_port_list
    content {
      description = "Allow traffic on port ${ingress.value}"
      from_port   = ingress.value
      to_port     = ingress.value
      protocol    = "tcp"
      cidr_blocks = [var.sg_ingress_cidr]
    }
  }

  tags = {
    Name = "Public Instance SG-${local.suffix}"
  }
}
```

### 🧱 Módulos en Terraform – Teoría

Usar módulos ayuda a que el código sea más fácil de mantener y reutilizar.

- Un módulo puede encargarse de la creación de subredes.
- Otro módulo puede gestionar las VPCs.
- Otro puede manejar las instancias.

📚 Puedes explorar el registro oficial de módulos aquí:  
🔗 https://registry.terraform.io/browse/modules

---

## ✅ Lo que aprendí

- Cómo aplicar `dynamic blocks` en recursos repetitivos.
- La ventaja de usar `for_each` con listas en bloques dinámicos.
- Beneficios del uso de módulos para mantener un código reutilizable y organizado.

---

## 📚 Recursos útiles

- [Terraform Dynamic Blocks](https://developer.hashicorp.com/terraform/language/expressions/dynamic-blocks)
- [Terraform Registry Modules](https://registry.terraform.io/browse/modules)

---

## 🌟 Resultado del día

Automatización de reglas de seguridad usando bloques dinámicos y refactorización de infraestructura para adoptar módulos reutilizables.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
