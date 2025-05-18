```markdown
# 1. Agente IA WA para Clínica Dental - Main

## Descripción
Workflow de n8n diseñado para actuar como un agente de inteligencia artificial integrado con WhatsApp, optimizado para la atención y gestión de pacientes en clínicas dentales. Facilita la interacción automatizada, consulta de información, y manejo de solicitudes mediante IA avanzada y herramientas de procesamiento de lenguaje natural.

## Requisitos
- Credenciales de OpenAI (para nodos de procesamiento de lenguaje y embeddings)
- Credenciales de OpenRouter (para nodos lmChatOpenRouter)
- Cuenta y credenciales de Supabase (para almacenamiento vectorial)
- Acceso a Redis (para caching y sesiones)
- API de Evolution (para integración con sistemas externos de la clínica)
- Cuenta y configuración de WhatsApp Business API o integración compatible para webhook recepción y envío de mensajes
- Base de datos PostgreSQL compatible para memoria conversacional (memoryPostgresChat)

## Instrucciones de Configuración
1. **Configurar credenciales en n8n:**
   - Añadir API keys de OpenAI, OpenRouter y Evolution API.
   - Configurar conexión a Redis y PostgreSQL.
   - Añadir credenciales de Supabase para vector store.
2. **Webhook:**
   - Configurar el nodo webhook para recibir mensajes entrantes de WhatsApp.
   - Vincular con la plataforma WhatsApp Business API o servicio equivalente.
3. **Ajustar parámetros de agentes y herramientas:**
   - Personalizar prompts y plantillas en nodos LangChain según necesidades específicas de la clínica.
   - Configurar flujos condicionales y reglas en nodos Switch e If para lógica de negocio.
4. **Desplegar y probar el workflow en n8n.**

## Detalles de Funcionamiento
- El workflow inicia con la recepción de mensajes vía webhook desde WhatsApp.
- Utiliza modelos de lenguaje OpenAI y OpenRouter para interpretar y generar respuestas inteligentes.
- Emplea embeddings y vector stores para consultas contextuales sobre información clínica o FAQ.
- Integra lógica personalizada mediante nodos Switch, If y Merge para rutas y validaciones.
- Usa memoria persistente con PostgreSQL para mantener contexto conversacional.
- Realiza llamadas a Evolution API para consultar o actualizar datos clínicos.
- Genera respuestas estructuradas y auto-corrige posibles errores mediante nodos outputParser.
- Controla tiempos de espera y orden de mensajes con nodos Wait, Aggregate, y Sort.

## Ejemplos de Uso
- **Consulta de horarios y disponibilidad:** Un paciente escribe a WhatsApp y recibe información actualizada sobre citas.
- **Recordatorio de citas:** El sistema envía mensajes automáticos recordando próximos turnos.
- **Soporte y respuestas a preguntas frecuentes:** Respuestas automáticas a dudas comunes sobre tratamientos, precios y protocolos.
- **Actualización de datos del paciente:** El agente puede ayudarte a modificar datos personales consultando sistemas internos vía Evolution API.

---

**Etiquetas:** Whatsapp, Clínicas  
**Categoría:** agentes-ia/clinica-dental  
**Número de nodos:** 51  
**Nodos principales utilizados:**  
@n8n/n8n-nodes-langchain.openAi,  
@n8n/n8n-nodes-langchain.embeddingsOpenAi,  
@n8n/n8n-nodes-langchain.lmChatOpenRouter,  
@n8n/n8n-nodes-langchain.outputParserStructured,  
n8n-nodes-base.httpRequest,  
n8n-nodes-base.wait,  
n8n-nodes-base.webhook,  
@n8n/n8n-nodes-langchain.lmChatOpenAi,  
n8n-nodes-base.switch,  
n8n-nodes-evolution-api.evolutionApi,  
@n8n/n8n-nodes-langchain.outputParserAutofixing,  
n8n-nodes-base.redis,  
n8n-nodes-base.merge,  
n8n-nodes-base.if,  
@n8n/n8n-nodes-langchain.memoryPostgresChat,  
@n8n/n8n-nodes-langchain.agent,  
n8n-nodes-base.aggregate,  
n8n-nodes-base.noOp,  
@n8n/n8n-nodes-langchain.chainLlm,  
n8n-nodes-base.convertToFile,  
n8n-nodes-base.sort,  
@n8n/n8n-nodes-langchain.toolWorkflow,  
@n8n/n8n-nodes-langchain.vectorStoreSupabase,  
n8n-nodes-base.set,  
n8n-nodes-base.splitOut
```
