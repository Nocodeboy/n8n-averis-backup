```markdown
# My workflow 3

## Descripción  
Workflow para agentes IA integrados con Telegram que combina diversas herramientas de LangChain y nodos base de n8n para gestionar consultas, acciones en calendarios, correo y búsquedas en Wikipedia y SERP API.

## Requisitos  
- Credenciales de Telegram (bot y usuario)  
- API Key de OpenAI  
- API Key de SerpApi  
- Credenciales de Gmail (acceso con permisos para enviar correos)  
- Credenciales de Google Calendar  
- Acceso a servicios de LangChain configurados en n8n  

## Instrucciones de configuración  
1. Configure en n8n las credenciales de Telegram, OpenAI, SerpApi, Gmail y Google Calendar.  
2. Importe el workflow "My workflow 3" en su instancia n8n.  
3. Ajuste parámetros específicos en nodos como @n8n/n8n-nodes-langchain.openAi y @n8n/n8n-nodes-langchain.toolSerpApi con sus claves API.  
4. Establezca las reglas deseadas en el nodo switch para direccionar el flujo según los inputs recibidos.  
5. Guarde y active el workflow.

## Detalles de funcionamiento  
- El flujo inicia con un trigger de Telegram que recibe mensajes del usuario.  
- Según la intención detectada, el nodo switch dirige la ejecución a distintas herramientas: búsqueda en Wikipedia, búsqueda con SERP API, manejo de agendas con Google Calendar, envío de correos con Gmail, o procesamiento con modelos OpenAI.  
- Se utiliza memoria buffer para mantener el contexto en conversaciones.  
- Los agentes LangChain gestionan llamadas a APIs externas con soporte para chat y generación de texto.  
- Respuestas y acciones se envían de vuelta vía Telegram y otros nodos cuando corresponde.  
- En total el workflow consta de 16 nodos interrelacionados para cubrir distintos casos de uso.

## Ejemplos de uso  
- Usuario pregunta por información en Wikipedia → respuesta detallada con extracción de contenido.  
- Solicita agendar un evento → se crea un evento en Google Calendar y se confirma por Telegram.  
- Consulta sobre resultados en buscadores → se responde con datos actuales obtenidos vía SerpApi.  
- Recibe notificaciones de correo o envía mensajes personalizados por Gmail desde Telegram.  
- Interacción dinámica y contextual con modelos OpenAI para consultas complejas.

---

*Categoría*: agentes-ia/telegram  
*Número de nodos*: 16  
*Nodos utilizados*:  
`@n8n/n8n-nodes-langchain.openAi`,  
`@n8n/n8n-nodes-langchain.lmChatOpenAi`,  
`n8n-nodes-base.telegramTrigger`,  
`n8n-nodes-base.switch`,  
`@n8n/n8n-nodes-langchain.toolSerpApi`,  
`@n8n/n8n-nodes-langchain.memoryBufferWindow`,  
`n8n-nodes-base.telegram`,  
`n8n-nodes-base.gmailTool`,  
`@n8n/n8n-nodes-langchain.agent`,  
`n8n-nodes-base.set`,  
`@n8n/n8n-nodes-langchain.toolWikipedia`,  
`n8n-nodes-base.googleCalendarTool`
```