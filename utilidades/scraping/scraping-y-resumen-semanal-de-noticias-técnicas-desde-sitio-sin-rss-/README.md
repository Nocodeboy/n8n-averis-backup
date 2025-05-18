```markdown
# Scraping y Resumen Semanal de Noticias Técnicas desde Sitio sin RSS

## Descripción
Workflow diseñado para extraer semanalmente noticias técnicas desde un sitio web sin feed RSS, realizar un resumen automatizado y almacenar los datos en una base NoCoDB para facilitar su consulta y análisis.

## Requisitos
- n8n instalado y funcionando.
- Credenciales de acceso a NoCoDB (API key y URL del proyecto).
- API Key de OpenAI para generación de resúmenes automáticos.
- Acceso HTTP permitido para el sitio web de noticias objetivo.
- Configuración adecuada del nodo `Schedule Trigger` para ejecución semanal.

## Instrucciones de configuración
1. Configure el nodo **Schedule Trigger** para definir el horario de ejecución (por ejemplo, una vez por semana).
2. Ingrese la URL del sitio web objetivo en el nodo **HTTP Request**.
3. Ajuste los selectores CSS o XPATH en el nodo **HTML** para extraer los títulos, enlaces y contenido de las noticias.
4. Configure el nodo **OpenAI** con su API Key para generar resúmenes de los textos extraídos.
5. Configure el nodo **NoCoDB** con las credenciales y la tabla destino para almacenar las noticias y sus resúmenes.
6. Personalice cualquier lógica adicional en los nodos **Code**, **Set** y **Merge** según necesidades específicas.

## Detalles de funcionamiento
- El workflow se activa semanalmente mediante el nodo `Schedule Trigger`.
- Realiza peticiones HTTP para obtener el HTML del sitio objetivo.
- Procesa el HTML para extraer la información relevante (noticias técnicas).
- Genera resúmenes brevísimos con la ayuda de OpenAI.
- Une y organiza los datos con nodos `Merge` y listas de ítems.
- Almacena las noticias y resúmenes en NoCoDB para consultas futuras.
- Incluye notas adhesivas para facilitar la documentación interna del flujo.

## Ejemplos de uso
- Automatizar la recopilación y resumen semanal de noticias técnicas para blogs o newsletters.
- Monitoreo simplificado de contenido relevante sin necesidad de RSS.
- Generación de informes rápidos para equipos de innovación o tecnología.

---

**Número de nodos:** 36  
**Categoría:** utilidades/scraping  
**Tipos de nodos utilizados:**  
`n8n-nodes-base.merge`, `n8n-nodes-base.nocoDb`, `n8n-nodes-base.html`, `n8n-nodes-base.code`, `n8n-nodes-base.scheduleTrigger`, `n8n-nodes-base.stickyNote`, `n8n-nodes-base.openAi`, `n8n-nodes-base.set`, `n8n-nodes-base.httpRequest`, `n8n-nodes-base.itemLists`
```