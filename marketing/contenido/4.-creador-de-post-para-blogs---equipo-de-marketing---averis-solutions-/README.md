```markdown
# 4. Creador de Post para Blogs - Equipo de Marketing - Averis Solutions

## Descripción
Workflow diseñado para automatizar la creación de posts para blogs del equipo de marketing de Averis Solutions. Integra Google Sheets y Google Drive para la gestión de datos, utiliza modelos de lenguaje mediante Langchain para generación de contenido creativo y coherente, y envía notificaciones vía Telegram para seguimiento.

## Requisitos
- Credenciales activas para:
  - Google Sheets API
  - Google Drive API
  - Telegram Bot API
- Acceso a Langchain con tokens para:
  - lmChatOpenRouter
  - Langchain Agents y herramientas HTTP Request
- Acceso a n8n con nodos mencionados instalados y habilitados

## Instrucciones de configuración
1. Configure las credenciales de Google Sheets y Google Drive en n8n.
2. Ingrese el token API necesario para Langchain (lmChatOpenRouter y agentes).
3. Configure el token de Telegram Bot para enviar mensajes.
4. Ajuste los IDs de hojas de Google Sheets y carpetas en Google Drive según el entorno.
5. Importe este workflow en su instancia n8n y conecte las credenciales configuradas.

## Detalles de funcionamiento
- Lee datos de fuentes estructuradas en Google Sheets.
- Genera contenido de blog mediante el modelo conversacional lmChatOpenRouter.
- Utiliza agentes Langchain para incorporar información externa vía HTTP Request.
- Convierte el contenido en archivos mediante `convertToFile` y los guarda en Google Drive.
- Envía notificaciones y resúmenes vía Telegram para seguimiento del equipo.
- Utiliza notas adhesivas (stickyNote) para comentarios internos y marca puntos clave.
- Ejecuta flujos secundarios mediante nodos `executeWorkflowTrigger` para modularidad.

## Ejemplos de uso
- Automatización semanal de creación de posts a partir de inputs en Google Sheets.
- Generación de contenido personalizado según temas definidos por el equipo.
- Notificación instantánea en Telegram cuando un nuevo post está listo para revisión.
- Integración con tareas externas usando agentes Langchain para enriquecer el contenido.

---

**Categoría:** marketing/contenido  
**Nodos utilizados:** 20 (googleSheets, googleDrive, lmChatOpenRouter, convertToFile, telegram, agent, stickyNote, executeWorkflowTrigger, toolHttpRequest, outputParserStructured, httpRequest)  
**Etiquetas:** _(ninguna)_
```