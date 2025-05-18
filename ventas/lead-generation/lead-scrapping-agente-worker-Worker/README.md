```markdown
# Lead Scrapping Agente Worker

## Descripción
Workflow orientado a la generación y gestión automatizada de leads para equipos de ventas. Extrae, filtra y procesa información de distintas fuentes, integrándola con Google Sheets para facilitar el seguimiento y la acción comercial.

## Requisitos
- Credenciales de Google Sheets con acceso a la hoja destino.
- Acceso a las APIs externas utilizadas en el nodo HTTP Request (según configuración).
- n8n instalado y con permisos para ejecutar workflows y nodos personalizados.

## Instrucciones de Configuración
1. Configure las credenciales de Google Sheets en n8n.
2. Establezca las URLs y parámetros necesarios en el nodo HTTP Request.
3. Ajuste los límites y filtros en los nodos Limit y RemoveDuplicates según volumen y criterios deseados.
4. Importe el workflow en n8n y vincule el trigger `Execute Workflow Trigger` a los eventos o schedules que desee.

## Detalles de Funcionamiento
- El workflow inicia mediante un trigger personalizado.
- Realiza solicitudes HTTP para obtener datos de leads.
- Procesa la información con nodos Code y Set para formatear y preparar los datos.
- Filtra duplicados y limita el volumen de leads procesados.
- Registra y actualiza la información final en Google Sheets, facilitando la gestión por parte del equipo de ventas.

## Ejemplos de Uso
- Automatizar la extracción diaria de leads desde una API externa y guardarlos organizadamente en Google Sheets.
- Filtrar automáticamente leads repetidos o que no cumplen criterios específicos antes de compartir con agentes de ventas.
- Integrar con otros workflows de n8n para asignar leads automáticamente a agentes o enviar notificaciones.

---

**Categoría:** ventas/lead-generation  
**Etiquetas:** Worker, Agente  
**Nodos utilizados (9):**  
- n8n-nodes-base.googleSheets  
- n8n-nodes-base.limit  
- n8n-nodes-base.code  
- n8n-nodes-base.executeWorkflowTrigger  
- n8n-nodes-base.set  
- n8n-nodes-base.httpRequest  
- n8n-nodes-base.removeDuplicates
```