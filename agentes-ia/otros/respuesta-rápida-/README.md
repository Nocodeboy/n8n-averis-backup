```markdown
# Respuesta rápida

## Descripción
Workflow avanzado diseñado para proporcionar respuestas rápidas y contextuales utilizando agentes de IA, integrando múltiples servicios como Gmail, Telegram y Google Calendar, apoyado en modelos de lenguaje y herramientas vectoriales para mejorar la precisión.

## Requisitos
- Credenciales configuradas en n8n para:
  - OpenAI (para nodos de LangChain: embeddings, chat, agentes y parser)
  - Gmail
  - Google Calendar
  - Telegram
  - Supabase (para vectorStore)
- Acceso a APIs correspondientes habilitado y con permisos adecuados.

## Instrucciones de configuración
1. Importar el workflow `Respuesta rápida` en n8n.
2. Configurar todas las credenciales necesarias en Preferencias > Credenciales de n8n:
   - OpenAI API Key
   - Gmail OAuth/SMTP
   - Google Calendar API
   - Telegram Bot Token
   - Supabase URL y API Key
3. Ajustar parámetros específicos en nodos como triggers, filtros y set según su entorno y preferencias.
4. Activar el workflow para comenzar a recibir y procesar solicitudes.

## Detalles de funcionamiento
- Utiliza nodos de disparo para detectar inputs por correo electrónico, Telegram u otros canales.
- Emplea modelos de lenguaje OpenAI para generar respuestas inteligentes y contextualizadas.
- Integra herramientas como vector stores y memoria buffer para mantener contexto y referencias.
- Realiza acciones sobre Gmail y Google Calendar basadas en las interacciones recibidas.
- Implementa nodos de control (switch, if, noOp) para lógica avanzada y manejo de flujo.
- Más de 90 nodos trabajando coordinadamente para asegurar respuestas ágiles y eficientes.

## Ejemplos de uso
- Recibir un correo con una consulta y responder automáticamente con información precisa.
- Agendar eventos en Google Calendar desde un mensaje de Telegram.
- Responder preguntas frecuentes usando contexto almacenado en el vector store.
- Ejecutar flujos secundarios vía ejecución de workflows anidados para tareas complejas.

---

**Número de nodos:** 97  
**Categoría:** agentes-ia/otros  
**Tipos de nodos utilizados:**  
`@n8n/n8n-nodes-langchain.embeddingsOpenAi`, `n8n-nodes-base.gmail`, `n8n-nodes-base.executeWorkflowTrigger`, `@n8n/n8n-nodes-langchain.outputParserStructured`, `n8n-nodes-base.httpRequest`, `n8n-nodes-base.googleCalendarTool`, `@n8n/n8n-nodes-langchain.lmChatOpenAi`, `n8n-nodes-base.switch`, `@n8n/n8n-nodes-langchain.memoryBufferWindow`, `n8n-nodes-base.telegram`, `n8n-nodes-base.stickyNote`, `@n8n/n8n-nodes-langchain.toolVectorStore`, `n8n-nodes-base.if`, `@n8n/n8n-nodes-langchain.agent`, `n8n-nodes-base.noOp`, `@n8n/n8n-nodes-langchain.chainLlm`, `@n8n/n8n-nodes-langchain.vectorStoreSupabase`, `n8n-nodes-base.set`, `@n8n/n8n-nodes-langchain.toolThink`, `n8n-nodes-base.googleCalendar`
```