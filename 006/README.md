# 📅 Día 006 – Uso del bloque `lifecycle {}` en Terraform

## 📌 Tema

Explorar el uso del bloque `lifecycle {}` en Terraform para controlar el comportamiento de los recursos durante su creación, actualización o destrucción.

---

## 📘 Descripción

Hoy estudié el bloque `lifecycle` en Terraform, el cual permite definir reglas sobre cómo se deben manejar los cambios en los recursos.  
Este bloque es especialmente útil cuando queremos evitar recrear recursos innecesariamente o forzar su reemplazo ante ciertos cambios.

---

## 🛠️ Herramientas utilizadas

- Visual Studio Code
- Terraform CLI

---

## ✅ Lo que aprendí

### 🔧 Sintaxis básica

```hcl
resource "aws_instance" "example" {
  ami           = "ami-123456"
  instance_type = "t2.micro"

  lifecycle {
    create_before_destroy = true
    prevent_destroy       = true
    ignore_changes        = [tags, user_data]
  }
}
```

## 📚 Recursos útiles

---

## 🎯 Resultado del día

Aprender el uso del bloque lifecycle.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)

---
