```markdown
# Agente chat con archivo para supabase

## Descripción
Workflow de n8n que implementa un agente de chat con recuperación aumentada (RAG) utilizando un archivo almacenado en Supabase. Combina procesamiento de archivos, generación de embeddings, búsqueda en vector store y modelado conversacional para ofrecer respuestas inteligentes basadas en documentos.

## Requisitos
- Cuenta y proyecto en [Supabase](https://supabase.com/) con acceso a la base de datos y almacenamiento de archivos.
- API Key de Supabase con permisos para lectura y escritura.
- Cuenta en OpenAI con API Key para utilizar modelos de embeddings y chat.
- n8n instalado y configurado con los nodos necesarios.

## Instrucciones de configuración
1. Configure las credenciales de Supabase en n8n con la URL del proyecto y la API Key.
2. Añada las credenciales de OpenAI en n8n para el acceso a embeddings y chat.
3. Cargue el archivo fuente en Supabase Storage o configure la URL de acceso en el workflow.
4. Ajuste parámetros del workflow (por ejemplo, nombres de tablas, llaves, modelos) según sus necesidades.
5. Active el workflow y ejecute el disparador manual para iniciar.

## Detalles de funcionamiento
- El workflow comienza con un disparador manual o chat trigger.
- Extrae y procesa el archivo desde Supabase, dividiéndolo en fragmentos mediante un text splitter recursivo.
- Genera embeddings con OpenAI para cada fragmento y los almacena en un vector store Supabase.
- Mediante nodos de agente y herramientas conectadas al vector store, responde consultas generando texto contextualizado.
- Utiliza lógica condicional, agregación y fusión para manejar flujos y estados internos.
- Incorpora nodos HTTP para solicitudes adicionales y manejo avanzado de la conversación.

## Ejemplos de uso
- Chatbots que responden preguntas específicas basadas en documentos corporativos alojados en Supabase.
- Asistentes inteligentes que consultan información almacenada en archivos PDF o texto.
- Proyectos RAG que integran almacenamiento, NLP y agentes conversacionales en un solo flujo.

---

**Número de nodos:** 33  
**Categoría:** agentes-ia/rag  
**Nodos usados:** n8n-nodes-base.aggregate, @n8n/n8n-nodes-langchain.embeddingsOpenAi, @n8n/n8n-nodes-langchain.lmChatOpenAi, n8n-nodes-base.switch, n8n-nodes-base.supabase, n8n-nodes-base.merge, n8n-nodes-base.if, n8n-nodes-base.manualTrigger, n8n-nodes-base.extractFromFile, @n8n/n8n-nodes-langchain.textSplitterRecursiveCharacterTextSplitter, @n8n/n8n-nodes-langchain.vectorStoreSupabase, @n8n/n8n-nodes-langchain.agent, n8n-nodes-base.stickyNote, @n8n/n8n-nodes-langchain.toolVectorStore, n8n-nodes-base.splitInBatches, n8n-nodes-base.httpRequest, @n8n/n8n-nodes-langchain.documentDefaultDataLoader, @n8n/n8n-nodes-langchain.chatTrigger
```