```markdown
# Scrappeador de Emails Google Maps

## Descripción
Workflow diseñado para extraer y recopilar correos electrónicos de negocios listados en Google Maps, automatizando el proceso de scraping y gestión de datos con integración en Google Sheets y Gmail.

## Requisitos
- Cuenta de Google con acceso a Google Drive y Google Sheets.
- Credenciales configuradas para las siguientes APIs y nodos:
  - Google Drive
  - Google Sheets
  - Gmail
- API Key de OpenAI para usar los nodos de LangChain (`lmChatOpenAi`, `chainLlm`, `outputParserStructured`).
- Acceso a n8n con los nodos necesarios instalados:
  - `n8n-nodes-base.aggregate`
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`
  - `n8n-nodes-base.limit`
  - `n8n-nodes-base.googleDrive`
  - `n8n-nodes-base.googleSheets`
  - `@n8n/n8n-nodes-langchain.chainLlm`
  - `n8n-nodes-base.formTrigger`
  - `n8n-nodes-base.filter`
  - `n8n-nodes-base.code`
  - `n8n-nodes-base.gmail`
  - `n8n-nodes-base.stickyNote`
  - `@n8n/n8n-nodes-langchain.outputParserStructured`
  - `n8n-nodes-base.splitInBatches`
  - `n8n-nodes-base.httpRequest`
  - `n8n-nodes-base.splitOut`
  - `n8n-nodes-base.removeDuplicates`

## Instrucciones de configuración
1. Importa el workflow en tu instancia de n8n.
2. Configura las credenciales de Google Drive, Google Sheets y Gmail en n8n.
3. Añade tu API Key de OpenAI en el nodo de LangChain.
4. Ajusta los parámetros del nodo `formTrigger` para iniciar el flujo según tus necesidades.
5. Define las URLs o términos de búsqueda en Google Maps para iniciar el scraping.
6. Revisa y personaliza los filtros y límites según volumen de datos esperado.

## Detalles de funcionamiento
- El workflow inicia con un disparador de formulario.
- Extrae datos desde Google Maps utilizando solicitudes HTTP y procesamiento en lotes.
- Procesa y limpia los datos para obtener únicamente emails válidos, eliminando duplicados.
- Aplica modelos de lenguaje de OpenAI mediante LangChain para mejorar la extracción y validación de correos.
- Agrega y almacena los datos finales en Google Sheets.
- Opcionalmente, envía notificaciones o correos desde Gmail con los resultados.
- Utiliza nodos de agregación, filtros, código personalizado y notas adhesivas para control y monitoreo interno.

## Ejemplos de uso
- Recopilar emails de negocios locales para campañas de marketing.
- Generar bases de datos de contacto para equipos comerciales.
- Automatizar la extracción periódica de información de Google Maps y actualizar hojas de cálculo.

---

**Categoría:** utilidades/scraping  
**Etiquetas:** Averis, Scrapping  
**Número de nodos:** 24  
```