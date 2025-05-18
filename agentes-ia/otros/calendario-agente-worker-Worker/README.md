```markdown
# Calendario Agente Worker

## Descripción
Workflow diseñado para gestionar y automatizar tareas relacionadas con calendarios mediante un agente inteligente que interactúa con Google Calendar y utiliza capacidades de lenguaje natural a través de OpenAI.

## Requisitos
- Credenciales de OpenAI configuradas para el nodo `lmChatOpenAi`.
- Acceso autorizado a Google Calendar mediante credenciales OAuth2 en el nodo `googleCalendarTool`.
- n8n instalado con los nodos:
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`
  - `@n8n/n8n-nodes-langchain.agent`
  - `n8n-nodes-base.set`
  - `n8n-nodes-base.executeWorkflowTrigger`
  - `n8n-nodes-base.googleCalendarTool`

## Instrucciones de configuración
1. Importar el workflow en n8n.
2. Configurar las credenciales de OpenAI en el nodo `lmChatOpenAi`.
3. Autorizar y configurar el acceso a Google Calendar en `googleCalendarTool`.
4. Ajustar cualquier parámetro específico del agente en el nodo `agent` según necesidades.
5. Activar el workflow para que responda a los triggers definidos.

## Detalles de funcionamiento
El workflow consta de 10 nodos que trabajan en conjunto para:
- Recibir triggers de ejecución.
- Gestionar las interacciones con el agente LangChain para procesamiento de lenguaje natural.
- Consultar, crear o modificar eventos en Google Calendar.
- Ajustar el flujo y datos mediante nodos `set` para un procesamiento flexible.

## Ejemplos de uso
- Crear un evento en Google Calendar solicitando al agente "Programar reunión para el próximo martes a las 10:00 AM".
- Consultar eventos existentes para una fecha específica vía interacción natural con el agente.
- Automatizar recordatorios o gestión de citas mediante comandos en lenguaje natural.

---
**Categoría:** agentes-ia/otros  
**Etiquetas:** Worker, Agente  
**Nodos utilizados:** 10  
```
