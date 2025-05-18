```markdown
# Newsletter Automatizada

## Descripción  
Workflow para automatizar la creación y envío de una newsletter personalizada. Extrae datos desde Google Sheets, genera contenido con OpenAI, evalúa condiciones, y envía emails automáticamente, optimizando procesos de marketing y contenido.

## Requisitos  
- Credenciales de Google Sheets (acceso a la hoja con datos de suscriptores o contenido)  
- API Key de OpenAI para los nodos Langchain (lmChatOpenAi, agent, outputParserStructured)  
- Cuenta de Gmail con permisos para envío mediante API  
- Acceso a n8n con los nodos instalados:  
  - `n8n-nodes-base.googleSheets`  
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`  
  - `n8n-nodes-base.merge`  
  - `n8n-nodes-base.if`  
  - `n8n-nodes-base.html`  
  - `n8n-nodes-base.code`  
  - `n8n-nodes-base.gmail`  
  - `@n8n/n8n-nodes-langchain.agent`  
  - `n8n-nodes-base.scheduleTrigger`  
  - `n8n-nodes-base.set`  
  - `n8n-nodes-base.stickyNote`  
  - `@n8n/n8n-nodes-langchain.outputParserStructured`  
  - `n8n-nodes-base.splitOut`  
  - `n8n-nodes-base.httpRequest`  
  - `n8n-nodes-base.splitInBatches`  

## Instrucciones de configuración  
1. Configure las credenciales de Google Sheets en n8n y vincúlelas con el nodo correspondiente.  
2. Ingrese su API Key de OpenAI en los nodos Langchain utilizados.  
3. Configure el nodo Gmail con la cuenta desde la cual enviará la newsletter.  
4. Personalice la hoja de Google Sheets con la información de suscriptores y contenido.  
5. Ajuste los parámetros en nodos `if`, `code` y `set` para controlar la lógica de segmentación y contenido.  
6. Programe la ejecución automática con el nodo `scheduleTrigger` según la frecuencia deseada.  

## Detalles de funcionamiento  
- El workflow comienza con un disparador programado (`scheduleTrigger`).  
- Extrae datos desde Google Sheets para obtener destinatarios y temas.  
- Usa agentes y modelos OpenAI (`lmChatOpenAi`, `agent`) para generar o refinar el contenido dinámicamente.  
- Aplica lógica condicional y merges para personalizar mensajes.  
- Convierte el contenido a HTML y prepara emails listos para envío.  
- Envía emails usando el nodo Gmail en lote para optimizar el proceso.  
- Utiliza nodos como `splitInBatches`, `splitOut` y `merge` para gestionar procesamiento y evitar cuotas.  
- Incluye nodos auxiliares para debugging y notas internas (`stickyNote`).  

## Ejemplos de uso  
- Enviar un boletín semanal con contenido generado automáticamente según intereses actuales de los suscriptores.  
- Personalizar newsletters segmentadas según la interacción previa de cada usuario.  
- Integrar datos externos vía httpRequest para incluir novedades y actualizar contenidos.  

---

**Categoría:** marketing/contenido  
**Etiquetas:** n8nCommunity  
**Número de nodos:** 21  
```