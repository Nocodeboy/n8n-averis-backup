```markdown
# Automatiza emails de respuesta de atención al cliente

## Descripción
Workflow de n8n diseñado para automatizar la generación y envío de respuestas personalizadas a emails de atención al cliente utilizando inteligencia artificial y diversos servicios integrados.

## Requisitos
- Credenciales de Gmail (para gatillar y enviar emails)
- Credenciales de Telegram (opcional, para notificaciones)
- API Key de OpenAI (para los nodos de LangChain: openAi, lmChatOpenAi, embeddingsOpenAi)
- Credenciales de Pinecone (para vectorStorePinecone y herramienta de búsqueda vectorial)
- n8n instalado y configurado para ejecutar workflows

## Instrucciones de configuración
1. Configure las credenciales de Gmail en n8n para activar los nodos `gmailTrigger` y `gmailTool`.
2. Añada su API Key de OpenAI en las credenciales para los nodos LangChain (`openAi`, `lmChatOpenAi`, `embeddingsOpenAi`).
3. Configure las credenciales de Pinecone para permitir el uso de los nodos `vectorStorePinecone` y `toolVectorStore`.
4. Opcionalmente, configure Telegram para recibir notificaciones mediante el nodo `telegram`.
5. Importe el workflow en n8n y ajuste cualquier parámetro específico, como filtros o direcciones de correo.

## Detalles de funcionamiento
- El workflow se activa con la recepción de un email en Gmail (`gmailTrigger`).
- Utiliza modelos OpenAI para interpretar el contenido del email y generar una respuesta adecuada.
- Emplea vectores de embeddings y Pinecone para consultas contextuales y mejoras en la precisión de las respuestas.
- A través de nodos `switch` se determinan diferentes caminos según el tipo de consulta.
- Las respuestas generadas son enviadas automáticamente por Gmail.
- Se pueden enviar notificaciones por Telegram para alertar al equipo de soporte o registrar los eventos.
- El nodo `set` permite configurar datos necesarios en el flujo y el nodo `agent` maneja la lógica de agentes de IA integrados.

## Ejemplos de uso
- Responder automáticamente preguntas frecuentes recibidas en el soporte al cliente.
- Enviar confirmaciones o información adicional basada en el contenido del email.
- Notificar vía Telegram cuando se recibe un email con una consulta compleja para atención humana.
- Resolver consultas utilizando un almacén de conocimiento vectorial para respuestas más precisas.

---

**Nodos utilizados**: @n8n/n8n-nodes-langchain.openAi, @n8n/n8n-nodes-langchain.lmChatOpenAi, @n8n/n8n-nodes-langchain.embeddingsOpenAi, n8n-nodes-base.switch, n8n-nodes-base.gmailTrigger, n8n-nodes-base.telegram, n8n-nodes-base.gmailTool, @n8n/n8n-nodes-langchain.agent, n8n-nodes-base.set, @n8n/n8n-nodes-langchain.toolVectorStore, @n8n/n8n-nodes-langchain.vectorStorePinecone

**Número de nodos**: 13  
**Categoría**: agentes-ia/otros
```