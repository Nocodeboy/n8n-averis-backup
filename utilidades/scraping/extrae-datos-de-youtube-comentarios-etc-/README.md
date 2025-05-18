```markdown
# Extrae datos de Youtube comentarios etc

## Descripción

Workflow de n8n diseñado para extraer, procesar y analizar datos de Youtube, incluyendo comentarios, utilizando capacidades avanzadas de IA y herramientas de scraping.

## Requisitos

- Cuenta y credenciales de OpenAI (API Key)
- Acceso a una base de datos PostgreSQL para el nodo memoryPostgresChat
- n8n configurado con los nodos y paquetes indicados
- Acceso a Youtube Data API (opcional, según configuración del scraping)

## Instrucciones de configuración

1. Instala los nodos requeridos en n8n:
   - `@n8n/n8n-nodes-langchain.openAi`
   - `@n8n/n8n-nodes-langchain.lmChatOpenAi`
   - `@n8n/n8n-nodes-langchain.memoryPostgresChat`
   - `@n8n/n8n-nodes-langchain.toolWorkflow`
   - `@n8n/n8n-nodes-langchain.agent`
   - `@n8n/n8n-nodes-langchain.chatTrigger`
   - `n8n-nodes-base.switch`
   - `n8n-nodes-base.stickyNote`
   - `n8n-nodes-base.executeWorkflowTrigger`
   - `n8n-nodes-base.set`
   - `n8n-nodes-base.httpRequest`

2. Configura tus credenciales de OpenAI y PostgreSQL en n8n.

3. Ajusta las URLs y parámetros del nodo `httpRequest` para apuntar a Youtube o la API correspondiente.

4. Configura triggers de inicio para lanzar el workflow automáticamente (por ejemplo, usando `executeWorkflowTrigger` o `chatTrigger`).

## Detalles de funcionamiento

- El workflow inicia con un trigger configurado para ejecutar automáticamente o via chat.
- Realiza peticiones HTTP para extraer información y comentarios de vídeos de Youtube.
- Utiliza nodos OpenAI para procesar y analizar comentarios, generando insights o resúmenes.
- Emplea memoria persistente con PostgreSQL para mantener contexto y administrar conversaciones.
- Incluye lógica condicional (switch) y agentes para dirección de flujo y manejo dinámico.
- Las notas adhesivas (`stickyNote`) ayudan a documentar y organizar pasos dentro del workflow.

## Ejemplos de uso

- Extraer los últimos 100 comentarios de un vídeo de Youtube para análisis de sentimiento.
- Generar resúmenes automáticos de debates en los comentarios de un canal.
- Automatizar respuestas inteligentes basadas en el tono y contenido de los comentarios.
- Monitorear palabras clave o temas recurrentes en vídeos y chats.

---

**Número de nodos:** 29  
**Categoría:** utilidades / scraping  
**Etiquetas:** *(no definidas)*  
```