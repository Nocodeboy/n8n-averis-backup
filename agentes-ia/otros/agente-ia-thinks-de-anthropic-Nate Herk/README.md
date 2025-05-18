```markdown
# Agente IA Thinks de Anthropic

## Descripción  
Workflow de n8n que implementa un agente de Inteligencia Artificial basado en Anthropic, integrado con múltiples nodos de LangChain y herramientas externas para procesamiento avanzado de texto, manejo de vectores, correos y automatización de tareas.

## Requisitos  
- Credenciales de API para:
  - Anthropic (LM Chat Anthropic)  
  - OpenAI (modelos OpenAi y embeddings)  
  - Google Gemini (lmChatGoogleGemini)  
  - Pinecone (vectorStore)  
  - Gmail (gmailTool)  
  - Airtable (airtableTool)  
- n8n con los siguientes nodos instalados:  
  - `@n8n/n8n-nodes-langchain` (varios subnodos)  
  - `n8n-nodes-base` (gmailTool, stickyNote, airtableTool, executeWorkflowTrigger)  

## Instrucciones de configuración  
1. Importa el workflow en tu instancia de n8n.  
2. Configura las credenciales API mencionadas en el apartado de Requisitos.  
3. Ajusta los nodos con tus parámetros específicos (p. ej. IDs de Pinecone, hojas de Airtable, cuentas Gmail).  
4. Verifica que los disparadores (`chatTrigger`, `executeWorkflowTrigger`) estén habilitados para iniciar el workflow.  

## Detalles de funcionamiento  
- El agente procesa consultas y tareas utilizando varios modelos de lenguaje y herramientas especializadas.  
- Integra embedding de texto para búsqueda y recuperación basada en vectores con Pinecone.  
- Usa Gmail para envíos y gestión de correos automáticos.  
- Almacena y recupera información desde Airtable.  
- Combina triggers conversacionales y ejecutores para orquestar múltiples flujos internos.  
- Incluye nodos para notas adhesivas (stickyNote) y llamadas HTTP personalizadas.  

## Ejemplos de uso  
- Responder preguntas complejas mediante combinación de motores IA.  
- Automatizar respuestas y notificaciones por correo electrónico.  
- Crear agentes conversacionales que integran datos almacenados en Airtable y vectores de Pinecone.  
- Ejecutar sub-workflows mediante herramientas internas del agente para modularidad y escalabilidad.  

---

**Número de nodos:** 38  
**Categoría:** agentes-ia/otros  
**Etiquetas:** Nate Herk  
**Nodos principales utilizados:**  
`@n8n/n8n-nodes-langchain.openAi`, `lmChatOpenAi`, `embeddingsOpenAi`, `lmChatGoogleGemini`, `lmChatAnthropic`, `toolWorkflow`, `gmailTool`, `stickyNote`, `toolThink`, `agent`, `vectorStorePinecone`, `airtableTool`, `toolHttpRequest`, `executeWorkflowTrigger`, `chatTrigger`  
```