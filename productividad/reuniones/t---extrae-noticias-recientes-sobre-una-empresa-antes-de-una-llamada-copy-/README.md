```markdown
# T - Extrae noticias recientes sobre una empresa antes de una llamada copy

## Descripción

Workflow diseñado para extraer noticias recientes sobre una empresa antes de una llamada, ayudando a preparar reuniones con información actualizada y relevante.

## Requisitos

- Credenciales de Gmail para enviar correos electrónicos.
- Credenciales de Google Calendar para acceder y gestionar eventos.
- Acceso a una API pública de noticias (configurada en el nodo HTTP Request).
- n8n instalado y configurado con los nodos base mencionados.

## Instrucciones de configuración

1. Configure sus credenciales de Gmail en n8n para el nodo `gmail`.
2. Configure sus credenciales de Google Calendar para el nodo correspondiente.
3. En el nodo `HTTP Request`, establezca la URL y parámetros de la API de noticias que utilizará, incluyendo la clave API si es necesaria.
4. Ajuste el nodo `Schedule Trigger` para definir la frecuencia de ejecución previas a las llamadas.
5. Personalice los nodos de código y condiciones (`if`, `code`) según las reglas de filtrado y procesamiento de noticias que necesite.

## Detalles de funcionamiento

- El workflow se activa automáticamente según el `Schedule Trigger`.
- Extrae los próximos eventos de Google Calendar para identificar llamadas programadas.
- Consulta una API de noticias para obtener artículos recientes relacionados con la empresa objetivo.
- Filtra y procesa las noticias mediante nodos `if` y `code` para destacar la información más relevante.
- Envía un correo electrónico con las noticias recopiladas a través de Gmail.
- Utiliza nodos `stickyNote` para notas internas o mensajes en la interfaz de n8n.
- Utiliza nodos `set` para preparar y gestionar datos a lo largo del flujo.
- El nodo `noOp` se utiliza para segmentar el flujo y organizar la lógica.

El workflow cuenta con un total de 12 nodos.

## Ejemplos de uso

- Ejecutar diariamente para preparar información antes de llamadas con clientes o socios.
- Obtener un resumen rápido de noticias relevantes justo antes de una reunión importante.
- Automatizar el envío de actualizaciones de noticias a los participantes de una llamada.

---
Categoría: productividad/reuniones  
Etiquetas: (sin etiquetas definidas)  
Nodos utilizados: n8n-nodes-base.noOp, n8n-nodes-base.if, n8n-nodes-base.code, n8n-nodes-base.scheduleTrigger, n8n-nodes-base.stickyNote, n8n-nodes-base.set, n8n-nodes-base.gmail, n8n-nodes-base.googleCalendar, n8n-nodes-base.httpRequest
```