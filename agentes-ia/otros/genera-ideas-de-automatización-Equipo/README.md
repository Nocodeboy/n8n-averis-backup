```markdown
# Genera ideas de Automatización

## Descripción
Workflow diseñado para generar y recopilar ideas de automatización utilizando múltiples fuentes de información y análisis de sentimiento, facilitando la gestión y evaluación de ideas innovadoras para el equipo.

## Requisitos
- Credenciales de Google Sheets para lectura y escritura en hojas de cálculo.
- API Key de OpenAI para los nodos de lenguaje (ChatOpenAi y OpenAi).
- Credenciales o acceso configurado para el nodo de Reddit.
- n8n versión compatible con nodos `@n8n/n8n-nodes-langchain` y nodos base.

## Instrucciones de configuración
1. Configure el nodo **Google Sheets** con las credenciales adecuadas apuntando a la hoja deseada.
2. Añada su API Key de OpenAI en los nodos `lmChatOpenAi` y `openAi`.
3. Configure el nodo **Reddit** con la autenticación necesaria para acceder a los subreddits de interés.
4. Personalice el nodo **Manual Trigger** para iniciar el workflow cuando desee generar nuevas ideas.
5. Ajuste los nodos `Set` y `Aggregate` según el formato y filtrado requerido para sus datos.

## Detalles de funcionamiento
- El workflow se inicia manualmente o mediante un disparador configurado.
- Recopila inputs desde Reddit y otras fuentes internas definidas por el equipo.
- Utiliza modelos de lenguaje OpenAI para generar, analizar y enriquecer ideas.
- Realiza análisis de sentimiento para valorar la recepción de las ideas propuestas.
- Agrega y organiza la información recopilada para su fácil revisión y seguimiento.
- Finalmente, actualiza una hoja de Google Sheets con las ideas generadas y sus detalles.

## Ejemplos de uso
- Generar nuevas ideas de automatización a partir de tendencias y discusiones en Reddit.
- Evaluar el sentimiento general de un conjunto de ideas para priorizar proyectos.
- Centralizar y documentar ideas para sesiones de brainstorming en equipo.

---

**Categoría:** agentes-ia/otros  
**Etiquetas:** Equipo, Ideas  
**Número de nodos:** 9  
**Nodos utilizados:** n8n-nodes-base.aggregate, @n8n/n8n-nodes-langchain.lmChatOpenAi, @n8n/n8n-nodes-langchain.openAi, n8n-nodes-base.googleSheets, n8n-nodes-base.reddit, n8n-nodes-base.manualTrigger, n8n-nodes-base.set, @n8n/n8n-nodes-langchain.sentimentAnalysis
```