```markdown
# Agente IA de ventas con Revisión Humana - Averis

## Descripción
Workflow diseñado para automatizar la gestión de ventas mediante un agente IA que interactúa con clientes y realiza revisiones humanas antes de enviar comunicaciones, optimizando el proceso comercial y garantizando calidad en las respuestas.

## Requisitos
- Credenciales de API para OpenAI (ChatGPT o modelo compatible)
- Cuenta y credenciales de Gmail para envío de correos
- Cuenta y credenciales de Airtable para gestión y almacenamiento de datos
- n8n con los siguientes nodos disponibles:
  - @n8n/n8n-nodes-langchain.lmChatOpenAi
  - n8n-nodes-base.formTrigger
  - n8n-nodes-base.gmail
  - @n8n/n8n-nodes-langchain.agent
  - n8n-nodes-base.airtableTool
  - n8n-nodes-base.airtable
  - @n8n/n8n-nodes-langchain.outputParserStructured
  - @n8n/n8n-nodes-langchain.textClassifier

## Instrucciones de configuración
1. **Configuración de credenciales**  
   - Configure las credenciales de OpenAI en n8n para el nodo `lmChatOpenAi`.  
   - Configure las credenciales de Gmail para el nodo `gmail`.  
   - Configure las credenciales de Airtable con acceso a las bases y tablas necesarias.
2. **Ajustes del workflow**  
   - Configure el nodo `formTrigger` para captar solicitudes de clientes.  
   - Configure los nodos de Airtable para almacenar y consultar registros de clientes y ventas.  
   - Ajuste parámetros del agente IA y clasificadores según las necesidades específicas del flujo comercial.
3. **Permisos y conexiones**  
   Asegúrese de que las APIs y servicios externos tienen los permisos necesarios para lectura y escritura.

## Detalles de funcionamiento
- El workflow inicia con la recepción de solicitudes a través del nodo `formTrigger`.
- El agente IA, mediante `lmChatOpenAi` y el nodo `agent` de LangChain, procesa la solicitud, generando una respuesta inicial.
- La respuesta se envía a un nodo `outputParserStructured` para estructurar el contenido, y a un `textClassifier` para categorizar la interacción.
- Toda información relevante se almacena o consulta desde Airtable con los nodos `airtable` y `airtableTool`.
- Antes del envío definitivo, la comunicación pasa por una revisión humana para asegurar calidad.
- Finalmente, al aprobarse, se envía el correo personalizado al cliente mediante el nodo `gmail`.

## Ejemplos de uso
- Atención y seguimiento automatizado de solicitudes de clientes en ventas.  
- Clasificación y priorización de leads mediante IA con supervisión humana.  
- Automatización parcial del envío de ofertas comerciales con validación manual.  
- Registro y análisis de interacción en Airtable para mejoras continuas del proceso comercial.

---

**Categoría:** agentes-ia/otros  
**Etiquetas:** Averis, Customer / Sales, Agente  
**Número de nodos:** 10
```