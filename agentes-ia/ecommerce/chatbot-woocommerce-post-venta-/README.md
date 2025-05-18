```markdown
# Chatbot WooCommerce Post-Venta

## Descripción  
Workflow orientado a automatizar la atención post-venta en tiendas WooCommerce mediante un chatbot inteligente potenciado con agentes IA y herramientas avanzadas de LangChain. Facilita la gestión de consultas, cálculo de datos, manejo de documentos y comunicación vía Telegram, integrando además almacenamiento en Google Drive y sistemas de vectorización para respuestas contextuales.

## Requisitos  
- n8n con acceso a los siguientes nodos y paquetes:
  - `@n8n/n8n-nodes-langchain` (toolCalculator, embeddingsOpenAi, lmChatOpenAi, textSplitterTokenSplitter, memoryBufferWindow, toolVectorStore, agent, vectorStoreQdrant, documentDefaultDataLoader, toolWorkflow, chatTrigger)
  - `n8n-nodes-base` (executeWorkflowTrigger, httpRequest, stickyNote, wooCommerceTool, telegramTool, googleDrive, manualTrigger, set)
- Credenciales/API keys necesarias:
  - OpenAI API Key (para embeddings y chat)
  - WooCommerce API (para consulta y gestión de pedidos)
  - Telegram Bot Token (para interacción vía Telegram)
  - Google Drive API (para almacenamiento y recuperación documental)
  - Qdrant o servicio vectorial compatible (para búsqueda y memoria vectorial)

## Instrucciones de Configuración  
1. Importar el workflow en n8n.  
2. Configurar todas las credenciales en `Settings > Credentials`:  
   - OpenAI  
   - WooCommerce  
   - Telegram  
   - Google Drive  
   - Qdrant (o vector store utilizado)  
3. Verificar y ajustar URLs, tokens y endpoints en nodos específicos como HTTP Request o toolVectorStore.  
4. Personalizar parámetros del chatbot y agentes acorde a necesidades concretas (mensajes, memoria, prompts).  
5. Activar manualTrigger o executeWorkflowTrigger según método deseado para iniciar interacciones.  

## Detalles de Funcionamiento  
- El chatbot recibe consultas post-venta via Telegram o HTTP.  
- Utiliza LangChain para dividir y vectorizar textos, junto con memoria buffer para contexto.  
- Calcula datos específicos con toolCalculator y accede a pedidos WooCommerce vía WooCommerceTool.  
- Gestiona documentos relacionados con Google Drive y usa Qdrant para búsquedas semánticas.  
- Implementa agentes que coordinan múltiples herramientas LangChain para respuestas dinámicas y contextuales.  
- Respuestas y acciones son enviadas al usuario por Telegram o canales configurados.  

## Ejemplos de Uso  
- Cliente consulta estado de su pedido o solicita devoluciones.  
- Solicitudes de soporte post-venta que requieren cálculos o acceso a documentos.  
- Gestión automatizada de FAQs o problemas recurrentes con actualizaciones en Google Drive.  
- Interacción en tiempo real para seguimiento detallado mediante memoria y vectorización avanzada.  

---

*Número de nodos:* 31  
*Categoría:* agentes-ia/ecommerce  
```