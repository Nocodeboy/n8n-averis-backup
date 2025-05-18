```markdown
# 3. Creador de Post en Linkedin - Equipo de Marketing - Averis Solutions

## Descripción
Workflow diseñado para automatizar la creación y publicación de posts en LinkedIn, optimizado para el equipo de marketing de Averis Solutions. Utiliza IA para generar contenido relevante y conecta con Google Sheets, Google Drive y Telegram para la gestión y notificación.

## Requisitos
- Credenciales de Google Sheets y Google Drive con acceso al archivo y carpeta correspondientes.
- API Key o configuración para el nodo `lmChatOpenRouter` (OpenRouter o similar compatible con Langchain).
- Acceso a la API de Telegram para enviar notificaciones.
- Credenciales para nodos HTTP Request (según configuraciones específicas).
- Configuración de agentes y herramientas Langchain (ej. HttpRequest, outputParserStructured).

## Instrucciones de configuración
1. Importar el workflow en n8n.
2. Configurar credenciales:
   - Google Sheets y Google Drive: registrar y autenticar con OAuth.
   - Telegram: crear un bot y obtener el token API.
   - Langchain nodes: establecer la API Key y parámetros del modelo `lmChatOpenRouter`.
3. Ajustar las rutas y IDs de los archivos o carpetas en Google Drive y Sheets según su entorno.
4. Configurar triggers y condiciones en nodos como `executeWorkflowTrigger` y `stickyNote` para adaptar a las necesidades de publicación.
5. Revisar y ajustar parámetros en nodos de generación y parsing de contenido.

## Detalles de funcionamiento
- El workflow extrae datos desde Google Sheets para obtener inputs o temas de post.
- Genera contenido textual utilizando modelos de lenguaje integrados con Langchain.
- Convierte el contenido generado en archivos almacenados en Google Drive.
- Envía notificaciones vía Telegram para alertar sobre nuevas publicaciones o errores.
- Utiliza nodos HTTP Request y agentes Langchain para enriquecer el contenido y realizar consultas externas si es necesario.
- Integra nodos estructurados para asegurar la correcta interpretación y publicación del contenido en LinkedIn.

## Ejemplos de uso
- Generar automáticamente posts mensuales a partir de un calendario de contenidos registrado en Google Sheets.
- Publicar alertas automáticas en Telegram cuando un post ha sido creado y almacenado correctamente.
- Enriquecer posts incluyendo datos externos usando agentes Langchain con consultas HTTP.
- Mantener un repositorio organizado de posts en Google Drive para revisión y reutilización.

---

**Categoría:** marketing/contenido  
**Número de nodos:** 20  
**Tipos de nodos utilizados:**  
- n8n-nodes-base.googleSheets  
- n8n-nodes-base.googleDrive  
- @n8n/n8n-nodes-langchain.lmChatOpenRouter  
- n8n-nodes-base.convertToFile  
- n8n-nodes-base.telegram  
- @n8n/n8n-nodes-langchain.agent  
- n8n-nodes-base.stickyNote  
- n8n-nodes-base.executeWorkflowTrigger  
- @n8n/n8n-nodes-langchain.toolHttpRequest  
- @n8n/n8n-nodes-langchain.outputParserStructured  
- n8n-nodes-base.httpRequest
```