```markdown
# Gestión de Tickets y Soporte

## Descripción  
Workflow diseñado para automatizar la gestión de tickets y soporte utilizando agentes de IA. Integra procesamiento inteligente de lenguaje natural, manejo de datos en Airtable y sistemas de toma de decisiones para optimizar la respuesta y seguimiento de solicitudes.

## Requisitos  
- Credenciales de Airtable con acceso a la base de datos de tickets.  
- API Key de OpenAI para el nodo `lmChatOpenAi`.  
- API Key de Google Gemini para el nodo `lmChatGoogleGemini`.  
- Configuración de webhook público para recibir y procesar solicitudes externas.  
- Acceso a internet para nodos HTTP y herramientas de llamadas API.

## Instrucciones de configuración  
1. Ingrese las credenciales de Airtable en la sección correspondiente del workflow.  
2. Configure las API Keys de OpenAI y Google Gemini en los nodos respectivos.  
3. Establezca el endpoint del webhook y asegúrese que sea accesible externamente.  
4. Modifique los parámetros de los nodos `switch` y `aggregate` para adaptarse a los criterios de su flujo de tickets.  
5. Revise y personalice los templates de mensajes en nodos `markdown` y `stickyNote` según necesidades.  

## Detalles de funcionamiento  
- Recepción de solicitudes a través del nodo `webhook`.  
- Análisis y clasificación de tickets usando agentes basados en Langchain (`lmChatOpenAi`, `lmChatGoogleGemini`, `chainLlm` y `agent`).  
- Enriquecimiento y agrupación de datos con `aggregate` y procesamiento lógico con `switch`.  
- Almacenamiento y actualización de registros en Airtable para seguimiento.  
- Uso de nodos `httpRequest` y `toolHttpRequest` para integraciones externas adicionales.  
- Generación de reportes y notas en formatos markdown y notas adhesivas para facilitar la revisión.

## Ejemplos de uso  
- Automatizar respuestas iniciales y derivación de tickets según complejidad.  
- Clasificar solicitudes en categorías personalizadas mediante IA.  
- Sincronizar tickets con bases de datos centralizadas y sistemas externos.  
- Generar resúmenes estructurados de conversaciones y acciones realizadas.  

---

**Categoría:** agentes-ia/otros  
**Etiquetas:** Circle, Perplexity  
**Número de nodos:** 27  
**Nodos principales usados:**  
`aggregate`, `lmChatOpenAi`, `switch`, `lmChatGoogleGemini`, `chainLlm`, `agent`, `set`, `airtable`, `stickyNote`, `outputParserStructured`, `splitOut`, `httpRequest`, `toolHttpRequest`, `markdown`, `webhook`
```