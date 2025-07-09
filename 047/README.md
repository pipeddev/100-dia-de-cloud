# 📅 Día 047 – Cloud SQL: Base de datos relacional administrada

## 📌 Tema

Bases de datos relacionales (estructuradas) y el servicio administrado Cloud SQL de Google Cloud.

---

## 📘 Descripción

### ¿Qué es Cloud SQL?

Cloud SQL es un servicio **completamente administrado** para bases de datos relacionales que permite utilizar:

- MySQL (5.6, 5.7, 8.0)
- PostgreSQL (versiones desde 9.6 hasta 15)
- Microsoft SQL Server (2017 y 2019 en ediciones Web, Express, Standard o Enterprise)

### ¿Por qué usar Cloud SQL y no una VM con SQL?

Aunque puedes instalar una base de datos en una VM, Cloud SQL simplifica la administración al encargarse automáticamente de:

- Aplicar parches y actualizaciones
- Realizar copias de seguridad y restauraciones
- Escalar vertical u horizontalmente
- Implementar alta disponibilidad
- Configurar conexiones seguras (IP privada, autenticación proxy, SSL)

### Características clave:

- Hasta **64 TB** de almacenamiento, **60,000 IOPS**, y **624 GB de RAM** por instancia.
- Escalamiento vertical (hasta 96 vCPUs) y horizontal (con réplicas de lectura).
- Soporte para herramientas externas como SQL Workbench, Toad, y controladores estándar de MySQL.
- Compatibilidad con App Engine, Cloud Shell y Google Workspace.

### Alta disponibilidad y replicación:

- Cloud SQL ofrece una configuración regional con instancia principal y de respaldo.
- Soporta **replicación síncrona entre zonas**.
- En caso de falla, se activa la **conmutación por error automática**.

### Copias de seguridad y recuperación:

- Copias de seguridad bajo demanda o programadas.
- Recuperación hasta un punto en el tiempo.
- Soporte para exportar/importar datos vía CSV o mysqldump.

### Conectividad:

- IP privada (mejor rendimiento y seguridad en la misma región)
- Proxy de autenticación de Cloud SQL
- Conexión externa mediante SSL o IP autorizada (menos recomendada)

### ¿Cuándo elegir Cloud SQL?

- Cuando necesitas una base de datos relacional sin requerir escalabilidad horizontal ni disponibilidad global.
- Es ideal si buscas una solución más **rentable** y **simple de administrar**.

Si tu aplicación necesita alta disponibilidad global y escalabilidad horizontal, se recomienda usar **Cloud Spanner**.

---

## ✅ Lo que aprendí

- Qué es Cloud SQL y para qué sirve.
- Las diferencias entre usar una VM con SQL vs. un servicio administrado.
- Cómo funciona la alta disponibilidad y escalabilidad.
- Qué opciones de conexión existen según el entorno.

---

## 📚 Recursos útiles

- [Documentación oficial Cloud SQL](https://cloud.google.com/sql/docs)
- [Conexión por IP privada](https://cloud.google.com/sql/docs/mysql/private-ip)

---

## 🌟 Resultado del día

✔️ Profundicé en el uso de Cloud SQL como base de datos relacional administrada, sus ventajas frente a soluciones autogestionadas y sus casos de uso más comunes.

---

## 🤝 Conecta conmigo

- [LinkedIn](https://www.linkedin.com/in/luis-felipe-carrasco/)
- [GitHub](https://github.com/pipeddev/100-dia-de-cloud)
