```markdown
# 1. Agente para Abogados - IA Principal Master

## Descripción
Workflow diseñado como un agente inteligente para abogados, que integra múltiples herramientas de IA y comunicación para asistir en tareas legales vía Telegram. Utiliza modelos de lenguaje avanzados, memoria dinámica en PostgreSQL y herramientas especializadas para proporcionar respuestas precisas y gestión eficaz.

## Requisitos
- Credenciales de OpenAI (API Key) para nodos de lenguaje y chat (`@n8n/n8n-nodes-langchain.openAi`, `@n8n/n8n-nodes-langchain.lmChatOpenAi`)
- Acceso a base de datos PostgreSQL para memoria de chat (`@n8n/n8n-nodes-langchain.memoryPostgresChat`)
- API y credenciales de Telegram para triggers y envío de mensajes (`n8n-nodes-base.telegramTrigger`, `n8n-nodes-base.telegram`)
- Acceso a n8n con los nodos instalados correspondientes

## Instrucciones de configuración
1. Configura las credenciales de OpenAI en n8n con tu API Key.
2. Configura una instancia PostgreSQL y vincúlala en el nodo de memoria.
3. Registra un bot en Telegram y añade sus credenciales en los nodos correspondientes.
4. Ajusta los parámetros del nodo `switch` para personalizar el flujo según necesidades.
5. Revisa y adapta las configuraciones de herramientas como la calculadora y workflow integrados.

## Detalles de funcionamiento
- El workflow inicia con un trigger vía Telegram que detecta mensajes de usuarios.
- Utiliza modelos OpenAI para procesar y generar respuestas inteligentes.
- Emplea memoria en PostgreSQL para mantener el contexto de conversaciones anteriores.
- Herramientas integradas como calculadora y ejecución de workflows automatizan tareas específicas.
- El nodo `switch` direcciona el flujo según comandos o tipos de consulta recibidos.
- Mensajes son enviados de vuelta al usuario por Telegram, con posibilidad de notas adhesivas internas para seguimiento.

## Ejemplos de uso
- El abogado envía una consulta legal a través de Telegram y recibe una respuesta contextualizada.
- Solicitudes de cálculos legales o financieros son procesadas utilizando la herramienta calculadora.
- Seguimiento de casos usando la memoria persistente para mantener conversaciones previas.
- Automatización de tareas recurrentes a través de workflows integrados disparados desde el chat.

---

**Nodos utilizados (18):**  
`@n8n/n8n-nodes-langchain.openAi`, `@n8n/n8n-nodes-langchain.lmChatOpenAi`, `n8n-nodes-base.switch`, `n8n-nodes-base.telegramTrigger`, `@n8n/n8n-nodes-langchain.toolCalculator`, `@n8n/n8n-nodes-langchain.memoryPostgresChat`, `n8n-nodes-base.telegram`, `@n8n/n8n-nodes-langchain.toolWorkflow`, `n8n-nodes-base.stickyNote`, `n8n-nodes-base.set`, `@n8n/n8n-nodes-langchain.agent`  
(Category: `agentes-ia/otros`)
```