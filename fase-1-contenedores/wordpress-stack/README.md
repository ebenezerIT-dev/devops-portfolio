# WordPress con Docker Compose

Stack de dos servicios (WordPress + MariaDB) orquestado con Docker Compose.
La base de datos no expone puertos al exterior; solo es accesible por WordPress
a traves de la red privada del stack. Las credenciales se gestionan con un
archivo .env (no versionado).

## Uso

1. Copia la plantilla de variables y editala con tus contrasenas: cp .env.example .env
2. Levanta el stack: docker compose up -d
3. Abre WordPress en http://localhost:8081

## Detener

- docker compose down     (detiene y elimina los contenedores)
- docker compose down -v  (ademas borra el volumen de la base de datos)

## Conceptos aplicados

- Orquestacion multi-servicio con Docker Compose
- Red privada entre servicios (WordPress encuentra la BD por su nombre "db")
- Base de datos sin puertos expuestos (buena practica de seguridad)
- Persistencia con volumen con nombre (db_data)
- Gestion de secretos mediante .env fuera del control de versiones

---
Autor: Alejandro Quevedo - Ebenezer
