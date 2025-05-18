```markdown
# Agente IA Asistente Personal

## Descripción

Workflow de n8n diseñado para actuar como un agente IA asistente personal, integrado con WhatsApp para interacción directa, utilizando múltiples herramientas y APIs para gestión de información, búsqueda inteligente y administración de calendarios y documentos.

## Requisitos

- Credenciales de OpenAI (OpenAI API Key)
- Cuenta y credenciales de Notion API
- Cuenta y configuración en Google (Calendar, Drive, Gmail)
- Credenciales de Pinecone para vector store
- Configuración de SerpAPI (opcional, para búsquedas web)
- WhatsApp Business API o acceso compatible con el nodo WhatsApp de n8n
- Acceso a n8n con los nodos mencionados instalados y actualizados

## Instrucciones de configuración

1. Instalar y habilitar todos los nodos listados en n8n.
2. Configurar las credenciales para:
   - OpenAI (incluyendo embeddings y chat)
   - Notion API
   - Google Calendar, Drive y Gmail
   - Pinecone
   - SerpAPI (si se usa)
   - WhatsApp Trigger y WhatsApp para mensajería
3. Ajustar los parámetros para cada nodo según su servicio (IDs de bases, tokens, claves API).
4. Revisar configuraciones específicas dentro del workflow para personalizar comportamientos, como filtros o triggers.
5. Guardar y activar el workflow.

## Detalles de funcionamiento

- El workflow inicia con una activación vía WhatsApp (nodo WhatsApp Trigger).
- Procesa texto entrante y lo divide para mejor análisis con textSplitterRecursiveCharacterTextSplitter.
- Utiliza nodos de LangChain para manejo de memoria y contexto con memoryBufferWindow y agentes inteligentes.
- Consulta y actualiza información en Notion, Google Calendar, Drive y Gmail según las solicitudes del usuario.
- Realiza búsquedas inteligentes en web usando SerpAPI y acceso a vectores semánticos mediante Pinecone.
- Controla el flujo con nodos Switch y Set para adaptarse a diferentes comandos y tipos de interacción.
- Responde de forma contextuada a través de WhatsApp, utilizando nodos específicos para envío.

## Ejemplos de uso

- **Consultar agenda diaria:** El usuario envía un mensaje por WhatsApp preguntando "¿Qué tengo en mi calendario hoy?" y recibe un resumen de eventos próximos extraídos de Google Calendar.
- **Buscar documentos relevantes:** Solicitar "Encuentra la nota sobre el proyecto XYZ" activa la búsqueda en Notion y Google Drive, devolviendo los documentos más relevantes.
- **Realizar una consulta web:** Preguntar por información actualizada o datos específicos, que se resuelve con SerpAPI y el agente AI.
- **Enviar un correo sencillo:** Solicitar "Envía un correo a [email] con el asunto y mensaje X" para enviar emails mediante Gmail integrado.

---

### Categoría
`agentes-ia/whatsapp`

### Etiquetas
WhatsApp, Agente, Averis

### Número de nodos
34
```