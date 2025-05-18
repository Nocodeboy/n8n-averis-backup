```markdown
# 2. Scrapping básico de Google Maps - Automatización

## Descripción
Workflow automatizado para realizar scrapping básico de Google Maps, procesar y almacenar datos relevantes utilizando diversas operaciones de filtrado, agregación y manipulación de datos dentro de n8n.

## Requisitos
- Credenciales de Google Sheets con acceso a la hoja donde se guardarán o leerán los datos.
- API key válida para acceder a la API de Google Maps o endpoints HTTP utilizados en el workflow.
- n8n instalado y configurado con los nodos necesarios.

## Instrucciones de configuración
1. Configure las credenciales de Google Sheets en n8n.
2. Inserte su API key o token necesario en el nodo HTTP Request para acceder a Google Maps.
3. Ajuste los parámetros de búsqueda o filtros dentro de los nodos de código o HTTP Request según sus necesidades.
4. Verifique las conexiones entre nodos para asegurar el flujo correcto de datos.

## Detalles de funcionamiento
El workflow consta de 13 nodos que realizan las siguientes tareas:
- Disparador (`executeWorkflowTrigger`) para iniciar el proceso automáticamente.
- Solicitudes HTTP a la API de Google Maps para obtener información de lugares.
- División de datos en lotes para procesamiento eficiente con `splitInBatches`.
- Filtrado de resultados duplicados y aplicación de condiciones mediante los nodos de filtro y `removeDuplicates`.
- Procesamiento y transformación de datos usando nodos de código y agregaciones.
- Almacenamiento y actualización de resultados en Google Sheets para consulta y análisis posteriores.

## Ejemplos de uso
- Obtener listados básicos de negocios o lugares de interés para análisis de mercado.
- Recolectar datos de ubicaciones para alimentar bases de datos internas.
- Automatizar la extracción de información de mapas para generar reportes periódicos sin intervención manual.
```