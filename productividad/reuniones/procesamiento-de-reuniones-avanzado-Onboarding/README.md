```markdown
# Procesamiento de Reuniones Avanzado

## Descripción
Workflow avanzado diseñado para optimizar la gestión y el procesamiento de reuniones, integrando análisis de contenido, automatización de tareas y gestión documental para mejorar la productividad y el onboarding.

## Requisitos
- Credenciales de API para:
  - OpenAI (`@n8n/n8n-nodes-langchain.openAi`)
  - SerpApi (`@n8n/n8n-nodes-langchain.toolSerpApi`)
  - Anthropic Chat (`@n8n/n8n-nodes-langchain.lmChatAnthropic`)
  - Notion (`n8n-nodes-base.notionTool`)
  - Airtable (`n8n-nodes-base.airtableTool`, `n8n-nodes-base.airtable`)
  - Google Drive (`n8n-nodes-base.googleDriveTrigger`)
  - Google Docs (`n8n-nodes-base.googleDocs`)
  - Google Calendar (`n8n-nodes-base.googleCalendarTool`)

## Instrucciones de configuración
1. Importe el workflow en n8n.
2. Configure las credenciales necesarias en la sección de credenciales de n8n.
3. Conecte las APIs (OpenAI, SerpApi, Anthropic, Notion, Airtable, Google Drive, Google Docs, Google Calendar) con sus respectivas credenciales.
4. Ajuste los parámetros específicos de cada nodo según sus necesidades operativas.
5. Active el workflow para comenzar la automatización.

## Funcionamiento
El workflow integra 26 nodos que combinan capacidades de procesamiento de lenguaje natural, herramientas de búsqueda, gestión documental y bases de datos para:
- Analizar y resumir contenido de reuniones usando modelos OpenAI y Anthropic.
- Buscar información relevante externa con SerpApi.
- Interactuar con sistemas internos y herramientas colaborativas (Notion, Airtable).
- Automatizar la creación y actualización de documentos y eventos en Google Docs y Calendar.
- Facilitar procesos de onboarding a través de la integración de herramientas y flujos de datos.

## Ejemplos de uso
- Resumen automático de actas de reuniones y distribución en Notion.
- Actualización sincronizada de tareas y bases de datos en Airtable tras reuniones.
- Creación automática de eventos y recordatorios en Google Calendar basados en discusiones.
- Búsqueda contextual de información adicional para toma de decisiones durante el onboarding.

---

**Categoría:** productividad/reuniones  
**Etiquetas:** Onboarding, *****  
**Número de nodos:** 26
```