# Caso Integrador - Préstamos y Mantenimiento de Equipos

## Comandos para levantar el entorno
- cp .env.ejemplo .env
- Editar .env y definir DB_CLAVE
- docker compose up -d --build

## Variables de entorno (.env)
- DB_CLAVE: 123456

## Operaciones nuevas de la API (/api)
| Método | Ruta | Descripción | Códigos de respuesta |
| :--- | :--- | :--- | :--- |
| GET | /mantenimientos | Lista todos los mantenimientos registrados | 200 OK |
| GET | /equipos/{id}/mantenimientos | Lista los mantenimientos de un equipo | 200 OK, 404 Equipo inexistente |
| POST | /mantenimientos | Registra un nuevo mantenimiento | 201 Creado, 422 Inválido, 400 Costo negativo |

