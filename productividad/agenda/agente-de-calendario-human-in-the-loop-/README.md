```markdown
# Agente de Calendario Human in the Loop

## Descripción
Workflow diseñado para gestionar y optimizar agendas mediante interacción humana asistida por IA. Integra Telegram, Airtable y Google Calendar para una experiencia productiva y controlada.

## Requisitos
- Credenciales de Telegram (bot y chat ID)
- API Key de OpenAI para `lmChatOpenAi`
- Acceso a Airtable (API Key y base configurada)
- Credenciales de Google Calendar (OAuth2)
- n8n con los nodos instalados:
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`
  - `n8n-nodes-base.telegramTrigger`
  - `n8n-nodes-base.telegram`
  - `n8n-nodes-base.airtableTool`
  - `@n8n/n8n-nodes-langchain.agent`
  - `n8n-nodes-base.set`
  - `@n8n/n8n-nodes-langchain.textClassifier`
  - `n8n-nodes-base.googleCalendarTool`

## Configuración
1. Configure las credenciales de Telegram, OpenAI, Airtable y Google Calendar en n8n.
2. Actualice los IDs y bases de datos en los nodos Airtable y Google Calendar según su entorno.
3. Ajuste parámetros en los nodos de lenguaje y clasificación de texto para adaptarlos a su caso.
4. Importe el workflow y conéctelo a su instancia n8n.

## Funcionamiento
- El trigger de Telegram recibe comandos o mensajes del usuario.
- El agente LangChain procesa la información junto con la clasificación de texto para entender la intención.
- Se consulta y actualiza información en Airtable y Google Calendar.
- En cierto punto, interviene el “human in the loop” para validar o ajustar decisiones antes de confirmar acciones.
- Respuestas y notificaciones se envían de vuelta a través de Telegram.

## Ejemplos de uso
- Gestión colaborativa y aprobada de eventos en el calendario.
- Clasificación y alimentación automática de tareas o citas desde Telegram.
- Supervisión humana en automatización de agenda para evitar errores o conflictos.

---
**Número de nodos:** 16  
**Categoría:** productividad/agenda  
```