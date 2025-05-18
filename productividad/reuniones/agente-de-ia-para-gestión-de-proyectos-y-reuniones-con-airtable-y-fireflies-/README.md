```markdown
# Agente de IA para gestión de proyectos y reuniones con Airtable y Fireflies

## Descripción

Workflow diseñado para optimizar la gestión de proyectos y reuniones mediante la integración de Airtable, Fireflies y herramientas inteligentes de IA. Automatiza la captura, seguimiento y análisis de información relevante usando nodos de Langchain, Gmail, Google Calendar y más.

## Requisitos

- Cuenta y credenciales para Airtable (API key y base configurada)
- Cuenta y API de Fireflies para transcripciones y análisis de reuniones
- Credenciales de Gmail para el nodo gmailTool (OAuth)
- Credenciales de Google Calendar (OAuth)
- API key de OpenAI para el nodo lmChatOpenAi
- Acceso configurado a n8n con nodos Langchain instalados

## Instrucciones de configuración

1. Configurar las credenciales en n8n para Airtable, Fireflies, Gmail y Google Calendar.
2. Añadir la API key de OpenAI en el nodo `lmChatOpenAi`.
3. Ajustar las IDs y rutas en los nodos Airtable y Google Calendar según tu estructura.
4. Configurar el webhook para recibir datos de Fireflies o disparar la ejecución del workflow.
5. Personalizar los permisos y triggers según los requerimientos de tu proyecto.

## Detalles de funcionamiento

- El workflow comienza con un trigger HTTP o ejecución manual.
- Recibe datos de reuniones via Fireflies y procesa transcripciones con Langchain.
- Analiza y genera resúmenes de reuniones usando IA.
- Actualiza y consulta bases de datos en Airtable para seguimiento de proyectos.
- Envía notificaciones y resúmenes a través de Gmail.
- Consulta eventos en Google Calendar para coordinar agendas.
- Maneja notas y fragmentos usando nodos stickyNote y splitOut para segmentar información.
- Integra ejecución de workflows adicionales mediante executeWorkflowTrigger para tareas complementarias.

## Ejemplos de uso

- Automatizar el resumen y envío de actas de reuniones a participantes.
- Actualizar estados y fechas en Airtable tras cada reunión.
- Coordinar agendas y enviar recordatorios automáticos desde Google Calendar.
- Extraer insights clave de transcripciones con IA para mejorar la toma de decisiones.

---

**Número de nodos:** 18  
**Categoría:** productividad / reuniones  
**Tipos de nodos:**  
@n8n/n8n-nodes-langchain.lmChatOpenAi,  
@n8n/n8n-nodes-langchain.toolWorkflow,  
n8n-nodes-base.gmailTool,  
@n8n/n8n-nodes-langchain.agent,  
n8n-nodes-base.executeWorkflowTrigger,  
n8n-nodes-base.airtable,  
n8n-nodes-base.stickyNote,  
n8n-nodes-base.splitOut,  
n8n-nodes-base.httpRequest,  
n8n-nodes-base.googleCalendarTool,  
n8n-nodes-base.webhook
```