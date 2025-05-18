```markdown
# Tool Calendario

## Descripción
Workflow diseñado para gestionar y automatizar interacciones con calendarios mediante agentes IA, integrando herramientas de Google Calendar y modelos de lenguaje OpenAI para facilitar la creación, consulta y manejo de eventos.

## Requisitos
- Credenciales de Google Calendar configuradas en n8n.
- API Key de OpenAI para el nodo `lmChatOpenAi`.
- n8n con los nodos: 
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`
  - `@n8n/n8n-nodes-langchain.agent`
  - `n8n-nodes-base.executeWorkflowTrigger`
  - `n8n-nodes-base.set`
  - `n8n-nodes-base.googleCalendarTool`

## Instrucciones de configuración
1. Configura las credenciales de Google Calendar en n8n.
2. Añade tu API Key de OpenAI en el nodo `lmChatOpenAi`.
3. Importa el workflow en tu instancia n8n.
4. Verifica las conexiones y ajusta los parámetros según tus necesidades.

## Detalles de funcionamiento
- El workflow consta de 7 nodos que integran agentes IA con herramientas de calendario.
- Usa `lmChatOpenAi` para gestionar interacciones en lenguaje natural.
- El agente (`agent`) coordina la lógica para interpretar solicitudes y ejecutar acciones.
- El nodo `googleCalendarTool` manipula eventos en Google Calendar.
- `executeWorkflowTrigger` permite activar la automatización mediante eventos externos.
- `set` prepara datos y variables para el flujo.

## Ejemplos de uso
- Crear un evento nuevo en Google Calendar mediante un comando en lenguaje natural.
- Consultar los próximos eventos de la agenda.
- Modificar o cancelar eventos existentes utilizando instrucciones conversacionales.

---

**Categoría:** agentes-ia/otros  
**Etiquetas:** Agente, Worker  
**Número de nodos:** 7
```