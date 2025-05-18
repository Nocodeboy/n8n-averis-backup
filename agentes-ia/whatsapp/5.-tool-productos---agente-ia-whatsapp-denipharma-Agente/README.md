```markdown
# 5. Tool Productos - Agente IA WhatsApp Denipharma

## Descripción
Workflow diseñado para gestionar consultas de productos a través de un agente de inteligencia artificial integrado en WhatsApp, optimizado para el entorno Denipharma. Utiliza procesamiento de lenguaje natural y herramientas avanzadas para ofrecer respuestas precisas y dinámicas.

## Requisitos
- Credenciales de OpenAI para el nodo `lmChatOpenAi`.
- Acceso a la API de Google Gemini para embeddings (`embeddingsGoogleGemini`).
- Configuración y acceso a un vector store Qdrant (`vectorStoreQdrant`).
- Webhook o canal habilitado para la integración con WhatsApp.
- n8n instalado con los siguientes paquetes/nodos:
  - `@n8n/n8n-nodes-langchain`
  - `n8n-nodes-base`

## Instrucciones de configuración
1. **Configurar credenciales:**
   - Añadir las credenciales de OpenAI en n8n.
   - Configurar acceso a Google Gemini API.
   - Configurar el acceso y conexión al vector store Qdrant.
2. **Integrar WhatsApp:**
   - Configurar el webhook o disparador que conecte WhatsApp con el nodo `manualTrigger` o `executeWorkflowTrigger`.
3. **Ajustar nodos:**
   - Revisar y personalizar los nodos `code`, `set` y `if` según la lógica del negocio.
   - Verificar y personalizar llamadas HTTP si aplica.
4. **Activar workflow:**
   - Guardar y activar el workflow en n8n para que responda a mensajes.

## Detalles de funcionamiento
- El workflow inicia mediante un disparador manual o trigger de ejecución.
- Se procesan queries entrantes de WhatsApp y se analizan empleando Langchain con OpenAI para generar respuestas contextuales.
- Utiliza embeddings de Google Gemini para mejorar la búsqueda semántica en la base de productos almacenados.
- Qdrant actúa como vector store para almacenar y consultar datos relevantes de productos.
- El agente IA toma decisiones mediante nodos condicionales y herramientas de pensamiento (`toolThink`) para seleccionar la mejor acción.
- Puede ejecutar sub-workflows para tareas especializadas y ajustar dinámicamente las respuestas.

## Ejemplos de uso
- Usuario envía consulta “¿Qué productos tienen para el dolor muscular?”
- El agente IA procesa la consulta, busca en la base de datos vectorial y responde con los productos disponibles.
- Se pueden automatizar respuestas frecuentes, recomendaciones personalizadas o derivar consultas complejas a un agente humano.

---

**Categoría:** agentes-ia/whatsapp  
**Etiquetas:** Agente, Worker  
**Número de nodos:** 15  
**Nodos utilizados:** `@n8n/n8n-nodes-langchain.lmChatOpenAi`, `n8n-nodes-base.if`, `n8n-nodes-base.manualTrigger`, `@n8n/n8n-nodes-langchain.embeddingsGoogleGemini`, `n8n-nodes-base.executeWorkflow`, `n8n-nodes-base.code`, `@n8n/n8n-nodes-langchain.agent`, `n8n-nodes-base.set`, `n8n-nodes-base.executeWorkflowTrigger`, `n8n-nodes-base.stickyNote`, `@n8n/n8n-nodes-langchain.toolThink`, `n8n-nodes-base.httpRequest`, `@n8n/n8n-nodes-langchain.vectorStoreQdrant`
```