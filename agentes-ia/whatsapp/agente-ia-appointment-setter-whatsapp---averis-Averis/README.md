```markdown
# Agente IA Appointment Setter WhatsApp - Averis

## Descripción

Workflow de n8n diseñado como un agente inteligente para gestionar y automatizar la programación de citas vía WhatsApp para Averis. Utiliza capacidades de IA para interpretar mensajes, gestionar calendarios y responder de forma dinámica a los usuarios.

## Requisitos

- Credenciales de WhatsApp (Webhook configurado para recibir mensajes)
- API Key de OpenAI para nodos `@n8n/n8n-nodes-langchain.openAi` y `@n8n/n8n-nodes-langchain.lmChatOpenAi`
- Credenciales de Google Calendar para gestionar eventos y citas
- Credenciales de Gmail para notificaciones y comunicaciones adicionales
- Acceso a Redis para manejo de memoria y estados (`n8n-nodes-base.redis`)
- Google Sheets API (opcional para gestión de datos de citas)
- Configuración de Webhook en n8n para recibir mensajes entrantes

## Instrucciones de configuración

1. Configure el webhook de WhatsApp para redirigir mensajes entrantes al nodo webhook del workflow.
2. Añada las credenciales API de OpenAI en n8n.
3. Configure Google Calendar y Gmail con sus respectivas credenciales en n8n.
4. Establezca conexión con Redis para manejo de memoria persistente.
5. (Opcional) Configure Google Sheets si se requiere registro o gestión de datos adicionales.
6. Verifique y ajuste las reglas y condiciones en nodos switch e if para adaptar el flujo a necesidades específicas.

## Detalles de funcionamiento

- El webhook recibe mensajes de WhatsApp y los envía a los nodos de procesamiento de lenguaje natural basados en OpenAI.
- El agente interpreta el mensaje y determina la intención, utilizando nodos como `agent`, `lmChatOpenAi` y parsers estructurados.
- Se verifican disponibilidades de calendario mediante Google Calendar y se gestionan citas automáticamente.
- Las respuestas generadas se envían de vuelta a través de WhatsApp.
- Se implementan nodos de control de flujo (`switch`, `if`, `merge`, `wait`) para manejar distintos escenarios y esperar confirmaciones.
- La memoria buffer y almacenamiento en Redis permiten mantener contexto durante la conversación.
- Se utilizan nodos auxiliares para manejo de archivos, notas, y organización de datos (Google Sheets, stickyNote, convertToFile).

## Ejemplos de uso

- Usuario envía mensaje por WhatsApp solicitando agendar una cita: el agente responde proponiendo fechas disponibles y gestiona la creación del evento en Google Calendar.
- Confirmación o cambio de cita: el agente procesa la solicitud, actualiza el calendario y notifica al usuario.
- Seguimiento automatizado mediante Gmail para recordar citas próximas o enviar información adicional.

---

**Categoría:** agentes-ia/whatsapp  
**Etiquetas:** Averis, Agente, Whatsapp  
**Nodos utilizados:** 49  
```