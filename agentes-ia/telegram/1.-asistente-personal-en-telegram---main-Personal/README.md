```markdown
# 1. Asistente Personal en Telegram - Main

## Descripción
Workflow diseñado para funcionar como un asistente personal mediante Telegram, integrando capacidades de IA a través de OpenAI y herramientas específicas para cálculos, memoria conversacional y ejecución de sub-workflows.

## Requisitos
- Cuenta y credenciales de Telegram Bot API.
- API Key de OpenAI para acceso a los nodos `openAi` y `lmChatOpenAi`.
- Credenciales configuradas en n8n para nodos LangChain (`@n8n/n8n-nodes-langchain.*`).
- Acceso a n8n con soporte para nodos personalizados y workflows.

## Instrucciones de configuración
1. Crear un bot en Telegram y obtener el token.
2. En n8n, configurar las credenciales de Telegram con el token del bot.
3. Configurar las credenciales de OpenAI con la API Key correspondiente.
4. Importar el workflow y verificar que las credenciales estén asignadas a cada nodo pertinente.
5. Ajustar parámetros específicos en nodos `switch` o de configuración según la necesidad personal.

## Detalles de funcionamiento
- El workflow inicia con un trigger de Telegram que escucha mensajes entrantes.
- Utiliza nodos LangChain para procesar texto mediante modelos OpenAI y manejo de memoria contextual.
- Implementa herramientas para cálculo dinámico (`toolCalculator`) y ejecución de sub-workflows (`toolWorkflow`).
- Usa nodos `switch` para dirigir el flujo según el tipo de consulta o comando recibido.
- La integración de memoria buffer permite mantener contexto en conversaciones largas.
- El agente LangChain coordina las respuestas combinando capacidades de IA y herramientas específicas.

## Ejemplos de uso
- Consultar información personalizada o general a través del bot de Telegram.
- Realizar cálculos matemáticos simples directamente en la conversación.
- Interactuar con el asistente para obtener respuestas que consideren el contexto histórico de la conversación.
- Ejecutar comandos que disparen flujos secundarios definidos en sub-workflows.

---

**Categoría:** agentes-ia/telegram  
**Etiquetas:** Personal, Telegram  
**Número de nodos:** 18  
**Tipos de nodos:**  
`@n8n/n8n-nodes-langchain.openAi, @n8n/n8n-nodes-langchain.lmChatOpenAi, @n8n/n8n-nodes-langchain.toolCalculator, n8n-nodes-base.telegramTrigger, n8n-nodes-base.switch, n8n-nodes-base.merge, @n8n/n8n-nodes-langchain.memoryBufferWindow, @n8n/n8n-nodes-langchain.toolWorkflow, n8n-nodes-base.telegram, @n8n/n8n-nodes-langchain.agent, n8n-nodes-base.set`
```
