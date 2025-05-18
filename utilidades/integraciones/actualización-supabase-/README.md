```markdown
# Actualización Supabase

## Descripción
Workflow diseñado para actualizar datos en Supabase integrando diversas utilidades y servicios, incluyendo procesamiento de texto con LangChain, manejo de archivos en Google Drive, y operaciones de límite y almacenamiento vectorial en Supabase.

## Requisitos
- Credenciales de Supabase (URL y API Key)
- Credenciales de Google Drive (OAuth2)
- API Key de OpenAI para nodos LangChain
- Acceso a n8n con los nodos instalados:
  - `@n8n/n8n-nodes-langchain`
  - `n8n-nodes-base`

## Instrucciones de configuración
1. Configure las credenciales de Supabase en n8n con la URL y API Key proporcionadas por su proyecto.
2. Configure la credencial de Google Drive con OAuth2 para acceso a sus archivos y triggers.
3. Agregue la API Key de OpenAI en la configuración de nodos LangChain.
4. Importe el workflow en n8n y valide que todos los nodos estén correctamente conectados y configurados.
5. Ajuste parámetros específicos como límites de procesamiento o rutas de archivos según sea necesario.

## Detalles de funcionamiento
- El workflow utiliza un disparador de Google Drive para detectar archivos nuevos o modificados.
- Los archivos son procesados mediante extracción y segmentación de texto usando `textSplitterRecursiveCharacterTextSplitter`.
- El contenido segmentado es convertido en embeddings con `embeddingsOpenAi`.
- Los vectores generados se almacenan y actualizan en Supabase a través del nodo `vectorStoreSupabase`.
- Control de ejecución y procesamiento mediante nodo `limit`.
- Uso adicional de nodos para manipulación y gestión de datos (`set`, `stickyNote`, `extractFromFile`) que facilitan el flujo de información dentro del workflow.
- Documentación y carga por defecto empleando nodos LangChain para facilitar el manejo de datos y documentos.

## Ejemplos de uso
- Actualizar la base de datos vectorial de Supabase con nuevos documentos almacenados en Google Drive automáticamente.
- Mantener sincronizados los embeddings de texto procesado para búsquedas rápidas o análisis posteriores.
- Limitar la ejecución del workflow para procesar un número controlado de documentos por ciclo.

---

**Número de nodos:** 16  
**Categoría:** utilidades/integraciones  
**Etiquetas:** (ninguna especificada)
```