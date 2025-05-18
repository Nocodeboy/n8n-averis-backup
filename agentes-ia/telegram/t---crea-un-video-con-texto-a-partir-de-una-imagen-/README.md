```markdown
# T - Crea un video con texto a partir de una imagen

## Descripción
Este workflow permite crear un video con texto generado a partir de una imagen recibida vía Telegram. Utiliza inteligencia artificial para analizar la imagen y generar contenido textual, que luego se incorpora en un video para enviar de regreso al usuario.

## Requisitos
- Credenciales de Telegram Bot para recibir y enviar mensajes.
- API Key de OpenAI para generación de texto (OpenAI node via LangChain).
- Acceso a Google Sheets para lectura o registro de datos (opcional).
- Configuración de acceso HTTP para tratar recursos externos si es necesario.

## Instrucciones de configuración
1. Configura las credenciales de Telegram en n8n (`telegramTrigger` y `telegram` nodes).
2. Añade la API Key de OpenAI en el nodo correspondiente (`@n8n/n8n-nodes-langchain.openAi`).
3. Vincula la credencial de Google Sheets para acceso a las hojas de cálculo utilizadas.
4. Ajusta parámetros de los nodos `httpRequest` y `code` según requiera el procesamiento del video.
5. Establece tiempos de espera oportunos en el nodo `wait` para controlar el flujo.

## Detalles de funcionamiento
- El flujo inicia con un mensaje o imagen recibida por Telegram (`telegramTrigger`).
- Se extrae y procesa la imagen para generar un texto descriptivo mediante OpenAI.
- El texto generado se procesa y registra en Google Sheets para control o log.
- Utilizando nodos `httpRequest` y `code`, se crea un video combinando la imagen original con el texto generado.
- Luego de un tiempo de espera controlado por el nodo `wait`, el video se envía de regreso al usuario vía Telegram.
- En total, el workflow utiliza 21 nodos que colaboran para automatizar la creación y distribución del contenido.

## Ejemplos de uso
- Enviar una imagen a tu bot de Telegram para recibir un video con una descripción o narración generada automáticamente.
- Generar reportes visuales en video a partir de imágenes y texto para uso educativo o marketing.
- Automatizar la creación de contenido dinámico para redes sociales basado en imágenes enviadas por usuarios.
```
