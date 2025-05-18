```markdown
# Asistente Telegram responde con Voz

## Descripción
Workflow para n8n que actúa como un asistente inteligente en Telegram, utilizando agentes de IA para responder mensajes de texto y convertir las respuestas en audio, permitiendo la interacción mediante voz.

## Requisitos
- Cuenta y bot de Telegram con token API.
- API Key de OpenAI para acceso a modelos de lenguaje.
- Credenciales configuradas en n8n para Telegram y OpenAI.
- n8n con nodos de LangChain instalados (`@n8n/n8n-nodes-langchain`).

## Instrucciones de configuración
1. Crear un bot en Telegram y obtener el token API.
2. Configurar la credencial de Telegram en n8n con dicho token.
3. Crear una cuenta en OpenAI y obtener la API Key.
4. Configurar la credencial de OpenAI en n8n.
5. Importar el workflow en n8n.
6. Configurar los nodos `telegramTrigger` y `telegram` con la credencial de Telegram.
7. Verificar que los nodos LangChain use la credencial de OpenAI correctamente.
8. Ajustar parámetros según el idioma o preferencias específicas.

## Detalles de funcionamiento
- El workflow escucha mensajes entrantes de Telegram.
- Usa agentes IA basados en modelos OpenAI para generar respuestas textuales.
- Aplica memoria de contexto a través de `memoryBufferWindow` para mantener la conversación coherente.
- Convierte el texto generado en mensajes de voz (audio) que se envían de vuelta al usuario.
- Incluye lógica condicional y switches para manejar diferentes tipos de mensajes o comandos.
- Usa nodos de código para procesamiento personalizado y nodos `set` para manipular datos.

## Ejemplos de uso
- El usuario envía un mensaje por Telegram, por ejemplo:  
  _"¿Cuál es el pronóstico del tiempo para hoy?"_  
  El bot responde con un mensaje de voz con la respuesta generada por el agente IA.
- Comandos especiales pueden activar modos específicos o respuestas diferentes según el flujo configurado.

---

**Número de nodos:** 16  
**Categoría:** agentes-ia/telegram  
**Etiquetas:** Telegram, Agente  
**Tipos de nodos:**  
`@n8n/n8n-nodes-langchain.openAi`,  
`@n8n/n8n-nodes-langchain.lmChatOpenAi`,  
`n8n-nodes-base.switch`,  
`n8n-nodes-base.telegramTrigger`,  
`n8n-nodes-base.if`,  
`@n8n/n8n-nodes-langchain.memoryBufferWindow`,  
`n8n-nodes-base.telegram`,  
`n8n-nodes-base.code`,  
`@n8n/n8n-nodes-langchain.agent`,  
`n8n-nodes-base.set`
```