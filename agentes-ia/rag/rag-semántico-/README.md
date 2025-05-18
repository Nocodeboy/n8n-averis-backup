```markdown
# RAG Semántico

## Descripción

Workflow de n8n diseñado para implementar un sistema de Recuperación Augmentada con Generación (RAG) semántica, integrando IA para procesamiento de lenguaje natural junto con gestión y extracción de datos desde Google Drive.

## Requisitos

- Credenciales de OpenAI (para el nodo `@n8n/n8n-nodes-langchain.openAi`)
- Acceso a Google Drive con credenciales OAuth (para nodos `n8n-nodes-base.googleDrive`)
- n8n instalado y configurado con los nodos listados
- Acceso a internet para nodos HTTP Request

## Instrucciones de Configuración

1. Configure las credenciales de OpenAI en n8n.
2. Conecte y autorice el nodo Google Drive con la cuenta correspondiente.
3. Ajuste los parámetros de los nodos según los documentos y consultas específicos de su caso.
4. Importe el workflow en n8n y verifique que todos los nodos estén correctamente configurados.

## Detalles de Funcionamiento

- El workflow inicia con un disparador manual (`manualTrigger`).
- Archivos relevantes son extraits y procesados desde Google Drive utilizando `extractFromFile`.
- Los datos se dividen en lotes manejables con `splitInBatches` para optimizar el procesamiento.
- El contenido es enriquecido y analizado usando nodos de OpenAI para generar respuestas semánticas precisas.
- Consultas adicionales y llamadas externas se realizan a través de `httpRequest`.
- Código personalizado puede ser ejecutado con el nodo `code` para lógica específica.

## Ejemplos de Uso

- Soporte al cliente con respuestas contextuales basadas en documentación interna.
- Generación de resúmenes semánticos de grandes volúmenes de documentos almacenados en Google Drive.
- Integración en agentes virtuales para proporcionar información actualizada y contextual.

---

**Categoría:** agentes-ia/rag  
**Número de nodos:** 14  
**Tipos de nodos:**  
`@n8n/n8n-nodes-langchain.openAi`, `n8n-nodes-base.googleDrive`, `n8n-nodes-base.manualTrigger`, `n8n-nodes-base.code`, `n8n-nodes-base.extractFromFile`, `n8n-nodes-base.splitInBatches`, `n8n-nodes-base.httpRequest`
```