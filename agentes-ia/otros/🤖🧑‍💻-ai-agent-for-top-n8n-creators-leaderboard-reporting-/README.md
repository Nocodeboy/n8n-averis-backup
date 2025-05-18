```markdown
# 🤖🧑‍💻 AI Agent for Top n8n Creators Leaderboard Reporting

## Descripción  
Workflow automatizado que recopila, procesa y reporta información del leaderboard de los principales creadores de n8n utilizando agentes de inteligencia artificial, integrando múltiples servicios para generar informes periódicos y enviarlos por distintos canales.

## Requisitos  
- Credenciales configuradas en n8n para los siguientes servicios:
  - Gmail  
  - Telegram  
  - Google Drive  
- API Keys para modelos de IA compatibles:  
  - OpenAI (para `lmChatOpenAi`)  
  - Google Gemini (para `lmChatGoogleGemini`)  
- Permisos para ejecutar workflows desde triggers (`executeWorkflowTrigger`)  

## Instrucciones de Configuración  
1. Importar el workflow a n8n.  
2. Configurar las credenciales necesarias: Gmail, Telegram, Google Drive y API Keys para OpenAI y Google Gemini en la sección de credenciales de n8n.  
3. Ajustar los parámetros del nodo `scheduleTrigger` para definir la frecuencia de ejecución del reporte.  
4. Revisar y personalizar plantillas Markdown y mensajes para adaptar el informe a necesidades específicas.  
5. Verificar los nodos de integración (HTTP Request, agentes Langchain, workflows anidados) para asegurar que apuntan a los endpoints y workflows correctos.  

## Detalles de Funcionamiento  
- El workflow se activa según la programación definida en el nodo `scheduleTrigger`.  
- Se extraen datos relevantes del leaderboard mediante solicitudes HTTP y consultas a workflows específicos.  
- Los agentes Langchain (`lmChatOpenAi`, `lmChatGoogleGemini`, `agent`, `chainLlm`) procesan y analizan la información para generar insights.  
- La información se formatea en Markdown y se exporta a archivos gestionados en Google Drive.  
- Los reportes se envían automáticamente vía Gmail y Telegram.  
- Uso de nodos de límite y combinación para controlar el flujo y volumen de datos procesados.  
- Se emplean nodos auxiliares (`stickyNote`, `set`, `splitOut`, `sort`, `aggregate`) para organizar y refinar la información entregada.  

## Ejemplos de Uso  
- Generar un resumen semanal de los creadores más activos en n8n y enviarlo a un grupo de Telegram.  
- Guardar reportes diarios en Google Drive para análisis histórico.  
- Notificar por correo electrónico a administradores del leaderboard con actualizaciones y recomendaciones generadas por IA.  

---

Número total de nodos en el workflow: 49  
Categoría: `agentes-ia/otros`  
Tipos principales de nodos utilizados:  
`n8n-nodes-base.scheduleTrigger`, `n8n-nodes-base.gmail`, `n8n-nodes-base.executeWorkflowTrigger`, `n8n-nodes-base.httpRequest`, `n8n-nodes-base.markdown`, `@n8n/n8n-nodes-langchain.lmChatOpenAi`, `n8n-nodes-base.limit`, `@n8n/n8n-nodes-langchain.lmChatGoogleGemini`, `n8n-nodes-base.telegram`, `n8n-nodes-base.stickyNote`, `n8n-nodes-base.readWriteFile`, `n8n-nodes-base.googleDrive`, `n8n-nodes-base.merge`, `@n8n/n8n-nodes-langchain.agent`, `n8n-nodes-base.aggregate`, `@n8n/n8n-nodes-langchain.chainLlm`, `n8n-nodes-base.convertToFile`, `n8n-nodes-base.sort`, `@n8n/n8n-nodes-langchain.toolWorkflow`, `n8n-nodes-base.set`, `n8n-nodes-base.splitOut`
```