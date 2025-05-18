```markdown
# Tool Apertura de ticket

## Descripción
Workflow diseñado para automatizar la apertura de tickets mediante un agente inteligente, integrando procesamiento de lenguaje natural con Gmail para notificaciones y seguimiento.

## Requisitos
- Credenciales de API de OpenAI configuradas para el nodo `@n8n/n8n-nodes-langchain.lmChatOpenAi`.
- Cuenta de Gmail con acceso mediante OAuth para el nodo `n8n-nodes-base.gmailTool`.
- n8n instalado y configurado con los nodos:
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`
  - `n8n-nodes-base.gmailTool`
  - `@n8n/n8n-nodes-langchain.agent`
  - `n8n-nodes-base.set`
  - `n8n-nodes-base.executeWorkflowTrigger`

## Instrucciones de configuración
1. Configure las credenciales de OpenAI en n8n.
2. Autentique la cuenta Gmail en el nodo correspondiente.
3. Importe el workflow en n8n y ajuste las variables necesarias según su entorno.
4. Verifique y active el disparador (`executeWorkflowTrigger`) para iniciar el flujo.

## Detalles de funcionamiento
- El nodo `executeWorkflowTrigger` inicia el workflow bajo demanda.
- `lmChatOpenAi` procesa el lenguaje natural para interpretar solicitudes.
- El agente (`langchain.agent`) analiza y decide acciones a tomar.
- `set` configura variables y estados intermedios.
- `gmailTool` envía notificaciones o confirma la apertura del ticket por correo electrónico.

## Ejemplos de uso
- Un agente recibe una petición vía chat, interpreta la solicitud y crea automáticamente un ticket.
- Envía un correo de confirmación al solicitante informando el número de ticket generado.
- Permite integración con otros sistemas mediante ejecución automática del workflow.

---

**Categoría:** agentes-ia/otros  
**Etiquetas:** Agente, Worker  
**Número de nodos:** 6
```