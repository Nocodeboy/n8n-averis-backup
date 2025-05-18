```markdown
# Newsletter de tecnología de IA personalizado con RSS, OpenAI y Gmail

## Descripción
Workflow de n8n que crea un newsletter personalizado sobre tecnología de inteligencia artificial, utilizando fuentes RSS, procesamiento con OpenAI y envío automático vía Gmail.

## Requisitos
- Credenciales de API de OpenAI (para embeddings, chat y agentes).
- Cuenta de Gmail configurada con acceso SMTP para el envío de correos.
- URLs de fuentes RSS relevantes sobre tecnología e IA.
- n8n con los siguientes nodos disponibles:
  - @n8n/n8n-nodes-langchain.embeddingsOpenAi
  - @n8n/n8n-nodes-langchain.lmChatOpenAi
  - n8n-nodes-base.rssFeedRead
  - @n8n/n8n-nodes-langchain.textSplitterRecursiveCharacterTextSplitter
  - n8n-nodes-base.scheduleTrigger
  - n8n-nodes-base.stickyNote
  - n8n-nodes-base.set
  - @n8n/n8n-nodes-langchain.agent
  - n8n-nodes-base.gmail
  - @n8n/n8n-nodes-langchain.vectorStoreInMemory
  - n8n-nodes-base.splitOut
  - @n8n/n8n-nodes-langchain.documentDefaultDataLoader
  - n8n-nodes-base.markdown

## Instrucciones de configuración
1. Agrega las URLs de tus fuentes RSS en el nodo `rssFeedRead`.
2. Configura tus credenciales de OpenAI en los nodos correspondientes (`embeddingsOpenAi`, `lmChatOpenAi`, `agent`).
3. Introduce tu cuenta Gmail y configura el nodo `gmail` para permitir el envío de correos.
4. Ajusta el nodo `scheduleTrigger` para definir la frecuencia de creación y envío del newsletter.
5. Personaliza las plantillas de contenido en nodos `set` y `markdown` según tus preferencias de formato.
6. Revisa y activa el workflow para comenzar la ejecución automática según el horario definido.

## Detalles de funcionamiento
- El workflow se activa en los horarios definidos por el `scheduleTrigger`.
- Se leen las últimas noticias y artículos de tecnología IA desde los feeds RSS.
- Los textos se dividen y procesan para extraer embeddings con OpenAI.
- Un agente Langchain resume y genera el contenido del newsletter basado en los datos procesados.
- El contenido formateado en Markdown se convierte en el cuerpo del correo.
- Finalmente, el correo se envía automáticamente a los destinatarios configurados via Gmail.
- El workflow utiliza 21 nodos para orquestar la lectura, procesamiento, generación y envío del newsletter.

## Ejemplos de uso
- Enviar un newsletter diario con las últimas noticias de IA.
- Personalizar el contenido según las áreas de interés usando OpenAI para filtrar y generar textos.
- Crear boletines semanales automatizados con resumen y análisis de artículos tecnológicos destacados.
- Integrar múltiples fuentes RSS para un contenido amplio y relevante.

---

**Etiquetas:** RSS Feed  
**Categoría:** marketing/contenido  
**Número de nodos:** 21
```