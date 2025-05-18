```markdown
# ******** Base de conocimiento RAG

## Descripción
Workflow n8n para implementar un agente de recuperación aumentada de conocimiento (RAG) utilizando Langchain y diversos nodos para gestionar documentos, embeddings y consultas inteligentes.

## Requisitos
- Credenciales de OpenAI para los nodos de lenguaje y embeddings (`lmChatOpenAi`, `embeddingsOpenAi`).
- Acceso a Google Drive con credenciales configuradas para nodos `googleDrive`, `googleDriveTrigger`.
- Conexión a Supabase para el vector store (`vectorStoreSupabase`, `retrieverVectorStore`).
- n8n actualizado con los nodos Langchain instalados.
- Acceso a APIs relacionadas según los nodos de Langchain.

## Instrucciones de configuración
1. Configure las credenciales de OpenAI en n8n.  
2. Añada y configure credenciales de Google Drive con permisos para monitorear y extraer archivos.  
3. Configure las variables de conexión para Supabase con datos de autenticación y URL.  
4. Importar este workflow en n8n.  
5. Ajustar los parámetros del nodo `textSplitterRecursiveCharacterTextSplitter` según el tamaño deseado del fragmento de texto.  
6. Configure los triggers (`googleDriveTrigger`, `executeWorkflowTrigger`) para iniciar el workflow automáticamente.  

## Detalles de funcionamiento
- El workflow inicia al detectarse cambios en Google Drive o a través de un trigger manual.  
- Los documentos son extraídos y procesados con el nodo `extractFromFile`.  
- El texto extraído es segmentado en fragmentos manejables mediante `textSplitterRecursiveCharacterTextSplitter`.  
- Cada fragmento se convierte en embeddings con `embeddingsOpenAi` y se almacena en Supabase usando `vectorStoreSupabase`.  
- En la consulta, se utiliza `retrieverVectorStore` para recuperar fragmentos relevantes de la base de datos.  
- El nodo `chainRetrievalQa` junto con `lmChatOpenAi` genera respuestas basadas en el conocimiento recuperado.  
- Nodos adicionales `set` y `documentDefaultDataLoader` gestionan variables y carga inicial de documentos.  

## Ejemplos de uso
- Automatizar la consulta y respuesta sobre documentos almacenados en Google Drive.  
- Implementar un sistema de soporte que responde dudas basadas en los documentos de una organización.  
- Integrar con chatbots para ofrecer respuestas enriquecidas por información actualizada y relevante.  

---

**Número de nodos:** 15  
**Categoría:** agentes-ia/rag  
**Nodos utilizados:**  
- @n8n/n8n-nodes-langchain.lmChatOpenAi  
- @n8n/n8n-nodes-langchain.embeddingsOpenAi  
- n8n-nodes-base.googleDrive  
- n8n-nodes-base.extractFromFile  
- @n8n/n8n-nodes-langchain.vectorStoreSupabase  
- @n8n/n8n-nodes-langchain.textSplitterRecursiveCharacterTextSplitter  
- n8n-nodes-base.set  
- n8n-nodes-base.googleDriveTrigger  
- n8n-nodes-base.executeWorkflowTrigger  
- @n8n/n8n-nodes-langchain.retrieverVectorStore  
- @n8n/n8n-nodes-langchain.documentDefaultDataLoader  
- @n8n/n8n-nodes-langchain.chainRetrievalQa  
```