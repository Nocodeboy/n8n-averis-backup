```markdown
# Automated daily workflow backup to GitHub

## Descripción
Este workflow automatiza la creación diaria de una copia de seguridad de tus datos y configuraciones, almacenándola directamente en un repositorio de GitHub. Ideal para mantener respaldos constantes sin intervención manual.

## Requisitos
- Cuenta y repositorio activo en GitHub con permisos para crear y actualizar archivos.
- Credenciales de GitHub configuradas en n8n (token con acceso a repositorios).
- n8n corriendo en una instancia con acceso a internet para interactuar con GitHub.

## Instrucciones de configuración
1. Obtener un [Personal Access Token](https://github.com/settings/tokens) en GitHub con permisos `repo`.
2. Agregar las credenciales de GitHub en n8n (Ajustes > Credenciales > GitHub).
3. Configurar el nodo **Schedule Trigger** para definir la hora a la que se realizará el backup diario.
4. Ajustar el repositorio, ruta y nombre de archivo en el nodo **GitHub** según tus preferencias.
5. Guardar y activar el workflow en n8n.

## Detalles de funcionamiento
- El workflow se activa diariamente mediante el nodo `scheduleTrigger`.
- Extrae y agrega datos relevantes con los nodos `extractFromFile`, `aggregate` y `set`.
- Convierte la información en un archivo con `convertToFile`.
- Evalúa condiciones con `if` para determinar acciones específicas.
- Guarda o actualiza el archivo de backup en el repositorio de GitHub usando el nodo `github`.
- El nodo `stickyNote` se utiliza para documentación interna y aclaraciones.
- Total de nodos: 13.

## Ejemplos de uso
- Respaldo automático de configuraciones o registros generados en otros workflows.
- Almacenamiento diario de logs o informes en GitHub para auditoría.
- Automatización de backups sin necesidad de intervenciones manuales ni scripts externos.

---
Categoría: utilidades/backup  
Etiquetas: (ninguna)
```