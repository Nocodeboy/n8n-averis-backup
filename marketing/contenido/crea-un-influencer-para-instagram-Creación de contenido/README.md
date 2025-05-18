```markdown
# Crea un Influencer para Instagram

## Descripción
Workflow de n8n diseñado para automatizar la creación y gestión de un influencer en Instagram, generando contenido visual y textual personalizado, gestionando perfiles y publicaciones mediante integración con múltiples APIs y servicios.

## Requisitos
- Credenciales de acceso para:
  - OpenAI (modelo ChatGPT para generación de texto)
  - Supabase (base de datos y almacenamiento)
  - Gmail (envío de correos)
  - Facebook Graph API (para gestión de Instagram)
- n8n con los siguientes nodos instalados:
  - n8n-nodes-base.aggregate
  - @n8n/n8n-nodes-langchain.lmChatOpenAi
  - n8n-nodes-base.supabase
  - n8n-nodes-base.if
  - n8n-nodes-base.manualTrigger
  - n8n-nodes-base.convertToFile
  - n8n-nodes-base.crypto
  - n8n-nodes-base.gmail
  - n8n-nodes-base.stickyNote
  - n8n-nodes-base.set
  - @n8n/n8n-nodes-langchain.informationExtractor
  - n8n-nodes-base.facebookGraphApi
  - n8n-nodes-base.httpRequest

## Instrucciones de configuración
1. Importa el workflow en tu instancia n8n.
2. Configura las credenciales para cada servicio requerido (OpenAI, Supabase, Gmail, Facebook).
3. Ajusta los parámetros en los nodos `set` y `httpRequest` según las necesidades particulares del proyecto.
4. Verifica los permisos y accesos en las APIs conectadas.
5. Ejecuta el workflow manualmente o programa disparadores según el caso.

## Detalles de funcionamiento
Este workflow consta de 53 nodos que trabajan conjuntamente para:

- Generar contenido textual con inteligencia artificial mediante OpenAI.
- Extraer información relevante usando nodos Langchain.
- Administrar y almacenar datos en Supabase.
- Crear imágenes y avatares personalizados para Instagram.
- Validar condiciones con nodos de tipo `if`.
- Convertir contenido para formatos de archivo compatibles.
- Enviar notificaciones y reportes por Gmail.
- Interactuar con Instagram mediante Facebook Graph API para publicar y gestionar contenido.
- Monitorizar y agregar datos usando nodos aggregate.
- Mantener notas y estados con sticky notes internos.

## Ejemplos de uso
- Automatización para creación semanal de posts de Instagram con textos y avatares generados automáticamente.
- Gestión centralizada de contenido para influencers emergentes.
- Integración con campañas de marketing digital, personalizando la comunicación según analíticas previas.
- Envío automático de reportes y alertas a equipos de contenido o marketing.

---

**Etiquetas:** Creación de contenido, Imagen, Avatar, *****
```