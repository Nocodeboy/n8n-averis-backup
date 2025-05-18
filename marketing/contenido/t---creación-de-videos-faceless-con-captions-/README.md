```markdown
# T - Creación de videos faceless con captions

## Descripción
Workflow automatizado para la creación de videos faceless con captions, optimizado para estrategias de marketing de contenido. Integra fuentes de datos, procesamiento de lenguaje natural y generación de contenido multimedia para facilitar la producción eficiente y escalable.

## Requisitos
- Credenciales de Google Sheets (acceso de lectura y escritura)
- Token de Telegram para el bot (para recibir y enviar mensajes)
- Acceso a APIs de LangChain y Anthropic (modelos de lenguaje)
- Permisos para realizar peticiones HTTP externas
- n8n instalado con nodos LangChain y otros nodos base requeridos

## Instrucciones de configuración
1. Configure las credenciales de Google Sheets en n8n.
2. Establezca el token de Telegram en las credenciales n8n.
3. Ingrese las claves/API tokens necesarios para LangChain y Anthropic.
4. Ajuste los IDs de hojas de Google Sheets y los endpoints HTTP según su proyecto.
5. Active los webhooks y permisos necesarios en n8n para la recepción de eventos.

## Detalles de funcionamiento
- El workflow inicia con un trigger de Telegram (`telegramTrigger`) que recibe comandos o datos.
- Se consulta y modifica información en Google Sheets usando nodos `googleSheets` y `googleSheetsTool`.
- Se emplean nodos de LangChain (`memoryBufferWindow`, `lmChatAnthropic`, `agent`) para la generación de captions y procesamiento inteligente.
- Estructuras condicionales con el nodo `switch` direccionan el flujo según los inputs.
- Se realizan peticiones HTTP para integrar servicios externos o enviar datos generados.
- El workflow utiliza nodos `wait` para controlar tiempos y nodos `stickyNote` para documentación interna visual.
- Finalmente, el contenido generado se envía mediante Telegram u otros medios definidos.

## Ejemplos de uso
- Generar automáticamente captions creativos para videos faceless a partir de prompts recibidos por Telegram.
- Actualizar una hoja de Google Sheets con el estado y resultados de cada video creado.
- Interactuar en tiempo real con usuarios vía Telegram para ajustar parámetros de producción.
- Integrar con servicios externos para publicar directamente el contenido generado.

---

**Nodos utilizados:**  
`googleSheets`, `switch`, `telegramTrigger`, `googleSheetsTool`, `code`, `telegram`, `memoryBufferWindow`, `lmChatAnthropic`, `stickyNote`, `set`, `agent`, `httpRequest`, `wait`, `webhook`  

**Número total de nodos:** 41  
**Categoría:** marketing/contenido  
**Etiquetas:** (ninguna)  
```