```markdown
# T - Manage Calendar, Reply to Emails, and Create To-Do Lists via Telegram

## Descripción
Workflow de productividad/agenda que permite gestionar calendarios, responder correos electrónicos y crear listas de tareas directamente desde Telegram. Integra Gmail, Google Calendar, Google Sheets y modelos de lenguaje para una experiencia automatizada y eficiente.

## Requisitos
- Credenciales configuradas para:
  - Telegram Bot (token)
  - Google APIs (Google Sheets, Google Calendar, Gmail)
  - OpenAI API Key (para nodos LangChain OpenAI)
  - Anthropic API Key (para nodo LM Chat Anthropic)
- Acceso a n8n con los nodos instalados mencionados
- Cuenta activa en los servicios utilizados (Google, Telegram, OpenAI, Anthropic)

## Instrucciones de configuración
1. **Telegram**: Crear un bot en Telegram y obtener el token. Configurar el nodo `telegramTrigger` y `telegram` con el token.
2. **Google**: Configurar credenciales OAuth2 para Google Sheets, Google Calendar y Gmail en n8n.
3. **APIs LangChain**:
   - Configurar las credenciales de OpenAI en el nodo `@n8n/n8n-nodes-langchain.openAi`.
   - Configurar la clave de Anthropic en `@n8n/n8n-nodes-langchain.lmChatAnthropic`.
4. Importar el workflow en n8n (22 nodos).
5. Revisar y ajustar configuraciones específicas (ej. IDs de hojas de cálculo, calendarios y filtros de Gmail).
6. Activar el workflow.

## Detalles de funcionamiento
- El nodo `telegramTrigger` escucha comandos y mensajes entrantes desde Telegram.
- Dependiendo del comando, el flujo decide si gestionar eventos en Google Calendar, responder correos usando Gmail y modelos de lenguaje o registrar tareas en Google Sheets.
- Modelos de lenguaje (OpenAI y Anthropic) procesan texto para generar respuestas inteligentes o para clasificar y crear tareas.
- `Switch` determina la ruta correcta según la interacción.
- `ScheduleTrigger` puede usarse para tareas recurrentes (ej. resumen diario).
- El nodo `code` ejecuta lógica personalizada para manipular datos entre servicios.
- Google Sheets funciona como repositorio de tareas y registros.
- Integración completa para automatizar gestión personal desde Telegram.

## Ejemplos de uso
- **Crear un evento:** Enviar mensaje al bot con detalles del evento y se añade al Google Calendar.
- **Responder emails:** El bot analiza correos recientes y crea borradores de respuesta basados en IA.
- **Agregar tareas:** Envía una tarea al bot y se registra automáticamente en la hoja de Google Sheets.
- **Resumen diario:** El workflow puede enviar un resumen de agenda y tareas pendientes al usuario vía Telegram.

---
**Nodos utilizados:**
`@n8n/n8n-nodes-langchain.openAi`, `n8n-nodes-base.googleSheets`, `n8n-nodes-base.switch`, `n8n-nodes-base.telegramTrigger`, `n8n-nodes-base.googleSheetsTool`, `@n8n/n8n-nodes-langchain.lmChatAnthropic`, `n8n-nodes-base.telegram`, `n8n-nodes-base.code`, `n8n-nodes-base.gmailTool`, `@n8n/n8n-nodes-langchain.agent`, `n8n-nodes-base.set`, `n8n-nodes-base.scheduleTrigger`, `n8n-nodes-base.googleCalendarTool`

**Número total de nodos:** 22
```