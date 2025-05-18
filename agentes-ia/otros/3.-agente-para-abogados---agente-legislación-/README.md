```markdown
# 3. Agente para Abogados - Agente legislación

## Descripción  
Workflow de n8n diseñado como un agente inteligente para abogados, especializado en legislación. Utiliza modelos de lenguaje y vectores semánticos para responder consultas legales con precisión, apoyándose en fuentes documentales.

## Requisitos  
- Credenciales de OpenAI con acceso a las APIs de embeddings y chat (`embeddingsOpenAi`, `lmChatOpenAi`).  
- Acceso a una instancia de Qdrant para el almacenamiento y consulta vectorial (`vectorStoreQdrant`).  
- n8n instalado y configurado.  

## Instrucciones de configuración  
1. Configure las credenciales de OpenAI en n8n.  
2. Configure las credenciales y conexión con la instancia de Qdrant.  
3. Importe el workflow en n8n.  
4. Ajuste los parámetros de los nodos si fuese necesario (e.g., collection de Qdrant, prompts).  
5. Active y ejecute el workflow para comenzar a recibir consultas.  

## Detalles de funcionamiento  
- El nodo `executeWorkflowTrigger` inicia la captura de la consulta.  
- `set` prepara los datos para su procesamiento.  
- `embeddingsOpenAi` genera vectores semánticos a partir de la consulta.  
- `vectorStoreQdrant` realiza la búsqueda semántica en la base de datos legal.  
- `lmChatOpenAi` formula respuestas basadas en la información encontrada.  
- `agent` orquesta el flujo y la lógica de interacción para entregar respuestas contextuales.  

## Ejemplos de uso  
- Consultas sobre normativas vigentes.  
- Búsqueda de jurisprudencia relevante.  
- Obtención de resúmenes legales sobre temas específicos.  

---

**Categoría:** agentes-ia/otros  
**Tipo de nodos:**  
- `@n8n/n8n-nodes-langchain.embeddingsOpenAi`  
- `@n8n/n8n-nodes-langchain.lmChatOpenAi`  
- `@n8n/n8n-nodes-langchain.agent`  
- `n8n-nodes-base.set`  
- `n8n-nodes-base.executeWorkflowTrigger`  
- `@n8n/n8n-nodes-langchain.vectorStoreQdrant`  

**Número de nodos:** 7  
**Etiquetas:** (ninguna)  
```