```markdown
# 1. MCPs + Claude - Main

## Descripción

Workflow principal que integra múltiples agentes de IA y herramientas para automatizar tareas complejas utilizando Claude y múltiples nodos especializados como LangChain, Gmail, Notion, Telegram, Google Calendar, entre otros.

## Requisitos

- Credenciales para APIs y servicios utilizados:
  - OpenAI (Embeddings)
  - SerpAPI (Búsquedas)
  - Supabase (Vector Store)
  - Gmail
  - Google Contacts
  - Google Calendar
  - Notion
  - Telegram Bot Token
- Acceso y configuración de n8n con los nodos correspondientes instalados:
  - @n8n/n8n-nodes-langchain
  - n8n-nodes-base

## Configuración

1. Importar el workflow en n8n.
2. Configurar las credenciales necesarias para cada nodo que lo requiera:
   - OpenAI API Key para `embeddingsOpenAi`.
   - SerpAPI Key para `toolSerpApi`.
   - Supabase URL y Key para `vectorStoreSupabase`.
   - Gmail, Google Contacts, Google Calendar con OAuth correctamente autorizados.
   - Notion Token para acceso a bases de datos.
   - Telegram Bot Token para recibir y enviar mensajes.
3. Ajustar parámetros específicos en nodos LangChain como `toolCalculator`, `toolThink`, y `mcpTrigger` según la lógica deseada.
4. Verificar interconexiones y flujo entre nodos.

## Funcionamiento

- El workflow arranca con el nodo `mcpTrigger` que activa la cadena de agentes IA.
- Utiliza `embeddingsOpenAi` para procesar y generar representaciones semánticas de datos.
- Se realizan búsquedas en tiempo real mediante `toolSerpApi`.
- Cálculos específicos se gestionan con `toolCalculator`.
- Maneja la memoria y datos en Supabase mediante `vectorStoreSupabase`.
- Integra mensajes y notas a través de Gmail, Telegram y Sticky Notes.
- Sincroniza y consulta información en Google Calendar, Google Contacts y Notion.
- El flujo combina estos servicios coordinados para ofrecer respuestas y acciones inteligentes con Claude.

## Ejemplos de uso

- Automatización avanzada de gestión de agenda y contactos usando IA.
- Respuestas inteligentes a consultas recibidas vía Telegram o Gmail.
- Generación y almacenamiento de insights semánticos con embeddings OpenAI.
- Automatización de cálculos complejos y búsquedas en tiempo real para soportar decisiones.

---

**Etiquetas:** MCP, *****, Claude  
**Categoría:** agentes-ia/otros  
**Número de nodos:** 64  
```