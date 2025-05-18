```markdown
# 5. Creador de Imágenes - Equipo de Marketing - Averis Solutions

## Descripción
Workflow orientado a la creación automatizada de imágenes para campañas de marketing, integrando generación de contenido, gestión de archivos y notificaciones a través de múltiples servicios como Google Sheets, Google Drive, Telegram y tecnologías de lenguaje avanzado.

## Requisitos

- Credenciales configuradas para:
  - Google Sheets
  - Google Drive
  - Telegram Bot API
- Acceso a la API OpenRouter para modelos de lenguaje (nodo lmChatOpenRouter)
- Permisos para ejecutar workflows en n8n y manejar solicitudes HTTP externas

## Instrucciones de configuración

1. **Google Sheets & Drive:** Configure y autentique sus credenciales en n8n para Google Sheets y Google Drive, asegurando acceso a las hojas y carpetas necesarias.
2. **Telegram:** Cree un bot en Telegram, obtenga el token y configúrelo en n8n para recibir y enviar mensajes.
3. **OpenRouter:** Obtenga la clave API de OpenRouter y configúrela en el nodo lmChatOpenRouter.
4. Importe el workflow en su instancia n8n.
5. Ajuste las hojas de Google Sheets y carpetas en Google Drive según su estructura.
6. Configure triggers y parámetros según sus necesidades específicas.

## Detalles de funcionamiento

- El workflow inicia con la activación mediante `executeWorkflowTrigger`.
- Consulta Google Sheets para obtener datos e instrucciones de imagen.
- Utiliza `lmChatOpenRouter` y `agent` para procesar prompts y generar descripciones o solicitudes para creación de imágenes.
- Convierte contenido generado a archivos con `convertToFile`.
- Guarda archivos y recursos relacionados en Google Drive.
- Envía notificaciones y actualizaciones a través del nodo Telegram.
- Usa `stickyNote` para anotaciones rápidas dentro del flujo.
- Realiza llamadas HTTP con `httpRequest` para integraciones adicionales o validaciones externas.

## Ejemplos de uso

- Generación automática de imágenes promocionales a partir de briefs almacenados en Google Sheets.
- Notificación al equipo de marketing en Telegram cada vez que una imagen es creada y almacenada.
- Anotaciones rápidas sobre versiones o feedback utilizando notas adhesivas digitales dentro del flujo de n8n.

---

**Número de nodos:** 14  
**Categoría:** marketing/contenido  
**Nodos utilizados:**  
- n8n-nodes-base.googleSheets  
- n8n-nodes-base.googleDrive  
- @n8n/n8n-nodes-langchain.lmChatOpenRouter  
- n8n-nodes-base.convertToFile  
- n8n-nodes-base.telegram  
- @n8n/n8n-nodes-langchain.agent  
- n8n-nodes-base.executeWorkflowTrigger  
- n8n-nodes-base.stickyNote  
- n8n-nodes-base.httpRequest
```