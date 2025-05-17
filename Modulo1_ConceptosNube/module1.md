# Módulo 1 – Información general sobre los conceptos de la nube

Este módulo introduce los principios básicos de la informática en la nube, sus beneficios, su relación con AWS y el marco CAF para la adopción efectiva en organizaciones.

---

## 📌 Temas

- Introducción a la informática en la nube
- Ventajas de la informática en la nube
- Introducción a Amazon Web Services (AWS)
- Marco de adopción de la nube de AWS (CAF de AWS)

---

## Sección 1: **Introducción a la informática en la nube**
### ¿Qué es la informática en la nube?
Es una forma de usar servicios tecnológicos (como servidores, almacenamiento, bases de datos, redes, entre otros.) a través de internet, sin tener que comprarlos o instalarlos en tu computadora.

**¿Cómo funciona?**
- Tú usas una aplicación o servicio por internet (ejemplo: Google Drive, Netflix, Amazon).
- Esa app no está en tu compu, está en servidores remotos (la nube).
- Tú solo necesitas conexión a internet.

**Características principales:**
- **Acceso bajo demanda:** Puedes usar los servicios cuando los necesites, como prender la luz.
- **Acceso desde cualquier lugar:** Solo necesitas internet.
- **Escalabilidad:** Puedes aumentar o reducir el uso fácilmente.
- **Pago por uso:** Solo pagas lo que consumes (como el agua o la luz).
- **Multitenencia:** Muchas personas pueden usar el mismo servicio al mismo tiempo, de forma segura.

### ¿Qué es la infraestructura como software?
Es una práctica que permite administrar y aprovisionar la infraestructura tecnológica (como redes, servidores, base de datos) usando código, en lugar de hacerlo manualmente.

**¿Por qué es importante?**
- Automatiza tareas repetitivas y reduce errores humanos.
- Permite replicar entornos fácilmente (como desarrollo, pruebas y producción).
- Hace más rápido y eficiente el despliegue de servicios.

    **Ejemplo:** En vez de instalar un servidor uno por uno, escribes un archivo de configuración (por ejemplo, en YAML o JSON), lo ejecutas, y la infraestructura se crea automáticamente.

**Herramientas populares:**
- AWS CloudFormation
- Terraform
- Ansible


#### 🖥️ Modelo tradicional (en sitio o "on-premises")
Es cuando la empresa compra, instala y mantiene sus propios servidores, redes y sistemas en sus instalaciones físicas.

**Características:**
- La empresa es responsable de todo: hardware, software, seguridad, energía, mantenimiento.
- Requiere gran inversión inicial y personal técnico.
- Es menos flexible para crecer o adaptarse rápidamente.

### ☁️ Modelo en la nube (cloud computing)
La empresa alquila recursos tecnológicos (como servidores, almacenamiento, entre otros) a través de internet desde un proveedor como AWS.

**Características:**
- No necesitas comprar hardware, todo está en centros de datos del proveedor.
- Se paga solo por lo que se usa.
- Alta escalabilidad, disponibilidad y menor mantenimiento.

💡 **Comparación rápida:**
| **Característica**       | **Tradicional (On-premises)** | **Nube (Cloud)**             |
| -------------------- | ------------------------- | ------------------------ |
| **Inversión inicial**    | Alta                      | Baja                     |
| **Escalabilidad**        | Limitada                  | Alta                     |
| **Mantenimiento**        | Manual (propio)           | El proveedor lo gestiona |
| **Tiempo de despliegue** | Lento                     | Rápido                   |
| **Accesibilidad**        | Local                     | Desde cualquier lugar    |

### 📌 Modelos de entrega de servicios en la nube
Existen tres modelos principales que definen qué parte del servicio gestiona el proveedor y cuál gestiona el usuario:

☁️ IaaS (Infraestructura como servicio)
- Te da acceso a recursos básicos como servidores, redes y almacenamiento.
- Tú instalas el sistema operativo, las apps y gestionas la seguridad.
- Ejemplo: Amazon EC2, Azure VM, Google Compute Engine.

