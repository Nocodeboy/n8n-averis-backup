```markdown
# T - Automatiza informes de Google Analytics

## Descripción
Workflow diseñado para automatizar la generación y envío de informes de Google Analytics, optimizando el análisis de datos de marketing y SEO de forma programada o manual.

## Requisitos
- Cuenta de Google con acceso a Google Analytics.
- Credenciales configuradas en n8n para Google Analytics API.
- Cuenta de Gmail configurada en n8n para el envío de correos.
- API habilitada para Google Analytics.
- Permisos adecuados para lectura de datos en Google Analytics.

## Instrucciones de configuración
1. Configure las credenciales de Google Analytics en n8n:
   - En n8n, añada credenciales usando OAuth2 con permisos para Google Analytics.
2. Configure las credenciales de Gmail en n8n para enviar correos:
   - Añada la cuenta Gmail con los permisos necesarios.
3. Ajuste los parámetros del nodo de Google Analytics para seleccionar las métricas y períodos deseados.
4. Configure el nodo `scheduleTrigger` para establecer la frecuencia de generación de informes.
5. Personalice el código en el nodo `code` si requiere modificar el formato o contenido del informe.

## Detalles de funcionamiento
- El workflow puede iniciarse manualmente (`manualTrigger`) o de forma automática mediante el `scheduleTrigger`.
- Extrae datos de Google Analytics según la configuración establecida.
- Procesa y formatea los datos usando nodos `code` y `set`.
- Añade notas o recordatorios con `stickyNote`.
- Finalmente, envía el informe generado por correo electrónico a través del nodo `gmail`.
- Cuenta con un total de 23 nodos, incluyendo todos los mencionados para cubrir el flujo completo.

## Ejemplos de uso
- Generar informes semanales automáticos con métricas SEO específicas.
- Enviar reportes diarios a un equipo de marketing vía Gmail.
- Ejecutar manualmente la generación de informes para análisis puntual.
```
