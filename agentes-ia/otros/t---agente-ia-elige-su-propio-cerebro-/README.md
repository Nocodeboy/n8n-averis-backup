```markdown
# T - Agente IA Elige su propio cerebro

## Descripción

Workflow avanzado que implementa un agente IA capaz de elegir y gestionar múltiples "cerebros" o fuentes de conocimiento para responder y actuar de forma inteligente. Integra diversas herramientas y servicios para potenciar las capacidades del agente.

## Requisitos

- Credenciales y acceso a:
  - Google Sheets
  - Google Drive
  - Slack (bot y triggers)
  - Gmail
  - Airtable
  - Google Calendar
  - Supabase (vector store)
  - API OpenAI (para embeddings y modelos de lenguaje)
  - OpenRouter (modelo de chat)
- n8n con nodos de la comunidad `@n8n/n8n-nodes-langchain` instalados

## Instrucciones de configuración

1. Configura las credenciales necesarias en n8n:
   - Añade cuentas de Google, Slack, Gmail, Airtable y Supabase.
   - Inserta tu API Key de OpenAI y OpenRouter en los nodos correspondientes.
2. Ajusta parámetros en los nodos de Langchain según tus necesidades de embeddings y modelos de lenguaje.
3. Personaliza las rutas y hojas de cálculo en Google Sheets y Drive según el contexto.
4. Activa los triggers (Slack, manual y chat) para iniciar el workflow.
5. Revisa y adapta los accesos a Google Calendar y otras herramientas vinculadas.

## Detalles de funcionamiento

- Dispone de 43 nodos que orquestan tareas como:
  - Escucha eventos y mensajes via Slack.
  - Generación y uso de embeddings OpenAI para búsqueda vectorial en Supabase.
  - División avanzada de texto para procesamiento óptimo con el textSplitter.
  - Carga y manejo de documentos variados para alimentar al agente.
  - Interacción dinámicas con sistemas de correo, calendario y bases de datos.
  - Uso de un agente Langchain para decidir la mejor herramienta o fuente de información según contexto.
  - Guardado y gestión de notas internas (stickyNote).
- El agente revisa múltiples fuentes (“cerebros”) y elige la más adecuada para resolver consultas o ejecutar tareas.

## Ejemplos de uso

- Responder preguntas complejas combinando datos de Google Sheets, Airtable y documentos almacenados en Drive.
- Automatizar respuestas en Slack utilizando información actualizada de calendario y correos.
- Gestionar bases de conocimiento vectoriales para búsquedas contextuales avanzadas usando embeddings.
- Crear y actualizar notas o tareas internas mediante interacciones en canales de Slack o comandos manuales.

---

_Este workflow es una potente base para desarrollar agentes IA multifuncionales, personalizable según las fuentes de datos y servicios integrados._
```
