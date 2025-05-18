```markdown
# Agente IA Whatsapp Averis - Base

## Descripción

Workflow diseñado para gestionar interacciones automatizadas en Whatsapp mediante agentes de inteligencia artificial. Integra procesamiento de lenguaje natural, manejo de memoria y conexión con diversas APIs para ofrecer respuestas contextuales y enriquecidas.

## Requisitos

- Credenciales de API de OpenAI (para nodos `openAi`, `embeddingsOpenAi`, `lmChatOpenAi`, `lmChatOpenRouter`)
- Credenciales de Evolution API (`n8n-nodes-evolution-api.evolutionApi`)
- Acceso a Redis (`n8n-nodes-base.redis`) para almacenamiento temporal
- Base de datos Postgres configurada para memoria de chat (`memoryPostgresChat`)
- Acceso y credenciales para Supabase Vector Store (`vectorStoreSupabase`)
- Credenciales para Google Docs (opcional, para integración con `googleDocsTool`)
- Configuración de webhook n8n para recepción de mensajes

## Instrucciones de configuración

1. **Configurar credenciales:**
   - Instalar y enlazar credenciales de OpenAI y Evolution API en n8n.
   - Configurar conexión Redis y Postgres para persistencia y memoria.
   - Añadir credenciales de Supabase y Google Docs si aplica.

2. **Importar el workflow:**
   - Cargar el archivo JSON del workflow en n8n.

3. **Ajustar variables y parámetros:**
   - Modificar nodos `set` para personalizar mensajes, llaves y rutas.
   - Configurar webhook URL para recibir mensajes entrantes de Whatsapp.

4. **Activar el workflow:**  
   - Poner en modo activo para comenzar a procesar.

## Detalles de funcionamiento

- El webhook recoge mensajes entrantes desde Whatsapp.
- Se procesan utilizando modelos OpenAI y OpenRouter para análisis y generación de respuestas.
- Se usan parsers estructurados y autofixing para asegurar claridad y coherencia.
- La memoria de chat queda almacenada en Postgres para mantener contexto.
- Redis se usa para sincronización y almacenamiento temporal.
- Se emplean herramientas externas como Google Docs y Supabase para enriquecer la interacción.
- Lógica condicional y de espera permiten control fluido del flujo de conversación.
- El agente IA evalúa alternativas vía el nodo agente para resolver consultas complejas.
- El workflow está compuesto por 47 nodos que trabajan en conjunto para una experiencia automatizada y robusta.

## Ejemplos de uso

- **Responder consultas de clientes vía Whatsapp** con contexto almacenado y memorización.
- **Automatizar atención y soporte** basado en IA para flujos conversacionales dinámicos.
- **Integrar documentación externa** (Google Docs) para enriquecer respuestas.
- **Realizar búsquedas semánticas** en bases de conocimiento vía embeddings OpenAI y Supabase.

---

**Categoría:** agentes-ia/whatsapp  
**Etiquetas:** Agente, Whatsapp, Test  
**Número de nodos:** 47  
**Nodos principales utilizados:**  
`@n8n/n8n-nodes-langchain.openAi`, `embeddingsOpenAi`, `lmChatOpenRouter`, `outputParserStructured`, `wait`, `webhook`, `lmChatOpenAi`, `switch`, `evolutionApi`, `outputParserAutofixing`, `redis`, `if`, `memoryPostgresChat`, `agent`, `noOp`, `chainLlm`, `googleDocsTool`, `convertToFile`, `vectorStoreSupabase`, `set`
```