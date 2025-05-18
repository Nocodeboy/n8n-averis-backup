```markdown
# Extracción de datos de Facturas

## Descripción
Workflow diseñado para extraer y procesar datos de facturas recibidas vía Telegram, integrando inteligencia artificial para la interpretación y estructuración automática de la información con soporte en Google Sheets y Google Drive.

## Requisitos
- Credenciales configuradas en n8n para:
  - Telegram (bot API)
  - Google Sheets
  - Google Drive
- API Key de OpenAI para el nodo `lmChatOpenAi`
- Acceso a la cadena de LangChain para procesamiento avanzado de lenguaje

## Instrucciones de configuración
1. Configure el bot de Telegram y obtenga el token para el nodo `telegramTrigger` y `telegram`.
2. Proporcione la API Key de OpenAI en el nodo `lmChatOpenAi`.
3. Configure las credenciales de Google Sheets y Google Drive en n8n.
4. Ajuste las hojas de cálculo y carpetas de Google Drive en los nodos correspondientes según su estructura.
5. Verifique las reglas del nodo `switch` para la correcta ramificación del flujo.

## Detalles de funcionamiento
- El flujo inicia con la recepción de mensajes en Telegram mediante `telegramTrigger`.
- Dependiendo del contenido, el mensaje pasa por un `switch` para definir la ruta de procesamiento.
- Los datos se envían a los nodos de LangChain (`lmChatOpenAi`, `chainLlm`, `outputParserStructured`) para extracción y estructuración de la información.
- Los datos estructurados se almacenan en Google Sheets y los archivos asociados en Google Drive.
- El nodo `merge` combina la información para enviar una respuesta al usuario vía Telegram.
- Se utilizan nodos `wait` y `set` para controlar temporizaciones y administrar variables internas.
- También se realizan llamadas HTTP con `httpRequest` para integraciones externas si es necesario.

## Ejemplos de uso
- Un usuario envía una foto o texto de una factura vía Telegram.
- El workflow extrae automáticamente campos clave: fecha, total, proveedor, etc.
- Los datos quedan registrados en una hoja de Google Sheets para seguimiento administrativo.
- El usuario recibe confirmación inmediata en Telegram con el resumen de los datos extraídos.

---

**Categoría:** agentes-ia/telegram  
**Etiquetas:** Averis, Telegram, Administración  
**Número de nodos:** 19  
**Nodos utilizados:**  
`n8n-nodes-base.googleSheets`, `@n8n/n8n-nodes-langchain.lmChatOpenAi`, `n8n-nodes-base.telegramTrigger`, `n8n-nodes-base.switch`, `n8n-nodes-base.googleDrive`, `n8n-nodes-base.merge`, `@n8n/n8n-nodes-langchain.chainLlm`, `n8n-nodes-base.telegram`, `n8n-nodes-base.set`, `@n8n/n8n-nodes-langchain.outputParserStructured`, `n8n-nodes-base.httpRequest`, `n8n-nodes-base.wait`
```