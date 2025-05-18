```markdown
# T - Programar la subida de Videos a Youtube

## Descripción
Workflow diseñado para automatizar la planificación y subida de videos a YouTube, integrando Google Sheets para el manejo de datos, Google Drive para la gestión de archivos y programación periódica con Schedule Trigger.

## Requisitos
- Credenciales de Google Sheets API con acceso al documento que contiene la programación.
- Credenciales de Google Drive API con acceso a la carpeta donde se almacenan los videos.
- Credenciales de YouTube API para subir videos.
- Configuración del nodo Schedule Trigger para ejecutar el workflow en intervalos deseados.

## Instrucciones de configuración
1. Configure las credenciales de Google en n8n para Google Sheets, Google Drive y YouTube.
2. Prepare una hoja de Google Sheets con la programación de videos: títulos, descripciones, fechas y enlaces a los archivos en Google Drive.
3. Configure el nodo **Schedule Trigger** para activar el workflow según la frecuencia deseada (ej: diariamente).
4. En el nodo Google Sheets, defina la hoja y rango donde se leerán los datos.
5. En el nodo Google Drive, asegúrese del acceso a la carpeta que contiene los archivos de video.
6. Ajuste los parámetros del nodo YouTube para subir el video con la metadata adecuada.

## Detalles de funcionamiento
- El workflow se activa periódicamente mediante el nodo **Schedule Trigger**.
- Consulta Google Sheets para obtener la lista de videos programados para esa fecha.
- Recupera los archivos de video desde Google Drive.
- Sube automáticamente los videos a YouTube con el título, descripción y demás metadatos definidos en Sheets.
- Actualiza la hoja de cálculo con el estado de subida para seguimiento.

## Ejemplos de uso
- Programar lanzamientos semanales de contenido en un canal de YouTube.
- Gestionar múltiples videos desde una única hoja de cálculo para publicación automática.
- Automatizar la carga de videos desde una carpeta compartida en Google Drive sin intervención manual.

---

**Categoría:** productividad/tareas  
**Nodos utilizados:** `n8n-nodes-base.googleSheets`, `n8n-nodes-base.youTube`, `n8n-nodes-base.googleDrive`, `n8n-nodes-base.scheduleTrigger`  
**Número de nodos:** 8  
**Etiquetas:** Youtube
```