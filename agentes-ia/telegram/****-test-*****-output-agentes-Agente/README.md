```markdown
# **** TEST ***** Output agentes

## Descripción
Workflow de n8n diseñado para gestionar agentes inteligentes integrados con Telegram, utilizando nodos de LangChain para procesamiento avanzado de lenguaje y lógica de agentes. Permite interacción dinámica y multicanal con usuarios vía Telegram, procesando y enrutando consultas mediante múltiples modelos de IA.

## Requisitos
- Cuenta y credenciales de Telegram Bot.
- API key de OpenAI configurada en los nodos LangChain.
- n8n con los siguientes paquetes instalados:
  - `@n8n/n8n-nodes-langchain`
  - nodos base estándar de n8n.
- Acceso a internet para llamadas a APIs externas.

## Instrucciones de configuración
1. **Telegram:**
   - Crear un bot en Telegram a través de BotFather.
   - Configurar las credenciales del bot en n8n (API Token).
2. **OpenAI:**
   - Obtener API Key en [OpenAI](https://platform.openai.com/account/api-keys).
   - Configurar la API Key en los nodos LangChain que requieran acceso a OpenAI.
3. **Importar workflow:**
   - Importar este workflow en tu instancia de n8n.
   - Revisar y adaptar variables o configuraciones específicas si fuera necesario.
4. **Credenciales adicionales:**
   - Configurar credenciales necesarias para nodos adicionales antes de activar el workflow.

## Detalles de funcionamiento
- El workflow inicia con un trigger de Telegram, capturando mensajes entrantes.
- Se evalúan condiciones mediante nodos `switch` y `if` para enrutar solicitudes.
- Nodos LangChain (`openAi`, `lmChatOpenAi`, `chainLlm`, `agent`, entre otros) procesan texto, gestionan contexto y ejecutan lógica compleja.
- Se utiliza memoria de ventana (`memoryBufferWindow`) para mantener el contexto en interacciones continuas.
- Mensajes y respuestas se estructuran y parsean antes de enviarse mediante nodos de salida (`telegram`).
- El control de flujo incluye pausas con nodos `wait`, procesamiento segmentado (`splitInBatches`, `splitOut`) y nodos no operativos (`noOp`) para optimización y claridad.

## Ejemplos de uso
- **Atención automatizada en Telegram:** Usuarios interactúan con un bot que responde preguntas complejas mediante agentes IA.
- **Soporte multicanal:** Adaptar el modelo para recibir e integrar respuestas desde múltiples fuentes y dar seguimiento personalizado.
- **Experimentación con agentes IA:** Probar distintas configuraciones y modelos en la arquitectura de LangChain dentro de n8n.

---

**Nodos utilizados:**  
`@n8n/n8n-nodes-langchain.openAi`, `@n8n/n8n-nodes-langchain.lmChatOpenAi`, `n8n-nodes-base.telegramTrigger`, `n8n-nodes-base.switch`, `n8n-nodes-base.noOp`, `@n8n/n8n-nodes-langchain.lmChatOpenRouter`, `n8n-nodes-base.if`, `@n8n/n8n-nodes-langchain.chainLlm`, `@n8n/n8n-nodes-langchain.memoryBufferWindow`, `n8n-nodes-base.telegram`, `@n8n/n8n-nodes-langchain.agent`, `n8n-nodes-base.set`, `@n8n/n8n-nodes-langchain.outputParserStructured`, `n8n-nodes-base.splitOut`, `n8n-nodes-base.splitInBatches`, `n8n-nodes-base.wait`

**Número de nodos:** 45  
**Categoría:** agentes-ia/telegram  
**Etiquetas:** Agente
```