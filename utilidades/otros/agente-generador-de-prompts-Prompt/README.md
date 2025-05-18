```markdown
# Agente generador de prompts

## Descripción
Este workflow de n8n automatiza la generación de prompts efectivos utilizando técnicas avanzadas de lenguaje natural y agentes inteligentes. Ideal para optimizar procesos que requieran creación dinámica de prompts para variadas aplicaciones.

## Requisitos
- Credenciales de OpenAI con acceso a modelos de lenguaje (para `lmChatOpenAi`).
- Configuración de nodos LangChain (`chainLlm`, `agent`, `chatTrigger`).
- n8n versión compatible con los nodos:
  - `n8n-nodes-base.aggregate`
  - `n8n-nodes-base.merge`
  - `@n8n/n8n-nodes-langchain`

## Instrucciones de configuración
1. Añadir las credenciales de OpenAI en n8n.
2. Configurar los nodos de LangChain con las credenciales y parámetros adecuados (modelos, temperatura, etc.).
3. Ajustar el nodo `chatTrigger` para iniciar el workflow según el tipo de interacción deseada.
4. Verificar las conexiones entre los 15 nodos que conforman el flujo para asegurar el correcto procesamiento.

## Detalles de funcionamiento
- El workflow comienza con un disparador de chat (`chatTrigger`).
- Utiliza agentes LangChain para interpretar y generar contenido basado en la conversación.
- Emplea nodos `aggregate` y `merge` para consolidar respuestas y datos.
- Finalmente, mediante el agente generador, construye prompts refinados y personalizados para la tarea requerida.

## Ejemplos de uso
- Generar prompts personalizados para asistentes virtuales.
- Crear preguntas específicas para chatbots en atención al cliente.
- Automatizar la generación de consultas para sistemas de análisis de texto.

---
**Categoría:** utilidades/otros  
**Etiquetas:** Prompt, Utilidad  
**Número de nodos:** 15  
**Nodos principales:** `n8n-nodes-base.aggregate`, `@n8n/n8n-nodes-langchain.lmChatOpenAi`, `n8n-nodes-base.merge`, `@n8n/n8n-nodes-langchain.chainLlm`, `@n8n/n8n-nodes-langchain.agent`, `@n8n/n8n-nodes-langchain.chatTrigger`
```