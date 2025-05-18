```markdown
# Chatbot de soporte técnico de RR. HH. y TI con transcripción de audio

## Descripción
Workflow de n8n que implementa un chatbot inteligente para soporte técnico en áreas de Recursos Humanos y Tecnologías de la Información. Incluye transcripción de mensajes de audio y utiliza modelos de lenguaje avanzados para ofrecer respuestas contextualizadas y precisas.

## Requisitos
- Cuenta y credenciales de OpenAI para nodos de lenguaje (`openAi`, `embeddingsOpenAi`, `lmChatOpenAi`).
- Base de datos PostgreSQL configurada para almacenamiento de memoria y vectores (`memoryPostgresChat`, `vectorStorePGVector`).
- Bot de Telegram con token y canal configurado para recibir y enviar mensajes (`telegramTrigger`, `telegram`).
- Acceso a internet para nodos que realizan peticiones HTTP (`httpRequest`).

## Instrucciones de configuración
1. Configure las credenciales de OpenAI en n8n.
2. Configure la conexión a PostgreSQL para memoria y vector store.
3. Proporcione el token del bot de Telegram y configure el webhook para recibir mensajes.
4. Ajuste cualquier parámetro específico en los nodos, como el tamaño de fragmentos en `textSplitterRecursiveCharacterTextSplitter`.
5. Importe y active el workflow en n8n.

## Detalles de funcionamiento
- El workflow inicia con disparadores manuales o por mensajes de Telegram.
- Los mensajes de audio son extraídos y transcritos para convertirlos en texto.
- Utiliza un splitter de texto para procesar documentos largos de forma eficiente.
- Se crean embeddings que alimentan una base vectorial PostgreSQL para búsqueda semántica.
- Un agente basado en LangChain coordina la consulta y contextualización para responder dudas de RR. HH. y TI.
- Se emplea memoria a largo plazo para mantener el contexto de conversación mediante PostgreSQL.
- Cambios en el flujo se controlan mediante nodos `switch` para diferenciar tipos de entrada.
- Respuestas se envían de vuelta al usuario vía Telegram.

## Ejemplos de uso
- Un empleado envía un mensaje de voz preguntando sobre políticas de vacaciones y recibe una respuesta transcrita y contextualizada.
- Un usuario consulta por problemas técnicos y el chatbot entrega pasos para solución basados en documentación previa almacenada.
- Administradores pueden iniciar el workflow manualmente para pruebas o mantenimiento.

---

_Nodos utilizados (27):_  
@n8n/n8n-nodes-langchain.openAi, @n8n/n8n-nodes-langchain.embeddingsOpenAi, n8n-nodes-base.telegramTrigger, n8n-nodes-base.switch, @n8n/n8n-nodes-langchain.lmChatOpenAi, n8n-nodes-base.manualTrigger, @n8n/n8n-nodes-langchain.memoryPostgresChat, n8n-nodes-base.extractFromFile, n8n-nodes-base.telegram, @n8n/n8n-nodes-langchain.textSplitterRecursiveCharacterTextSplitter, n8n-nodes-base.stickyNote, @n8n/n8n-nodes-langchain.vectorStorePGVector, @n8n/n8n-nodes-langchain.agent, n8n-nodes-base.set, @n8n/n8n-nodes-langchain.toolVectorStore, n8n-nodes-base.httpRequest, @n8n/n8n-nodes-langchain.documentDefaultDataLoader
```