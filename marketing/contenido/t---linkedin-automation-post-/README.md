```markdown
# T - Linkedin Automation Post

## Descripción
Workflow de automatización para la generación y publicación de contenido en LinkedIn, integrando Google Sheets para disparadores y datos, junto con modelos de lenguaje OpenAI para creación de contenido inteligente.

## Requisitos
- Credenciales de Google Sheets configuradas en n8n.
- API Key de OpenAI para el nodo `lmChatOpenAi`.
- Acceso a LinkedIn (a través de API o herramienta externa para publicación, configuración personalizada).
- Permisos adecuados para conectar con APIs externas (HTTP Request).

## Instrucciones de configuración
1. Configura las credenciales de Google Sheets en n8n.
2. Ingresa tu API Key de OpenAI en el nodo `lmChatOpenAi`.
3. Ajusta el ID y rango de la hoja en el nodo `googleSheetsTrigger` y `googleSheets`.
4. Configura la lógica condicional y parámetros en los nodos `if` y `code` según tus reglas de publicación.
5. Configura el nodo `httpRequest` para enviar la publicación a LinkedIn o servicio intermediario.
6. Ajusta límites y lotes en los nodos `limit` y `splitInBatches` para controlar el flujo.

## Detalles de funcionamiento
- El workflow se inicia con un trigger de Google Sheets que detecta nuevos datos.
- Se procesan y generan publicaciones basadas en prompts mediante el modelo OpenAI.
- Se utilizan nodos de agente y parser estructurado para construir contenido coherente.
- La lógica condicional y el código personalizado garantizan validaciones y formato correcto.
- Finalmente, el contenido es enviado vía HTTP Request para su publicación en LinkedIn.

## Ejemplos de uso
- Automatizar publicaciones semanales en LinkedIn a partir de un calendario en Google Sheets.
- Generar contenido dinámico personalizado aprovechando modelos de lenguaje AI.
- Controlar el flujo de publicación con reglas específicas para evitar duplicados o errores.

---

**Número de nodos:** 14  
**Categoría:** marketing/contenido  
**Tipos de nodos:**  
`n8n-nodes-base.googleSheets`, `n8n-nodes-base.googleSheetsTrigger`, `n8n-nodes-base.limit`, `@n8n/n8n-nodes-langchain.lmChatOpenAi`, `n8n-nodes-base.merge`, `n8n-nodes-base.if`, `n8n-nodes-base.code`, `@n8n/n8n-nodes-langchain.agent`, `@n8n/n8n-nodes-langchain.outputParserStructured`, `n8n-nodes-base.splitInBatches`, `n8n-nodes-base.httpRequest`
```