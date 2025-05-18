```markdown
# Genera Videos AUTOMÁTICOS para tu Marketing

## Descripción
Workflow diseñado para crear videos automáticos orientados a marketing de contenido utilizando inteligencia artificial, integración con Google Drive y envío por Gmail, optimizando la creación y distribución de material audiovisual.

## Requisitos
- Credenciales de API para OpenAI (modelo GPT-4)
- Cuenta y credenciales de Google Drive con permisos para crear y subir archivos
- Cuenta Gmail con permisos para enviar correos (SMTP configurado en n8n)
- Acceso a n8n con nodos instalados:  
  `@n8n/n8n-nodes-langchain.lmChatOpenAi`,  
  `@n8n/n8n-nodes-langchain.agent`,  
  `n8n-nodes-base.googleDrive`,  
  `n8n-nodes-base.gmail`,  
  `n8n-nodes-base.if`,  
  `n8n-nodes-base.formTrigger`,  
  `n8n-nodes-base.convertToFile`,  
  `n8n-nodes-base.stickyNote`,  
  `n8n-nodes-base.httpRequest`,  
  `n8n-nodes-base.wait`

## Instrucciones de Configuración
1. Importa el workflow en tu instancia de n8n.
2. Configura las credenciales de OpenAI en el nodo `lmChatOpenAi`.
3. Vincula tu cuenta de Google Drive en el nodo correspondiente para almacenar videos generados.
4. Configura el nodo Gmail con tu cuenta para envío automático de emails.
5. Ajusta los parámetros del nodo `formTrigger` según los inputs que recibirás para la generación de contenido.
6. Revisa y adapta cualquier URL o endpoint que utilice el nodo `httpRequest`.
7. Guarda y activa el workflow.

## Detalles de Funcionamiento
- El flujo se inicia mediante un formulario (`formTrigger`) donde se recibe información para el video.
- Utiliza modelos de lenguaje OpenAI a través de LangChain para generar guiones o textos creativos para los videos.
- Convierte el contenido generado en archivos multimedia mediante nodos de conversión.
- Sube los videos resultantes a Google Drive para almacenamiento y acceso.
- Envía notificaciones o comparte los videos vía Gmail.
- Incluye lógica condicional y pausas controladas para manejo eficiente del proceso.
- Se incorporan stickyNotes para anotaciones internas que facilitan el seguimiento del workflow.

## Ejemplos de Uso
- Automatizar la creación de videos promocionales basados en briefs recibidos por formulario.
- Generar contenido audiovisual personalizado para campañas de email marketing.
- Crear un repositorio centralizado de videos en Google Drive para equipos de marketing.

---

**Número de nodos:** 15  
**Categoría:** marketing/contenido  
**Etiquetas:** _(no asignadas)_
```