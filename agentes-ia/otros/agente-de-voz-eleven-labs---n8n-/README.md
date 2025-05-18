```markdown
# Agente de voz Eleven Labs - n8n

## Descripción
Workflow de n8n que implementa un agente de voz utilizando Eleven Labs y capacidades de IA con Langchain. Permite procesar consultas mediante modelos de lenguaje y responder con audio generado, integrando almacenamiento vectorial para mejorar la contextualización.

## Requisitos
- Cuenta y credenciales de Eleven Labs para síntesis de voz.
- API Key de OpenAI para modelos de lenguaje y embeddings.
- Acceso a Pinecone para el vector store.
- n8n instalado y configurado con los nodos requeridos.

## Nodos utilizados
- `@n8n/n8n-nodes-langchain.lmChatOpenAi`
- `@n8n/n8n-nodes-langchain.embeddingsOpenAi`
- `n8n-nodes-base.respondToWebhook`
- `@n8n/n8n-nodes-langchain.agent`
- `n8n-nodes-base.stickyNote`
- `@n8n/n8n-nodes-langchain.toolVectorStore`
- `@n8n/n8n-nodes-langchain.vectorStorePinecone`
- `n8n-nodes-base.webhook`

## Instrucciones de configuración
1. Configure las credenciales de OpenAI en n8n.
2. Configure las credenciales de Eleven Labs para la generación de audio.
3. Configure las credenciales de Pinecone para el vector store.
4. Importe el workflow a n8n.
5. Ajuste los parámetros en los nodos de acuerdo con sus claves API y configuraciones regionales.
6. Configure el webhook para recibir solicitudes externas.

## Funcionamiento
- El webhook recibe la solicitud del usuario.
- El agente Langchain procesa la consulta mediante `lmChatOpenAi`.
- Se generan embeddings para contextualizar la información usando `embeddingsOpenAi`.
- La base vectorial Pinecone se usa para recuperar información relevante.
- El agente responde con texto y genera audio mediante Eleven Labs.
- La respuesta se entrega a través de `respondToWebhook`.

## Ejemplos de uso
- Enviar una consulta de texto al webhook para recibir respuesta en audio.
- Integrar en sistemas de atención al cliente para respuestas automáticas con voz natural.
- Crear asistentes de voz personalizados con memoria contextual basada en vector stores.

---

**Número de nodos:** 9  
**Categoría:** agentes-ia/otros  
**Etiquetas:** (sin etiquetas)
```