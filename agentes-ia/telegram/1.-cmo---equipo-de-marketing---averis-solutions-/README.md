```markdown
# 1. CMO - Equipo de Marketing - Averis Solutions

## Descripción
Workflow diseñado para el equipo de marketing de Averis Solutions que integra agentes IA y Telegram para automatizar interacciones, gestión de consultas y procesos de comunicación efectivos usando nodos de Langchain y Telegram.

## Requisitos
- Credenciales de OpenAI configuradas en n8n (`@n8n/n8n-nodes-langchain.openAi`)
- Cuenta y API de Telegram para el bot (Telegram Trigger y Telegram nodes)
- Configuración de Langchain (OpenRouter, agent, memory, tools)
- Acceso a n8n con permisos para configurar workflows y credenciales

## Instrucciones de configuración
1. Configure las credenciales de Telegram con el token del bot en n8n.
2. Añada las credenciales de OpenAI en n8n (API Key).
3. Asegure que las configuraciones de Langchain (OpenRouter, memory buffer, agentes y herramientas) estén correctamente vinculadas con sus respectivas credenciales.
4. Importe el workflow en n8n y verifique que los 24 nodos estén conectados correctamente.
5. Ajuste cualquier parámetro específico según la operación del equipo de marketing.

## Detalles de funcionamiento
- El workflow inicia con un `telegramTrigger` que escucha mensajes entrantes.
- Usa nodos Langchain, incluyendo `openAi`, `lmChatOpenRouter` y agentes para generar respuestas inteligentes.
- Implementa lógica condicional con nodos `switch`.
- Maneja memoria conversacional mediante `memoryBufferWindow` para mantener contexto.
- Herramientas integradas permiten extender funcionalidades mediante `toolWorkflow` y procesos internos de pensamiento (`toolThink`).
- Mensajes y respuestas se envían y gestionan vía nodos de Telegram.
- Notas adhesivas (`stickyNote`) y nodos `set` se utilizan para almacenamiento temporal y configuración interna.

## Ejemplos de uso
- Responder consultas de clientes del equipo de marketing directamente desde Telegram con respuestas generadas por IA.
- Automatización de tareas y recordatorios internos usando interacción por chat.
- Soporte en generación y gestión de contenido para campañas gracias a agentes IA integrados.
```