🧱 PaaS (Plataforma como servicio)
- Ofrece un entorno ya configurado para desarrollar y ejecutar aplicaciones.
- Solo te enfocas en el código, el proveedor se encarga del resto.
- Ejemplo: AWS Elastic Beanstalk, Google App Engine, Heroku.

🧑‍💻 SaaS (Software como servicio)
- Usas directamente la aplicación en internet, sin instalar ni mantener nada.
- El proveedor se encarga de todo.
- Ejemplo: Gmail, Microsoft 365, Dropbox.

**Comparación visual (basado en la imagen):**
| **Modelo** | **Nivel de control** | **¿Qué gestionas tú?**        | **¿Qué gestiona el proveedor?**       |
| ------ | ---------------- | ------------------------- | --------------------------------- |
| **IaaS**   | Alto             | SO, apps, configuraciones | Infraestructura física            |
| **PaaS**   | Medio            | Aplicación y datos        | Infraestructura, SO, plataforma   |
| **SaaS**   | Bajo             | Solo el uso de la app     | Todo (infraestructura y software) |

### 📌 Modelos de implementación de informática en la nube
Existen tres formas principales en las que una organización puede implementar la informática en la nube, dependiendo de sus necesidades de control, seguridad y flexibilidad:

**☁️ Nube pública**
- Toda la infraestructura (servidores, almacenamiento, redes) es propiedad del proveedor de servicios en la nube (como AWS, Google Cloud o Azure).
- El cliente accede a los recursos por internet.
- Es el modelo más común y económico.
- 🧩 Ejemplo: Hospedar una web o aplicación en AWS.

**🔁 Nube híbrida**
- Combina infraestructura local (servidores propios) con servicios en la nube.
- Permite mantener ciertos datos críticos en local y aprovechar la nube para escalar o procesar datos menos sensibles.
- 🧩 Ejemplo: Una empresa que guarda su base de datos en su servidor pero usa la nube para realizar copias de seguridad o análisis de datos.

**🏢 Infraestructura local / Nube privada**
- La infraestructura se encuentra dentro de la empresa, pero utiliza tecnologías similares a la nube (virtualización, automatización).
- Permite más control y personalización, pero con mayor responsabilidad y costos.
- 🧩 Ejemplo: Un banco que mantiene toda su infraestructura física por temas de seguridad.

**📊 Resumen visual (según la imagen):**
| **Modelo**             | **Dónde están los recursos**       | **¿Quién los gestiona?** | **Nivel de control** |
| ------------------ | ------------------------------ | -------------------- | ---------------- |
| **Nube pública**       | En la nube (proveedor externo) | El proveedor de nube | Bajo             |
| **Nube híbrida**       | En la nube y en la empresa     | Compartido           | Medio            |
| **Nube privada/local** | Dentro de la empresa           | La propia empresa    | Alto             |



### 📌 Similitudes entre AWS y la TI tradicional
Aunque la informática en la nube funciona de forma diferente a la tradicional, los conceptos básicos son los mismos. AWS ofrece versiones equivalentes para casi todos los componentes que se usaban en centros de datos físicos.

**🔐 Seguridad**
| **TI tradicional**          | **AWS**                          |
| ----------------------- | ---------------------------- |
| Firewalls               | Grupos de seguridad          |
| ACL (listas de control) | ACL de red                   |
| Administradores         | IAM (gestión de identidades) |

**🌐 Redes**
| **TI tradicional**        | **AWS**                    |
| --------------------- | ---------------------- |
| Enrutadores           | Amazon VPC             |
| Conmutadores y redes  | Elastic Load Balancing |
| Canalizaciones de red | Subredes en la VPC     |

**💻 Informática**
| **TI tradicional**      | **AWS**                        |
| ------------------- | -------------------------- |
| Servidores físicos  | Instancias EC2             |
| Imágenes de sistema | AMI (Amazon Machine Image) |

**💾 Almacenamiento y bases de datos**
| **TI tradicional**         | **AWS**                 |
| ---------------------- | ------------------- |
| DAS, SAN, NAS          | Amazon EBS, EFS, S3 |
| Bases de datos locales | Amazon RDS          |

---

## Sección 2: Ventajas de la informática en la nube
---

## Sección 3: Introducción a AWS
---

## Sección 4: Migración a la nube de AWS