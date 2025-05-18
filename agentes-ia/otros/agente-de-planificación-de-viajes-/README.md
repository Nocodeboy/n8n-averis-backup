```markdown
# Agente de planificación de viajes

## Descripción

Workflow para asistir en la planificación de viajes mediante IA, integrando servicios de correo, agentes conversacionales y APIs externas para ofrecer recomendaciones personalizadas y gestionar solicitudes.

## Requisitos

- Credenciales de OpenAI para nodos `lmChatOpenAi` y `chainLlm`
- Credenciales de Anthropic para nodo `lmChatAnthropic`
- Cuenta de Gmail configurada para nodo `gmail`
- API externas accesibles mediante nodo `httpRequest`
- Credenciales configuradas en n8n para nodos `webhook` y `respondToWebhook`

## Instrucciones de configuración

1. Importar el workflow `Agente de planificación de viajes` en n8n.
2. Configurar credenciales de OpenAI y Anthropic en n8n.
3. Configurar la cuenta Gmail para envío y recepción de correos.
4. Ajustar URLs y parámetros en nodos `httpRequest` según las APIs externas utilizadas.
5. Definir y activar Webhooks para iniciar el agente.

## Detalles de funcionamiento

- Combina múltiples modelos de lenguaje (OpenAI y Anthropic) para procesamiento y generación de texto.
- Utiliza agentes LangChain para orquestar tareas de planificación.
- Gestiona comunicación vía Gmail para interacción con usuarios.
- Emplea nodos `set` y `outputParserStructured` para estructura y formateo de datos.
- Maneja solicitudes entrantes a través de webhooks HTTP y responde automáticamente.

## Ejemplos de uso

- Un usuario envía una solicitud de planificación de viaje por correo electrónico.
- El agente analiza la solicitud mediante IA, consulta APIs para vuelos y alojamientos.
- Responde al usuario con un itinerario personalizado, gestionando toda la comunicación automáticamente.
```