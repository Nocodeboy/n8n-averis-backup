```markdown
# Creación Automática de Contenido para Instagram desde Tendencias con IA Multimodal

## Descripción  
Workflow diseñado para generar contenido atractivo y relevante para Instagram utilizando inteligencia artificial multimodal basada en tendencias actuales. Automatiza la captura de datos, generación de texto e imágenes, y publicación en redes sociales.

## Requisitos  
- Credenciales de OpenAI para acceso al nodo `@n8n/n8n-nodes-langchain.openAi`  
- Acceso a base de datos PostgreSQL para almacenamiento y consulta de datos (`n8n-nodes-base.postgres`)  
- Token de Facebook Graph API con permisos de gestión para Instagram (`n8n-nodes-base.facebookGraphApi`)  
- Token de Telegram para notificaciones en canales específicos (`n8n-nodes-base.telegram`)  
- API públicas para consulta de tendencias o datos externos (configurable en `n8n-nodes-base.httpRequest`)  

## Instrucciones de configuración  
1. Configurar las credenciales necesarias en n8n: OpenAI, PostgreSQL, Facebook Graph API y Telegram.  
2. Ajustar en el nodo `scheduleTrigger` la frecuencia con la que se desea ejecutar el workflow.  
3. Personalizar consultas en nodos HTTP para fuentes de tendencias según preferencia.  
4. Modificar los parámetros de generación en el nodo OpenAI para adaptar el tono y formato del contenido.  
5. Verificar configuración y permisos en la cuenta de Instagram vinculada en Facebook Graph API.  
6. Guardar y activar el workflow.

## Detalles de funcionamiento  
- El trigger de programación inicia el flujo según intervalo definido.  
- Se recopilan tendencias e información desde APIs externas mediante solicitudes HTTP.  
- Se procesan y filtran datos relevantes mediante nodos Merge, If y Code para preparar inputs.  
- IA multimodal genera textos y sugerencias de imágenes utilizando OpenAI.  
- Contenido generado se divide en batches y se revisa antes de publicación.  
- Publicación automática en Instagram mediante Facebook Graph API.  
- Notificaciones por Telegram informan estado y errores del proceso.  
- Datos y logs almacenados en PostgreSQL para análisis posterior.

## Ejemplos de uso  
- Automatizar campañas de marketing basadas en tendencias virales.  
- Generar posts diarios con texto y visuales optimizados para Instagram.  
- Recibir alertas inmediatas en Telegram sobre el estado de las publicaciones.  
- Utilizar como base para expansión a otras redes sociales con ajustes mínimos.

---

**Categoría:** marketing/contenido  
**Nodos utilizados:** @n8n/n8n-nodes-langchain.openAi, n8n-nodes-base.merge, n8n-nodes-base.if, n8n-nodes-base.code, n8n-nodes-base.telegram, n8n-nodes-base.scheduleTrigger, n8n-nodes-base.stickyNote, n8n-nodes-base.set, n8n-nodes-base.postgres, n8n-nodes-base.splitInBatches, n8n-nodes-base.httpRequest, n8n-nodes-base.facebookGraphApi  
**Número de nodos:** 44
```