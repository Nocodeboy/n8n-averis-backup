```markdown
# T - Crea un video hablando a partir de una imagen

## Descripción
Workflow de n8n que genera un video narrado basado en una imagen enviada vía Telegram. Utiliza inteligencia artificial para analizar la imagen, generar un guion y producir un video con locución automatizada.

## Requisitos
- Credenciales de Google Sheets (acceso para lectura/escritura)
- API de OpenAI (para generación de texto mediante Langchain)
- Token de Telegram Bot (para interactuar con usuarios)
- Acceso a servicios HTTP necesarios para creación y almacenamiento del video

## Instrucciones de configuración
1. Configure el nodo `Telegram Trigger` con el token de su bot de Telegram.
2. Proporcione las credenciales de Google Sheets para acceder a la hoja correspondiente.
3. Configure el nodo de OpenAI con su API key válida.
4. Ajuste los nodos HTTP Request para apuntar a los endpoints del servicio de generación y almacenamiento de videos, si aplica.
5. Revise y adapte cualquier configuración personalizada en nodos `Code` y `Wait` según sus necesidades.
6. Habilite el workflow y pruébelo enviando una imagen vía Telegram al bot.

## Detalles de funcionamiento
- El flujo inicia con la recepción de una imagen por Telegram.
- Utiliza OpenAI para analizar la imagen y generar un texto descriptivo o narrativo.
- Se guarda información relevante en Google Sheets para seguimiento.
- Posteriormente, se crea un video con locución a partir del texto generado.
- El video final se envía de vuelta al usuario por Telegram.
- Incluye esperas y validaciones para asegurar un procesamiento correcto y sincrónico.

## Ejemplos de uso
- Enviar una foto desde Telegram al bot.
- Recibir automáticamente un video narrado que describe o comenta la imagen enviada.
- Utilizar para creación de contenido multimedia automático en canales o chats.

---
**Categoría:** agentes-ia/telegram  
**Nodos utilizados:** n8n-nodes-base.googleSheets, @n8n/n8n-nodes-langchain.openAi, n8n-nodes-base.telegramTrigger, n8n-nodes-base.code, n8n-nodes-base.telegram, n8n-nodes-base.httpRequest, n8n-nodes-base.wait  
**Número de nodos:** 26
```