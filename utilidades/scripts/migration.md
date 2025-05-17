# Script de Migración

Este script está diseñado para gestionar la migración de workflows en este repositorio hacia la nueva estructura de carpetas organizada.

## Funcionalidad

El script reorganiza los workflows siguiendo estas reglas:

1. Analiza el nombre y contenido de cada workflow
2. Identifica la categoría apropiada basada en etiquetas y patrones de nombrado
3. Crea la estructura de carpetas necesaria
4. Mueve el archivo a su carpeta correspondiente
5. Genera documentación básica para cada workflow

## Categorías principales

Los workflows se reorganizan en estas categorías:

- **agentes-ia/**: Agentes de IA para diferentes plataformas
- **marketing/**: Herramientas de marketing digital
- **ventas/**: Workflows de ventas y CRM
- **productividad/**: Herramientas de productividad interna
- **utilidades/**: Herramientas generales y utilidades

## Uso

Para ejecutar el script de migración:

```bash
# Utilizando el script integrado en n8n
cd utilidades/scripts
n8n execute workflow.json
```

## Proceso de migración

El proceso de migración seguirá estos pasos:

1. **Respaldo inicial**: Se crea un respaldo de la estructura actual
2. **Análisis de workflows**: Se analizan todos los workflows para identificar categorías
3. **Creación de estructura**: Se generan las carpetas necesarias
4. **Documentación**: Se crean READMEs para cada workflow o categoría
5. **Traslado**: Se mueven los archivos a sus nuevas ubicaciones

## Estado de la migración

- [ ] **Análisis preliminar**: Identificación de todas las categorías
- [ ] **Estructura inicial**: Creación de carpetas principales
- [x] **Backups**: Migración de herramientas de backup
- [ ] **Agentes IA**: Migración de agentes inteligentes
- [ ] **Marketing**: Migración de herramientas de marketing
- [ ] **Ventas**: Migración de workflows de ventas
- [ ] **Productividad**: Migración de herramientas de productividad
- [ ] **Utilidades**: Migración de utilidades generales

## Notas

- La migración se está realizando gradualmente para minimizar interrupciones
- Los archivos se moverán manteniendo su historial de cambios
- Cada workflow tendrá su propia documentación detallada
