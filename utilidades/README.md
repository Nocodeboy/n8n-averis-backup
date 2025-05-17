# Utilidades

Esta carpeta contiene herramientas y utilidades generales para n8n que pueden utilizarse en diversos contextos.

## Subcategorías

- **backup/**: Scripts de respaldo para workflows y configuraciones
- **scraping/**: Herramientas para extracción de datos web
- **integraciones/**: Conectores con servicios externos
- **helpers/**: Funciones auxiliares reutilizables

## Workflows destacados

- **Backup diario n8n**: Automatización de respaldos a GitHub
- **Scraping básico de Google Maps**: Extracción de datos de negocios
- **Conectores RAG**: Integraciones con bases de datos vectoriales

## Backup y mantenimiento

El workflow de backup es especialmente importante:

```
backup-diario-n8n-Backup.json
```

Este workflow:
1. Exporta todos los workflows de n8n
2. Los sube al repositorio de GitHub
3. Mantiene un historial de versiones
4. Se ejecuta automáticamente cada día

### Configuración del backup

Para configurar correctamente el backup:

1. Genera un token de acceso personal en GitHub con permisos de repositorio
2. Configura las credenciales de GitHub en n8n
3. Ajusta la programación según tus necesidades (diaria, semanal, etc.)
4. Opcional: Configura notificaciones por correo o Slack

## Herramientas de scraping

Las utilidades de scraping te permiten extraer datos de:

- Google Maps
- LinkedIn
- Sitios web generales
- Resultados de búsqueda

Recuerda utilizar estas herramientas de manera responsable y respetando los términos de servicio de cada plataforma.

## Integraciones

Incluye conectores predefinidos para:

- Supabase
- Firebase
- Google Drive
- Airtable
- APIs personalizadas

## Cómo contribuir nuevas utilidades

Si desarrollas una nueva utilidad:

1. Crea una subcarpeta apropiada
2. Incluye un README detallado
3. Documenta requisitos y dependencias
4. Proporciona ejemplos de uso
