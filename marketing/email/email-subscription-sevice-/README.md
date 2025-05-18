```markdown
# Email Subscription Service

## Descripción
Workflow de n8n orientado a marketing por email que gestiona suscripciones, automatiza la comunicación utilizando inteligencia artificial y facilita la integración con servicios externos como Gmail y Airtable.

## Requisitos
- Credenciales de Gmail para envío y gestión de correos electrónicos.
- API Key de OpenAI para nodos `@n8n/n8n-nodes-langchain.openAi` y `@n8n/n8n-nodes-langchain.lmChatGroq`.
- Credenciales de Airtable para almacenamiento y consulta de datos de suscriptores.
- Configuración de webhook o formulario para disparar el workflow.
- Permisos para ejecutar workflows y utilizar nodos personalizados (LangChain, Wikipedia, etc.).

## Instrucciones de configuración
1. Configurar credenciales:
   - Agrega las credenciales de Gmail en n8n.
   - Configura la API Key de OpenAI en los nodos LangChain correspondientes.
   - Introduce las credenciales de Airtable con la base y tabla adecuadas.
2. Configurar el nodo `formTrigger` para capturar las suscripciones entrantes.
3. Ajustar filtros y condiciones específicos según las reglas de suscripción o segmentación deseada.
4. Personalizar mensajes y plantillas en los nodos de código y correo.
5. Configurar el nodo de `scheduleTrigger` para envíos recurrentes o campañas periódicas.
6. Revisar y activar el workflow.

## Detalles de funcionamiento
- El workflow inicia con la captura de datos de suscripción a través del nodo `formTrigger`.
- Se usa inteligencia artificial (OpenAI y Groq) para personalizar respuestas, resolver consultas y gestionar flujos dinámicos mediante agentes y memoria en buffer.
- La información se valida y segmenta con nodos de filtro y código personalizado.
- Los suscriptores quedan registrados y actualizados en Airtable.
- Se envían emails automáticos con Gmail según la etapa del proceso.
- El workflow puede ejecutarse manualmente o programarse con `scheduleTrigger`.
- Herramientas adicionales: generación de contenido (Wikipedia Tool), edición de imágenes y notas adhesivas para control interno.

## Ejemplos de uso
- Captura automática de suscriptores desde un formulario web.
- Envío personalizado de emails de bienvenida y seguimiento utilizando IA.
- Segmentación dinámica de listas según interacciones y respuestas.
- Actualización automática de base de datos en Airtable con nuevos registros.
- Ejecución programada para newsletters o promociones periódicas.
```