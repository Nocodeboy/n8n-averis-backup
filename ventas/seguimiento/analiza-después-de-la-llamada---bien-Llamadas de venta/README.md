```markdown
# Analiza después de la llamada - Bien

## Descripción
Workflow diseñado para automatizar el análisis y seguimiento después de llamadas de venta. Integra procesamiento de lenguaje natural, gestión de tareas y comunicación con clientes para optimizar el flujo de trabajo comercial.

## Requisitos
- Credenciales de OpenAI para el nodo `@n8n/n8n-nodes-langchain.openAi`
- Cuenta y API Key de HubSpot para `n8n-nodes-base.hubspot`
- Credenciales de Gmail para el nodo `n8n-nodes-base.gmail`
- Cuenta de Asana con token API para `n8n-nodes-base.asana`
- Acceso a los servicios de webhook y HTTP Request configurados en n8n

## Instrucciones de configuración
1. Configura las credenciales de OpenAI, Gmail, HubSpot y Asana en n8n.
2. Ajusta los endpoints y claves API en nodos `httpRequest` y `webhook` según tu infraestructura.
3. Personaliza las reglas lógicas en nodos `if` y la lógica en nodos `code` según tus criterios de negocio.
4. Define las plantillas HTML y Markdown para el procesamiento y generación de reportes o comunicaciones.

## Detalles de funcionamiento
- Recibe datos tras la llamada de venta mediante un webhook.
- Utiliza OpenAI para análisis semántico y generación de insights.
- Agrega y filtra información con nodos de agregación y condición.
- Gestiona tareas en Asana y actualiza contactos en HubSpot.
- Envía notificaciones y resumen de seguimiento vía Gmail.
- Divide, transforma y formatea los contenidos usando nodos `splitOut`, `set`, `html` y `markdown`.
- Incluye notas y recordatorios visuales con nodos `stickyNote`.

## Ejemplos de uso
- Automatizar el resumen y clasificación de llamadas de ventas entrantes.
- Actualizar automáticamente el estado de clientes en HubSpot post-llamada.
- Crear tareas de seguimiento en Asana basadas en el resultado del análisis de la conversación.
- Enviar emails con reportes personalizados al equipo comercial tras cada llamada.

---

**Categoría:** ventas/seguimiento  
**Etiquetas:** Llamadas de venta  
**Número de nodos:** 43  
**Tipos de nodos:**  
`@n8n/n8n-nodes-langchain.openAi`, `n8n-nodes-base.aggregate`, `n8n-nodes-base.hubspot`, `n8n-nodes-base.html`, `n8n-nodes-base.if`, `n8n-nodes-base.asana`, `n8n-nodes-base.code`, `n8n-nodes-base.gmail`, `n8n-nodes-base.stickyNote`, `n8n-nodes-base.set`, `n8n-nodes-base.splitOut`, `n8n-nodes-base.httpRequest`, `n8n-nodes-base.markdown`, `n8n-nodes-base.webhook`
```