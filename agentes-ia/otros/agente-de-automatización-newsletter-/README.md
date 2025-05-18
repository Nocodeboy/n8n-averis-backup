```markdown
# Agente de automatización Newsletter

## Descripción  
Workflow de n8n diseñado para automatizar la creación, gestión y envío de newsletters utilizando agentes de IA y múltiples integraciones. Facilita la agregación de información, generación de contenido personalizado y envío automático vía Gmail.

## Requisitos  
- Credenciales de Gmail configuradas en n8n para enviar correos.  
- API Key de OpenAI para nodos LangChain (lmChatOpenAi, openAi, agent).  
- Acceso a Internet para llamadas HTTP y uso de herramientas externas.  
- n8n instalado con los nodos mencionados disponibles.

## Instrucciones de configuración  
1. Importar el workflow en n8n.  
2. Configurar las credenciales de Gmail en el nodo correspondiente.  
3. Añadir la API Key de OpenAI en los nodos LangChain.  
4. Ajustar cualquier parámetro del nodo `scheduleTrigger` para definir la frecuencia de ejecución.  
5. Personalizar plantillas o textos en nodos `set` o `stickyNote` según necesidades.  

## Detalles de funcionamiento  
- El workflow se activa según programación definida (scheduleTrigger).  
- Agrega y procesa datos con nodos como `aggregate`, `splitOut` y `summarize`.  
- Genera contenido y respuestas usando modelos OpenAI a través de LangChain (lmChatOpenAi, openAi, agent).  
- Mantiene contexto con `memoryBufferWindow`.  
- Realiza peticiones HTTP para obtener información externa con `toolHttpRequest` y `httpRequest`.  
- Envía newsletters personalizados por correo mediante el nodo Gmail.  
- Los nodos `stickyNote` y `set` se usan para gestión interna y almacenamiento temporal de datos.

## Ejemplos de uso  
- Automatizar el envío semanal de newsletters con resúmenes de noticias y actualizaciones.  
- Crear boletines personalizados basados en consultas dinámicas y resultados de APIs.  
- Integrar contenido generado por IA en campañas de email marketing sin intervención manual.

---

**Número de nodos:** 31  
**Categoría:** agentes-ia/otros  
**Etiquetas:** _(Sin etiquetas asignadas)_  
**Tipos de nodos utilizados:**  
- n8n-nodes-base.aggregate  
- @n8n/n8n-nodes-langchain.lmChatOpenAi  
- @n8n/n8n-nodes-langchain.openAi  
- @n8n/n8n-nodes-langchain.memoryBufferWindow  
- n8n-nodes-base.gmail  
- n8n-nodes-base.stickyNote  
- n8n-nodes-base.set  
- @n8n/n8n-nodes-langchain.agent  
- n8n-nodes-base.scheduleTrigger  
- @n8n/n8n-nodes-langchain.toolHttpRequest  
- n8n-nodes-base.splitOut  
- n8n-nodes-base.summarize  
- n8n-nodes-base.httpRequest
```