```markdown
# Subida de recursos a Airtable - Averis

## Descripción
Workflow diseñado para automatizar la subida y gestión de recursos en Airtable, integrando servicios como Google Drive y potentes modelos de lenguaje de IA mediante nodos Langchain. Ideal para optimizar flujos de trabajo relacionados con almacenamiento y clasificación de archivos.

## Requisitos
- Credenciales de Airtable con acceso a la base y tabla correspondiente.
- API Key y configuración de Google Drive para acceso y gestión de archivos.
- Credenciales/keys para los nodos Langchain:
  - OpenAI
  - Google Gemini (LM Chat)
  - OpenRouter (LM Chat)
- Permisos para ejecutar webhooks mediante el nodo Form Trigger.

## Instrucciones de configuración
1. Configure el nodo **Form Trigger** para recibir datos o archivos desde formularios o integraciones externas.
2. Introduzca sus credenciales en los nodos correspondientes:
   - Airtable: API Key y base ID.
   - Google Drive: OAuth2 o API Key.
   - Langchain (OpenAI, Google Gemini, OpenRouter): Claves API en cada nodo.
3. Ajuste cualquier parámetro específico de cada nodo (tablas, carpetas, prompts, etc.) según su caso de uso.
4. Asegúrese que el workflow cuenta con los permisos y configuraciones para ejecutar código y dividir batchs de datos conforme sea necesario.

## Detalles de funcionamiento
- El workflow comienza con un **Form Trigger**, capturando recursos a subir.
- Archivos o datos son procesados y almacenados temporalmente usando nodos como **Google Drive** y transformados con nodos de código y batch.
- Se aplican modelos de lenguaje IA (OpenAI, Google Gemini, OpenRouter) para análisis, clasificación o enriquecimiento de datos.
- Los recursos y metadatos enriquecidos se sincronizan finalmente en Airtable mediante su nodo dedicado, manteniendo la base actualizada.
- Los nodos Langchain permiten crear cadenas de procesamiento y agentes inteligentes para manejo avanzado de la información.

## Ejemplos de uso
- Subir documentos desde formularios web y clasificarlos automáticamente en Airtable.
- Enriquecer metadatos de archivos subidos utilizando IA para mejorar búsquedas y organización.
- Automatizar el control y seguimiento de recursos en proyectos gestionados vía Google Drive y Airtable.

---

**Número de nodos:** 21  
**Categoría:** utilidades/integraciones  
**Etiquetas:** Averis, Airtable  
**Nodos utilizados:**  
`@n8n/n8n-nodes-langchain.openAi`, `n8n-nodes-base.googleDrive`, `@n8n/n8n-nodes-langchain.lmChatGoogleGemini`, `@n8n/n8n-nodes-langchain.chainLlm`, `n8n-nodes-base.formTrigger`, `@n8n/n8n-nodes-langchain.lmChatOpenRouter`, `n8n-nodes-base.code`, `@n8n/n8n-nodes-langchain.agent`, `n8n-nodes-base.set`, `n8n-nodes-base.airtable`, `n8n-nodes-base.splitInBatches`
```