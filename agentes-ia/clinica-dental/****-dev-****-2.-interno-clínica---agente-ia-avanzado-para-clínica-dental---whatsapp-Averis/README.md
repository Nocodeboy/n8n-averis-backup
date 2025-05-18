```markdown
# **** DEV **** 2. Interno Clínica - Agente IA Avanzado para Clínica Dental - WhatsApp

## Descripción
Workflow diseñado para gestionar la comunicación y reservas de una clínica dental a través de WhatsApp y Telegram, utilizando un agente IA avanzado para brindar respuestas inteligentes y asistidas por memoria persistente.

## Categoría
agentes-ia/clinica-dental

## Requisitos
- Credenciales de OpenAI para el nodo `@n8n/n8n-nodes-langchain.lmChatOpenAi`
- Acceso a base de datos PostgreSQL para `@n8n/n8n-nodes-langchain.memoryPostgresChat`
- Token de Telegram para `n8n-nodes-base.telegramTrigger` y `n8n-nodes-base.telegram`
- Configuración de Google Tasks API para `n8n-nodes-base.googleTasksTool`
- Credenciales para `@n8n/n8n-nodes-langchain.mcpClientTool` (según configuración interna)

## Instrucciones de configuración
1. Configurar las credenciales de OpenAI en n8n.
2. Establecer la conexión a la base de datos PostgreSQL con acceso a la memoria de chat.
3. Obtener y configurar el token de Telegram bot para escuchar y enviar mensajes.
4. Configurar el acceso a Google Tasks para la gestión de bookings y recordatorios.
5. Definir parámetros del agente IA en el nodo `@n8n/n8n-nodes-langchain.agent` según necesidades de la clínica.
6. Implementar y activar el workflow dentro de n8n.

## Detalles de funcionamiento
- El workflow inicia con un trigger desde Telegram.
- El agente IA procesa consultas utilizando OpenAI y maneja herramientas mediante `mcpClientTool` y Google Tasks.
- La memoria de conversación está almacenada en PostgreSQL para mantener contexto en interacciones.
- Se integran respuestas y gestión de booking para la clínica dental vía WhatsApp y Telegram.
- Con un total de 7 nodos, se controla el flujo completo de comunicación y administración.

## Ejemplos de uso
- Un paciente envía un mensaje solicitando turno dental vía Telegram o WhatsApp.
- El agente IA responde con opciones disponibles y confirma la reserva.
- El booking se registra automáticamente en Google Tasks y queda almacenado en la memoria de conversación para seguimiento.
- El personal de la clínica recibe notificaciones y puede interactuar con el paciente mediante el flujo.

---

**Etiquetas:** Averis, Telegram, Clínicas, Booking  
**Número de nodos:** 7
```