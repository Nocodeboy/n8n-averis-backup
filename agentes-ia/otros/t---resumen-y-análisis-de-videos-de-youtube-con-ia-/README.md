# T - Resumen y análisis de videos de YouTube con IA

## Descripción
Workflow que permite obtener la transcripción, resumen y análisis de videos de YouTube utilizando inteligencia artificial. Ideal para extraer información clave y generar reportes automáticos de contenido audiovisual.

## Requisitos
- Credenciales de YouTube API para acceder a videos y transcripciones.
- API Key de OpenAI para usar los nodos de lenguaje (ChatOpenAi y chainLlm).
- Configuración de Telegram Bot para enviar notificaciones o respuestas.
- n8n instalado y configurado con los nodos necesarios.

## Instrucciones de configuración
1. Configura las credenciales de YouTube en n8n.
2. Añade y configura las credenciales de OpenAI (API Key).
3. Configura el webhook para recibir solicitudes externas.
4. Configura el bot de Telegram con su token y chat ID si deseas recibir resultados vía Telegram.
5. Importa y activa el workflow en tu instancia de n8n.

## Detalles de funcionamiento
El workflow consta de 12 nodos que permiten:

- Capturar el enlace o ID del video vía webhook o Telegram.
- Obtener los datos e iniciar la transcripción utilizando el nodo `youtubeTranscripter`.
- Procesar y dividir el texto transcrito para facilitar su análisis.
- Resumir y analizar la información con modelos de lenguaje basados en OpenAI mediante los nodos `lmChatOpenAi` y `chainLlm`.
- Enviar el resumen y análisis final al usuario vía Telegram o respuesta webhook.

## Ejemplos de uso
- Ingresar un link de video de YouTube a través del webhook para recibir un resumen detallado por Telegram.
- Usar Telegram para enviar un ID de video y obtener un análisis del contenido directamente en el chat.
- Automatizar la creación de informes de videos educativos o conferencias para facilitar su revisión.

---

**Categoría:** agentes-ia/otros  
**Nodos utilizados:**  
`@n8n/n8n-nodes-langchain.lmChatOpenAi`, `@n8n/n8n-nodes-langchain.chainLlm`, `n8n-nodes-base.code`, `n8n-nodes-base.telegram`, `n8n-nodes-youtube-transcription.youtubeTranscripter`, `n8n-nodes-base.set`, `n8n-nodes-base.splitOut`, `n8n-nodes-base.summarize`, `n8n-nodes-base.respondToWebhook`, `n8n-nodes-base.youTube`, `n8n-nodes-base.webhook`  

**Número de nodos:** 12