```markdown
# Enriquece FAQs

## Descripción  
Workflow diseñado para enriquecer y gestionar FAQs mediante integración con múltiples servicios como Google Sheets, Webflow, Strapi, WordPress y modelos de lenguaje OpenAI. Automatiza la recopilación, procesamiento y publicación de contenido FAQ actualizado y optimizado.

## Requisitos  
- Credenciales configuradas para:
  - Google Sheets  
  - Google Drive  
  - Webflow  
  - Strapi  
  - WordPress  
  - OpenAI (para el nodo lmChatOpenAi)  
- Permisos adecuados para ejecutar workflows y acceder a las APIs mencionadas.

## Instrucciones de configuración  
1. Añade y configura las credenciales necesarias en n8n para cada servicio.  
2. Ajusta los parámetros de cada nodo para apuntar a tus recursos específicos (hojas de cálculo, sitios web, colecciones Strapi, etc.).  
3. Configura la clave API de OpenAI en el nodo `lmChatOpenAi`.  
4. Revisa y personaliza las reglas en nodos de tipo `switch` e `if` según tu lógica de enriquecimiento.  
5. Activa el trigger manual o programado para iniciar el workflow.

## Detalles de funcionamiento  
- El workflow inicia mediante un trigger manual o evento programado.  
- Los datos FAQ se extraen principalmente de Google Sheets y se agregan usando el nodo `aggregate`.  
- La información se procesa y enriquece con modelos de lenguaje OpenAI a través de `lmChatOpenAi` y `chainLlm`.  
- Dependiendo de las condiciones, los datos son enviados a plataformas como Webflow, Strapi o WordPress para su publicación o actualización.  
- Los nodos `switch` e `if` controlan el flujo según criterios definidos.  
- Se emplean nodos de lotes (`splitInBatches`, `splitOut`) para manejar grandes volúmenes.  
- Integración con Google Drive ayuda en la gestión documental relacionada.  
- El workflow puede llamar a otros workflows a través de `executeWorkflow` y `executeWorkflowTrigger`.  
- Se utilizan notas adhesivas (`stickyNote`) para documentación interna y seguimiento.

## Ejemplos de uso  
- Enriquecer FAQs de un sitio Webflow con contenido generado automáticamente por OpenAI.  
- Sincronizar y actualizar FAQs almacenadas en Google Sheets con una plataforma WordPress.  
- Gestionar colecciones FAQ en Strapi alimentadas por datos dinámicos y enriquecidos.  
- Automatización de procesos FAQ para e-commerce o plataformas de soporte usando flujos integrados y condiciones personalizadas.

---
**Categoría:** utilidades/integraciones  
**Número de nodos:** 36  
**Nodos utilizados:**  
`n8n-nodes-base.aggregate`,  
`@n8n/n8n-nodes-langchain.lmChatOpenAi`,  
`n8n-nodes-base.googleSheets`,  
`n8n-nodes-base.googleDrive`,  
`n8n-nodes-base.switch`,  
`n8n-nodes-base.webflow`,  
`n8n-nodes-base.if`,  
`n8n-nodes-base.manualTrigger`,  
`@n8n/n8n-nodes-langchain.chainLlm`,  
`n8n-nodes-base.executeWorkflow`,  
`n8n-nodes-base.strapi`,  
`n8n-nodes-base.stickyNote`,  
`n8n-nodes-base.set`,  
`n8n-nodes-base.executeWorkflowTrigger`,  
`n8n-nodes-base.splitInBatches`,  
`n8n-nodes-base.splitOut`,  
`n8n-nodes-base.httpRequest`,  
`n8n-nodes-base.wordpress`
```