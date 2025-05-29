# 📅 Día 017 – Retomar curso de Terraform

## 📌 Tema

Crear un Internet Gateway en AWS utilizando Terraform para permitir el acceso público a una instancia.

---

## 📘 Descripción

Hoy trabajé con recursos de red en AWS usando Terraform, enfocándome en la creación de un gateway de Internet para habilitar el tráfico desde y hacia internet.

### 🔌 Internet Gateway

Es el punto de entrada y salida entre una VPC y la red pública (Internet).

```hcl
resource "aws_internet_gateway" "gw" {
  vpc_id = aws_vpc.main.id

  tags = {
    Name = "main"
  }
}
```

🧭 Tabla de rutas
Define cómo llegar a otras redes (en este caso, Internet) desde la subnet pública.

```hcl
resource "aws_route_table" "example" {
  vpc_id = aws_vpc.example.id

  route {
    cidr_block = "10.0.1.0/24"
    gateway_id = aws_internet_gateway.example.id
  }

  route {
    ipv6_cidr_block        = "::/0"
    egress_only_gateway_id = aws_egress_only_internet_gateway.example.id
  }

  tags = {
    Name = "example"
  }
}
```

🔗 Asociación de rutas
Se asocia la tabla de rutas a una subred específica:

```hcl
resource "aws_route_table_association" "a" {
  subnet_id      = aws_subnet.foo.id
  route_table_id = aws_route_table.bar.id
}
```

🔒 Grupo de seguridad
Permite el tráfico SSH entrante y todo el tráfico saliente:

```hcl
resource "aws_security_group" "sg_public_instance" {
  name        = "Public Instance SG"
  description = "Allow SSH traffic and ALL egress traffic"
  vpc_id      = aws_vpc.vpc_virginia.id

  tags = {
    Name = "Public Instance SG"
  }
}

resource "aws_vpc_security_group_ingress_rule" "allow_tls_ipv4" {
  security_group_id = aws_security_group.sg_public_instance.id
  cidr_ipv4         = var.sg_ingress_cidr
  from_port         = 22
  ip_protocol       = "tcp"
  to_port           = 22
}

resource "aws_vpc_security_group_egress_rule" "allow_all_traffic_ipv4" {
  security_group_id = aws_security_group.sg_public_instance.id
  cidr_ipv4         = "0.0.0.0/0"
  ip_protocol       = "-1"
}

resource "aws_vpc_security_group_egress_rule" "allow_all_traffic_ipv6" {
  security_group_id = aws_security_group.sg_public_instance.id
  cidr_ipv6         = "::/0"
  ip_protocol       = "-1"
}
```

---

## ✅ Lo que aprendí

Cómo se configura un Internet Gateway en AWS con Terraform.

Cómo establecer rutas de salida hacia Internet desde una subnet pública.

Cómo aplicar reglas de seguridad para habilitar acceso SSH.

El flujo básico para exponer una instancia a Internet desde infraestructura como código.

---

## 📚 Recursos útiles

[recursos terraform](https://registry.terraform.io/providers/hashicorp/aws/5.97.0/docs/resources/security_group)

[recursos terraform](https://registry.terraform.io/providers/hashicorp/aws/5.97.0/docs/resources/vpc_security_group_egress_rule)

---

## 🎯 Resultado del día

Logré crear y asociar un Internet Gateway a una VPC, habilitando el acceso externo a una instancia pública. Esto refuerza mis conocimientos sobre redes en la nube y Terraform como herramienta de infraestructura como código.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
