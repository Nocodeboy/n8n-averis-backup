```markdown
# 2. Agente para Abogados - Carga de documentos

## Descripción
Workflow diseñado para automatizar la carga, extracción y procesamiento inteligente de documentos legales desde Google Drive, integrando capacidades avanzadas de IA para facilitar la gestión documental en entornos jurídicos.

## Requisitos
- Credenciales n8n configuradas para:
  - Google Drive (acceso y triggers)
  - Gmail (envío y recepción de correos)
- API keys para los nodos Langchain:
  - OpenAI (modelo de texto y embeddings)
  - Google Gemini (modelos de lenguaje)
  - Qdrant (vector database para almacenamiento y búsqueda)
- Acceso a los nodos estándar de n8n mencionados instalados y habilitados

## Instrucciones de configuración
1. Configure las credenciales de Google Drive en n8n para permitir acceso a las carpetas donde se almacenan los documentos legales.
2. Configure las credenciales de Gmail para el envío y recepción de correos relacionados con notificaciones o consultas.
3. Ingrese las API keys necesarias para OpenAI, Google Gemini y Qdrant en los nodos correspondientes.
4. Ajuste los parámetros del nodo `textSplitterTokenSplitter` según el tamaño y tipo de los documentos que se procesarán.
5. Personalice las reglas del nodo `if` para controlar el flujo según el tipo o contenido del documento.
6. Asegúrese de que el trigger de Google Drive esté apuntando a la carpeta correcta donde se subirán los documentos.

## Detalles de funcionamiento
- El workflow se inicia con un trigger de Google Drive cuando se detecta un nuevo archivo.
- Se extrae contenido relevante del documento mediante `extractFromFile`.
- El texto se divide en fragmentos optimizados para procesamiento con IA.
- Utiliza nodos Langchain para generar embeddings y realizar análisis semántico de los documentos.
- Los datos procesados se almacenan en un vector store Qdrant para facilitar búsquedas rápidas y eficientes.
- Integración con Gmail permite enviar notificaciones o consultas automáticas basadas en la información extraída.
- Se emplean nodos de agregación y merge para consolidar resultados y controlar el flujo del proceso.
- Opcionalmente, se utiliza información extraída con `informationExtractor` para enriquecer los metadatos.

## Ejemplos de uso
- Carga automática de contratos recibidos en una carpeta de Google Drive con procesamiento y clasificación inmediata.
- Búsqueda semántica rápida dentro de un repositorio de documentos legales gracias a los vectores almacenados en Qdrant.
- Envío automático de resúmenes o alertas vía Gmail basados en la detección de cláusulas o términos específicos en documentos nuevos.
- Integración sencilla con agentes IA para responder consultas legales a partir de la documentación cargada.

---

**Nodos utilizados (20):**

`@n8n/n8n-nodes-langchain.openAi`,  
`@n8n/n8n-nodes-langchain.embeddingsOpenAi`,  
`n8n-nodes-base.aggregate`,  
`n8n-nodes-base.googleDrive`,  
`n8n-nodes-base.merge`,  
`@n8n/n8n-nodes-langchain.lmChatGoogleGemini`,  
`n8n-nodes-base.if`,  
`@n8n/n8n-nodes-langchain.textSplitterTokenSplitter`,  
`n8n-nodes-base.extractFromFile`,  
`n8n-nodes-base.gmail`,  
`n8n-nodes-base.set`,  
`n8n-nodes-base.googleDriveTrigger`,  
`@n8n/n8n-nodes-langchain.informationExtractor`,  
`n8n-nodes-base.httpRequest`,  
`@n8n/n8n-nodes-langchain.vectorStoreQdrant`,  
`@n8n/n8n-nodes-langchain.documentDefaultDataLoader`  
*(y otros nodos base para completar los 20 nodos)*  
```