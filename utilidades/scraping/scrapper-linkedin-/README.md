```markdown
# Scrapper Linkedin

## Descripción
Workflow de n8n diseñado para extraer y procesar información de LinkedIn, integrando múltiples nodos para scrapear datos, analizarlos con modelos de lenguaje, y almacenarlos en Google Sheets.

## Requisitos
- Cuenta y credenciales válidas para acceder a la API de Google Sheets.
- Acceso a LinkedIn (puede requerir autentificación vía HTTP Request).
- Credenciales para nodos de LangChain (`chainLlm`, `lmChatDeepSeek`, `outputParserStructured`).
- n8n versión compatible con los nodos utilizados.

## Instrucciones de configuración
1. Configure sus credenciales de Google Sheets en n8n.
2. Configure las credenciales/API necesarias para realizar peticiones HTTP a LinkedIn o al servicio que utilice para scrapear.
3. Añada las claves y configuraciones necesarias para los nodos de LangChain.
4. Importe y habilite el workflow en n8n.
5. Ajuste los parámetros en los nodos de acuerdo al tipo de datos que desea scrapear y procesar.

## Detalles de funcionamiento
- El workflow inicia con un nodo Manual Trigger para ejecución manual.
- Extrae datos de LinkedIn mediante nodos HTTP Request y procesa respuestas.
- Divide la información en batches para manejo eficiente.
- Utiliza nodos de código y filtros para limpiar y filtrar datos relevantes.
- Envía datos a modelos de lenguaje LangChain para análisis avanzado y estructuración de la información.
- Agrega resultados y los almacena finalmente en Google Sheets.
- Genera salidas en formato Markdown para presentación o informes.

## Ejemplos de uso
- Recolectar perfiles públicos de LinkedIn basados en criterios específicos.
- Analizar tendencias profesionales o habilidades destacadas en un sector.
- Generar reportes estructurados y automatizados integrados en Google Sheets para su posterior revisión.

---

**Nodos utilizados (17):**  
`n8n-nodes-base.googleSheets`, `n8n-nodes-base.aggregate`, `@n8n/n8n-nodes-langchain.chainLlm`, `n8n-nodes-base.manualTrigger`, `n8n-nodes-base.filter`, `n8n-nodes-base.code`, `n8n-nodes-base.set`, `@n8n/n8n-nodes-langchain.outputParserStructured`, `n8n-nodes-base.splitInBatches`, `n8n-nodes-base.httpRequest`, `n8n-nodes-base.markdown`, `@n8n/n8n-nodes-langchain.lmChatDeepSeek`
```