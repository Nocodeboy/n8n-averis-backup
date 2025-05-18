```markdown
# SEO - Trends Post

## Descripción
Workflow automatizado para identificar tendencias SEO y generar publicaciones optimizadas, integrando análisis de datos, generación de contenido con IA y publicación directa en WordPress.

## Requisitos
- Credenciales de Google Sheets (acceso a las hojas usadas para datos)
- Clave API de OpenAI (para generación de contenido con LangChain)
- Credenciales de WordPress (para publicar posts vía API)
- Acceso a Internet para llamadas HTTP externas

## Instrucciones de Configuración
1. Importar el workflow en n8n.
2. Configurar nodos de credenciales:
   - Google Sheets: añadir credenciales con acceso a documentos necesarios.
   - OpenAI: configurar la clave API en el nodo LangChain.
   - WordPress: configurar usuario y clave para la API REST.
3. Ajustar parámetros del nodo `scheduleTrigger` para definir la frecuencia de ejecución.
4. Revisar las URLs y endpoints en nodos `httpRequest` según las fuentes de tendencias.
5. Guardar y activar el workflow.

## Detalles de Funcionamiento
- El workflow se activa según la programación definida.
- Utiliza el nodo `aggregate` para procesar datos de tendencias recopilados.
- Consulta APIs externas para obtener información actualizada.
- Emplea LangChain con OpenAI para generar textos optimizados SEO.
- Almacena datos y resultados en Google Sheets para seguimiento.
- Publica automáticamente en WordPress usando las credenciales configuradas.
- Incluye nodos `code` y `set` para manipulación personalizada de datos.
- Utiliza `stickyNote` para documentación interna y claridad del flujo.

## Ejemplos de Uso
- Publicar automáticamente artículos basados en las últimas tendencias de búsqueda.
- Generar contenido SEO optimizado sin intervención manual.
- Mantener actualizados blogs o sitios web marketing con contenido relevante y oportuno.
```