```markdown
# 3. Actualiza en la base de datos - Ruby

## Descripción
Workflow diseñado para actualizar información en la base de datos utilizando Ruby, integrando herramientas de procesamiento de texto, almacenamiento y gestión de datos mediante Google Drive, Supabase y OpenAI.

## Requisitos
- Credenciales de Google Drive con permisos para acceder y monitorear archivos.
- Cuenta y credenciales de Supabase para acceso a la base de datos.
- API Key de OpenAI para generar embeddings y procesamiento de lenguaje natural.
- n8n instalado y configurado, con los nodos necesarios disponibles:
  - `@n8n/n8n-nodes-langchain`
  - `n8n-nodes-base`

## Instrucciones de configuración
1. **Configurar Credenciales:**
   - Añadir credenciales de Google Drive en n8n.
   - Conectar Supabase con las credenciales de su proyecto.
   - Insertar la API Key de OpenAI en el nodo correspondiente.

2. **Importar Workflow:**
   - Importar el archivo JSON del workflow en n8n.

3. **Ajustar parámetros:**
   - Configurar los nodos de acuerdo con las rutas y bases de datos específicas.
   - Validar los triggers de Google Drive según la carpeta o eventos deseados.

4. **Activar el workflow:**
   - Una vez configurado, activar para iniciar la automatización.

## Detalles de funcionamiento
- El workflow monitoriza Google Drive para detectar cambios o nuevos archivos mediante el nodo `googleDriveTrigger`.
- Extrae el contenido de los archivos utilizando `extractFromFile`.
- El texto se procesa y divide en segmentos con `textSplitterRecursiveCharacterTextSplitter`.
- Se generan embeddings a partir del texto usando `embeddingsOpenAi`.
- Estos vectores se almacenan y actualizan en Supabase con `vectorStoreSupabase`.
- Límites y validaciones se manejan mediante el nodo `limit`.
- Se utilizan nodos adicionales como `stickyNote` para anotaciones y `set` para manipulación de datos durante el flujo.

## Ejemplos de uso
- Actualizar una base de datos de documentos indexados para búsqueda semántica.
- Procesar y almacenar información relevante extraída de archivos en Google Drive.
- Integrar con sistemas que requieran actualización automática de datos procesados con IA.

---

**Número de nodos:** 16  
**Categoría:** utilidades/integraciones  
**Tipos de nodos utilizados:**  
`@n8n/n8n-nodes-langchain.embeddingsOpenAi`,  
`n8n-nodes-base.limit`,  
`n8n-nodes-base.googleDrive`,  
`n8n-nodes-base.supabase`,  
`n8n-nodes-base.extractFromFile`,  
`@n8n/n8n-nodes-langchain.textSplitterRecursiveCharacterTextSplitter`,  
`@n8n/n8n-nodes-langchain.vectorStoreSupabase`,  
`n8n-nodes-base.stickyNote`,  
`n8n-nodes-base.set`,  
`n8n-nodes-base.googleDriveTrigger`,  
`@n8n/n8n-nodes-langchain.documentDefaultDataLoader`
```