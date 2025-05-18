```markdown
# HR expert revisa curriculums

## Descripción
Workflow diseñado para automatizar la revisión de curriculums mediante inteligencia artificial y herramientas de productividad, integrando Google Sheets y Google Drive para gestionar documentos y aplicar análisis avanzados con nodos LangChain.

## Requisitos
- Cuenta y credenciales de Google Sheets y Google Drive con permisos adecuados.
- API key de OpenAI para el nodo `lmChatOpenAi` y otros nodos LangChain.
- n8n versión compatible con los siguientes nodos:
  - `n8n-nodes-base.googleSheets`
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`
  - `n8n-nodes-base.googleDrive`
  - `n8n-nodes-base.merge`
  - `@n8n/n8n-nodes-langchain.chainLlm`
  - `n8n-nodes-base.formTrigger`
  - `n8n-nodes-base.extractFromFile`
  - `n8n-nodes-base.stickyNote`
  - `n8n-nodes-base.set`
  - `@n8n/n8n-nodes-langchain.informationExtractor`
  - `@n8n/n8n-nodes-langchain.outputParserStructured`
  - `@n8n/n8n-nodes-langchain.chainSummarization`

## Instrucciones de configuración
1. Importe el workflow en su instancia de n8n.
2. Configure las credenciales de Google Sheets y Google Drive en la sección de credenciales.
3. Agregue y configure la API Key de OpenAI en los nodos LangChain.
4. Ajuste los IDs de hojas de cálculo y carpetas de Google Drive según su estructura.
5. Configure el trigger del formulario para capturar nuevos curriculums y activar el flujo.
6. Revise y personalice los prompts y los parámetros de los nodos LangChain para adaptar la revisión a sus necesidades.

## Detalles de funcionamiento
- **Input:** El flujo se inicia mediante un formulario (`formTrigger`) donde se suben curriculums.
- **Procesamiento:** 
  - Se extraen los archivos (`extractFromFile`) y se almacenan en Google Drive.
  - Los datos de cada curriculum se analizan usando modelos de lenguaje (OpenAI) a través de los nodos LangChain.
  - Se extrae información estructurada (`informationExtractor`), se resumen datos clave (`chainSummarization`) y se combinan resultados mediante el nodo `merge`.
- **Output:** Resultados estructurados y análisis son almacenados y actualizados en Google Sheets, y notas resumen pueden generarse con `stickyNote`.

## Ejemplos de uso
- Automatizar la clasificación y puntuación de curriculums recibidos para procesos de selección.
- Generar reportes resumidos de candidatos con información clave para HR.
- Integrar con sistemas adicionales para notificar o registrar avances basados en los resultados obtenidos.

---

**Número de nodos:** 18  
**Categoría:** productividad/tareas  
**Etiquetas:** (no especificadas)  
```