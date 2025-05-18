```markdown
# Subida a Supabase

## Descripción
Workflow de n8n diseñado para gestionar la subida y procesamiento de documentos desde Google Drive, extraer y dividir el contenido, generar embeddings con OpenAI, y almacenarlos en Supabase para su posterior consulta y análisis.

## Requisitos
- Cuenta y credenciales de Google Drive con permiso para acceder a los archivos a procesar.
- Cuenta en Supabase con acceso a la base de datos y credenciales API necesarias.
- API Key de OpenAI para generar embeddings.
- n8n configurado con los nodos necesarios instalados:
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
1. Configure la credencial de Google Drive con acceso a la carpeta o archivos que desee procesar.
2. Cree y configure la credencial de Supabase con los parámetros de conexión (URL y clave).
3. Añada la API Key de OpenAI en la credencial para el nodo de embeddings.
4. Importe o configure el workflow en n8n y verifique que todos los nodos estén correctamente enlazados.
5. Active el trigger de Google Drive para que el workflow inicie al detectar nuevos archivos o cambios.

## Detalles de funcionamiento
- El workflow inicia con un trigger de Google Drive que detecta archivos nuevos o modificados.
- Extrae el contenido del archivo con el nodo `extractFromFile`.
- Divide el texto en fragmentos manejables utilizando `textSplitterRecursiveCharacterTextSplitter`.
- Genera embeddings vectoriales de los fragmentos mediante el nodo `embeddingsOpenAi`.
- Los embeddings se almacenan y organizan en Supabase usando `vectorStoreSupabase`.
- Nodos adicionales como `stickyNote` y `set` se utilizan para manejar datos temporales y configuraciones internas.
- Se utiliza el `documentDefaultDataLoader` para manejar la carga y normalización de documentos.

## Ejemplos de uso
- Procesar documentos automáticamente al subirlos a Google Drive para su análisis semántico.
- Indexar textos para motores de búsqueda internos basados en vectores almacenados en Supabase.
- Integrar con asistentes basados en IA que consulten la base de datos vectorial para respuestas contextuales.

---

*Número de nodos en el workflow: 13*  
*Categoría: utilidades/integraciones*
```