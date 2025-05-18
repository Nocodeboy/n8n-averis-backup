```markdown
# Scrapeador Anuncios Meta Ads

## Descripción
Workflow de n8n diseñado para extraer, procesar y organizar anuncios de Meta Ads utilizando scraping y procesamiento avanzado con herramientas de IA. Ideal para automatizar la recopilación y análisis de contenido publicitario.

## Requisitos
- Credenciales de Google Sheets y Google Drive con permisos de lectura/escritura.
- API Key de OpenAI para nodos LangChain (`openAi`, `lmChatOpenAi`, `lmChatOpenRouter`, `chainLlm`).
- Acceso a la API o endpoints necesarios para scraping de Meta Ads (configurable en nodos HTTP Request).
- n8n instalado y configurado con los paquetes de nodos mencionados.

## Instrucciones de configuración
1. Importar el workflow en n8n.
2. Configurar las credenciales de Google Sheets y Google Drive en n8n.
3. Añadir la clave API de OpenAI en los nodos correspondientes de LangChain.
4. Ajustar los parámetros de las peticiones HTTP para apuntar a las fuentes correctas de Meta Ads.
5. Verificar y configurar los límites de procesamiento por lote según la capacidad deseada.

## Detalles de funcionamiento
- El workflow inicia con un disparador manual o programado que activa la recopilación.
- Realiza scraping de anuncios desde Meta Ads mediante nodos HTTP Request.
- Procesa y limpia los datos en batch, aplicando lógica condicional para filtrado.
- Utiliza nodos de inteligencia artificial LangChain para analizar y estructurar el contenido.
- Almacena los resultados en Google Sheets y organiza los archivos en Google Drive.
- Incorpora notas integradas y esperas controladas para mejorar la coordinación del workflow.

## Ejemplos de uso
- Extracción periódica de anuncios nuevos para análisis de mercado.
- Generación de reportes automatizados con insights basados en IA.
- Consolidación de contenido publicitario para campañas internas o clientes.
- Monitorización de cambios en anuncios con alertas configuradas.

---

**Categoría:** utilidades/scraping  
**Etiquetas:** Meta Ads, Heygen, Contenido  
**Número de nodos:** 58  
**Tipos de nodos utilizados:**  
`n8n-nodes-base.googleSheets`, `@n8n/n8n-nodes-langchain.openAi`, `@n8n/n8n-nodes-langchain.lmChatOpenAi`, `n8n-nodes-base.googleDrive`, `n8n-nodes-base.merge`, `@n8n/n8n-nodes-langchain.lmChatOpenRouter`, `n8n-nodes-base.if`, `n8n-nodes-base.manualTrigger`, `@n8n/n8n-nodes-langchain.chainLlm`, `n8n-nodes-base.stickyNote`, `n8n-nodes-base.set`, `@n8n/n8n-nodes-langchain.outputParserStructured`, `n8n-nodes-base.splitInBatches`, `n8n-nodes-base.httpRequest`, `n8n-nodes-base.splitOut`, `@n8n/n8n-nodes-langchain.outputParserAutofixing`, `n8n-nodes-base.wait`
```