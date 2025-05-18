```markdown
# My workflow 2

## Descripción
Workflow creado en n8n para integrar agentes de inteligencia artificial con Telegram, facilitando la interacción dinámica mediante nodos basados en LangChain y el manejo eficiente de mensajes y respuestas.

## Requisitos
- Credenciales de Telegram Bot API configuradas en n8n.
- API Key de OpenAI para nodos `openAi` y `lmChatOpenAi`.
- Acceso a n8n con los nodos necesarios instalados:
  - `@n8n/n8n-nodes-langchain`
  - `n8n-nodes-base`

## Instrucciones de configuración
1. Configurar el bot de Telegram y obtener el token.
2. Importar el workflow en n8n.
3. Añadir las credenciales de Telegram en el nodo `telegramTrigger` y `telegram`.
4. Proveer la API Key de OpenAI en los nodos LangChain.
5. Revisar y ajustar los parámetros en los nodos `switch`, `set` y `toolCode` según sea necesario.
6. Activar el workflow para comenzar a recibir y procesar mensajes.

## Detalles de funcionamiento
Este workflow consta de 17 nodos que combinan:
- Disparadores y envíos de mensajes mediante Telegram.
- Procesamiento y generación de texto con modelos de OpenAI.
- Memoria buffer para contexto en las conversaciones.
- Manejo de lógica condicional con nodos `switch`.
- Ejecución de código y workflows adicionales a través de herramientas integradas.
- Agentes inteligentes capaces de responder y tomar decisiones dinámicas.

## Ejemplos de uso
- Automatización de respuestas personalizadas en un grupo de Telegram.
- Asistente virtual que mantiene contexto de conversación.
- Ejecución de tareas específicas activadas por comandos en Telegram.
- Integración de agentes IA para consultas y soporte a través de chat.

---

**Etiqueta:** agentes-ia/telegram  
**Número de nodos:** 17
```