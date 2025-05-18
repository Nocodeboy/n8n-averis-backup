```markdown
# Agente IA Avanzado para Ecommerce Averis v4

## Descripción  
Workflow avanzado para n8n que actúa como un agente de inteligencia artificial orientado a ecommerce, integrando comunicación vía WhatsApp para atención y ventas. Utiliza múltiples fuentes y modelos de lenguaje para ofrecer respuestas precisas y automatizar flujos de interacción con clientes.

## Requisitos  
- Credenciales de OpenAI (modelos GPT)  
- Acceso a Google Docs y Google Sheets API  
- Redis para gestión de memoria y sesiones  
- Base de datos Postgres para almacenamiento de contexto de chat  
- APIs específicas (Evolution API) según uso personalizado  
- n8n versión compatible con nodos Langchain y evolución API  

## Instrucciones de configuración  
1. Importe el workflow en su instancia n8n.  
2. Configure las credenciales:  
   - Añada las credenciales de OpenAI (`lmChatOpenAi`, `openAi`)  
   - Configure acceso a Google Docs y Google Sheets (`googleDocs`, `googleSheetsTool`)  
   - Configure conexión a Redis y Postgres para memoria y estado  
   - Añada credenciales para Evolution API si aplica  
3. Ajuste los nodos webhook para recibir mensajes entrantes de WhatsApp (integración externa requerida).  
4. Revise y personalice los nodos de herramientas (Wikipedia, Think, ToolWorkflow) según necesidades específicas.  
5. Activar el workflow y monitorizar su funcionamiento inicial.  

## Detalles de funcionamiento  
- Recibe mensajes vía webhook de WhatsApp.  
- Procesa consultas combinando modelos GPT y Google Gemini para respuestas enriquecidas.  
- Emplea parsers estructurados y autofixing para mejorar la calidad de salida.  
- Usa memoria Postgres y Redis para contexto conversacional persistente.  
- Integra documentos (Google Docs) y hojas de cálculo para datos y seguimiento.  
- Implementa lógica condicional y de flujo con nodos Switch, If y Merge para ramificación dinámica.  
- Aplica herramientas específicas para búsqueda en Wikipedia, pensamiento y workflow personalizados.  
- Permite espera y sincronización con nodos Wait y NoOp para control de tiempos.  
- Utiliza nodos SplitOut y Aggregate para dividir y consolidar información según contexto.  

## Ejemplos de uso  
- Atención al cliente automatizada vía WhatsApp con respuestas personalizadas basadas en historial y contexto.  
- Automatización de procesos de venta y consulta de productos integrando datos desde Google Sheets.  
- Soporte escalable para consultas frecuentes, integrando fuentes externas como Wikipedia para contenido educativo.  
- Recordatorios y seguimiento automatizados mediante nodos temporizados y estados persistentes.  

---

**Categoría:** agentes-ia/whatsapp  
**Etiquetas:** Whatsapp, Customer / Sales  
**Número de nodos:** 84  
**Nodos principales:** @n8n/n8n-nodes-langchain.openAi, googleDocs, outputParserStructured, httpRequest, wait, webhook, lmChatOpenAi, switch, lmChatGoogleGemini, stickyNote, evolutionApi, outputParserAutofixing, redis, merge, if, memoryPostgresChat, agent, aggregate, noOp, googleSheetsTool, chainLlm, convertToFile, sort, toolWorkflow, code, set, toolThink, toolWikipedia, splitOut  
```