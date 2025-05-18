```markdown
# 2. Cargar en la base de datos - Ruby

## Descripción  
Workflow diseñado para cargar y procesar documentos desde Google Drive, extraer su contenido, generar embeddings con OpenAI y almacenar los vectores en una base de datos Supabase. Ideal para aplicaciones RAG (Recuperación Augmentada por Generación).

## Requisitos  
- Credenciales de Google API con acceso a Google Drive.  
- API Key de OpenAI para generación de embeddings.  
- Credenciales y configuración de Supabase para el vector store.  
- n8n con nodos correspondientes instalados:
  - `@n8n/n8n-nodes-langchain.embeddingsOpenAi`
  - `n8n-nodes-base.googleDrive`
  - `n8n-nodes-base.extractFromFile`
  - `@n8n/n8n-nodes-langchain.textSplitterRecursiveCharacterTextSplitter`
  - `@n8n/n8n-nodes-langchain.vectorStoreSupabase`
  - `n8n-nodes-base.stickyNote`
  - `n8n-nodes-base.set`
  - `n8n-nodes-base.googleDriveTrigger`
  - `@n8n/n8n-nodes-langchain.documentDefaultDataLoader`

## Instrucciones de configuración  
1. Configure las credenciales de Google Drive en n8n (Google API).  
2. Establezca la API Key de OpenAI en las credenciales de Langchain.  
3. Configure la conexión a Supabase con las claves y URL apropiadas.  
4. Ajuste el disparador de Google Drive para apuntar a la carpeta deseada.  
5. Revise y personalice los parámetros del text splitter y demás nodos según necesidad.

## Detalles de funcionamiento  
- El workflow se activa con cambios o cargas en Google Drive.  
- Extrae los archivos nuevos o modificados para procesar su contenido.  
- Utiliza el text splitter para fragmentar textos en bloques manejables.  
- Genera embeddings vía OpenAI por cada fragmento.  
- Inserta los vectores generados en una tabla de Supabase para consultas futuras.  
- Incluye nodos de configuración y notas para mantener claridad y flexibilidad.

## Ejemplos de uso  
- Indexar documentos corporativos para consultas semánticas internas.  
- Preparar datasets para agentes conversacionales basados en RAG.  
- Automatizar la actualización de bases de datos vectoriales a partir de documentos en Google Drive.

---

**Categoría:** agentes-ia/rag  
**Número de nodos:** 12  
**Etiquetas:** (ninguna)
```