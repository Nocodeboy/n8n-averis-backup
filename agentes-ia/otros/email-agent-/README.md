```markdown
# Email agent

## Descripción
Workflow diseñado para gestionar y automatizar interacciones por correo electrónico utilizando agentes de IA. Integra procesamiento inteligente de mensajes y respuestas automáticas mediante modelos de lenguaje avanzados.

## Requisitos
- Credenciales de Google Gmail (OAuth2) para el nodo `gmailTool`.
- API Key de OpenAI para el nodo `lmChatOpenAi`.
- Acceso configurado para los nodos de agente de Langchain (`@n8n/n8n-nodes-langchain.agent`).
- n8n versión compatible con los nodos mencionados.

## Instrucciones de configuración
1. Configure la credencial de Gmail con acceso a la cuenta que gestionará los correos.
2. Ingrese la API Key de OpenAI en el nodo `lmChatOpenAi`.
3. Ajuste los parámetros del agente de Langchain para definir comportamiento y contexto.
4. Importe y conecte el workflow en su instancia de n8n.
5. Habilite el disparador para activar el workflow con nuevos correos o eventos relacionados.

## Detalles de funcionamiento
El workflow consta de 12 nodos que interactúan para:
- Detectar y recibir correos entrantes.
- Procesar el contenido con un agente IA basado en OpenAI.
- Generar respuestas inteligentes y personalizadas.
- Ejecutar acciones adicionales según lógica definida en el agente.
- Enviar respuestas automatizadas por Gmail.
- Registrar o manipular datos intermedios mediante nodos `set` y desencadenadores.

Se utilizan los siguientes tipos de nodos:
- `@n8n/n8n-nodes-langchain.lmChatOpenAi`
- `n8n-nodes-base.gmailTool`
- `@n8n/n8n-nodes-langchain.agent`
- `n8n-nodes-base.set`
- `n8n-nodes-base.executeWorkflowTrigger`

## Ejemplos de uso
- Responder automáticamente correos con consultas frecuentes.
- Filtrar y clasificar correos usando IA antes de la gestión manual.
- Integrar agentes para asistencia personalizada vía email.
- Automatizar workflows complejos basados en contenido de mensajes recibidos.

---
Categoría: agentes-ia/otros  
Nodos totales: 12
```