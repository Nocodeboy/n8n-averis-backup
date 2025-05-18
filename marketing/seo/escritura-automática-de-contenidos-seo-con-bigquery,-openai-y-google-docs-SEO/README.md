```markdown
# Escritura Automática de Contenidos SEO con BigQuery, OpenAI y Google Docs

## Descripción
Workflow de n8n para automatizar la generación de contenidos SEO optimizados. Extrae datos relevantes desde BigQuery, crea contenido con OpenAI y lo guarda en Google Docs, facilitando la publicación eficiente y escalable de artículos optimizados para motores de búsqueda.

## Requisitos
- Cuenta con acceso a Google Cloud (BigQuery, Google Sheets, Google Drive, Google Docs)
- Credenciales configuradas en n8n para:
  - Google BigQuery
  - Google Sheets
  - Google Drive/Docs
- API Key de OpenAI con permisos para generación de textos
- n8n configurado con nodos compatibles (versión que soporte los nodos listados)

## Instrucciones de Configuración
1. **Configurar Credenciales:**
   - Añadir credenciales de Google Cloud en n8n (incluyendo acceso a BigQuery, Sheets, Drive).
   - Configurar credenciales API de OpenAI en n8n.
2. **Importar Workflow:**
   - Importar el workflow JSON en n8n.
3. **Ajustar Parámetros:**
   - Configurar consultas BigQuery específicas según tus datos.
   - Personalizar prompts de OpenAI para el tipo de contenido deseado.
   - Definir carpetas destino en Google Drive para la creación de documentos.
4. **Habilitar Trigger:**
   - Configurar el nodo Form Trigger para iniciar el flujo manual o programado.

## Detalles de Funcionamiento
- El workflow inicia mediante un formulario o disparador programado.
- Extrae datos e insights desde Google BigQuery usando consultas definidas.
- Procesa y agrega datos con nodos `aggregate` y de lógica condicional (`if`).
- Genera textos SEO utilizando OpenAI mediante el nodo Langchain.
- Convierte textos a archivos Markdown o Google Docs y los guarda en Google Drive.
- Integra operaciones intermedias para manejo de archivos, merge de datos y esperas (`wait`), asegurando secuencialidad.
- Permite registros y anotaciones internas con nodos `stickyNote` y `code` para trazabilidad y personalización avanzada.

## Ejemplos de Uso
- Generar semanalmente artículos SEO basados en análisis de BigQuery sobre tendencias de búsqueda.
- Crear automáticamente descripciones optimizadas para productos desde catálogos almacenados en BigQuery.
- Actualizar documentos colaborativos en Google Docs con contenidos frescos generados por IA para campañas de marketing digital.

---

**Categoría:** marketing/seo  
**Etiquetas:** SEO  
**Nodos utilizados (28):**  
`googleSheets`, `aggregate`, `openAi`, `googleDrive`, `merge`, `if`, `formTrigger`, `convertToFile`, `wait`, `code`, `stickyNote`, `set`, `googleBigQuery`, `httpRequest`, `markdown` (entre otros).
```
