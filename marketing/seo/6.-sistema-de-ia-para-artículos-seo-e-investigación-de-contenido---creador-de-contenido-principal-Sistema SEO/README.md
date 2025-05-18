```markdown
# 6. Sistema de IA para artículos SEO e Investigación de Contenido - Creador de Contenido Principal

## Descripción

Workflow diseñado para automatizar la creación de contenido SEO y realizar investigación de temas utilizando inteligencia artificial avanzada, facilitando la generación de artículos optimizados para posicionamiento web.

## Requisitos

- Credenciales de n8n configuradas para ejecutar workflows.
- API Key válida de OpenAI para el nodo `lmChatOpenAi`.
- Permiso para utilizar los nodos de Langchain (`@n8n/n8n-nodes-langchain`).

## Instrucciones de configuración

1. Configure las credenciales de OpenAI en n8n:
   - Navegue a **Credenciales** > **OpenAI** > agregue su API Key.
2. Importe el workflow en su instancia de n8n.
3. Verifique que los nodos `executeWorkflowTrigger`, `lmChatOpenAi` y `agent` estén correctamente vinculados y configurados según sus necesidades.
4. Ajuste los parámetros del agente Langchain en caso de requerir configuración específica para la investigación o creación de contenido.

## Detalles de funcionamiento

- **Trigger (`executeWorkflowTrigger`)**: Inicia el workflow cuando se ejecuta manualmente o mediante evento programado.
- **Generación de contenido (`lmChatOpenAi`)**: Utiliza el modelo de lenguaje de OpenAI para crear texto optimizado para SEO basado en las pautas definidas.
- **Agente Langchain (`agent`)**: Realiza investigación dinámica para enriquecer el contenido con datos relevantes y actualizados.

## Ejemplos de uso

- Generar automáticamente un artículo optimizado para una palabra clave específica.
- Realizar análisis y resumen de contenido relacionado para crear un briefing de investigación.
- Integrar con otros workflows para publicación directa en plataformas CMS.

---

**Etiqueta**: Sistema SEO  
**Categoría**: marketing/seo  
**Número de nodos**: 3
```