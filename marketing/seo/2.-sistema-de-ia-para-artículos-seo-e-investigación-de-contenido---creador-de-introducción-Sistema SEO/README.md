```markdown
# 2. Sistema de IA para artículos SEO e Investigación de Contenido - Creador de Introducción

## Descripción
Workflow diseñado para automatizar la creación de introducciones optimizadas para artículos SEO mediante inteligencia artificial. Combina técnicas avanzadas de generación de texto y agentes inteligentes para producir contenido relevante y atractivo.

## Requisitos
- Credenciales para acceder a los nodos de LangChain:
  - API key para el modelo Anthropic (lmChatAnthropic)
- Acceso a n8n con permisos para ejecutar workflows anidados (`executeWorkflowTrigger`)
- Configuración del nodo `@n8n/n8n-nodes-langchain.agent` que gestione la lógica de agente

## Instrucciones de configuración
1. Configure las credenciales de Anthropic en n8n.
2. Importe este workflow en su instancia de n8n.
3. Ajuste el nodo `executeWorkflowTrigger` para activar otros workflows si aplica.
4. Verifique que las conexiones entre nodos estén correctamente definidas.
5. Personalice los parámetros del agente LangChain para optimizar la generación según su nicho SEO.

## Detalles de funcionamiento
- El trigger `executeWorkflowTrigger` inicia el proceso.
- `lmChatAnthropic` se encarga de generar texto basado en prompts específicos para introducciones SEO.
- El nodo agente (`@n8n/n8n-nodes-langchain.agent`) supervisa, ajusta y mejora la generación utilizando técnicas de inteligencia artificial contextualizadas.

## Ejemplos de uso
- Generar automáticamente la introducción para un blog post sobre tendencias de marketing digital.
- Crear contenido introductorio para páginas de productos optimizadas para motores de búsqueda.
- Producir resúmenes breves que capturen la atención del lector en artículos SEO.

---

**Categoría:** marketing/seo  
**Etiquetas:** Sistema SEO  
**Número de nodos:** 3  
**Tipos de nodos utilizados:** n8n-nodes-base.executeWorkflowTrigger, @n8n/n8n-nodes-langchain.lmChatAnthropic, @n8n/n8n-nodes-langchain.agent
```