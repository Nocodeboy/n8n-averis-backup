```markdown
# Agente de Calendario con Revisión Humana

## Descripción
Workflow de n8n que integra un agente IA para gestionar eventos de calendario vía Telegram, combinando automatización con revisión humana para confirmar acciones. Ideal para organizar citas y coordinar agendas de forma eficiente.

## Requisitos
- Credenciales de Telegram (Bot API)
- API Key de OpenAI para `lmChatOpenAi`
- Credenciales de Airtable (base y tabla configuradas)
- Credenciales de Google Calendar (API habilitada y autorizada)
- n8n con los nodos:
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`
  - `n8n-nodes-base.telegramTrigger`
  - `n8n-nodes-base.telegram`
  - `n8n-nodes-base.airtableTool`
  - `@n8n/n8n-nodes-langchain.agent`
  - `n8n-nodes-base.set`
  - `@n8n/n8n-nodes-langchain.textClassifier`
  - `n8n-nodes-base.googleCalendarTool`

## Instrucciones de configuración
1. Configure el bot de Telegram y agregue su token en el nodo `telegramTrigger` y `telegram`.
2. Agregue la API Key de OpenAI en el nodo `lmChatOpenAi`.
3. Configure sus credenciales de Airtable para la gestión de datos.
4. Conecte su cuenta de Google Calendar en el nodo `googleCalendarTool`.
5. Ajuste el flujo para adaptar etiquetas, condiciones y mensajes según su caso particular.

## Detalles de funcionamiento
- El workflow escucha mensajes entrantes en Telegram.
- Clasifica el texto recibido para identificar solicitudes relacionadas con el calendario.
- El agente IA elabora respuestas contextuales y propone acciones (crear, modificar o eliminar eventos).
- Antes de ejecutar cambios en Google Calendar, envía una solicitud de revisión humana vía Telegram para confirmar.
- Registra la actividad y detalles en Airtable para seguimiento.
- Una vez aprobado, actualiza el calendario y notifica al usuario.

## Ejemplos de uso
- Usuario envía a Telegram: "Agendar reunión con Juan el viernes a las 3pm".
- El agente interpreta la solicitud y propone crear el evento.
- Usuario confirma o modifica la propuesta.
- Evento creado en Google Calendar y confirmación enviada al usuario.
- Otra función puede ser: "Eliminar la cita del lunes con Ana", que también pasará por revisión antes de la eliminación.

---

**Categoría:** agentes-ia/telegram  
**Etiquetas:** *****, Agente, Telegram  
**Nodos utilizados:** 16
```