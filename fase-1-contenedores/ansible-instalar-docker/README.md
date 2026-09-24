# Instalacion de Docker con Ansible

Playbook de Ansible que instala Docker Engine en Ubuntu de forma automatizada
e idempotente: repositorio oficial, clave GPG, paquetes y arranque del servicio.

## Uso

- Probar en la propia maquina (localhost):
  ansible-playbook -i inventory.ini instalar-docker.yml

- En un servidor real: edita inventory.ini con la IP y el usuario SSH del
  servidor, y ejecuta el mismo comando. Ansible se conectara por SSH.

## Conceptos aplicados

- Playbook idempotente (se puede ejecutar muchas veces sin efectos secundarios)
- Modulos: apt, file, get_url, apt_repository, service
- Uso de facts del sistema (ansible_facts) para adaptarse a la version de Ubuntu
- Inventario con grupos de hosts

---
Autor: Alejandro Quevedo - Ebenezer
