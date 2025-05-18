```markdown
# Seguimiento de Posicionamiento SEO con Google Sheets (Keyword Rank Tracker)

## Descripción
Workflow diseñado para monitorear y registrar la posición de palabras clave en motores de búsqueda, utilizando Google Sheets como base de datos para el seguimiento histórico. Ideal para especialistas en SEO que desean automatizar la recopilación y análisis de rankings de keywords.

## Requisitos
- Credenciales válidas de Google Sheets para lectura y escritura.
- Credenciales de Google BigQuery (opcional, para almacenamiento avanzado y análisis).
- Acceso a las APIs necesarias para obtener datos de posicionamiento SEO (configurable según la fuente de datos externa).
- Cuenta en n8n con permisos para utilizar los nodos especificados.

## Instrucciones de Configuración
1. Importar el workflow en tu instancia de n8n.
2. Configurar las credenciales de Google Sheets dentro de n8n.
3. (Opcional) Configurar credenciales de Google BigQuery si se desea habilitar almacenamiento en BigQuery.
4. Ajustar los parámetros de búsqueda de palabras clave y los índices de motores de búsqueda según tus necesidades.
5. Verificar y actualizar los nodos `Code` para adaptar la lógica de extracción y procesamiento de datos externos si es necesario.

## Detalles de Funcionamiento
- El workflow se activa manualmente o con triggers programados.
- Se consultan las posiciones de las keywords mediante APIs personalizadas o importación de datos.
- Los datos se procesan y organizan utilizando nodos de filtrado, ordenamiento y combinación (`limit`, `merge`, `if`, `sort`).
- Se actualizan las hojas de Google Sheets con los resultados para facilitar la visualización y análisis histórico.
- Opcionalmente, los datos pueden cargarse en Google BigQuery para análisis avanzados.
- Cuenta con nodos de control de ejecución para manejar lotes y flujos condicionales (splitInBatches, splitOut, set).
- Incluye notas y configuraciones internas para facilitar la personalización y mantenimiento (stickyNote).

## Ejemplos de Uso
- Rastreo semanal de posicionamiento SEO para un conjunto de palabras clave.
- Comparación histórica de rankings en Google Sheets para detectar mejoras o caídas.
- Integración con dashboards basados en BigQuery para análisis de tendencias SEO.
- Automatización de reportes personalizados enviados a stakeholders utilizando datos actualizados.

---

**Categoría:** marketing/seo  
**Tags:** SEO, templates  
**Número de nodos:** 31  
**Nodos utilizados:**  
`googleSheets`, `limit`, `merge`, `if`, `manualTrigger`, `sort`, `code`, `stickyNote`, `set`, `googleBigQuery`, `splitOut`, `splitInBatches`
```