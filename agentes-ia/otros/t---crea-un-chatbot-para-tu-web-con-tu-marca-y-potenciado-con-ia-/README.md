```markdown
# T - Crea un chatbot para tu web con tu marca y potenciado con IA

## Descripción  
Este workflow crea un chatbot personalizado para tu sitio web, potenciado con inteligencia artificial, que responde con el estilo y marca de tu empresa. Utiliza nodos de LangChain para procesamiento avanzado de lenguaje y permite integración con Outlook para gestión de comunicaciones.

## Requisitos  
- Cuenta y credenciales de OpenAI para el nodo `lmChatOpenAi`  
- Credenciales de Microsoft Outlook para nodos relacionados (`microsoftOutlook`)  
- Acceso y configuración de n8n con los nodos LangChain instalados  
- Permisos para ejecutar solicitudes HTTP y responder a webhooks  

## Instrucciones de configuración  
1. Configura las credenciales de OpenAI en n8n.  
2. Añade y autentica tu cuenta de Microsoft Outlook en n8n.  
3. Personaliza el agente LangChain (`agent`) con los detalles de tu marca y preferencias en el nodo `set`.  
4. Ajusta las URLs y parámetros en los nodos `httpRequest` y `toolHttpRequest` según tus endpoints.  
5. Implanta el workflow y conecta el disparador web (`respondToWebhook`) a tu sitio web para recibir consultas.  

## Detalles de funcionamiento  
- El chatbot se activa mediante un webhook web (`respondToWebhook` y `chatTrigger`).  
- Usa el modelo de OpenAI (`lmChatOpenAi`) para procesar y generar respuestas inteligentes.  
- Maneja la memoria conversacional con `memoryBufferWindow`.  
- Toma decisiones y bifurca el flujo con nodos `switch` e `if`.  
- Integra herramientas externas y workflows adicionales mediante `toolWorkflow` y llamadas HTTP.  
- Gestiona comunicaciones y envíos desde Microsoft Outlook.  
- Permite ejecución condicional y manipulación de datos con nodos `code` y `set`.  
- Usa notas adhesivas (`stickyNote`) para referencias internas durante el diseño.  

## Ejemplos de uso  
- Implementar un asistente virtual en la página de soporte para respuestas rápidas y contextualizadas.  
- Automatizar respuestas a consultas frecuentes con enlace a recursos de tu empresa.  
- Integrar gestión de correos y tareas mediante Outlook para seguimiento de interacciones.  

---

**Número de nodos:** 24  
**Categoría:** agentes-ia/otros  
**Nodos utilizados:**  
`@n8n/n8n-nodes-langchain.lmChatOpenAi`, `n8n-nodes-base.switch`, `n8n-nodes-base.microsoftOutlook`, `n8n-nodes-base.if`, `@n8n/n8n-nodes-langchain.memoryBufferWindow`, `n8n-nodes-base.code`, `@n8n/n8n-nodes-langchain.toolWorkflow`, `@n8n/n8n-nodes-langchain.chatTrigger`, `n8n-nodes-base.stickyNote`, `n8n-nodes-base.executeWorkflowTrigger`, `n8n-nodes-base.set`, `@n8n/n8n-nodes-langchain.agent`, `@n8n/n8n-nodes-langchain.toolHttpRequest`, `n8n-nodes-base.httpRequest`, `n8n-nodes-base.respondToWebhook`
```