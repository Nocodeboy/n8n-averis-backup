```markdown
# ********** Agente test para WA 🧑‍💻🤖

## Descripción  
Workflow para n8n que implementa un agente inteligente de prueba para WhatsApp, integrando capacidades de IA mediante nodos LangChain y OpenAI. Permite gestionar conversaciones, ejecutar tareas automatizadas y conectar con Google Drive para facilitar interacciones avanzadas en WhatsApp.

## Requisitos  
- Cuenta en OpenAI con clave API válida  
- Credenciales de Google Drive con permisos adecuados  
- Credenciales de WhatsApp (nodo WhatsApp / WhatsApp Trigger configurados)  
- Base de datos PostgreSQL para memoria de chat (configuración de memoryPostgresChat)  
- Acceso a n8n versión compatible con nodos LangChain y nodos base mencionados  

## Instrucciones de configuración  
1. Configure las credenciales de OpenAI en n8n (`@n8n/n8n-nodes-langchain.openAi` y `lmChatOpenAi`).  
2. Establezca las credenciales de Google Drive en n8n para acceso y manipulación de archivos.  
3. Configure el trigger de WhatsApp para recibir mensajes entrantes y asegure conexión activa.  
4. Ajuste la conexión a PostgreSQL para habilitar la memoria de conversación persistente.  
5. Revise y modifique las variables y parámetros en los nodos `set`, `switch` y demás según necesidades específicas.  

## Detalles de funcionamiento  
- El workflow inicia con un trigger de WhatsApp, capturando mensajes entrantes.  
- Se procesan y clasifican inputs mediante nodos `switch` y se envían a los agentes LangChain para respuestas inteligentes.  
- Mediante `chainLlm` y `agent`, se gestionan las interacciones utilizando modelos OpenAI, con memoria gestionada en PostgreSQL.  
- Se conectan herramientas externas y flujos secundarios a través de `toolWorkflow` para ampliar funcionalidades.  
- Archivos relacionados se manejan mediante nodos de Google Drive para consultas o almacenamiento.  
- Se manejan procesos asíncronos y esperas con nodos `wait`, y control granular con `splitInBatches` y `splitOut`.  

## Ejemplos de uso  
- Responder consultas o dudas enviadas a un número de WhatsApp automatizado.  
- Gestionar tareas específicas como búsqueda o descarga de documentos desde Google Drive mediante chat.  
- Registrar y mantener contexto de conversación para agentes conversacionales en WhatsApp.  
- Ejecutar flujos condicionales o personalizados basados en la entrada recibida del usuario.  

---

**Nodos usados:** @n8n/n8n-nodes-langchain.openAi, @n8n/n8n-nodes-langchain.lmChatOpenAi, n8n-nodes-base.switch, n8n-nodes-base.googleDrive, n8n-nodes-base.whatsApp, n8n-nodes-base.noOp, @n8n/n8n-nodes-langchain.chainLlm, @n8n/n8n-nodes-langchain.memoryPostgresChat, @n8n/n8n-nodes-langchain.toolWorkflow, @n8n/n8n-nodes-langchain.agent, n8n-nodes-base.set, n8n-nodes-base.splitOut, n8n-nodes-base.httpRequest, n8n-nodes-base.whatsAppTrigger, n8n-nodes-base.splitInBatches, n8n-nodes-base.wait  
**Número de nodos:** 33  
**Categoría:** agentes-ia/whatsapp  
**Etiquetas:** _(por definir)_  
```