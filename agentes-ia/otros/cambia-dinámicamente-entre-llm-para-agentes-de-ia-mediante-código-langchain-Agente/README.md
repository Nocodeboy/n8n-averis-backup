```markdown
# Cambia dinámicamente entre LLM para Agentes de IA mediante código LangChain

## Descripción
Este workflow permite seleccionar y cambiar dinámicamente entre diferentes modelos de lenguaje grandes (LLM) para agentes de IA utilizando nodos de código con LangChain en n8n. Ideal para adaptar respuestas según contexto o requisitos específicos de la conversación.

## Requisitos
- Credenciales API para OpenAI o cualquier otro proveedor compatible con LangChain.
- Acceso configurado a n8n con los siguientes nodos instalados:
  - @n8n/n8n-nodes-langchain.lmChatOpenAi
  - @n8n/n8n-nodes-langchain.code
  - @n8n/n8n-nodes-langchain.chainLlm
  - @n8n/n8n-nodes-langchain.chatTrigger
  - @n8n/n8n-nodes-langchain.sentimentAnalysis
  - n8n-nodes-base.noOp
  - n8n-nodes-base.if
  - n8n-nodes-base.stickyNote
  - n8n-nodes-base.set

## Instrucciones de configuración
1. Configure las credenciales de los LLMs en n8n (por ejemplo, OpenAI API Key).
2. Ajuste los parámetros del nodo `lmChatOpenAi` y los nodos de LangChain según las APIs y modelos que desee utilizar.
3. Defina las condiciones en los nodos `if` para controlar la selección dinámica de LLM.
4. Personalice el código LangChain en el nodo `code` para gestionar la lógica de cambio entre agentes.

## Detalles de funcionamiento
- El workflow se inicia con un trigger de chat (`chatTrigger`).
- Mediante análisis de sentimiento y reglas condicionales (`sentimentAnalysis`, `if`), determina qué LLM es el más adecuado.
- Usa nodos de código LangChain para cambiar dinámicamente entre modelos y encadenar llamadas.
- Los nodos `set` y `stickyNote` permiten ajustar y documentar el flujo según las necesidades.
- El nodo `noOp` se emplea para control de flujo sin afectar la ejecución.
- Total de 22 nodos en el flujo para cobertura completa de interacción y lógica.

## Ejemplos de uso
- Un agente de soporte que selecciona distintos modelos según la complejidad o tono del usuario.
- Chatbots multilingües que alternan entre LLM especializados en distintos idiomas.
- Agentes de IA que adaptan su comportamiento analizando el sentimiento detectado en las conversaciones.

---

**Categoría:** agentes-ia/otros  
**Etiquetas:** Agente, Base, *****  
**Número de nodos:** 22
```