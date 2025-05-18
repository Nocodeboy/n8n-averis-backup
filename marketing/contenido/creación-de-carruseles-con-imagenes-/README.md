```markdown
# Creación de Carruseles con imágenes

## Descripción
Workflow automatizado para la creación de carruseles de contenido visual utilizando imágenes. Ideal para marketing y generación de contenido dinámico en redes sociales y campañas digitales.

## Requisitos
- Credenciales de OpenAI para el nodo `lmChatOpenAi`
- Acceso a APIs externas consumidas mediante `httpRequest` (configurar según fuentes de imágenes o servicios)
- n8n versión compatible con los siguientes nodos:
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`
  - `n8n-nodes-base.scheduleTrigger`
  - `n8n-nodes-base.stickyNote`
  - `n8n-nodes-base.set`
  - `@n8n/n8n-nodes-langchain.agent`
  - `@n8n/n8n-nodes-langchain.outputParserStructured`
  - `n8n-nodes-base.httpRequest`
  - `n8n-nodes-base.wait`

## Instrucciones de configuración
1. Importa el workflow en tu instancia de n8n.
2. Configura las credenciales de OpenAI en n8n para el nodo `lmChatOpenAi`.
3. Ajusta las URLs y parámetros en el nodo `httpRequest` para las fuentes de imágenes o APIs externas que desees utilizar.
4. Modifica el horario del nodo `scheduleTrigger` según la frecuencia deseada para la creación automática.
5. Revisa y personaliza cualquier texto o dato por defecto en nodos `set` o `stickyNote`.
6. Guarda y activa el workflow para iniciar la ejecución programada.

## Detalles de funcionamiento
- El nodo `scheduleTrigger` inicia el flujo en el horario definido.
- Se utilizan nodos de Langchain (`lmChatOpenAi`, `agent`, `outputParserStructured`) para generar contenido textual y estructurar la información.
- El nodo `httpRequest` obtiene imágenes o datos externos necesarios para el carrusel.
- Nodos `set` y `stickyNote` almacenan y organizan datos intermedios.
- El nodo `wait` controla pausas para manejo de tiempos o espera de respuestas.
- En total, el workflow cuenta con 20 nodos configurados para asegurar un flujo robusto y eficiente.

## Ejemplos de uso
- Generar automáticamente carruseles para Instagram o LinkedIn con imágenes y textos descriptivos diarios o semanales.
- Campañas de marketing que requieren actualización frecuente de contenido visual con copy optimizado.
- Creación rápida de material visual para blogs o newsletters aprovechando IA para textos y APIs para imágenes.

---

**Categoría:** marketing/contenido  
**Número de nodos:** 20  
**Etiquetas:** *(ninguna definida)*  
```