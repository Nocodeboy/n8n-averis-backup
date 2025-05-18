```markdown
# 1. Joe - Lead Generator Master

## Descripción
Workflow diseñado para generar y gestionar leads de manera automatizada utilizando agentes de inteligencia artificial, integrados con Telegram para interacción en tiempo real.

## Requisitos
- Credenciales API de OpenAI configuradas (`@n8n/n8n-nodes-langchain.openAi` y `lmChatOpenAi`).
- Acceso a Telegram Bot API con token válido.
- n8n con nodos instalados:
  - `@n8n/n8n-nodes-langchain`
  - `n8n-nodes-base`
- Permisos adecuados para ejecutar workflows y conectarse a APIs externas.

## Instrucciones de configuración
1. Importa el workflow en tu instancia de n8n.
2. Configura las credenciales de OpenAI en los nodos correspondientes.
3. Configura el webhook del nodo `telegramTrigger` vinculándolo a tu bot de Telegram.
4. Ajusta cualquier parámetro específico del agente o flujo según tus necesidades.
5. Guarda y habilita el workflow para iniciar su ejecución.

## Detalles de funcionamiento
El workflow utiliza nodos de LangChain para procesamiento inteligente de texto y gestión de memoria temporal. Recibe mensajes desde Telegram (`telegramTrigger`), procesa las solicitudes con agentes AI (`agent`, `toolWorkflow`), evalúa condiciones mediante el nodo `switch` y responde automáticamente a través del nodo `telegram`. La memoria buffer permite mantener contexto para interacciones más naturales. Un total de 12 nodos orquestan esta lógica para un lead generation eficiente.

## Ejemplos de uso
- Recepción y clasificación de solicitudes de contacto vía Telegram.
- Respuestas automáticas a consultas frecuentes con IA personalizada.
- Seguimiento inteligente de leads con historial de conversación almacenado.
- Activación de flujos específicos basados en criterios definidos en el nodo switch.
```