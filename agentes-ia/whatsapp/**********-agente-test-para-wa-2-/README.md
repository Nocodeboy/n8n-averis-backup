```markdown
# ********** Agente test para WA 2

## Descripción
Workflow diseñado para integrar un agente de inteligencia artificial en WhatsApp utilizando nodos de Langchain y herramientas auxiliares como Google Calendar. Permite gestionar interacciones automatizadas mediante un modelo de lenguaje avanzado.

## Requisitos
- Credenciales de OpenAI para el nodo `@n8n/n8n-nodes-langchain.lmChatOpenAi`
- Configuración del agente Langchain (`@n8n/n8n-nodes-langchain.agent`)
- Acceso a Google Calendar con credenciales API para `n8n-nodes-base.googleCalendarTool`
- n8n configurado para ejecutar workflows disparados (`executeWorkflowTrigger`)

## Instrucciones de configuración
1. Configure las credenciales de OpenAI en n8n.
2. Establezca las credenciales de Google Calendar en n8n.
3. Importe el workflow en n8n.
4. Revise y adapte las conexiones entre nodos según sea necesario.
5. Active el workflow para comenzar a recibir y procesar solicitudes.

## Detalles de funcionamiento
- El workflow consta de 8 nodos que interactúan para procesar mensajes de WhatsApp.
- Utiliza un modelo de lenguaje para generar respuestas inteligentes y ejecutar acciones.
- El nodo `executeWorkflowTrigger` inicia la ejecución con un disparador externo.
- `set` permite configurar variables necesarias durante el flujo.
- La integración con Google Calendar facilita la gestión de eventos y recordatorios desde WhatsApp.

## Ejemplos de uso
- Responder a consultas básicas de usuarios en WhatsApp con información personalizada.
- Crear o consultar eventos en Google Calendar a través de mensajes.
- Ejecutar tareas automatizadas basadas en comandos recibidos por WhatsApp.

---
**Categoría:** agentes-ia/whatsapp  
**Número de nodos:** 8  
**Tipos de nodos:**  
- @n8n/n8n-nodes-langchain.lmChatOpenAi  
- @n8n/n8n-nodes-langchain.agent  
- n8n-nodes-base.executeWorkflowTrigger  
- n8n-nodes-base.set  
- n8n-nodes-base.googleCalendarTool
```