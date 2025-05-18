```markdown
# Test Agente WA Devuelve mensaje voz

## Descripción  
Workflow de n8n que integra un agente basado en IA para WhatsApp, capaz de procesar mensajes recibidos y devolver respuestas en formato de voz utilizando modelos de OpenAI.

## Requisitos  
- Credenciales de WhatsApp configuradas en n8n (API o conexión oficial).  
- Clave API de OpenAI (para nodos Langchain: openAi, lmChatOpenAi, agent).  
- n8n versión compatible con los nodos utilizados.  

## Instrucciones de configuración  
1. Configura las credenciales de WhatsApp en n8n (nodo `whatsApp`, `whatsAppTrigger`).  
2. Añade tu API key de OpenAI en los nodos correspondientes: `@n8n/n8n-nodes-langchain.openAi`, `lmChatOpenAi`, `agent`.  
3. Ajusta parámetros en nodos como `if`, `switch` y `set` para condiciones específicas del flujo.  
4. Revisa las configuraciones del buffer de memoria (`memoryBufferWindow`) para optimizar el contexto de la conversación.  
5. Carga o personaliza el código en el nodo `code` para la conversión de texto a voz si aplica.  

## Detalles de funcionamiento  
- El workflow se activa con mensajes entrantes en WhatsApp (`whatsAppTrigger`).  
- Se procesa el texto mediante modelos de lenguaje (OpenAI) para interpretar la intención.  
- Mediante nodos `switch` e `if` se definen rutas según el contexto.  
- Se utiliza memoria de ventana (`memoryBufferWindow`) para mantener contexto conversacional.  
- La respuesta generada se convierte en mensaje de voz y se envía de vuelta por WhatsApp (`whatsApp`).  
- El flujo cuenta con nodos auxiliares para manejo de archivos (`extractFromFile`), peticiones HTTP (`httpRequest`) y ejecución de código personalizado (`code`).  

## Ejemplos de uso  
- Un cliente envía un mensaje de voz o texto preguntando por información.  
- El agente analiza el mensaje, genera una respuesta apropiada y la envía en formato de voz.  
- Soporta flujos condicionados para distintos tipos de consultas o comandos.  

---

**Número de nodos:** 31  
**Categoría:** agentes-ia/whatsapp  
**Etiquetas:** Whatsapp  
**Nodos destacados:**  
@n8n/n8n-nodes-langchain.openAi, lmChatOpenAi, agent, whastAppTrigger, whatsapp, switch, if, memoryBufferWindow, extractFromFile  
```