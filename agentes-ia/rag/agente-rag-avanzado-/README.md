```markdown
# Agente RAG Avanzado

## Descripción
Workflow avanzado para la implementación de un agente RAG (Retrieval-Augmented Generation) que combina capacidades de recuperación de información y generación de texto usando nodos de Langchain, Supabase, Google Drive y otras herramientas integradas en n8n. Ideal para automatizar procesos de consulta y resumen con soporte de memoria y búsqueda vectorial.

## Requisitos
- Cuenta y credenciales de OpenAI (API Key) para nodos relacionados con modelos de lenguaje y embeddings.
- Cuenta y acceso a Supabase (API Key, URL) para almacenamiento y recuperación vectorial.
- Cuenta de Google con acceso a Google Drive y configuración del trigger correspondiente.
- Base de datos PostgreSQL para nodos de memoria `memoryPostgresChat` (configurada y accesible).
- Configuración de credenciales en n8n para cada servicio utilizado.

## Instrucciones de configuración
1. **OpenAI**: Configure la API Key en las credenciales para nodos `openAi`, `embeddingsOpenAi`, `lmChatOpenAi`.
2. **Supabase**: Configure la URL y la API Key en las credenciales para nodos `supabase` y `vectorStoreSupabase`.
3. **Google Drive**: Configure la integración con Google Drive para nodos `googleDriveTrigger` y `googleDrive`.
4. **PostgreSQL**: Configure el acceso a la base de datos para el nodo `memoryPostgresChat`.
5. Importe el workflow en n8n y establezca las credenciales en cada nodo antes de activarlo.

## Detalles de funcionamiento
- El workflow detecta nuevos archivos o consultas vía trigger de Google Drive y chat trigger.
- Los documentos son procesados y divididos usando el nodo `textSplitterRecursiveCharacterTextSplitter`.
- El contenido es indexado y almacenado en Supabase como un vector store para recuperación eficiente.
- Se realizan consultas al vector store para recuperar información relevante.
- El agente RAG genera respuestas basadas en contenido recuperado, usando generación de texto avanzada con el nodo `agent` y modelos OpenAI.
- El nodo `memoryPostgresChat` mantiene el contexto y la memoria conversacional.
- Incluye mecanismos de control de flujo y gestión mediante nodos `switch`, `limit`, `if` y batch processing.
- El workflow produce resúmenes, respuestas y acciones automatizadas basadas en la interacción con los datos.

## Ejemplos de uso
- Automatizar soporte al cliente con respuestas enriquecidas y contextualizadas.
- Generación de resúmenes y reportes a partir de documentos almacenados en Google Drive.
- Consulta avanzada de bases de conocimiento con integración dinámica y memoria conversacional.
- Herramienta de asistencia para equipos que manejan grandes volúmenes de información no estructurada.

---

**Número de nodos:** 47  
**Categoría:** agentes-ia/rag  
**Etiquetas:** (ninguna asignada)  
**Nodos principales utilizados:**  
`@n8n/n8n-nodes-langchain.openAi`, `embeddingsOpenAi`, `supabase`, `textSplitterRecursiveCharacterTextSplitter`, `summarize`, `httpRequest`, `lmChatOpenAi`, `switch`, `limit`, `stickyNote`, `googleDriveTrigger`, `toolVectorStore`, `splitInBatches`, `googleDrive`, `if`, `memoryPostgresChat`, `agent`, `documentDefaultDataLoader`, `aggregate`, `extractFromFile`, `vectorStoreSupabase`, `set`, `chatTrigger`.
```