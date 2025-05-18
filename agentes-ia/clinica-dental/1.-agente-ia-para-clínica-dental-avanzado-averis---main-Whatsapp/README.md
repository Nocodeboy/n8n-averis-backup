```markdown
# 1. Agente IA para Clínica Dental Avanzado Averis - Main

## Descripción
Workflow avanzado diseñado para gestionar operaciones clave de una clínica dental utilizando agentes de inteligencia artificial. Integra comunicación vía WhatsApp, gestión de reservas (Booking), y procesamiento avanzado de datos para optimizar la experiencia del paciente en la plataforma Averis.

## Requisitos
- Credenciales de OpenAI (para nodos LangChain: OpenAi, lmChatOpenAi, lmChatGoogleGemini, chainLlm)
- Acceso a Google Docs API
- Credenciales para Gmail API
- API de Evolution (n8n-nodes-evolution-api.evolutionApi)
- Acceso a Redis para almacenamiento temporal y cache
- Base de datos Postgres configurada para memoria de agentes (memoryPostgresChat)
- Webhook externo configurado (para integración con WhatsApp)
- Acceso a Telegram API (opcional, para notificaciones)
- Permisos y claves para MCP Client Tool y otras herramientas integradas en LangChain

## Instrucciones de configuración
1. Configure las credenciales en n8n para cada servicio: OpenAI, Google Docs, Gmail, Evolution API, Redis, Postgres, Telegram, entre otros.
2. Establezca las URLs y tokens para los webhooks usados, asegurándose que estén activos y accesibles.
3. Ajuste los parámetros específicos de su clínica en nodos de configuración, como datos de Booking y plantilla de documentos en Google Docs.
4. Importe el workflow completo en n8n, revise conexiones y habilite los nodos según corresponda.
5. Realice pruebas iniciales simulando interacciones para verificar la respuesta y almacenamiento de memoria.

## Detalles de funcionamiento
El workflow consta de 96 nodos que permiten:
- Recepción y procesamiento de mensajes vía WhatsApp y Telegram.
- Consultas y gestión de reservas en Booking.
- Uso de modelos avanzados de Lenguaje Natural (LangChain con OpenAI y Google Gemini) para interpretar y responder solicitudes.
- Creación y actualización de documentos en Google Docs.
- Uso de herramientas especiales como MCP Client Tool y output parsers para respuestas estructuradas y auto-corrección.
- Almacenamiento de contexto conversacional y memoria a largo plazo mediante Redis y Postgres.
- Control de flujo con nodos switch, if y merge para adaptación a distintas situaciones.
- Envío de notificaciones y correos electrónicos a través de Gmail.
- Manejo de espera y sincronización entre tareas con nodos wait y aggregate.

## Ejemplos de uso
- Un paciente envía un mensaje vía WhatsApp solicitando una cita; el agente identifica la solicitud, consulta disponibilidad en Booking y confirma la reserva automáticamente.
- El sistema genera un resumen en Google Docs de la interacción clínica para el seguimiento interno.
- Se envían notificaciones por email o Telegram para confirmar citas o recordar próximas visitas.
- El agente usa memoria almacenada para personalizar respuestas según historial del paciente.

---

**Etiquetas:** `Whatsapp`, `Booking`, `Clínicas`, `Averis`  
**Categoría:** agentes-ia/clinica-dental  
**Número de nodos:** 96
```