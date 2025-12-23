# TaskTracker CLI

**CLI simple para gestión de tareas usando un archivo JSON local.**

---

## Descripción

Proyecto minimalista que proporciona una interfaz de línea de comandos para crear, listar, actualizar y eliminar tareas. Las tareas se almacenan en `tasks.json` en el directorio del proyecto.

## Requisitos

- Python 3.8+
- (Opcional) Un entorno virtual (se incluye uno en `./env` si lo has creado)

## Uso

Ejecuta la CLI con el Python del entorno virtual (o `python3` del sistema):

```bash
./env/bin/python ./tareasCLI <comando> [opciones]
# o
python3 ./tareasCLI <comando> [opciones]
```

Comandos disponibles:

- `add <name> -d <description>` — Crear una tarea
- `update <id> <name> -d <description>` — Actualizar el nombre y/o descripción de una tarea
- `delete <id>` — Eliminar una tarea por id
- `list --status {all,todo,done}` — Listar tareas (por defecto `all`)
- `mark-done <id>` — Marcar una tarea como terminada
- `mark-in-progress <id>` — Marcar una tarea como en progreso

Ejemplo:

```bash
python3 ./tareasCLI add "Comprar pan" -d "Pan integral para el desayuno"
python3 ./tareasCLI list --status all
python3 ./tareasCLI mark-done 1
```

## Contribuir

1. Abrir un issue o un PR con la mejora propuesta.
2. Añadir tests (si procede) y documentar los cambios en el README.

---

Proyecto de roadmap.sh
https://roadmap.sh/projects/task-tracker

Licencia: MIT (añade o ajusta según prefieras)
