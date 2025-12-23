# TaskTracker CLI

**CLI simple para gestión de tareas usando un archivo JSON local.**

---

## 🧭 Descripción

Proyecto minimalista que proporciona una interfaz de línea de comandos para crear, listar, actualizar y eliminar tareas. Las tareas se almacenan en `tasks.json` en el directorio del proyecto.

## ✅ Requisitos

- Python 3.8+
- (Opcional) Un entorno virtual (se incluye uno en `./env` si lo has creado)

## ⚙️ Instalación

1. Crear y activar un entorno virtual (opcional pero recomendado):

```bash
python3 -m venv env
source env/bin/activate
```

2. Instalar dependencias (si fuera necesario):

```bash
pip install -r requirements.txt
```

> Nota: este proyecto utiliza `click` y no requiere un `setup.py` para usar la CLI directamente mediante `python ./tareasCLI`.

## 🚀 Uso

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

## 🧪 Script de pruebas

Hay un script `add_test_tasks.sh` que limpia `tasks.json`, añade 10 tareas de prueba y muestra el listado:

```bash
bash add_test_tasks.sh
```

## 📝 Notas y mejoras propuestas

- Actualmente la CLI solo admite `name` y `--description`. No hay flags para prioridad, fecha de vencimiento o etiquetas (puedo añadirlos si quieres).
- Se muestra un DeprecationWarning por `datetime.utcnow()`. Se recomienda cambiar a objetos timezone-aware (`datetime.now(timezone.utc)`), puedo aplicar el cambio.

## 🤝 Contribuir

1. Abrir un issue o un PR con la mejora propuesta.
2. Añadir tests (si procede) y documentar los cambios en el README.

---

Licencia: MIT (añade o ajusta según prefieras)
