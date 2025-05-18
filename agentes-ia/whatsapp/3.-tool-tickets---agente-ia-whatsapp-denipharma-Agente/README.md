```markdown
# 3. Tool Tickets - Agente IA WhatsApp Denipharma

## Descripción  
Workflow diseñado para gestionar tickets utilizando un agente de inteligencia artificial integrado con WhatsApp para Denipharma. Este agente utiliza capacidades de lenguaje natural para interactuar y procesar solicitudes recibidas, además de enviar notificaciones vía Gmail.

## Requisitos  
- Credenciales de OpenAI configuradas para el nodo `lmChatOpenAi`  
- Cuenta y permisos de Gmail para el nodo `gmailTool`  
- Acceso a n8n con permisos para ejecutar workflows y nodos personalizados  
- Configuración previa del agente LangChain (`agent`) compatible con los flujos de tickets  

## Instrucciones de configuración  
1. Configure las credenciales OpenAI en n8n (`lmChatOpenAi`).  
2. Autentique el nodo `gmailTool` con su cuenta Gmail.  
3. Ajuste el nodo `agent` según los parámetros específicos del flujo de interacción de tickets.  
4. Verifique que el nodo `executeWorkflowTrigger` esté apuntando al workflow deseado si se encadena con otros flujos.  

## Detalles de funcionamiento  
- El workflow inicia con un trigger que puede ser activado por eventos externos o flujos internos.  
- Se procesan los mensajes recibidos a través del agente AI (`lmChatOpenAi` + `agent`), interpretando las solicitudes de tickets.  
- Se utilizan nodos de configuración (`set`) para definir y manipular datos específicos del ticket.  
- El nodo Gmail envía notificaciones o respuestas relacionadas con el estado del ticket.  
- En total, el flujo utiliza 6 nodos para orquestar la interacción completa.  

## Ejemplos de uso  
- Un cliente envía una consulta por WhatsApp sobre un producto Denipharma.  
- El agente IA interpreta la consulta, genera un ticket y notifica al equipo vía Gmail.  
- Se puede activar un workflow secundario para seguimiento automático de tickets mediante el nodo trigger.  

---

**Categoría:** agentes-ia/whatsapp  
**Etiquetas:** Agente, Worker  
**Nodos utilizados:**  
- `@n8n/n8n-nodes-langchain.lmChatOpenAi`  
- `n8n-nodes-base.gmailTool`  
- `@n8n/n8n-nodes-langchain.agent`  
- `n8n-nodes-base.set`  
- `n8n-nodes-base.executeWorkflowTrigger`  
```