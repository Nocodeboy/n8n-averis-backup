```markdown
# Email Agente Worker

## Descripción
Workflow diseñado para gestionar y automatizar tareas relacionadas con el correo electrónico mediante agentes inteligentes. Utiliza modelos de lenguaje y herramientas de Gmail para procesar, analizar y responder emails de forma autónoma.

## Requisitos
- Credenciales de Gmail con permisos para lectura y envío de correos.
- API Key de OpenAI para el nodo `lmChatOpenAi`.
- n8n instalado con los siguientes nodos disponibles:
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`
  - `n8n-nodes-base.gmailTool`
  - `@n8n/n8n-nodes-langchain.agent`
  - `n8n-nodes-base.set`
  - `n8n-nodes-base.executeWorkflowTrigger`

## Instrucciones de configuración
1. Configure las credenciales de Gmail en n8n.
2. Añada la API Key de OpenAI en las credenciales correspondientes.
3. Importe o copie el workflow en su instancia n8n.
4. Revise y adapte las configuraciones específicas de cada nodo según su entorno y necesidades.

## Detalles de funcionamiento
El workflow cuenta con 12 nodos que coordinan la recepción de correos, análisis mediante un modelo de lenguaje, ejecución de agentes para acciones específicas, y respuestas automáticas. Utiliza gatillos para iniciar procesos, nodos de configuración y agentes basados en Langchain para manejar tareas complejas.

## Ejemplos de uso
- Automatizar respuestas a consultas frecuentes recibidas por email.
- Filtrar y categorizar mails usando inteligencia artificial.
- Ejecutar acciones específicas en base al contenido del correo recibido.
- Coordinar trabajo entre agentes para gestión avanzada de emails.

---

**Categoría:** agentes-ia/otros  
**Etiquetas:** Worker, Agente  
**Número de nodos:** 12
```