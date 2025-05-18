```markdown
# Contact agent

## Descripción
Workflow diseñado para gestionar la comunicación y automatización con agentes de IA mediante nodos de LangChain, integrando herramientas como Airtable para el almacenamiento y manipulación de datos.

## Requisitos
- Credenciales de OpenAI para el nodo `lmChatOpenAi`.
- Acceso a Airtable con API Key y base configurada para `airtableTool`.
- n8n instalado con los siguientes nodos disponibles:
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`
  - `@n8n/n8n-nodes-langchain.agent`
  - `n8n-nodes-base.set`
  - `n8n-nodes-base.executeWorkflowTrigger`
  - `n8n-nodes-base.airtableTool`

## Instrucciones de configuración
1. Configura las credenciales de OpenAI en n8n.
2. Añade y configura el acceso a Airtable con tu API Key y la base/datos correspondientes.
3. Importa el workflow en n8n.
4. Ajusta los nodos `set` y `agent` según tus necesidades específicas.
5. Activa o ejecuta el workflow manualmente o mediante el trigger configurado.

## Detalles de funcionamiento
El workflow consta de 7 nodos que interactúan para recibir inputs, procesarlos a través de un agente IA usando LangChain, y almacenar o actualizar información en Airtable. Utiliza:
- Un nodo trigger para iniciar el flujo.
- Un nodo `set` para definir parámetros iniciales.
- Un agente IA que procesa la consulta usando `lmChatOpenAi`.
- Integración con Airtable para persistencia y consulta de datos.

## Ejemplos de uso
- Automatización de atención al cliente a través de agentes conversacionales.
- Gestión y seguimiento de solicitudes o tareas registradas en Airtable.
- Procesamiento automatizado de consultas complejas usando IA integrada.

---
**Categoría:** agentes-ia/otros  
**Nodos utilizados:** @n8n/n8n-nodes-langchain.lmChatOpenAi, @n8n/n8n-nodes-langchain.agent, n8n-nodes-base.set, n8n-nodes-base.executeWorkflowTrigger, n8n-nodes-base.airtableTool  
**Número de nodos:** 7
```