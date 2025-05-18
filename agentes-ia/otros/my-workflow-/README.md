```markdown
# My workflow

## Descripción  
Workflow diseñado para integrar agentes de IA con herramientas de comunicación y gestión como Zoom, ClickUp y Microsoft Outlook, facilitando la automatización de tareas, manejo de correos, control de flujos y ejecución dinámica de sub-workflows.

## Requisitos  
- Credenciales para las siguientes integraciones:  
  - OpenAI (API key para nodos LangChain)  
  - Zoom  
  - ClickUp  
  - Microsoft Outlook  
- Permisos para ejecutar workflows anidados y enviar correos.  
- n8n versión compatible con nodos LangChain y nodos base mencionados.

## Instrucciones de configuración  
1. Importar el workflow en n8n.  
2. Configurar y añadir las credenciales correspondientes para OpenAI, Zoom, ClickUp y Outlook en la sección de credenciales de n8n.  
3. Revisar y adaptar variables en los nodos `Set` según necesidades específicas del entorno.  
4. Validar los nodos y conexiones para asegurar la correcta secuencia de tareas.  
5. Activar el workflow o ejecutarlo manualmente para pruebas.

## Detalles de funcionamiento  
- El workflow incluye 24 nodos que interactúan para:  
  - Ejecutar consultas y agentes basados en OpenAI usando nodos LangChain.  
  - Gestionar reuniones y eventos mediante Zoom.  
  - Manipular tareas y proyectos en ClickUp.  
  - Enviar correos electrónicos y manejar eventos en Microsoft Outlook.  
  - Controlar flujos mediante filtros, divisiones en lotes y manejo de errores.  
  - Ejecutar sub-workflows y código personalizado para adaptaciones específicas.  
- Se inicia principalmente mediante triggers manuales o eventos específicos configurados.  
- Incluye nodos para extracción y procesamiento de datos desde archivos y APIs.

## Ejemplos de uso  
- Automatización de respuestas inteligentes a solicitudes de clientes a través de correo electrónico.  
- Coordinación automática de reuniones y actualizaciones en Zoom y ClickUp.  
- Procesamiento y filtrado de datos en lotes para generación de reportes con IA.  
- Orquestación de agentes de IA para tareas complejas combinando múltiples herramientas.

---

**Categoría:** agentes-ia/otros  
**Nodos utilizados:** @n8n/n8n-nodes-langchain.openAi, n8n-nodes-base.zoom, n8n-nodes-base.executeWorkflowTrigger, n8n-nodes-base.httpRequest, @n8n/n8n-nodes-langchain.lmChatOpenAi, n8n-nodes-base.filter, n8n-nodes-base.stickyNote, n8n-nodes-base.splitInBatches, n8n-nodes-base.emailSend, n8n-nodes-base.manualTrigger, @n8n/n8n-nodes-langchain.agent, n8n-nodes-base.stopAndError, n8n-nodes-base.extractFromFile, n8n-nodes-base.code, @n8n/n8n-nodes-langchain.toolWorkflow, n8n-nodes-base.clickUp, n8n-nodes-base.set, n8n-nodes-base.splitOut, n8n-nodes-base.microsoftOutlookTool  
**Número de nodos:** 24
```