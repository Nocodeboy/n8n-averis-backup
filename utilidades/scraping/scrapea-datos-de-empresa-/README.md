```markdown
# Scrapea datos de empresa

## Descripción
Workflow de n8n diseñado para extraer y procesar datos relevantes de empresas utilizando scraping avanzado, procesamiento con inteligencia artificial y almacenamiento en Google Sheets.

## Requisitos
- Cuenta en Google Cloud con credenciales habilitadas para Google Sheets.
- API Key para OpenAI (lmChatOpenAi).
- API Key para SerpAPI.
- Acceso a n8n con los siguientes nodos instalados:
  - `n8n-nodes-base.googleSheets`
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`
  - `n8n-nodes-base.merge`
  - `@n8n/n8n-nodes-langchain.toolSerpApi`
  - `n8n-nodes-base.manualTrigger`
  - `@n8n/n8n-nodes-langchain.toolWorkflow`
  - `n8n-nodes-base.scheduleTrigger`
  - `n8n-nodes-base.stickyNote`
  - `n8n-nodes-base.set`
  - `@n8n/n8n-nodes-langchain.agent`
  - `@n8n/n8n-nodes-langchain.outputParserStructured`
  - `n8n-nodes-base.splitInBatches`

## Configuración
1. Configure las credenciales de Google Sheets en n8n.
2. Configure las API Keys de OpenAI y SerpAPI en n8n.
3. Ajuste el nodo `scheduleTrigger` o `manualTrigger` según la frecuencia deseada de ejecución.
4. Verifique y configure las variables en nodos `set` para definir parámetros específicos de scraping.
5. Configure la hoja de cálculo de Google Sheets con la estructura requerida para almacenar los datos extraídos.

## Funcionamiento
- El workflow puede ser activado manualmente o mediante un disparador programado.
- Los datos de la empresa son buscados mediante SerpAPI y procesados con OpenAI para estructurarlos.
- La información se divide en batches para optimizar el procesamiento.
- Los datos procesados son ordenados y fusionados usando el nodo merge.
- Finalmente, los datos limpios y estructurados se guardan en Google Sheets para su consulta o análisis posterior.

## Ejemplos de uso
- Extraer y analizar información pública de empresas para generar reportes automáticos.
- Monitorear cambios en datos empresariales periódicamente.
- Integrar con otros sistemas mediante exportación de datos desde Google Sheets.

---

**Número de nodos:** 22  
**Categoría:** utilidades/scraping  
**Etiquetas:** _(ninguna)_
```