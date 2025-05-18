```markdown
# Averis - Generación automática de informe muy breve de asistentes a reuniones

## Descripción

Workflow que automatiza la generación de informes breves sobre los asistentes a reuniones, integrando datos de Google Calendar y Gmail para facilitar el seguimiento y la productividad en entornos laborales.

## Requisitos

- Credenciales de Google Calendar (OAuth2)
- Credenciales de Gmail (OAuth2)
- Permisos para acceder a las APIs de Google Calendar y Gmail
- Acceso a n8n para importar y ejecutar el workflow

## Instrucciones de configuración

1. Configure las credenciales de Google Calendar y Gmail en n8n.
2. Importe el workflow en su instancia de n8n.
3. Asegúrese de que el disparador `Google Calendar Trigger` esté activo.
4. Ajuste los filtros y parámetros del nodo `Set` si es necesario para adaptarlo a su contexto.
5. Verifique los permisos de acceso para las cuentas vinculadas.

## Detalles de funcionamiento

El workflow utiliza 18 nodos que incluyen agregación de datos, filtrado condicional y consultas a APIs para:

- Detectar eventos de reuniones en Google Calendar.
- Extraer la lista de asistentes y mensajes relacionados en Gmail.
- Generar un resumen muy breve en formato Markdown.
- Enviar el informe vía Gmail o almacenarlo en notas adhesivas (Sticky Notes) dentro del workflow.

Los nodos principales incluidos son:  
`aggregate`, `if`, `filter`, `gmail`, `stickyNote`, `set`, `googleCalendarTrigger`, `splitInBatches`, `splitOut`, `httpRequest` y `markdown`.

## Ejemplos de uso

- Enviar automáticamente un resumen diario de asistentes a reuniones programadas para el equipo.
- Generar informes rápidos después de cada reunión para registrar asistencia y puntos clave.
- Integrar el reporte con otras herramientas mediante HTTP Request para flujos personalizados.

---
Categoría: productividad/reuniones  
Número de nodos: 18
```