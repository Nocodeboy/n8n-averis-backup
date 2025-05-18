```markdown
# Búsqueda de leads Agente Worker

## Descripción
Workflow diseñado para automatizar la generación y gestión de leads en el área de ventas. Utiliza integración con OpenAI, Google Sheets y Gmail para buscar, procesar y contactar potenciales clientes de manera eficiente.

## Requisitos
- Credenciales de API de OpenAI.
- Credenciales y acceso a Google Sheets.
- Cuenta Gmail configurada con acceso SMTP/IMAP.
- n8n instalado y configurado con los siguientes nodos disponibles:
  - `@n8n/n8n-nodes-langchain.openAi`
  - `n8n-nodes-base.googleSheets`
  - `n8n-nodes-base.html`
  - `n8n-nodes-base.code`
  - `n8n-nodes-base.gmail`
  - `n8n-nodes-base.stickyNote`
  - `n8n-nodes-base.executeWorkflowTrigger`
  - `n8n-nodes-base.set`
  - `n8n-nodes-base.httpRequest`

## Instrucciones de configuración
1. Configure sus credenciales en n8n para OpenAI, Google Sheets y Gmail.
2. En el nodo Google Sheets, establezca la hoja y rango donde se almacenarán o leerán los leads.
3. En el nodo OpenAI, asegure la correcta configuración del modelo y prompts para la búsqueda y filtrado de leads.
4. Ajuste los parámetros del nodo HTTP Request si se integran APIs externas para enriquecimiento de datos.
5. Configure las plantillas de correo electrónico en el nodo Gmail para el contacto con leads.
6. Active el trigger del workflow para iniciar la automatización según la necesidad.

## Detalles de funcionamiento
- El workflow consta de 20 nodos, integrando procesos desde la extracción y generación de leads con OpenAI, hasta su almacenamiento y gestión en Google Sheets.
- Se utiliza Node HTML para formatear la información, y nodos de código para lógica personalizada.
- Correos de contacto se envían automáticamente con Gmail según criterios definidos.
- Sticky Notes y otros nodos permiten seguimiento y anotaciones internas durante el proceso.
- El workflow puede ser iniciado manualmente o mediante triggers configurados.

## Ejemplos de uso
- Generar una lista semanal de leads cualificados para seguimiento comercial.
- Enriquecer contactos existentes con información adicional obtenida vía API.
- Automatizar el envío de correos personalizados a nuevos leads identificados.
- Mantener un registro sincronizado y actualizado de leads en Google Sheets para el equipo de ventas.

---

**Categoría:** ventas/lead-generation  
**Etiquetas:** Worker, Agente  
**Número de nodos:** 20
```