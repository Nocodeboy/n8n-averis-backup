# Backup

Esta carpeta contiene workflows de n8n para realizar copias de seguridad automáticas.

## Workflow principal

El workflow principal `backup-diario-n8n-Backup.json` automatiza el respaldo de todos los workflows de n8n hacia este repositorio de GitHub.

## Características principales

- **Respaldo automático**: Se ejecuta diariamente sin intervención manual
- **Exportación completa**: Respalda todos los workflows activos en n8n
- **Control de versiones**: Utiliza Git para mantener historial de cambios
- **Notificaciones**: Puede configurarse para enviar alertas de éxito/error
- **Personalizable**: Ajustable para diferentes frecuencias y destinos

## Funcionamiento

El workflow:

1. Se activa mediante un trigger programado (por defecto, diariamente)
2. Accede a la API interna de n8n para exportar todos los workflows
3. Formatea los archivos JSON para mejor legibilidad
4. Realiza una organización básica por categorías (opcional)
5. Sube los cambios al repositorio de GitHub
6. Registra el resultado de la operación

## Configuración necesaria

Para utilizar este workflow, necesitas:

1. **Token de GitHub**: Crear un token de acceso personal con permisos de repo
2. **Credenciales de n8n**: Configurar acceso a la API interna
3. **Webhooks** (opcional): Para notificaciones a Slack, Teams, etc.

### Parámetros ajustables

- `REPO_OWNER`: Propietario del repositorio de GitHub
- `REPO_NAME`: Nombre del repositorio
- `BACKUP_BRANCH`: Rama donde se guardarán los backups
- `BACKUP_FREQUENCY`: Frecuencia de ejecución (cron)
- `NOTIFICATION_ENABLED`: Activar/desactivar notificaciones

## Recomendaciones de uso

- Mantén un repositorio privado para los backups
- Revisa periódicamente que los backups se estén ejecutando correctamente
- Considera aumentar la frecuencia para entornos críticos (cada 6-12 horas)
- Añade pruebas de integridad para verificar los backups

## Restauración

Para restaurar workflows desde el backup:

1. Clona el repositorio o descarga los archivos JSON específicos
2. Importa manualmente en la interfaz de n8n o usa la API
3. Verifica las credenciales y configuraciones específicas del entorno

## Workflows relacionados

- **Verificador de backups**: Comprueba la integridad de los backups realizados
- **Limpieza de backups antiguos**: Gestiona versiones históricas (opcional)
