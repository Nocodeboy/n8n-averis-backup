```markdown
# ***** Crea post de Linkedin - Dani

## Descripción  
Workflow de n8n para la creación y publicación automatizada de posts en LinkedIn. Integra fuentes RSS, generación de contenido con OpenAI y publicación directa para optimizar la estrategia de marketing de contenido.

## Requisitos  
- Credenciales LinkedIn con permisos para publicar posts.  
- API key de OpenAI (compatible con el nodo `lmChatOpenAi`).  
- Acceso a Gmail configurado para envío o recepción de notificaciones (opcional).  
- Fuente RSS relevante para la base de contenido.  

## Instrucciones de configuración  
1. Configurar credenciales LinkedIn en n8n.  
2. Añadir API key de OpenAI en el nodo correspondiente.  
3. Ingresar detalles de la fuente RSS a monitorear.  
4. Ajustar nodos `set` y `if` según criterios específicos de contenido y filtrado.  
5. Configurar Gmail si se desea enviar notificaciones o reportes.  

## Detalles de funcionamiento  
- El workflow inicia con un disparador manual o lectura periódica del feed RSS.  
- Los datos extraídos son agregados y procesados mediante modelos de lenguaje OpenAI para generar contenido original.  
- Utiliza nodos de análisis y parseo para estructurar la información antes de crear el post.  
- Luego, publica directamente en LinkedIn utilizando el nodo oficial.  
- Opcionalmente, envía confirmaciones o alertas vía Gmail.  

## Ejemplos de uso  
- Actualizar automáticamente la presencia en LinkedIn con contenido relevante y personalizado.  
- Generar resúmenes o insights a partir de feeds RSS sectoriales y compartirlos con la comunidad.  
- Automatizar campañas de marketing de contenido sin intervención manual constante.

---

**Etiquetas:** Contenido, *****, Linkedin  
**Categoría:** marketing/contenido  
**Número de nodos:** 29  
**Tipos de nodos utilizados:** n8n-nodes-base.aggregate, n8n-nodes-base.linkedIn, @n8n/n8n-nodes-langchain.lmChatOpenAi, n8n-nodes-base.rssFeedRead, @n8n/n8n-nodes-langchain.chainLlm, n8n-nodes-base.manualTrigger, n8n-nodes-base.html, n8n-nodes-base.if, n8n-nodes-base.gmail, n8n-nodes-base.stickyNote, n8n-nodes-base.set, @n8n/n8n-nodes-langchain.outputParserStructured, n8n-nodes-base.splitOut, n8n-nodes-base.httpRequest
```