```markdown
# Joe Agente Worker

## Descripción
Joe Agente Worker es un workflow de n8n diseñado para actuar como un agente inteligente que interactúa vía Telegram. Utiliza modelos de lenguaje de OpenAI para procesar mensajes, tomar decisiones inteligentes y ejecutar acciones automáticas en función del contexto y las instrucciones recibidas.

## Requisitos
- Cuenta activa en [n8n](https://n8n.io/)
- Credenciales de OpenAI con acceso a modelos GPT (para nodos `@n8n/n8n-nodes-langchain.openAi` y `@n8n/n8n-nodes-langchain.lmChatOpenAi`)
- Token de Telegram Bot para el manejo de mensajes entrantes y respuestas (`telegramTrigger` y `telegram` nodos)
- Configuración adecuada de credenciales en n8n para cada servicio utilizado

## Instrucciones de configuración
1. Crear un bot en Telegram y obtener el token del bot.
2. Configurar las credenciales de Telegram en n8n con el token del bot.
3. Configurar las credenciales de OpenAI en n8n con tu API Key.
4. Importar el workflow "Joe Agente Worker" a tu instancia de n8n.
5. Revisar los nodos `toolWorkflow` y `agent` para adaptarlos si es necesario a tus casos de uso o herramientas adicionales.
6. Ejecutar el workflow o activarlo para que escuche los mensajes entrantes en Telegram.

## Detalles de funcionamiento
- El workflow comienza con un nodo `telegramTrigger` que captura los mensajes entrantes del usuario.
- Utiliza modelos de lenguaje OpenAI para interpretar y generar respuestas mediante los nodos `openAi` y `lmChatOpenAi`.
- La memoria contextual se maneja con el nodo `memoryBufferWindow`, permitiendo mantener una conversación coherente.
- Con un nodo `switch` se toman decisiones basadas en el contenido o estado del mensaje.
- El nodo `agent` coordina la ejecución de acciones o la invocación de sub-workflows (`toolWorkflow`) según la lógica del agente.
- Finalmente, se envían respuestas o resultados al usuario a través del nodo `telegram`.
- Nodos `set` se emplean para preparar y manejar datos durante el flujo.

## Ejemplos de uso
- Envíe un mensaje al bot de Telegram para recibir respuestas inteligentes y contextuales.
- Solicite información o ejecución de tareas específicas que el agente puede manejar mediante workflows auxiliares.
- Use como base para construir agentes personalizados que interactúen con usuarios vía Telegram y aprovechen capacidades avanzadas de IA.

---

*Categoría: agentes-ia/telegram*  
*Nodos totales: 12*  
*Etiquetas: Worker, Agente*  
```