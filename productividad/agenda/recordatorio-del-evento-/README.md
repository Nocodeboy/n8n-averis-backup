```markdown
# Recordatorio del evento

## Descripción
Workflow diseñado para gestionar recordatorios de eventos guardados en Google Calendar, enviando notificaciones por Gmail para mejorar la productividad y la organización de la agenda.

## Requisitos
- Credenciales configuradas para:
  - Google Calendar API
  - Gmail API
- Acceso a n8n con permisos para ejecutar workflows
- Nodo `scheduleTrigger` para activar el flujo en intervalos definidos

## Instrucciones de configuración
1. Configure las credenciales de Google Calendar y Gmail en n8n.
2. Ajuste el nodo `scheduleTrigger` con la frecuencia deseada para revisar eventos.
3. En el nodo `filter`, configure las condiciones para filtrar los eventos relevantes.
4. Personalice el código en el nodo `code` si desea modificar el formato del recordatorio.
5. Verifique que el nodo Gmail utilice la cuenta adecuada para enviar los correos.

## Detalles de funcionamiento
- El workflow se activa según la programación del nodo `scheduleTrigger`.
- Obtiene eventos próximos a través del nodo `googleCalendar`.
- Filtra eventos según criterios definidos en el nodo `filter`.
- Utiliza el nodo `code` para preparar el contenido del recordatorio.
- Envía el recordatorio por Gmail a los destinatarios configurados.

## Ejemplos de uso
- Enviar un correo 30 minutos antes de un evento importante.
- Recordar reuniones diarias o llamadas programadas.
- Notificar sobre eventos con etiquetas o categorías específicas en Google Calendar.

---

**Número de nodos:** 5  
**Categoría:** productividad / agenda  
**Tipos de nodos:** filter, code, gmail, scheduleTrigger, googleCalendar  
```