```markdown
# Eliminar evento

## Descripción
Workflow diseñado para gestionar y eliminar eventos en Google Calendar automáticamente, integrando hojas de cálculo para control y notificaciones por Gmail, optimizando la productividad y la gestión de agenda.

## Requisitos
- Credenciales de Google (Google Sheets y Google Calendar)
- Cuenta de Gmail configurada en n8n
- Permisos para acceder y modificar hojas de cálculo y eventos del calendario
- n8n con nodos base necesarios instalados

## Instrucciones de configuración
1. Configure las credenciales de Google Sheets y Google Calendar en n8n.
2. Configure la credencial de Gmail para enviar notificaciones.
3. Ajuste los IDs de hojas y calendarios en los nodos correspondientes.
4. Personalice los filtros y scripts en los nodos `filter` y `code` según sus criterios de eliminación.
5. Programe el disparador `scheduleTrigger` según la frecuencia deseada para ejecutar el workflow.

## Detalles de funcionamiento
- El workflow se inicia mediante un trigger programado.
- Recupera datos de Google Sheets para identificar eventos a eliminar.
- Utiliza nodos de filtro y código para validar las condiciones de eliminación.
- Divide y procesa la información con `splitOut`.
- Elimina los eventos correspondientes en Google Calendar.
- Envía notificaciones a través de Gmail confirmando las acciones realizadas.
- Incluye nodos `noOp` para control de flujo y manejo de excepciones.

## Ejemplos de uso
- Eliminación automática de eventos cancelados o inválidos listados en una hoja de cálculo.
- Limpieza programada de agenda eliminando eventos antiguos o duplicados.
- Notificación automática al usuario al completar la eliminación de eventos.

---

**Categoría:** productividad/agenda  
**Número de nodos:** 10  
**Tipos de nodos usados:** `googleSheets`, `noOp`, `filter`, `code`, `gmail`, `scheduleTrigger`, `googleCalendar`, `splitOut`
```