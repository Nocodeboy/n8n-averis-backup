```markdown
# Seguimiento de Posiciones SEO con PostgreSQL (Keyword Rank Tracker)

## Descripción
Este workflow de n8n permite realizar un seguimiento automatizado de las posiciones SEO de palabras clave, almacenando y gestionando los datos en una base de datos PostgreSQL. Ideal para monitorear rankings y analizar el rendimiento SEO a lo largo del tiempo.

## Requisitos
- **n8n** instalado y funcionando.
- Credenciales configuradas para:
  - PostgreSQL (acceso a base de datos para lectura y escritura).
  - Google BigQuery (opcional, para análisis y reportes avanzados).
- Acceso a APIs de consultas SEO externas (según configuración personalizada).
  
## Instrucciones de configuración
1. Importa el workflow en tu instancia de n8n.
2. Configura las credenciales para PostgreSQL y Google BigQuery en n8n.
3. Ajusta las consultas y credenciales de APIs SEO en los nodos de tipo `code` o `set`.
4. Personaliza los parámetros de seguimiento (palabras clave, dominios, etc.) según tus necesidades.
5. Guarda y activa el workflow para que corra automáticamente o ejecútalo manualmente para pruebas.

## Detalles de funcionamiento
- El workflow consta de **29 nodos** que manejan la obtención, filtrado, almacenamiento y análisis de datos SEO.
- Nodos clave utilizados:
  - `manualTrigger` para inicio manual.
  - `code` para procesamiento personalizado de datos.
  - `postgres` para interacción con la base de datos.
  - `googleBigQuery` para exportar y analizar datos.
  - `merge`, `if`, `splitInBatches`, `splitOut` para control de flujo y manejo de datos.
- Permite actualizar posiciones SEO, validar cambios y almacenar resultados históricos.
- Incluye notas adhesivas (`stickyNote`) para organizar y documentar el workflow internamente.

## Ejemplos de uso
- Ejecutar manualmente el seguimiento periódico de keywords.
- Integrar con alertas personalizadas si una posición SEO baja más allá de un umbral.
- Exportar resultados históricos a Google BigQuery para reportes avanzados.
- Modificar parámetros para añadir nuevas palabras clave o dominios a monitorear.

---
**Etiquetas:** SEO, Templates  
**Categoría:** marketing/seo
```
