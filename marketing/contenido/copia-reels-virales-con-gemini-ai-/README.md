```markdown
# Copia Reels Virales con Gemini AI

## Descripción
Workflow de n8n orientado a marketing de contenido, diseñado para copiar y gestionar Reels virales utilizando Gemini AI. Automatiza la recopilación, procesamiento y almacenamiento de contenido, facilitando la creación de copias atractivas y optimizadas para redes sociales.

## Requisitos
- Credenciales de n8n con acceso a:
  - Airtable API (para almacenamiento y recuperación de datos).
  - Gemini AI API (para generación de contenido).
- Acceso configurado a los nodos base de n8n.
- Configuración de disparadores programados para ejecuciones automáticas.

## Instrucciones de configuración
1. **Airtable**: Configure las credenciales de Airtable en n8n y establezca las bases y tablas destino.
2. **Gemini AI**: Ingrese la clave API en las credenciales personalizadas dentro de n8n.
3. **Workflow**: Importe el workflow y ajuste los parámetros de los nodos `set` y `scheduleTrigger` según frecuencia y criterios deseados.
4. **Limit y SplitInBatches**: Configure los límites y tamaños de lote para manejar el procesamiento sin sobrecarga.
5. **HTTP Request**: Verifique las URL y parámetros para integración con APIs externas.

## Detalles de funcionamiento
- El workflow inicia mediante un disparador programado (`scheduleTrigger`).
- Consulta Airtable para obtener datos de reels virales.
- Utiliza Gemini AI para generar textos y copias referentes a los reels.
- Procesa y ordena los datos con nodos de límite (`limit`) y ordenamiento (`sort`).
- Divide las tareas en lotes para optimizar la ejecución (`splitInBatches`).
- Incluye pausas controladas (`wait`) para respetar límites de API.
- Almacena y actualiza la información procesada en Airtable.
- Dispone de notas adhesivas (`stickyNote`) para gestión interna y documentación.

## Ejemplos de uso
- Generar automáticamente descripciones de reels virales para campañas de marketing.
- Actualizar bases de datos de contenido para redes sociales con copias generadas por IA.
- Programar publicaciones con texto optimizado y seguimiento desde Airtable.
- Integrar flujos de trabajo de marketing digital con Gemini AI para mejorar el engagement.

---

**Número de nodos:** 29  
**Categoría:** marketing/contenido  
**Tipos de nodos utilizados:** limit, sort, executeWorkflow, scheduleTrigger, stickyNote, set, airtable, executeWorkflowTrigger, splitInBatches, httpRequest, wait
```