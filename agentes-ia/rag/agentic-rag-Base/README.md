```markdown
# Agentic RAG

## Descripción  
Agentic RAG es un workflow para n8n que facilita la implementación de un agente IA basado en Retrieval-Augmented Generation (RAG). Integra múltiples nodos especializados para procesamiento de texto, manejo de memoria, y conexión con bases de datos y servicios en la nube, permitiendo consultas inteligentes apoyadas en datos externos.

## Requisitos  
- Credenciales de OpenAI para acceso a modelos de lenguaje y embeddings  
- Acceso a Supabase para almacenamiento y vectorización de datos  
- Credenciales para bases de datos PostgreSQL  
- Permisos para Google Drive y configuración del Google Drive Trigger  
- API keys y configuraciones necesarias para n8n  

## Instrucciones de configuración  
1. Añadir credenciales de OpenAI en n8n (`embeddingsOpenAi`, `lmChatOpenAi`).  
2. Configurar la conexión a Supabase para los nodos `n8n-nodes-base.supabase` y `vectorStoreSupabase`.  
3. Establecer las credenciales y el acceso a PostgreSQL para los nodos relacionados (`postgres`, `memoryPostgresChat`, `postgresTool`).  
4. Configurar el disparador de Google Drive (`googleDriveTrigger`) y permisos asociados.  
5. Personalizar variables y parámetros en nodos como `switch`, `set` y `stickyNote` según el caso de uso.  
6. Validar los webhooks (`webhook`, `respondToWebhook`, `chatTrigger`) para recibir y responder solicitudes externas.  

## Detalles de funcionamiento  
- El workflow inicia con un disparador en Google Drive o webhook que activa el proceso.  
- Utiliza la división y extracción de texto para manejar documentos grandes (`textSplitterCharacterTextSplitter`, `extractFromFile`).  
- Genera embeddings con OpenAI para buscar información relevante en Supabase.  
- La lógica del agente se maneja a través del nodo `agent` y se apoya en memoria PostgreSQL para contexto.  
- Se usan nodos de agregación y resumen para sintetizar la información antes de la respuesta final.  
- Decisiones internas se gestionan con nodos `switch` para controlar el flujo según condiciones definidas.  

## Ejemplos de uso  
- Consulta contextualizada sobre documentos almacenados en Google Drive.  
- Resúmenes automáticos y respuestas inteligentes basados en datos actualizados en Supabase/PostgreSQL.  
- Implementación rápida de agentes conversacionales con acceso a memoria a largo plazo.  

---

**Categoría:** agentes-ia/rag  
**Etiquetas:** Base, *****  
**Nodos utilizados:** 42  
```