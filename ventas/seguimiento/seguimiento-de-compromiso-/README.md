```markdown
# Seguimiento de compromiso

## Descripción
Workflow diseñado para automatizar el seguimiento de compromiso con clientes dentro del proceso de ventas. Utiliza Google Sheets para la gestión de datos, envía notificaciones por Gmail y programa acciones automáticas mediante triggers y esperas.

## Requisitos
- Credenciales de Google Sheets con acceso a la hoja de seguimiento de clientes.
- Cuenta de Gmail configurada con acceso SMTP para enviar correos desde n8n.
- API habilitada para Google Sheets y Gmail en el proyecto asociado.
- n8n instalado y configurado con los nodos necesarios.

## Instrucciones de configuración
1. Configure las credenciales de Google Sheets en n8n.
2. Establezca el acceso SMTP en la credencial de Gmail.
3. Importe el workflow y vincule las credenciales a cada nodo correspondiente.
4. Ajuste la hoja de cálculo y las columnas según su estructura de datos.
5. Defina los intervalos de tiempo en el nodo Wait y el disparador ScheduleTrigger según la frecuencia deseada.

## Detalles de funcionamiento
- El workflow se activa automáticamente en el horario definido por el ScheduleTrigger.
- Recupera datos actualizados desde Google Sheets con el nodo GoogleSheets.
- Utiliza el nodo Wait para programar tiempos específicos entre acciones.
- Envía correos personalizados a contactos mediante Gmail para realizar el seguimiento.
- Contiene 9 nodos distribuidos entre disparadores, operaciones en hojas de cálculo, espera y envío de email.

## Ejemplos de uso
- Enviar recordatorios de seguimiento a clientes que no han respondido en X días.
- Actualizar estados de compromiso en Google Sheets automáticamente.
- Programar envíos periódicos de emails de seguimiento según cronogramas establecidos.
```