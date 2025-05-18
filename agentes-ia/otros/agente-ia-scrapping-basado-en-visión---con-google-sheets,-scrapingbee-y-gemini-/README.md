```markdown
# Agente IA Scrapping basado en visión - con Google Sheets, ScrapingBee y Gemini

## Descripción  
Workflow de n8n que integra un agente IA con capacidades de scraping basado en visión, utilizando Google Sheets para la gestión de datos, ScrapingBee para la extracción web, y Gemini como modelo de lenguaje para procesamiento y análisis.

## Requisitos  
- Credenciales de Google Sheets configuradas en n8n  
- API Key de ScrapingBee  
- Acceso y configuración del modelo Gemini en LangChain  
- n8n con nodos de la colección `@n8n/n8n-nodes-langchain` instalados

## Instrucciones de configuración  
1. Configura las credenciales de Google Sheets en n8n (Google API).  
2. Añade tu API Key de ScrapingBee en el nodo HTTP Request correspondiente.  
3. Configura el nodo `lmChatGoogleGemini` con tu acceso a Gemini (Google LangChain).  
4. Ajusta las hojas y rangos de Google Sheets a usar según tus datos.  
5. Verifica los endpoints y parámetros de ScrapingBee para el scraping óptimo.

## Detalles de funcionamiento  
- El workflow se inicia manualmente o mediante triggers configurados.  
- Usa ScrapingBee para extraer contenido visual y textual desde URLs definidas.  
- El agente Gemini procesa y analiza la información extraída, estructurándola y generando insights.  
- Los datos procesados se almacenan y actualizan en Google Sheets.  
- Incluye nodos para manejo avanzado de flujo, notas, y parseo estructurado para garantizar la correcta manipulación de la información.

## Ejemplos de uso  
- Realizar scraping visual y análisis automático de datos públicos o internos.  
- Actualizar informes en Google Sheets con información extraída y procesada por IA.  
- Automatizar la recolección y procesamiento de datos para investigaciones o monitoreo.

---

**Número de nodos:** 29  
**Categoría:** agentes-ia/otros  
**Etiquetas:** *(ninguna)*  
**Tipos de nodos utilizados:**  
`n8n-nodes-base.googleSheets`,  
`@n8n/n8n-nodes-langchain.lmChatGoogleGemini`,  
`n8n-nodes-base.manualTrigger`,  
`@n8n/n8n-nodes-langchain.toolWorkflow`,  
`n8n-nodes-base.stickyNote`,  
`n8n-nodes-base.set`,  
`@n8n/n8n-nodes-langchain.agent`,  
`n8n-nodes-base.executeWorkflowTrigger`,  
`@n8n/n8n-nodes-langchain.outputParserStructured`,  
`n8n-nodes-base.splitOut`,  
`n8n-nodes-base.httpRequest`,  
`n8n-nodes-base.markdown`
```