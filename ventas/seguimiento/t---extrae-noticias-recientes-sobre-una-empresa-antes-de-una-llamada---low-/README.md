```markdown
# T - Extrae noticias recientes sobre una empresa antes de una llamada - Low

## Descripción
Workflow diseñado para extraer automáticamente noticias recientes sobre una empresa antes de una llamada de seguimiento en ventas, proporcionando información actualizada que facilite la conversación.

## Requisitos
- Credenciales configuradas para:
  - Gmail (envío o recepción de correos)
  - Google Calendar (manejo de eventos y llamadas)
- Acceso a APIs de noticias a través de HTTP Request
- n8n versión compatible con los nodos utilizados

## Instrucciones de configuración
1. Configure las credenciales de Gmail y Google Calendar en n8n.
2. Ajuste el nodo `httpRequest` con la API de noticias de su preferencia, incluyendo la clave API y parámetros de búsqueda, enfocándose en el nombre de la empresa.
3. Modifique el `scheduleTrigger` para definir la frecuencia de ejecución acorde a sus necesidades.
4. Personalice las condiciones en el nodo `if` según criterios específicos de noticias relevantes.
5. Opcionalmente, configure el nodo `set` para adaptar los datos extraídos y el nodo `gmail` para notificaciones o resúmenes por correo.

## Detalles de funcionamiento
- El workflow se activa automáticamente según la programación definida.
- Realiza una consulta HTTP a una API de noticias para obtener las publicaciones recientes sobre la empresa en cuestión.
- Procesa y filtra la información relevante utilizando nodos `code` e `if`.
- Eventualmente, envía un resumen vía Gmail o lo guarda en el calendario antes de la llamada programada.
- Incluye nodos auxiliares como `noOp` y `stickyNote` para control de flujo y documentación interna.

## Ejemplos de uso
- Antes de una llamada de seguimiento con un cliente potencial, obtener un resumen actualizado de las últimas noticias que puedan influir en la conversación.
- Envío automático de un correo con las noticias recientes al equipo de ventas antes de una reunión programada.
- Actualización de eventos en Google Calendar con información relevante extraída automáticamente para preparar llamadas estratégicas.

---
**Categoría:** ventas/seguimiento  
**Nodos utilizados:** noOp, if, code, scheduleTrigger, stickyNote, set, gmail, googleCalendar, httpRequest  
**Número de nodos:** 12  
```