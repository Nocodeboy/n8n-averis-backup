```markdown
# T - Revisa las tendencias en canal de Youtube

## Descripción
Workflow de n8n diseñado para revisar y analizar las tendencias de un canal de YouTube, utilizando scraping y procesamiento con inteligencia artificial para extraer y organizar la información relevante.

## Requisitos
- Credenciales de API de OpenAI para el nodo `@n8n/n8n-nodes-langchain.openAi`.
- Acceso a Google Sheets con credenciales configuradas para `n8n-nodes-base.googleSheets`.
- URL del canal de YouTube objetivo.
- n8n instalado y configurado con los nodos necesarios.

## Instrucciones de configuración
1. Configure las credenciales de OpenAI en n8n.
2. Configure las credenciales de Google Sheets y otorgue permisos sobre la hoja donde se almacenarán los datos.
3. Introduzca la URL del canal de YouTube en el nodo HTTP Request para obtener el feed XML.
4. Ajuste las hojas y rangos en el nodo Google Sheets según su estructura.
5. Verifique que el nodo Manual Trigger esté listo para iniciar el flujo a demanda.

## Detalles de funcionamiento
- El flujo comienza con un disparador manual (`Manual Trigger`).
- Se realiza una petición HTTP (`HTTP Request`) para obtener el feed XML de tendencias del canal.
- El nodo XML procesa y extrae los datos relevantes del feed.
- El nodo de OpenAI (`@n8n/n8n-nodes-langchain.openAi`) analiza la información para generar insights o resúmenes basados en IA.
- Finalmente, los datos procesados se almacenan y organizan en una hoja de Google Sheets.

## Ejemplos de uso
- Monitorear diariamente los videos más populares de un canal de YouTube.
- Generar resúmenes automáticos de las tendencias actuales para informar a un equipo de marketing.
- Almacenar y comparar la evolución de tendencias en Google Sheets para análisis posterior.

---

**Número de nodos:** 5  
**Categoría:** utilidades/scraping  
**Tipos de nodos utilizados:**  
- `@n8n/n8n-nodes-langchain.openAi`  
- `n8n-nodes-base.googleSheets`  
- `n8n-nodes-base.manualTrigger`  
- `n8n-nodes-base.xml`  
- `n8n-nodes-base.httpRequest`  
```