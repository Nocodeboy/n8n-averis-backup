```markdown
# Copia Reels Virales con Gemini

## Descripción
Workflow de n8n diseñado para automatizar la copia y gestión de reels virales, integrando Gemini para análisis y recopilación de datos. Ideal para equipos de marketing y creación de contenido interesados en investigación y optimización de reels.

## Categoría
marketing/contenido

## Etiquetas
Contenido, Reels, Investigación

## Requisitos
- Credenciales de **Airtable** para almacenar y gestionar los datos de los reels.
- Acceso a la API de **Gemini** (u otro servicio relevante para análisis de contenido).
- Configuración de n8n con los nodos base utilizados en el workflow.
- Permisos para ejecutar workflows desde nodos de tipo `executeWorkflow` y `executeWorkflowTrigger`.

## Nodos Utilizados
- limit  
- sort  
- executeWorkflow  
- scheduleTrigger  
- stickyNote  
- set  
- airtable  
- executeWorkflowTrigger  
- splitInBatches  
- httpRequest  
- wait

Total: 27 nodos

## Instrucciones de Configuración
1. **Importar el workflow** en tu instancia de n8n.
2. **Configurar credenciales**:
   - Añade tus credenciales de Airtable en n8n.
   - Configura el nodo de httpRequest con la API Key y endpoint de Gemini.
3. **Editar parámetros de nodos**:
   - Ajusta los límites, filtros y ordenamientos según tus necesidades específicas.
   - Establece horarios en `scheduleTrigger` para la frecuencia de ejecución.
4. **Guardar y activar el workflow** para que corra automáticamente.

## Detalles de Funcionamiento
- El workflow se activa según una programación establecida en `scheduleTrigger`.
- Utiliza `httpRequest` para obtener datos de Gemini y analizar tendencias de reels virales.
- Los datos se procesan con nodos `limit`, `sort` y `splitInBatches` para administrar volumen y prioridad.
- Resultados relevantes se almacenan en Airtable mediante el nodo `airtable`.
- Se usan nodos `set` y `stickyNote` para manejo interno de variables y anotaciones.
- `executeWorkflow` y `executeWorkflowTrigger` permiten modularizar y reusar procesos internos.
- El nodo `wait` ayuda a manejar pausas entre lotes o solicitudes para evitar saturación de APIs.

## Ejemplos de Uso
- Monitorear diariamente reels virales para inspiración y creación de contenido optimizado.
- Crear bases de datos actualizadas con reels segmentados por categoría o relevancia.
- Ejecutar análisis automáticos para detectar patrones en contenido viral usando Gemini.

---

Workflow preparado para optimizar tu estrategia de marketing de contenido con reels virales utilizando la potencia de n8n y Gemini.
```