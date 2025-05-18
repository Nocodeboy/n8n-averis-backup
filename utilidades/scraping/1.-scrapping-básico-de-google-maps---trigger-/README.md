```markdown
# 1. Scrapping básico de Google Maps - Trigger

## Descripción
Workflow para realizar un scrapping básico de Google Maps activado manualmente. Ideal para obtener datos iniciales de ubicaciones utilizando un disparador personalizado.

## Requisitos
- n8n instalado y configurado.
- Credenciales válidas para acceder a Google Maps si se requiere (API Key opcional según el método de scrapping).
- Permisos para ejecutar workflows en n8n.

## Instrucciones de configuración
1. Importa el workflow en tu instancia de n8n.
2. Configura el nodo `Manual Trigger` para iniciar el proceso cuando lo desees.
3. Ajusta el nodo `Execute Workflow` si utilizas workflows secundarios para procesamiento de datos.
4. Configura los parámetros en nodos `Split In Batches` y `Wait` según la cantidad de datos y tiempos de espera deseados.
5. Añade cualquier nota o documentación en el nodo `Sticky Note` para referencia interna.

## Detalles de funcionamiento
- El workflow se activa manualmente mediante un disparador.
- Datos se manejan en lotes a través del nodo `Split In Batches` para optimizar procesos.
- Se incluyen pausas controladas con el nodo `Wait` para evitar bloqueos o límites de API.
- El nodo `Execute Workflow` permite delegar tareas a workflows adicionales si es necesario.
- Utiliza un nodo `Sticky Note` para mantener información importante visible dentro del diseño del workflow.

## Ejemplos de uso
- Recopilar información periódica sobre ubicaciones de interés en Google Maps.
- Iniciar un scrapping controlado manualmente para evitar sobrecargas.
- Probar integraciones con otros workflows para procesamiento o almacenamiento posterior de datos.

---

**Categoría:** utilidades/scraping  
**Nodos utilizados:** Manual Trigger, Execute Workflow, Sticky Note, Split In Batches, Wait  
**Número de nodos:** 5  
**Etiquetas:** _(ninguna)_
```