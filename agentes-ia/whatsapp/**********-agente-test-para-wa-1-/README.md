```markdown
# ********** Agente test para WA 1

## Descripción
Workflow para n8n que implementa un agente inteligente para WhatsApp, integrando capacidades avanzadas de IA mediante nodos LangChain y OpenAI. Permite la gestión dinámica de conversaciones, acceso a Google Drive y procesamiento eficiente de mensajes entrantes y salientes.

## Requisitos
- Credenciales de OpenAI con acceso a API keys para nodos `@n8n/n8n-nodes-langchain.openAi` y `lmChatOpenAi`.
- Configuración de cuenta y credenciales para el nodo `n8n-nodes-base.whatsApp` y `n8n-nodes-base.whatsAppTrigger`.
- Acceso y permisos adecuados a Google Drive para el nodo `n8n-nodes-base.googleDrive`.
- Base de datos PostgreSQL configurada para `@n8n/n8n-nodes-langchain.memoryPostgresChat`.
- Acceso a internet para nodos HTTP Request y herramientas externas.

## Instrucciones de Configuración
1. **OpenAI**: Ingrese su API key en las credenciales de OpenAI dentro de n8n.
2. **WhatsApp**: Configure el nodo WhatsApp Trigger y WhatsApp con las credenciales y parámetros necesarios para recepción y envío de mensajes.
3. **Google Drive**: Establezca las credenciales OAuth2 para acceder y manipular archivos en Google Drive.
4. **PostgreSQL**: Configure la conexión a la base de datos para la memoria conversacional.
5. **Variables y entorno**: Asegúrese de definir las variables necesarias y revisar los parámetros en los nodos `set` y `switch` según su caso de uso.

## Detalles de Funcionamiento
- El workflow escucha mensajes entrantes vía WhatsApp Trigger.
- Utiliza modelos de lenguaje OpenAI a través de LangChain para analizar y generar respuestas contextuales.
- Implementa lógica condicional con nodos `switch`.
- Almacena el estado y contexto conversacional en PostgreSQL para mantener coherencia.
- Accede a Google Drive para recuperar o almacenar información relevante.
- Control de flujo y paralelización mediante nodos `splitInBatches`, `wait` y `noOp`.
- Manejo de herramientas y agentes personalizados para ampliar funcionalidades.

## Ejemplos de Uso
- Responder consultas automatizadas recibidas en WhatsApp con soporte de IA.
- Integrar documentos o recursos almacenados en Google Drive en las respuestas.
- Mantener conversación persistente optimizando seguimiento contextual.
- Analizar y filtrar mensajes para distintas rutas de procesamiento según reglas definidas.

---

**Número de nodos:** 37  
**Categoría:** agentes-ia/whatsapp  
**Etiquetas:** *Sin etiquetas definidas*  
**Nodos clave:**  
`@n8n/n8n-nodes-langchain.openAi`, `@n8n/n8n-nodes-langchain.lmChatOpenAi`, `n8n-nodes-base.whatsApp`, `n8n-nodes-base.googleDrive`, `@n8n/n8n-nodes-langchain.memoryPostgresChat`, `n8n-nodes-base.switch`, entre otros.
```