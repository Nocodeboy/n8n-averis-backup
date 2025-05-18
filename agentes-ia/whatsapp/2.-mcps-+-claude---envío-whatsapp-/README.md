```markdown
# 2. MCPs + Claude - Envío WhatsApp

## Descripción
Workflow diseñado para integrar múltiples modelos de procesamiento cognitivo (MCPs) junto con Claude, facilitando el envío automatizado de mensajes a través de WhatsApp.

## Requisitos
- Cuenta de n8n con permisos para importar y ejecutar workflows.
- Credenciales configuradas para:
  - API de OpenAI (usada por el nodo `@n8n/n8n-nodes-langchain.openAi`).
  - API de Evolution (usada por el nodo `n8n-nodes-evolution-api.evolutionApi`).
  - Acceso a WhatsApp Business API o servicio compatible para envío de mensajes.
- Nodo `n8n-nodes-base.executeWorkflowTrigger` disponible.
- Configuración de credenciales para nodos base (`set`).

## Instrucciones de configuración
1. Importa el workflow en n8n.
2. Añade y configura las credenciales necesarias para OpenAI y Evolution API en n8n.
3. Ajusta el webhook o trigger en el nodo `executeWorkflowTrigger` según el punto de entrada deseado.
4. Configura el nodo `set` para parametrizar datos específicos del mensaje o destinatario.
5. Asegúrate que las integraciones para envío por WhatsApp están correctamente configuradas y activas.

## Detalles de funcionamiento
- El workflow inicia mediante un trigger (`executeWorkflowTrigger`).
- Utiliza los modelos de OpenAI y Evolution API para procesar y generar contenido inteligente a través de los nodos correspondientes.
- El nodo `set` prepara los datos y parámetros para el mensaje.
- Finalmente, el flujo realiza el envío del mensaje a través de la integración de WhatsApp configurada.

## Ejemplos de uso
- Envío automático de respuestas inteligentes basadas en análisis de múltiples modelos cognitivos.
- Notificaciones personalizadas vía WhatsApp utilizando la combinación de Claude y MCPs.
- Automatización de comunicaciones para atención al cliente con soporte IA híbrida.

---

**Categoría:** agentes-ia/whatsapp  
**Tipos de nodos utilizados:**  
- n8n-nodes-base.executeWorkflowTrigger  
- @n8n/n8n-nodes-langchain.openAi  
- n8n-nodes-evolution-api.evolutionApi  
- n8n-nodes-base.set  

**Número de nodos:** 4
```