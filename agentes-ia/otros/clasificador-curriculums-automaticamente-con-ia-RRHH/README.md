```markdown
# Clasificador Curriculums automaticamente con IA

## Descripción  
Workflow desarrollado en n8n para clasificar curriculums de forma automática utilizando inteligencia artificial. Integra procesamiento de documentos, extracción de información y análisis mediante modelos de lenguaje, optimizando procesos de RRHH.

## Requisitos  
- Credenciales de Google Sheets (para acceso y manipulación de hojas de cálculo).  
- Credenciales de Google Drive (para el manejo y almacenamiento de archivos).  
- API Key de OpenAI (para el uso de nodos LangChain con modelos de lenguaje GPT).  
- n8n configurado con los nodos necesarios instalados:  
  - n8n-nodes-base.googleSheets  
  - n8n-nodes-base.googleDrive  
  - n8n-nodes-base.merge  
  - n8n-nodes-base.formTrigger  
  - n8n-nodes-base.extractFromFile  
  - n8n-nodes-base.stickyNote  
  - n8n-nodes-base.set  
  - @n8n/n8n-nodes-langchain.lmChatOpenAi  
  - @n8n/n8n-nodes-langchain.chainLlm  
  - @n8n/n8n-nodes-langchain.informationExtractor  
  - @n8n/n8n-nodes-langchain.outputParserStructured  
  - @n8n/n8n-nodes-langchain.chainSummarization

## Instrucciones de configuración  
1. Configure las credenciales de Google Sheets y Google Drive en n8n.  
2. Añada su API Key de OpenAI en las credenciales de LangChain/ChatGPT.  
3. Importe el workflow y revise que todos los nodos estén configurados correctamente con sus respectivas credenciales.  
4. Personalice las hojas de cálculo y carpetas de Google Drive según sus necesidades.  
5. Ajuste los parámetros de los nodos LangChain para optimizar la extracción y clasificación según su modelo de curriculums.

## Detalles de funcionamiento  
- El workflow se activa mediante un formulario (formTrigger) donde se carga el curriculum.  
- Los archivos son extraídos y convertidos para su análisis (extractFromFile).  
- La información relevante es extraída con nodos LangChain especializados en extracción y parsing.  
- Se resume la información clave y se clasifica automáticamente según criterios predefinidos.  
- Los resultados se almacenan en Google Sheets para su consulta y seguimiento.  
- Notas adhesivas (stickyNote) permiten añadir observaciones manuales si es necesario.  
- El sistema integra 18 nodos para gestionar todo el flujo desde la recepción hasta la clasificación final.

## Ejemplos de uso  
- Automatización en RRHH para filtrar curriculums según experiencia y habilidades.  
- Preselección de candidatos basada en análisis automático de documentos adjuntos.  
- Generación de reportes consolidados de candidatos para reuniones internas.  

---

**Etiquetas:** RRHH  
**Categoría:** agentes-ia/otros  
**Número de nodos:** 18
```