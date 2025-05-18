```markdown
# 1. Main Agent - Agente IA Ecommerce RAG Avanzado en WhatsApp byAveris

## Descripción

Workflow avanzado para gestión de ecommerce mediante un agente IA RAG (Retrieval-Augmented Generation) integrado en WhatsApp. Facilita atención al cliente, ventas y soporte con respuestas contextuales basadas en datos actualizados y diversas fuentes.

## Requisitos

- Cuenta activa en n8n con permisos para importar workflows complejos.
- Credenciales y APIs configuradas para:
  - OpenAI (modelos GPT y embeddings)
  - OpenRouter (modelos de chat)
  - Google Gemini (modelo de chat)
  - Supabase (vector store y memoria Postgres)
  - Airtable (gestión de datos)
  - Gmail (herramientas de correo)
  - Google Drive (disparadores y archivos)
  - PostgreSQL (memoria y almacenamiento)
  - Redis (cache/almacenamiento temporal)
  - Evolution API (API externa específica)
- Webhook para integración con WhatsApp (por ejemplo, Twilio u otro proveedor compatible).
- Acceso y permisos a las bases de datos y servicios listados.

## Instrucciones de configuración

1. Importar el workflow `1. Main Agent - Agente IA Ecommerce RAG Avanzado en WhatsApp byAveris` en n8n.
2. Configurar las credenciales necesarias en n8n para cada nodo/API:
   - OpenAI, OpenRouter, Google Gemini
   - Supabase, Airtable, PostgreSQL, Redis
   - Gmail, Google Drive, Evolution API
3. Establecer el webhook para recibir mensajes de WhatsApp y hacer trigger del flujo.
4. Ajustar parámetros específicos en nodos (limites, filtros, batches) según volumen y uso esperado.
5. Validar permisos y accesos a las bases de datos y recursos conectados.
6. Realizar pruebas de interacción para asegurar respuestas adecuadas y correcta integración.

## Detalles de funcionamiento

- El agente utiliza múltiples modelos de lenguaje (OpenAI, OpenRouter, Google Gemini) para generación y comprensión avanzada.
- Apoyo en memoria a través de Postgres y Redis para mantener contexto conversacional y datos del cliente.
- Manejo y procesamiento de documentos mediante text splitters y loaders para consulta eficiente.
- Integración con herramientas externas para soporte, correo y almacenamiento.
- Uso de nodos condicionales, agrupadores y limitadores para controlar flujo, rendimiento y lógica del proceso.
- Capacidad de dividir y unir datos para procesamiento por lotes.
- Automatización rica en funciones para elector respuestas, sumarizaciones y extracción de información estructurada.

## Ejemplos de uso

- Atención personalizada en WhatsApp con contexto histórico y datos actualizados del cliente y productos.
- Generación de respuestas en lenguaje natural para consultas de stock, precios y recomendaciones.
- Soporte postventa con acceso rápido a información almacenada en Airtable y bases relacionales.
- Notificaciones automáticas de estado de pedidos vía Gmail y WhatsApp.
- Manejo avanzado de documentos y archivos relacionados con ecommerce mediante integración con Google Drive.

---

**Categoría:** agentes-ia/ecommerce  
**Etiquetas:** Averis, Customer / Sales, Whatsapp, *****  
**Número de nodos:** 135
```