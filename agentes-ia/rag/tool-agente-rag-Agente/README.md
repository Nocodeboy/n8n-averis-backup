```markdown
# Tool Agente RAG

## Descripción
Workflow de n8n diseñado como un agente RAG (Retrieval-Augmented Generation) que integra múltiples fuentes de datos mediante embeddings y búsqueda vectorial, facilitando respuestas contextuales y precisas mediante IA. Ideal para automatizar procesos inteligentes con herramientas de Langchain y servicios externos.

## Requisitos
- Credenciales de OpenAI para acceso a modelos GPT y embeddings.
- Cuenta y credenciales de Supabase para vector stores y bases de datos.
- Acceso a Google Drive con permisos para lectura y escritura.
- n8n instalado con los siguientes nodos habilitados:
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`
  - `@n8n/n8n-nodes-langchain.embeddingsOpenAi`
  - `n8n-nodes-base.googleDrive`
  - `n8n-nodes-base.supabase`
  - `n8n-nodes-base.limit`
  - `@n8n/n8n-nodes-langchain.memoryBufferWindow`
  - `n8n-nodes-base.extractFromFile`
  - `@n8n/n8n-nodes-langchain.vectorStoreSupabase`
  - `@n8n/n8n-nodes-langchain.textSplitterRecursiveCharacterTextSplitter`
  - `@n8n/n8n-nodes-langchain.agent`
  - `n8n-nodes-base.executeWorkflowTrigger`
  - `n8n-nodes-base.set`
  - `n8n-nodes-base.googleDriveTrigger`
  - `@n8n/n8n-nodes-langchain.toolVectorStore`
  - `n8n-nodes-base.stickyNote`
  - `@n8n/n8n-nodes-langchain.documentDefaultDataLoader`

## Instrucciones de configuración
1. Configure las credenciales de OpenAI en n8n.
2. Configure las credenciales de Supabase y asegúrese de que el proyecto tiene habilitado el vector store.
3. Autentique su cuenta de Google Drive para acceso a los archivos necesarios.
4. Importar el workflow "Tool Agente RAG" en n8n.
5. Ajustar parámetros específicos del agente, como fuentes de datos, límites de ejecución y configuraciones de memoria.
6. Habilitar triggers de Google Drive u otros disparadores para iniciar el agente automáticamente.

## Detalles de funcionamiento
- Utiliza embeddings de OpenAI para vectorizar documentos y consultas.
- Almacena y consulta documentos vectorizados en Supabase.
- Divide textos con TextSplitter para mejorar la granularidad de búsqueda.
- Usa un buffer de memoria para mantener el contexto conversacional.
- Ejecuta acciones inteligentes mediante nodos agent y herramientas integradas.
- Monitorea actividades con nodos limit y disparadores que controlan el flujo.
- Integra documentos desde Google Drive, extractores de archivos y loaders personalizados.

Número total de nodos en el workflow: 39.

## Ejemplos de uso
- Automatización de respuestas inteligentes basadas en documentos corporativos alojados en Google Drive.
- Agente de soporte que consulta bases de conocimiento internas almacenadas en Supabase.
- Workflow para extracción y análisis contextual de archivos PDF, documentos y notas compartidas.
- Integración en pipelines IA para generación con información actualizada y enriquecida.

---

**Etiquetas:** Agente, RAG, Worker  
**Categoría:** agentes-ia/rag
```
