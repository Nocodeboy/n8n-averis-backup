```markdown
# 1. Main Agent - Agente IA Avanzado para Clínica Dental - WhatsApp

## Descripción
Workflow avanzado que actúa como un agente IA para gestionar interacciones y reservas en clínicas dentales a través de WhatsApp. Utiliza integración con APIs de lenguaje natural, bases de datos y servicios externos para ofrecer respuestas inteligentes, gestionar bookings y optimizar la experiencia del paciente.

## Requisitos
- Credenciales API para:
  - OpenAI (openAi, lmChatOpenAi)
  - OpenRouter (lmChatOpenRouter)
  - Google Gemini (lmChatGoogleGemini)
  - Evolution API (evolutionApi)
- Acceso a bases de datos PostgreSQL
- Airtable API Key y base configurada
- Credenciales Redis para almacenamiento de sesión y cache
- Integración con Gmail, Telegram y WhatsApp APIs
- Configuración de webhook para recepción de mensajes WhatsApp
- Permisos y API keys para herramientas personalizadas (mcpClientTool, agent, toolWorkflow)

## Instrucciones de Configuración
1. Importar el workflow en n8n.
2. Configurar todas las credenciales necesarias bajo "Credenciales" en n8n.
3. Ajustar los secretos y tokens en los nodos de integración (OpenAI, Airtable, PostgreSQL, Redis, Evolution API, Gmail, Telegram).
4. Configurar el webhook para recibir mensajes de WhatsApp y vincularlo con la plataforma correspondiente.
5. Verificar la conexión con bases de datos y herramientas externas.
6. Realizar pruebas de envío y recepción para validar conexión y permisos.

## Detalles de Funcionamiento
- El flujo inicia con un disparador manual o webhook que recibe mensajes entrantes de WhatsApp.
- Se procesan consultas mediante modelos de lenguaje (OpenAI, OpenRouter, Google Gemini).
- Se aplica lógica de filtrado y parsing estructurado para extraer información relevante (reservas, dudas, datos personales).
- Datos se consultan y actualizan en Airtable y PostgreSQL para manejar bookings y estados.
- El agente puede ejecutar herramientas adicionales para gestionar tareas específicas (mcpClientTool, evolutionApi).
- Mensajes de respuesta se envían vía WhatsApp, Gmail o Telegram según el contexto.
- Se almacena el contexto y memoria de conversación en Redis y PostgreSQL para continuidad y personalización.
- Nodo de espera, switches y filtros permiten manejo dinámico de flujos y contingencias.
- Uso de nodos de agregación, combinación y conversión para formatear respuesta final y reportes.

## Ejemplos de Uso
- Paciente envía un mensaje por WhatsApp para agendar cita dental.
- El agente IA reconoce la intención, consulta disponibilidad en base de datos e confirma booking.
- Responde automáticamente con detalles de la cita y opciones de rescheduling.
- En caso de duda, ejecuta llamada a Evolution API para obtener información adicional.
- Envío de notificaciones posteriores vía Gmail o Telegram para recordatorios.

---

## Detalles Adicionales

- **Categoría:** agentes-ia/clinica-dental  
- **Número de nodos:** 95  
- **Tipos de nodos utilizados:**  
  `@n8n/n8n-nodes-langchain.openAi`, `@n8n/n8n-nodes-langchain.lmChatOpenRouter`, `n8n-nodes-base.airtableTool`, `@n8n/n8n-nodes-langchain.outputParserStructured`, `n8n-nodes-base.httpRequest`, `n8n-nodes-base.wait`, `n8n-nodes-base.webhook`, `@n8n/n8n-nodes-langchain.lmChatOpenAi`, `n8n-nodes-base.switch`, `@n8n/n8n-nodes-langchain.mcpClientTool`, `@n8n/n8n-nodes-langchain.lmChatGoogleGemini`, `n8n-nodes-base.filter`, `n8n-nodes-base.gmailTool`, `n8n-nodes-base.stickyNote`, `n8n-nodes-base.postgres`, `n8n-nodes-evolution-api.evolutionApi`, `@n8n/n8n-nodes-langchain.outputParserAutofixing`, `n8n-nodes-base.telegramTool`, `n8n-nodes-base.merge`, `n8n-nodes-base.redis`, `n8n-nodes-base.if`, `n8n-nodes-base.manualTrigger`, `@n8n/n8n-nodes-langchain.memoryPostgresChat`, `@n8n/n8n-nodes-langchain.agent`, `n8n-nodes-base.aggregate`, `n8n-nodes-base.noOp`, `@n8n/n8n-nodes-langchain.chainLlm`, `n8n-nodes-base.convertToFile`, `n8n-nodes-base.sort`, `n8n-nodes-base.code`, `@n8n/n8n-nodes-langchain.toolWorkflow`, `n8n-nodes-base.set`, `n8n-nodes-base.splitOut`

## Etiquetas
Averis, Whatsapp, Clínicas, Booking, *****
```