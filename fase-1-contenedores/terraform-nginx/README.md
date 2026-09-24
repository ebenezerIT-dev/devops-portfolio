# Contenedor nginx con Terraform

Infraestructura como codigo con Terraform y el proveedor de Docker.
Crea una imagen y un contenedor de nginx (puerto 8082) de forma declarativa.

## Uso

- terraform init      (descarga el proveedor)
- terraform plan      (previsualiza los cambios)
- terraform apply     (crea la infraestructura)
- terraform destroy   (la elimina)

## Conceptos aplicados

- Infraestructura como codigo (HCL) declarativa e idempotente
- Providers, resources y referencias entre recursos
- Flujo init / plan / apply / destroy
- Gestion del estado y buenas practicas de .gitignore (no versionar tfstate)

---
Autor: Alejandro Quevedo - Ebenezer
