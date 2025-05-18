```markdown
# Búsqueda de Prospectos en Linkedin

## Descripción
Workflow diseñado para automatizar la búsqueda y generación de prospectos en LinkedIn utilizando fuentes RSS, procesamiento con modelos OpenAI, y gestión vía Gmail. Ideal para equipos de ventas y generación de leads que buscan optimizar su flujo de trabajo.

## Requisitos
- Cuenta de n8n con acceso a los siguientes nodos y paquetes:
  - `n8n-nodes-base.gmail`
  - `@n8n/n8n-nodes-langchain` (incluyendo `outputParserStructured`, `lmChatOpenAi`, `chainLlm`)
  - `n8n-nodes-base.httpRequest`
  - `n8n-nodes-base.rssFeedRead`
  - Otros nodos integrados por defecto en n8n (wait, limit, filter, etc.)
- Credenciales configuradas para:
  - Gmail API (enviar y recibir correos)
  - OpenAI API (para procesamiento del lenguaje natural)
  - Acceso a fuentes RSS relacionadas con LinkedIn / lead generation
- Permisos para ejecutar workflows y acceso a internet desde el entorno n8n

## Instrucciones de configuración
1. **Configurar Credenciales**
   - Añade las credenciales para Gmail en n8n.
   - Configura la API key de OpenAI en el nodo `lmChatOpenAi`.
2. **Actualizar Fuentes RSS**
   - En el nodo `rssFeedRead`, introduce las URLs de los feeds relevantes para la búsqueda de prospectos.
3. **Personalizar Parámetros**
   - Ajusta filtros, límites y condiciones según tu necesidad de búsqueda o segmentación.
4. **Activar el Workflow**
   - Ejecuta el nodo `manualTrigger` para iniciar la búsqueda o activa el workflow en modo automático según frecuencia deseada.

## Detalles de funcionamiento
- El workflow inicia leyendo múltiples fuentes RSS relacionadas con posibles prospectos.
- Usa nodos `filter`, `if` y `splitInBatches` para depurar y segmentar datos.
- Emplea nodos `lmChatOpenAi` y `chainLlm` para enriquecer y analizar textos de los prospectos.
- Realiza llamadas HTTP para obtener información adicional mediante el nodo `httpRequest`.
- Arma mensajes estructurados y los envía a través de Gmail automatizado.
- Maneja tiempos de espera (`wait`) y límites para respetar cuotas y optimizar el rendimiento.
- Integra notas (`stickyNote`) y código personalizado para extender funcionalidades específicas.
- Finalmente, combina y agrega datos para generar reportes o acciones posteriores.

## Ejemplos de uso
- Generar una lista semanal de prospectos potenciales extraídos de noticias o publicaciones en LinkedIn.
- Enviar correos personalizados a leads calificados automáticamente tras procesar y analizar su información.
- Monitorizar nuevos posts en RSS feeds y enriquecerlos con inteligencia artificial para determinar su relevancia.
- Integrar con sistemas CRM mediante nodos HTTP para sincronizar prospectos generados.

---

**Número de nodos:** 56  
**Categoría:** ventas/lead-generation  
**Etiquetas:** LeadGen, RSS Feed
```