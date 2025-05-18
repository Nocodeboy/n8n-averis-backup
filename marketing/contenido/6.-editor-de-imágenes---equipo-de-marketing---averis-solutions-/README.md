```markdown
# 6. Editor de Imágenes - Equipo de Marketing - Averis Solutions

## Descripción
Workflow diseñado para el equipo de marketing que automatiza la edición y gestión de imágenes utilizando Google Sheets, Google Drive y canales de comunicación como Telegram. Facilita la captura, conversión y distribución de contenido visual de manera eficiente.

## Requisitos
- Credenciales de Google Sheets (para acceder y modificar hojas de cálculo)
- Credenciales de Google Drive (para gestionar archivos en la nube)
- Token/API de Telegram (para enviar notificaciones o imágenes)
- Acceso a n8n con los nodos utilizados instalados

## Instrucciones de configuración
1. Configure las credenciales en n8n para Google Sheets, Google Drive y Telegram.
2. En Google Sheets, prepare la hoja con los datos de imágenes a procesar.
3. En Google Drive, cree la carpeta destino para almacenar imágenes editadas.
4. Actualice el nodo HTTP Request con la URL o API de edición de imágenes si es necesario.
5. Configure el workflow para iniciar mediante el nodo Execute Workflow Trigger.
6. Ajuste los parámetros de los nodos Sticky Note para notas o instrucciones internas.

## Detalles de funcionamiento
- El workflow se activa manualmente o mediante trigger definido.
- Obtiene datos desde Google Sheets para identificar imágenes y parámetros a procesar.
- Descarga y convierte archivos usando nodos ConvertToFile y HTTP Request para aplicar edición.
- Guarda las imágenes procesadas en Google Drive para acceso posterior.
- Envía notificaciones o los resultados al canal Telegram configurado.
- Utiliza Sticky Notes para documentar estados o comentarios dentro del flujo.
- Total de nodos utilizados: 12.

## Ejemplos de uso
- Actualizar campañas visuales con imágenes procesadas automáticamente según planilla de diseño.
- Distribuir imágenes editadas al equipo vía Telegram para revisión rápida.
- Centralizar asesoría y notas internas relacionadas con el contenido visual mediante Sticky Notes.
```
