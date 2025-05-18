```markdown
# 1. Ruby - Agente de Respuestas Rápidas

## Descripción  
Workflow diseñado para ofrecer respuestas rápidas y efectivas mediante un agente IA integrado con diversas herramientas y servicios, incluyendo Gmail, Google Calendar, Telegram y bases de datos vectoriales. Utiliza modelos de lenguaje OpenAI para procesar, analizar y responder consultas automatizadas.

## Requisitos  
- Credenciales válidas para:
  - OpenAI (API Key para modelos `openAi`, `lmChatOpenAi` y embeddings)
  - Gmail API (para nodos `gmail`)
  - Google Calendar API (para nodos `googleCalendar` y `googleCalendarTool`)
  - Telegram Bot API (para nodos `telegram`)
  - Supabase (para el vector store con `vectorStoreSupabase`)
- Acceso y permisos configurados en las plataformas mencionadas

## Instrucciones de configuración  
1. **Configurar APIs y credenciales**  
   - Agregar las credenciales de OpenAI, Gmail, Google Calendar, Telegram y Supabase en n8n.  
2. **Importar el workflow**  
   - Importar el archivo JSON del workflow `1. Ruby - Agente de Respuestas Rápidas` en n8n.  
3. **Ajustes personalizados**  
   - Revisar y modificar las variables y parámetros relacionados a usuarios, horarios y condiciones en nodos `set`, `if` y `switch` según necesidades.  
4. **Activar el trigger**  
   - Configurar el nodo `scheduleTrigger` para definir la frecuencia de activación del agente.

## Detalles de funcionamiento  
- El agente utiliza un pipeline de 74 nodos que combina:  
  - Modelos de lenguaje y embeddings de OpenAI para comprensión y generación de texto.  
  - Herramientas inteligentes para organizar eventos en Google Calendar y administrar correos vía Gmail.  
  - Memoria integrada para mantener contexto entre interacciones con `memoryBufferWindow`.  
  - Valoración condicional y bifurcación del flujo mediante nodos `switch`, `filter` y `if`.  
  - Comunicación bidireccional con usuarios vía Telegram.  
  - Manejo avanzado de vectores y búsqueda con Supabase y herramientas vectoriales personalizadas.  
- El agente responde rápido a consultas, organiza tareas y ofrece interacción fluida y personalizada.

## Ejemplos de uso  
- Responder consultas entrantes por Telegram sobre agenda y eventos.  
- Gestionar correos prioritarios automáticamente y programar reuniones en Google Calendar.  
- Ejecutar tareas basadas en condiciones preestablecidas según filtros configurados.  
- Mantener contexto conversacional y realizar búsquedas semánticas en bases vectoriales.

---

**Etiqueta:** agentes-ia/otros  
**Nodos utilizados:**  
`@n8n/n8n-nodes-langchain.openAi`, `@n8n/n8n-nodes-langchain.embeddingsOpenAi`, `n8n-nodes-base.gmail`, `n8n-nodes-base.scheduleTrigger`, `@n8n/n8n-nodes-langchain.outputParserStructured`, `n8n-nodes-base.googleCalendarTool`, `@n8n/n8n-nodes-langchain.lmChatOpenAi`, `n8n-nodes-base.switch`, `n8n-nodes-base.filter`, `@n8n/n8n-nodes-langchain.memoryBufferWindow`, `n8n-nodes-base.telegram`, `n8n-nodes-base.stickyNote`, `@n8n/n8n-nodes-langchain.toolVectorStore`, `n8n-nodes-base.splitInBatches`, `n8n-nodes-base.merge`, `n8n-nodes-base.if`, `@n8n/n8n-nodes-langchain.agent`, `n8n-nodes-base.noOp`, `@n8n/n8n-nodes-langchain.chainLlm`, `n8n-nodes-base.code`, `@n8n/n8n-nodes-langchain.vectorStoreSupabase`, `n8n-nodes-base.set`, `@n8n/n8n-nodes-langchain.toolThink`, `n8n-nodes-base.googleCalendar`

**Número de nodos:** 74
```