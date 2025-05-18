```markdown
# Agente de Recursos Humanos - Calificación de Curriculums

## Descripción
Workflow diseñado para automatizar la calificación y evaluación de curriculums vitae mediante IA, integrando Google Sheets y Google Drive para la gestión de documentos y datos, y modelos de lenguaje de OpenAI para el análisis avanzado.

## Requisitos
- Credenciales de Google API (Google Sheets y Google Drive) configuradas en n8n.
- API Key de OpenAI para nodos de LangChain (lmChatOpenAi, chainLlm, informationExtractor, outputParserStructured, chainSummarization).
- n8n versión compatible con los nodos usados.
- Permisos adecuados para lectura y escritura en las hojas de cálculo y almacenamiento en Drive.

## Instrucciones de configuración
1. Importar el workflow en n8n.
2. Configurar las credenciales de Google Sheets y Google Drive.
3. Añadir y configurar la API Key de OpenAI en los nodos que la requieran.
4. Ajustar los IDs de documentos y carpetas en Google Drive y Sheets según el entorno.
5. Personalizar los parámetros de los nodos de LangChain si es necesario, para adaptar el análisis a las necesidades específicas.

## Detalles de funcionamiento
- El workflow comienza con un formulario (`formTrigger`) para la recepción de curriculums.
- Extrae archivos cargados (`extractFromFile`), los procesa y extrae información relevante mediante modelos de lenguaje.
- Combina y analiza datos con nodos de LangChain, generando calificaciones y resúmenes.
- Los resultados se integran y almacenan en Google Sheets, mientras que los documentos procesados se gestionan en Google Drive.
- Se utiliza un nodo de merge para consolidar datos y varios nodos de parsing para estructurar la salida.

## Ejemplos de uso
- Automatizar la evaluación preliminar de candidatos para procesos de selección.
- Generar reportes resumidos y estructurados a partir de múltiples CVs recibidos.
- Integrar con sistemas internos mediante Google Sheets para seguimiento y análisis continuo del proceso de selección.

---

**Categoría:** agentes-ia/otros  
**Etiquetas:** *****, Averis  
**Número de nodos:** 12
```