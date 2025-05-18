```markdown
# **** DEV**** Agente IA Avanzado WhatsApp

## Descripción  
Workflow avanzado para n8n que implementa un agente IA conversacional para WhatsApp, integrando capacidades de recuperación de información (RAG), memoria persistente y múltiples modelos de lenguaje (OpenAI, Google Gemini). Ideal para automatizar respuestas inteligentes, consultas de datos y procesos basados en IA sobre la plataforma WhatsApp.

## Requisitos  
- Credenciales de API para:
  - OpenAI (OpenAI GPT y ChatOpenRouter)
  - Google Gemini (lmChatGoogleGemini)
  - Airtable (para herramientas de consulta de datos)
  - Postgres (memoria y almacenamiento)
  - Gmail (automatización de correos si aplica)
  - Redis (cache y estados)
  - Evolution API (si se usa para datos externos)
- n8n con soporte a los nodos mencionados (versión recomendada acorde)
- Webhook público para recepción de mensajes desde WhatsApp (usualmente vía Twilio u otro gateway)

## Instrucciones de configuración  
1. Configure las credenciales correspondientes en n8n para cada servicio/API usado.  
2. Actualice los valores de conexión a bases de datos Postgres y Redis según su infraestructura.  
3. Ajuste los endpoints y tokens para las APIs externas (Airtable, Evolution API).  
4. Configure el webhook para recibir eventos de WhatsApp y conecte la URL pública con su gateway de WhatsApp.  
5. Modifique parámetros dentro del workflow según las necesidades específicas del agente o datos iniciales.

## Detalles de funcionamiento  
- Recepción de mensajes vía nodo webhook y preprocesamiento mediante filtros y switches.  
- Uso de modelos de lenguaje (OpenAI, Gemini, OpenRouter) para generación y procesamiento de respuestas.  
- Memoria conversacional persistente gestionada mediante Postgres y Redis para contexto a largo plazo.  
- Incorporación de herramientas auxiliares: consultas a Airtable, envíos de email, llamadas a APIs externas (Evolution API).  
- Uso de nodos especializados de Langchain para manejo de agentes, cadenas de pensamiento, parsing estructurado y flujos de herramientas integradas.  
- Control de flujo y esperas para sincronización y manejo eficiente de la conversación en tiempo real.  
- Más de 100 nodos orquestados para garantizar flexibilidad, robustez y escalabilidad.

## Ejemplos de uso  
- Responder consultas de clientes en WhatsApp con información actualizada desde bases Airtable o Postgres.  
- Realizar reservas, gestionar tickets o incidencias vía conversación natural.  
- Envío automático de correos electrónicos posteriores a interacciones clave.  
- Integración de información de APIs externas para respuestas enriquecidas en conversación (p.ej. datos de evolución clínica o de mercado).  
- Uso de memoria para mantener contexto en conversaciones prolongadas y mejorar la experiencia.

---

**Etiquetas:** Drive, RAG, OpenAi, Gemini, Whatsapp  
**Número de nodos:** 104  
**Categoría:** agentes-ia/whatsapp  
```