```markdown
# Actioning meeting next steps - Medium

## Descripción  
Workflow orientado a la productividad en reuniones que automatiza la identificación y gestión de las siguientes acciones a tomar tras una reunión, integrando procesamiento de lenguaje natural, gestión de archivos y coordinación de calendarios.

## Requisitos  
- Credenciales de OpenAI para el nodo `@n8n/n8n-nodes-langchain.lmChatOpenAi`  
- Acceso y credenciales de Google Drive (para nodos `googleDrive` y `extractFromFile`)  
- Acceso y credenciales de Google Calendar (`googleCalendar`)  
- Conexión a internet para llamadas HTTP (`httpRequest`)  
- Permisos para ejecutar flujos de trabajo (`executeWorkflowTrigger`)  

## Instrucciones de configuración  
1. Configurar las credenciales de OpenAI en n8n.  
2. Añadir y autenticar las cuentas de Google Drive y Google Calendar en n8n.  
3. Ajustar los nodos de entrada manual (`manualTrigger`) para iniciar el workflow según el caso de uso.  
4. Personalizar los filtros y condiciones en el nodo `switch` para adaptar el flujo.  
5. Verificar y personalizar las plantillas y parámetros de los nodos Langchain para el procesamiento del lenguaje.  

## Detalles de funcionamiento  
- El workflow comienza con un disparador manual que activa la captura y análisis de notas de reuniones.  
- El nodo `extractFromFile` obtiene contenido relevante desde documentos almacenados en Google Drive.  
- Utilizando componentes Langchain (`lmChatOpenAi`, `agent`, `outputParserStructured`), se procesan y estructuran los datos para extraer las siguientes acciones.  
- El nodo `switch` decide rutas condicionales según la información extraída.  
- Las acciones detectadas se registran y organizan mediante notas adhesivas (`stickyNote`) y se actualizan eventos en Google Calendar.  
- Herramientas adicionales como `httpRequest` y `splitOut` facilitan integración y procesamiento paralelo.  

## Ejemplos de uso  
- Tras una reunión semanal, activar el workflow para generar automáticamente una lista estructurada de tareas y asignaciones.  
- Automatizar la creación de recordatorios y eventos en Google Calendar basados en acuerdos de la reunión.  
- Extraer y distribuir resúmenes y siguientes pasos desde documentos compartidos en Google Drive.  

---

**Número de nodos:** 28  
**Categoría:** productividad/reuniones  
**Etiquetas:** _(sin etiquetas asignadas)_  
**Tipos de nodos utilizados:**  
`@n8n/n8n-nodes-langchain.lmChatOpenAi`, `n8n-nodes-base.switch`, `n8n-nodes-base.googleDrive`, `n8n-nodes-base.manualTrigger`, `n8n-nodes-base.extractFromFile`, `@n8n/n8n-nodes-langchain.toolWorkflow`, `n8n-nodes-base.stickyNote`, `n8n-nodes-base.executeWorkflowTrigger`, `n8n-nodes-base.set`, `@n8n/n8n-nodes-langchain.agent`, `@n8n/n8n-nodes-langchain.outputParserStructured`, `n8n-nodes-base.googleCalendar`, `n8n-nodes-base.httpRequest`, `n8n-nodes-base.splitOut`
```