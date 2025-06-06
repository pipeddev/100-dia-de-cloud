# 📅 Día 024 – Finalización del módulo de redes virtuales y Terraform

## 📌 Tema

Repasar conceptos clave de redes en GCP y comprender el uso adecuado de `count` vs `for_each` en Terraform para la creación dinámica de recursos.

---

## 📘 Descripción

### ✅ Apuntes clave del módulo de redes virtuales

**1. ¿Cuál es la ventaja de aplicar reglas de firewall por etiquetas en lugar de direcciones IP?**  
Cuando se crea una VM con una etiqueta asociada, las reglas de firewall se aplican automáticamente, sin importar la IP asignada.  
🔹 Esto permite reglas más **flexibles, reutilizables y fáciles de mantener**, ya que no dependen de direcciones IP específicas.

**2. ¿Cuáles son los tres tipos de redes que ofrece Google Cloud?**

- Predeterminada
- Automática
- Personalizada

Cada tipo tiene características específicas según el control que deseas sobre las subredes y rangos de IP.

**3. ¿Cuántas direcciones IP necesita una VM como mínimo?**  
🔹 **Una IP interna**. La IP externa es opcional.

---

### ⚙️ Terraform: `count` vs `for_each`

#### Ejemplo con `count`

```hcl
variable "instancias" {
  description = "Nombre de instancias"
  type        = list(string)
  default     = ["apache", "mysql", "jumpserver"]
}

resource "aws_instance" "public_instance" {
  count         = length(var.instancias)
  ami           = var.ec2_specs.ami
  instance_type = var.ec2_specs.instance_type
  subnet_id     = aws_subnet.public_subnet.id
  key_name      = data.aws_key_pair.key.key_name
  vpc_security_group_ids = [aws_security_group.sg_public_instance.id]
  user_data = file("scripts/userdata.sh")

  tags = {
    Name = var.instancias[count.index]
  }
}
```

🧠 Problema: Si eliminas "apache" de la lista, "mysql" y "jumpserver" se reordenan, lo que puede ocasionar que se destruyan y vuelvan a crear recursos innecesariamente.

#### Ejemplo con for_each

```
variable "instancias" {
  description = "Nombre de instancias"
  type        = set(string)
  default     = ["apache", "mysql", "jumpserver"]
}

resource "aws_instance" "public_instance" {
  for_each      = var.instancias
  ami           = var.ec2_specs.ami
  instance_type = var.ec2_specs.instance_type
  subnet_id     = aws_subnet.public_subnet.id
  key_name      = data.aws_key_pair.key.key_name
  vpc_security_group_ids = [aws_security_group.sg_public_instance.id]
  user_data = file("scripts/userdata.sh")

  tags = {
    Name = each.value
  }
}
```

🔍 Beneficios de for_each:

- Identifica los recursos por nombre ("apache", "mysql", etc.) en lugar de por índice.
- Si eliminas una entrada (ej: "apache"), solo ese recurso se destruye.
- Al ejecutar terraform state list, verás recursos como:
  `aws_instance.public_instance["apache"]`

---

## ✅ Lo que aprendí

- Cómo aplicar reglas de firewall de forma dinámica con etiquetas en GCP.
- Diferencias prácticas entre redes predeterminadas, automáticas y personalizadas.
- Buenas prácticas para el manejo de múltiples instancias en Terraform usando for_each.

---

## 📚 Recursos útiles

- Terraform: count vs for_each
- Firewall Rules en GCP

---

## 🎯 Resultado del día

Consolidé el uso práctico de Terraform para aprovisionamiento flexible de infraestructura y repasé conceptos críticos sobre redes en GCP que ayudarán en el examen Associate Cloud Engineer.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
