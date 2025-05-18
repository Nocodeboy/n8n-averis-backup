```markdown
# Calendar agent

## Descripción  
Workflow orientado a productividad y gestión de agenda que utiliza inteligencia artificial para interactuar y gestionar eventos de Google Calendar de forma automática y eficiente.

## Requisitos  
- Cuenta de Google con acceso a Google Calendar API  
- Credenciales configuradas para `n8n-nodes-base.googleCalendarTool`  
- API key o credenciales para OpenAI (utilizados en `@n8n/n8n-nodes-langchain.lmChatOpenAi`)  
- Configuración del agente LangChain (`@n8n/n8n-nodes-langchain.agent`)

## Instrucciones de configuración  
1. Configure las credenciales de Google Calendar en n8n.  
2. Añada las credenciales de OpenAI para el nodo `lmChatOpenAi`.  
3. Importe el workflow en n8n y verifique que los nodos estén conectados correctamente.  
4. Ajuste los parámetros del workflow según sus necesidades.  

## Detalles de funcionamiento  
Este workflow consta de 10 nodos, incluyendo:  
- `executeWorkflowTrigger`: Punto de entrada del flujo.  
- `set`: Nodo para configurar variables o parámetros iniciales.  
- `lmChatOpenAi`: Procesa solicitudes y genera respuestas inteligentes con OpenAI.  
- `agent`: Controla la lógica del agente LangChain para la toma de decisiones automatizada.  
- `googleCalendarTool`: Interactúa con Google Calendar para crear, modificar o consultar eventos.  

El agente interpreta las solicitudes de gestión de eventos, consulta el calendario, y ejecuta acciones como agregar, editar o eliminar citas.

## Ejemplos de uso  
- "Agrega una reunión con el equipo el próximo martes a las 10 AM."  
- "¿Qué eventos tengo programados para esta semana?"  
- "Cancela mi cita del jueves a las 3 PM en el calendario."  

---

*Categoría:* productividad/agenda  
*Número de nodos:* 10  
```