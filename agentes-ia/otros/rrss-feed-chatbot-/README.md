```markdown
# RRSS Feed Chatbot

## Descripción  
Workflow diseñado para leer feeds RSS de redes sociales y generar respuestas automatizadas mediante un agente conversacional potenciado por IA, utilizando modelos de lenguaje y herramientas de vectorización y memoria.

## Requisitos  
- Credenciales de OpenAI (para nodos lmChatOpenAi y embeddingsOpenAi)  
- Acceso a una base de datos Postgres (para memoryPostgresChat)  
- Credenciales Supabase (para vectorStoreSupabase y toolVectorStore)  
- Endpoint RSS válido para trigger de feeds  
- n8n con nodos instalados:
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`
  - `@n8n/n8n-nodes-langchain.embeddingsOpenAi`
  - `@n8n/n8n-nodes-langchain.memoryPostgresChat`
  - `n8n-nodes-base.code`
  - `@n8n/n8n-nodes-langchain.vectorStoreSupabase`
  - `@n8n/n8n-nodes-langchain.textSplitterRecursiveCharacterTextSplitter`
  - `n8n-nodes-base.stickyNote`
  - `@n8n/n8n-nodes-langchain.agent`
  - `@n8n/n8n-nodes-langchain.toolVectorStore`
  - `n8n-nodes-base.splitInBatches`
  - `n8n-nodes-base.httpRequest`
  - `n8n-nodes-base.rssFeedReadTrigger`
  - `@n8n/n8n-nodes-langchain.documentDefaultDataLoader`
  - `@n8n/n8n-nodes-langchain.chatTrigger`

## Instrucciones de configuración  
1. Configurar las credenciales de OpenAI en n8n.  
2. Configurar la conexión a la base de datos Postgres para el nodo de memoria.  
3. Añadir credenciales Supabase para los nodos de vectorStore.  
4. Establecer la URL del feed RSS en el nodo `rssFeedReadTrigger`.  
5. Revisar y ajustar parámetros de los nodos de lenguaje y manejo de texto según necesidades específicas.  
6. Activar el workflow.

## Detalles de funcionamiento  
- El workflow se activa mediante la detección de nuevas entradas en el feed RSS.  
- El contenido se divide en fragmentos gestionables con el nodo `textSplitterRecursiveCharacterTextSplitter`.  
- Se generan embeddings para cada fragmento con OpenAI y se almacenan/consultan en Supabase para búsquedas vectoriales eficientes.  
- La memoria conversacional se mantiene en Postgres mediante la integración `memoryPostgresChat`.  
- El agente IA procesa la información, realiza consultas a la base vectorial y genera respuestas contextuales.  
- Se puede ejecutar código personalizado con `code` y controlar el flujo de datos con nodos base como `splitInBatches`.  
- Respuestas o notificaciones pueden gestionarse usando nodos HTTP o sticky notes para monitorización.

## Ejemplos de uso  
- Responder automáticamente consultas sobre contenidos recientes de redes sociales.  
- Mantener un chatbot alimentado con información actualizada de diversas fuentes RSS.  
- Realizar análisis y síntesis de tendencias o temas emergentes en feeds de noticias sociales.

---

**Número de nodos:** 25  
**Categoría:** agentes-ia/otros  
**Etiquetas:** (sin etiquetas asignadas)
```