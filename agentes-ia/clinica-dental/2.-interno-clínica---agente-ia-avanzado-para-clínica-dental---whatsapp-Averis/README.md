```markdown
# 2. Interno Clínica - Agente IA Avanzado para Clínica Dental - WhatsApp

## Descripción  
Workflow diseñado para gestionar interacciones internas en clínicas dentales a través de WhatsApp y Telegram, utilizando un agente IA avanzado que facilita la gestión de citas, consultas y recordatorios automatizados.

## Requisitos  
- Credenciales de OpenAI (para `lmChatOpenAi`)  
- Acceso a MCP Client Tool (para `mcpClientTool`)  
- Base de datos PostgreSQL configurada para `memoryPostgresChat` (memoria conversacional)  
- Token de bot de Telegram (para `telegramTrigger` y `telegram`)  
- Credenciales de Google para Google Tasks API (para `googleTasksTool`)  

## Instrucciones de configuración  
1. Configure las credenciales de OpenAI y MCP Client en n8n.  
2. Prepare y conecte su base de datos PostgreSQL para almacenar el contexto de conversación.  
3. Configure el bot de Telegram con el token correcto, asegurándose que el bot esté activo y con permisos.  
4. Configure el acceso a Google Tasks para gestión de tareas y recordatorios.  
5. Importe el workflow en su instancia de n8n y asigne las credenciales correspondientes a cada nodo.  

## Detalles de funcionamiento  
- El flujo inicia con un disparador de Telegram (`telegramTrigger`) que recibe mensajes de los agentes o personal de la clínica.  
- Utiliza `lmChatOpenAi` para generar respuestas inteligentes basadas en el contexto previo almacenado en `memoryPostgresChat`.  
- El agente IA (`agent`) coordina acciones como respuesta al usuario y gestión de tareas.  
- Herramientas adicionales como `mcpClientTool` y `googleTasksTool` permiten integrar funcionalidades específicas para la clínica dental, incluyendo recordatorio y booking.  
- La comunicación se devuelve a través de Telegram, cerrando el ciclo de interacción en tiempo real.  

## Ejemplos de uso  
- Un agente interno recibe un mensaje en Telegram de un paciente solicitando una cita.  
- El agente IA procesa el mensaje, verifica disponibilidad y crea una tarea en Google Tasks para el equipo.  
- Se envía confirmación automática al agente o personal responsable vía Telegram.  
- El historial de conversación se guarda para mantener el contexto en interacciones futuras.

---

**Categoría:** agentes-ia/clinica-dental  
**Etiquetas:** Averis, Clínicas, Booking, Telegram  
**Número de nodos:** 7  
**Tipos de nodos:**  
- @n8n/n8n-nodes-langchain.lmChatOpenAi  
- @n8n/n8n-nodes-langchain.mcpClientTool  
- n8n-nodes-base.telegramTrigger  
- @n8n/n8n-nodes-langchain.memoryPostgresChat  
- n8n-nodes-base.telegram  
- @n8n/n8n-nodes-langchain.agent  
- n8n-nodes-base.googleTasksTool  
```