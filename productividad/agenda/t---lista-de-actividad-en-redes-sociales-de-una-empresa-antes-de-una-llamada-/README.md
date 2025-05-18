```markdown
# T - Lista de actividad en redes sociales de una empresa antes de una llamada

## Descripción
Workflow diseñado para recopilar y presentar la actividad en redes sociales de una empresa antes de una llamada, facilitando una preparación eficiente y contextualizada. Automatiza la búsqueda, filtrado y organización de información relevante en distintas plataformas y servicios.

## Requisitos
- Credenciales de Gmail (para enviar y recibir correos electrónicos).
- Credenciales de Google Calendar (para gestionar eventos).
- API Key de Clearbit (para obtener información empresarial).
- Acceso a servicios HTTP para realizar solicitudes a APIs externas.
- Permisos para configurar nodos como `httpRequest`, `gmail` y `googleCalendar` en n8n.

## Instrucciones de configuración
1. Importa el workflow en tu instancia de n8n.
2. Configura las credenciales necesarias:
   - Gmail: Autentica tu cuenta para enviar y recibir correos.
   - Google Calendar: Autoriza acceso a tu calendario.
   - Clearbit: Añade tu API Key en el nodo correspondiente.
3. Ajusta los parámetros de los nodos `scheduleTrigger` para definir la frecuencia de ejecución.
4. Configura filtros y condiciones en nodos `switch` y `filter` según tus criterios comerciales o preferencias.
5. Personaliza los nodos `set` y `code` para adaptar los datos procesados a tus necesidades específicas.
6. Revisa y adapta las solicitudes en `httpRequest` para apuntar a los endpoints de redes sociales o APIs que desees monitorear.

## Detalles de funcionamiento
- El flujo se inicia con un disparador programado (`scheduleTrigger`) que activa el proceso previo a una llamada.
- Se recopilan datos de diversas fuentes, incluyendo correo electrónico, calendarios, APIs web y Clearbit.
- Los nodos `switch` y `filter` gestionan la toma de decisiones y filtrado de información relevante.
- El nodo `code` permite procesamiento personalizado de datos para adaptar la información ante necesidades específicas.
- Finalmente, la información procesada se organiza y presenta mediante nodos `html` y `stickyNote`.
- La integración con Gmail y Google Calendar permite sincronizar la información de manera efectiva antes de la llamada.

## Ejemplos de uso
- Preparación automática para una reunión comercial con información actualizada de la empresa cliente.
- Seguimiento de menciones y actividades relevantes en redes sociales antes de una llamada de soporte.
- Envío de resúmenes personalizados vía correo electrónico con datos clave extraídos de diversas fuentes.

---

**Número de nodos:** 19  
**Categoría:** productividad/agenda  
**Nodos utilizados:** switch, merge, html, filter, code, scheduleTrigger, gmail, set, stickyNote, clearbit, splitOut, googleCalendar, httpRequest  
```