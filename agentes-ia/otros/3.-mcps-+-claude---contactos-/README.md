```markdown
# 3. MCPs + Claude - Contactos

## Descripción
Workflow que integra agentes IA con Google Contacts para gestionar y analizar contactos mediante Claude y Google Gemini, optimizando la interacción y manejo de información.

## Requisitos
- Credenciales de Google Contacts API configuradas en n8n.
- Acceso a los nodos de LangChain correspondientes:
  - `@n8n/n8n-nodes-langchain.lmChatGoogleGemini`
  - `@n8n/n8n-nodes-langchain.agent`
- Permisos para ejecutar workflows en n8n.
  
## Instrucciones de configuración
1. Configure las credenciales de Google Contacts en n8n con acceso a su cuenta.
2. Asegúrese de tener las APIs de LangChain y Google Gemini disponibles y vinculadas.
3. Importe el workflow en n8n.
4. Revise y personalice los parámetros de cada nodo según sus necesidades específicas.

## Detalles de funcionamiento
- Utiliza `executeWorkflowTrigger` para iniciar el proceso.
- Obtiene datos de contactos con `googleContactsTool`.
- Procesa y analiza los datos mediante agentes IA con nodos `lmChatGoogleGemini` y `agent`.
- Usa el nodo `set` para manipular datos intermedios y preparar la información final.

## Ejemplos de uso
- Automatizar la clasificación y enriquecimiento de contactos en Google Contacts.
- Responder consultas o generar insights sobre la base de contactos utilizando IA integrada.
- Integrar flujos automatizados que combinen datos de contactos con capacidades avanzadas de lenguaje natural.

---
**Categoría:** agentes-ia/otros  
**Número de nodos:** 5  
**Tipos de nodos utilizados:** `@n8n/n8n-nodes-langchain.lmChatGoogleGemini`, `n8n-nodes-base.googleContactsTool`, `@n8n/n8n-nodes-langchain.agent`, `n8n-nodes-base.set`, `n8n-nodes-base.executeWorkflowTrigger`
```