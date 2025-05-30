# 📅 Día 018 – Curso de Terraform y GCP

## 📌 Tema

Aprender cómo usar provisioners en una instancia y comenzar el módulo "Essential Google Cloud Infrastructure: Foundation" para la certificación Associate Cloud Engineer.

---

## 📘 Descripción

### Provisioners en Terraform

Los _provisioners_ permiten ejecutar código local o remoto dentro de una instancia que estamos creando.

```hcl
provisioner "local-exec" {
  command = "echo instance created with IP: ${aws_instance.public_instance.public_ip} >> datos_instancia.txt"
}
```

```hcl
provisioner "remote-exec" {
  inline = [
    "echo 'Hello, World!' > ~/saludo.txt"
  ]

  connection {
    type        = "ssh"
    host        = self.public_ip
    user        = "ec2-user"
    private_key = file("terraform-key.pem") # Asegúrate de que la ruta al archivo de clave privada sea correcta
  }
}
```

---

### Essential Google Cloud Infrastructure: Foundation

#### ¿Cómo interactuar con GCP?

Google Cloud ofrece 4 formas principales para interactuar con sus servicios:

1. **Google Cloud Console**: interfaz gráfica accesible desde [console.google.com](https://console.google.com)
2. **Cloud Shell y Google Cloud CLI**: terminal web con CLI preinstalada, comandos como:
   ```bash
   gcloud compute instances list
   ```
3. **API REST**: acceso programático a servicios de GCP, útil para crear herramientas personalizadas.
4. **Cloud Mobile App**: gestión de servicios desde dispositivos Android/iOS.

#### Actividades del laboratorio

- Obtener acceso a Google Cloud
- Crear un bucket de Cloud Storage desde la consola y desde Cloud Shell
- Familiarizarse con Cloud Shell

**Crear un bucket:**

```bash
gcloud storage buckets create gs://[BUCKET_NAME]
```

**Subir archivo al bucket:**

```bash
gcloud storage cp [MY_FILE] gs://[BUCKET_NAME]
```

**Listar regiones disponibles:**

```bash
gcloud compute regions list
```

**Crear y verificar una variable de entorno:**

```bash
INFRACLASS_REGION=[YOUR_REGION]
echo $INFRACLASS_REGION
```

---

## ✅ Lo que aprendí

- Cómo usar `local-exec` y `remote-exec` en Terraform para ejecutar comandos en instancias.
- Distintos métodos para interactuar con GCP.
- Comandos básicos para gestionar buckets y variables desde la terminal.

---

## 📚 Recursos útiles

- [Documentación oficial de Terraform Provisioners](https://developer.hashicorp.com/terraform/language/resources/provisioners/syntax)
- [Google Cloud CLI Docs](https://cloud.google.com/sdk/gcloud)

---

## 🎯 Resultado del día

Avancé en el curso de Terraform creando provisioners funcionales y entendí cómo interactuar con Google Cloud de forma efectiva a través de consola, CLI y Cloud Shell.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/)
