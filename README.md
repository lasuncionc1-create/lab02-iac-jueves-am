# Proyecto de Infraestructura como Código (IAC) con Terraform y Docker

Este proyecto utiliza Terraform para automatizar la creación y gestión de contenedores Docker para el entorno de desarrollo (dev) y calidad (qa). Se configura una arquitectura con un contenedor para el Frontend (nginx), Backend (node.js) y Base de Datos (PostgreSQL).

## Tecnologías Utilizadas
- Terraform: para la automatización de infraestructura.
- Docker: para la creación y ejecución de contenedores.
- PostgreSQL: como base de datos.
- nginx: como servidor web para el frontend.
- Node.js: para el backend.

## Requisitos

- Terraform: (versión recomendada: `>=1.0.0`).
- Docker: (versión recomendada: última estable).
- Git: para clonar el repositorio.

## Instalación y Configuración

1. Clonar el repositorio:

   ```bash
   git clone https://github.com/lasuncionc1-create/lab02-iac-jueves-am
   cd mi-repo
   ```

2. Instalar Terraform:

   Si aún no tienes Terraform instalado, sigue los pasos en la (https://www.terraform.io/downloads).

3. Inicializar Terraform:

   ```bash
   terraform init
   ```

4. Validar la configuración de Terraform:

   ```bash
   terraform validate
   ```

5. Aplicar los cambios de Terraform:

   ```bash
   terraform apply
   ```

6. Acceder a la aplicación:

   Una vez que los contenedores estén corriendo, se podrá acceder a la API en el siguiente URL:

   - `http://localhost:4002` para el Backend (API).
   - `http://localhost:4001` para el Frontend (nginx).

   Dependiendo de mi configuración de puertos (en tu `terraform.tfvars`), estos puertos pueden cambiar.

### Variables de Configuración

- api_port: Puerto externo para la API.
  - dev: 4002
  - qa: 5002

- web_port: Puerto externo para el Frontend.
  - dev: 4001
  - qa: 5001

- bd_port: Puerto externo para la base de datos.
  - dev: 4003
  - qa: 5003

Estas variables se definen en el archivo `terraform.tfvars` y se puede cambiar según el entorno que estés utilizando.