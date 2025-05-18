```markdown
# Agente de viajes con IA Elevenlabs

## Descripción
Workflow diseñado para actuar como un agente de viajes inteligente utilizando modelos de lenguaje de OpenAI y síntesis de voz con Elevenlabs, facilitando la gestión y asistencia personalizada en reservas, consultas y recomendaciones.

## Requisitos
- Cuenta y credenciales de OpenAI (API Key) para nodos LangChain:  
  - `@n8n/n8n-nodes-langchain.openAi`  
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`  
  - `@n8n/n8n-nodes-langchain.chainLlm`  
  - `@n8n/n8n-nodes-langchain.agent`  
  - `@n8n/n8n-nodes-langchain.outputParserStructured`
- Credenciales SMTP/Gmail para envío de correos (`n8n-nodes-base.gmail`)
- API de Elevenlabs para síntesis y gestión de voz (configurable en nodos HTTP Request o similares)
- n8n instalado y configurado para ejecutar los 25 nodos del workflow

## Instrucciones de configuración
1. Importar el workflow en n8n.
2. Configurar credenciales de OpenAI en n8n.
3. Añadir credenciales de Gmail para envío/recepción de correos.
4. Registrar y configurar la API key de Elevenlabs en los nodos de HTTP Request o código personalizados.
5. Ajustar los nodos `webhook` para conectarse a las fuentes de entrada deseadas.
6. Verificar y ajustar variables y parámetros según el caso de uso específico.

## Detalles de funcionamiento
- El workflow utiliza múltiples nodos de LangChain para procesamiento, comprensión y generación de texto con inteligencia artificial.
- El agente interpreta las solicitudes de viaje y genera respuestas enriquecidas.
- La salida estructurada permite emitir formatos claros y usables para posteriores acciones.
- El módulo de síntesis de voz con Elevenlabs transforma las respuestas en audio.
- Se envían correos vía Gmail para confirmaciones o notificaciones.
- Utiliza un webhook para recibir solicitudes externas, y nodos de código para lógica personalizada.
- En total constan 25 nodos interconectados que optimizan la experiencia del agente.

## Ejemplos de uso
- Un usuario envía una consulta a través del webhook preguntando por opciones de vuelos a París.
- El agente procesa la solicitud, consulta las APIs internas, genera respuesta en texto y audio.
- Se envía un correo con el itinerario al usuario.
- El usuario recibe notificaciones personalizadas y recomendaciones inmediatas vía voz o email.

---

**Categoría:** agentes-ia/otros  
**Número de nodos:** 25  
**Nodos utilizados:**  
`@n8n/n8n-nodes-langchain.openAi`,  
`@n8n/n8n-nodes-langchain.lmChatOpenAi`,  
`@n8n/n8n-nodes-langchain.chainLlm`,  
`n8n-nodes-base.code`,  
`n8n-nodes-base.gmail`,  
`@n8n/n8n-nodes-langchain.agent`,  
`n8n-nodes-base.set`,  
`@n8n/n8n-nodes-langchain.outputParserStructured`,  
`n8n-nodes-base.httpRequest`,  
`n8n-nodes-base.webhook`
```