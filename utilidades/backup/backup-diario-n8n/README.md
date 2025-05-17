# Backup Diario n8n

Este workflow automatiza el proceso de respaldo diario de todos los workflows de n8n a Google Drive.

## Funcionalidad

El workflow:
- Se ejecuta automáticamente una vez al día
- Exporta todos los workflows activos en n8n
- Los guarda en una carpeta específica en Google Drive
- Mueve los backups anteriores a una carpeta de archivos antiguos
- Elimina backups más viejos que 30 días para mantener el almacenamiento limpio

## Estructura

El workflow está estructurado en varias secciones:
1. **Verificación de carpetas**: Comprueba si existen las carpetas necesarias
2. **Creación de carpetas**: Crea las carpetas si no existen
3. **Exportación de workflows**: Obtiene los workflows actuales de n8n
4. **Almacenamiento**: Guarda los workflows como archivos JSON
5. **Gestión de archivos antiguos**: Organiza y limpia backups antiguos

## Requisitos

Para que este workflow funcione correctamente necesitas:

- Credenciales configuradas para Google Drive
- Credenciales de API para n8n
- Las carpetas `n8n_backups` y `n8n_old` en Google Drive

## Notas de implementación

- El workflow está configurado para ejecutarse diariamente, pero puedes ajustar la frecuencia según tus necesidades
- Los archivos antiguos se eliminan automáticamente después de 30 días
- Se añade una marca de tiempo a cada backup para facilitar la identificación

## Configuración

Si necesitas modificar el workflow:

1. Ajusta la programación del trigger según tus necesidades
2. Modifica las rutas de las carpetas en Google Drive si es necesario
3. Cambia el período de retención de backups (actualmente 30 días)

## Solución de problemas

Si el workflow falla:
- Verifica que las credenciales de Google Drive sean válidas
- Asegúrate de que las carpetas necesarias existan o se puedan crear
- Comprueba los permisos de acceso a la API de n8n
