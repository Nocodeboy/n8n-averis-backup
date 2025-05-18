```markdown
# Agente para WhatsApp Clínica - Base

## Descripción  
Workflow diseñado para gestionar interacciones vía WhatsApp en una clínica dental, integrando agentes IA para brindar respuestas inteligentes, manejo de tareas y coordinación mediante Telegram y otras herramientas conectadas.

## Requisitos  
- Credenciales de OpenAI para nodos Langchain (`openAi`, `lmChatOpenAi`)  
- Acceso y configuración de MCP (Medical Care Provider) vía `mcpClientTool`  
- Base de datos PostgreSQL para almacenamiento de memoria (`memoryPostgresChat`)  
- Configuración de Webhook para recepción de mensajes WhatsApp  
- Credenciales para API de Telegram (bot y trigger)  
- Acceso a API Evolution (para funcionalidades específicas)  
- Permisos y credenciales para Google Tasks (gestión de tareas)  

## Instrucciones de configuración  
1. Configure las credenciales de OpenAI en n8n.  
2. Configure credenciales MCP para el nodo `mcpClientTool`.  
3. Establezca la conexión a PostgreSQL para el nodo de memoria.  
4. Configure el webhook público para recibir mensajes de WhatsApp.  
5. Configure el bot y trigger de Telegram con las credenciales correspondientes.  
6. Añada credenciales para Evolution API y Google Tasks.  
7. Revise y ajuste los parámetros del agente y las herramientas según las necesidades clínicas.

## Detalles de funcionamiento  
- El workflow inicia con triggers en WhatsApp y Telegram para captar mensajes.  
- Se utiliza el agente IA basado en Langchain para procesar y responder consultas.  
- El nodo Switch determina el flujo según el tipo de mensaje o acción requerida.  
- Las respuestas y tareas se manejan mediante nodos específicos (`googleTasksTool`, `telegramTool`).  
- La memoria del chat se mantiene en PostgreSQL para contextos persistentes.  
- Herramientas adicionales y workflows se enlazan para funcionalidades extendidas.  
- Se programan acciones automáticas con nodos de scheduleTrigger para recordatorios o seguimiento.

## Ejemplos de uso  
- Paciente envía consulta por WhatsApp → agente IA responde con horarios y disponibilidad.  
- Solicitud de recordatorio para cita dental → se crea tarea en Google Tasks y se notifica por Telegram.  
- Coordinación interna mediante notas adhesivas (`stickyNote`) para seguimiento administrativo.  
- Actualización automática de estados o respuestas según evolución de la interacción.

---

**Categoría:** agentes-ia/clinica-dental  
**Etiquetas:** Base, MCP  
**Nodos utilizados:** 38 (incluye nodos OpenAI, Telegram, Switch, Webhook, Evolution API, Google Tasks, entre otros)  
```