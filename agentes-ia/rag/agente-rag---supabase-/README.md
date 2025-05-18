```markdown
# Agente RAG - supabase

## Descripción

Workflow basado en n8n que implementa un agente RAG (Retrieval-Augmented Generation) utilizando Supabase como vector store y diversas integraciones de inteligencia artificial para gestión y respuesta inteligente de datos.

## Requisitos

- Credenciales API de OpenAI para nodos Langchain (`embeddingsOpenAi`, `lmChatOpenAi`).
- Cuenta y credenciales de Supabase para almacenamiento y búsqueda vectorial.
- Acceso a Google Drive para gatillos (`googleDriveTrigger`) y manejo de archivos.
- Acceso a base de datos Postgres compatible para memoria y herramientas adicionales.
- Configuración de webhook para integraciones externas.

## Instrucciones de configuración

1. Configure las credenciales de OpenAI en n8n (`embeddingsOpenAi`, `lmChatOpenAi`).
2. Agregue y configure la integración con Supabase (URL y API Key) para nodos `supabase` y `vectorStoreSupabase`.
3. Configurar credenciales de Google Drive para activar y acceder a archivos.
4. Defina los detalles de conexión para Postgres (nodos `postgres` y `memoryPostgresChat`).
5. Ajuste los nodos webhook y respondToWebhook según el endpoint deseado.
6. Revise y adapte los parámetros del agente (`agent`) y el splitter de texto para el caso de uso específico.

## Detalles de funcionamiento

- El flujo inicia con triggers desde Google Drive o webhook.
- Los documentos entrantes se procesan y dividen en fragmentos usando `textSplitterCharacterTextSplitter`.
- Se generan embeddings vía OpenAI para almacenar en Supabase como vector store.
- El agente Langchain utiliza la memoria Postgres para contextos de conversación y realiza consultas vectoriales para enriquecer respuestas.
- Se emplean nodos de resumen y agregación para optimizar la gestión de información.
- El flujo controla la lógica mediante nodos `switch` y gestiona respuestas con `respondToWebhook`.
- Integración nativa con herramientas Postgres y Google Drive permite extensión flexible y manejo robusto de datos.

## Ejemplos de uso

- Soporte automatizado con contexto de documentos almacenados en Supabase.
- Búsqueda avanzada y generación de respuestas basadas en datos externos y memoria conversacional.
- Monitoreo y procesamiento de archivos añadidos en Google Drive con respuestas dinámicas vía webhook.
- Agentes IA personalizados con capacidades RAG para asistentes inteligentes o análisis documental.
```
