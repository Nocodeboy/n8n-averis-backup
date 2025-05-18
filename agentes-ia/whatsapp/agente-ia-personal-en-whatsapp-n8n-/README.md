```markdown
# Agente IA Personal en WhatsApp N8N

## Descripción  
Workflow diseñado para crear un agente de inteligencia artificial personalizado que interactúa vía WhatsApp utilizando n8n. Permite gestionar consultas, realizar búsquedas contextuales, acceder a herramientas externas como Google Calendar, Gmail, Notion y Google Drive, e integrar capacidades avanzadas de procesamiento de lenguaje natural mediante nodos LangChain y OpenAI.

## Requisitos  
- Cuenta y credenciales de **OpenAI** (API Key)  
- Credenciales de **WhatsApp Business API** o integración compatible para los nodos `whatsAppTrigger` y `whatsApp`  
- Accesos OAuth para:  
  - **Google Calendar**  
  - **Gmail**  
  - **Google Drive**  
- Acceso y credenciales a **Notion**  
- Claves y configuración para servicios adicionales:  
  - **Pinecone** (vector DB)  
  - **SerpAPI** (buscador)  
- n8n con soporte para nodos LangChain (versiones compatibles)  

## Instrucciones de configuración  
1. **Importar el workflow** en tu instancia de n8n.  
2. Configurar credenciales para cada servicio indicado en n8n: OpenAI, WhatsApp, Google, Notion, Pinecone y SerpAPI.  
3. Revisar y ajustar los parámetros de los nodos `httpRequest`, `switch` y cualquier parámetro específico de tus cuentas o preferencias.  
4. Activar el workflow para comenzar a recibir y enviar mensajes vía WhatsApp.  

## Detalles de funcionamiento  
- El trigger principal es el nodo `whatsAppTrigger` que recibe mensajes entrantes.  
- Se emplean nodos OpenAI para procesamiento del lenguaje (`openAi`, `lmChatOpenAi`) y generación de respuestas.  
- El texto se fragmenta y vectoriza usando nodos LangChain especializados para mejorar búsqueda semántica.  
- Se integran herramientas externas como Google Calendar, Gmail, Notion y Google Drive para consultas personalizadas.  
- El agente mantiene contexto mediante memoria buffer (`memoryBufferWindow`).  
- Se utiliza Pinecone como vector store para gestionar embeddings y búsquedas.  
- El flujo incluye lógica condicional (`switch`) para direccionar las solicitudes según el contexto y tipo de consulta.  
- El agente puede realizar búsquedas web usando SerpAPI y ejecutar workflows adicionales para casos complejos.  
- Respuestas se envían nuevamente mediante nodo `whatsApp` al usuario final.  

## Ejemplos de uso  
- Solicitar eventos próximos en Google Calendar.  
- Consultar documentos relevantes almacenados en Google Drive o Notion.  
- Enviar y recibir correos electrónicos mediante Gmail.  
- Realizar búsquedas en web contextualizadas sobre un tema particular.  
- Mantener conversaciones dinámicas y contextuales con el agente IA vía WhatsApp.  

---

**Número de nodos:** 34  
**Categoría:** agentes-ia/whatsapp  
**Nodos principales:**  
`@n8n/n8n-nodes-langchain.openAi`, `@n8n/n8n-nodes-langchain.embeddingsOpenAi`, `n8n-nodes-base.notionTool`, `@n8n/n8n-nodes-langchain.textSplitterRecursiveCharacterTextSplitter`, `n8n-nodes-base.httpRequest`, `n8n-nodes-base.whatsAppTrigger`, `n8n-nodes-base.googleCalendarTool`, `@n8n/n8n-nodes-langchain.lmChatOpenAi`, `n8n-nodes-base.switch`, `n8n-nodes-base.whatsApp`, `@n8n/n8n-nodes-langchain.memoryBufferWindow`, `n8n-nodes-base.gmailTool`, `n8n-nodes-base.googleDriveTrigger`, `@n8n/n8n-nodes-langchain.toolVectorStore`, `n8n-nodes-base.googleDrive`, `n8n-nodes-base.manualTrigger`, `@n8n/n8n-nodes-langchain.agent`, `@n8n/n8n-nodes-langchain.documentDefaultDataLoader`, `@n8n/n8n-nodes-langchain.vectorStorePinecone`, `@n8n/n8n-nodes-langchain.toolSerpApi`, `@n8n/n8n-nodes-langchain.toolWorkflow`, `n8n-nodes-base.set`
```