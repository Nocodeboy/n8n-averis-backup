```markdown
# 4. Sistema de IA para artículos SEO e Investigación de Contenido - Creador de Cabeceras

## Descripción
Workflow diseñado para generar cabeceras optimizadas para artículos SEO mediante un sistema de inteligencia artificial, facilitando la investigación de contenido relevante para estrategias de marketing digital.

## Requisitos
- Cuenta activa en n8n.
- Credenciales para el nodo `@n8n/n8n-nodes-langchain.lmChatAnthropic` (Anthropic API key).
- Configuración del nodo `@n8n/n8n-nodes-langchain.agent` para gestionar la lógica conversacional.
- Permisos para ejecutar workflows mediante el nodo `n8n-nodes-base.executeWorkflowTrigger`.

## Instrucciones de configuración
1. Agrega tu API key de Anthropic en el nodo `lmChatAnthropic`.
2. Configura el nodo `agent` con las instrucciones o agentes personalizados necesarios para la generación de contenido SEO.
3. Ajusta el workflow trigger para habilitar la ejecución automática o manual según tu flujo de trabajo.
4. Revisa y ajusta parámetros específicos en los nodos según tu caso de uso.

## Detalles de funcionamiento
- El workflow se activa mediante el nodo `executeWorkflowTrigger`.
- El nodo `lmChatAnthropic` envía solicitudes a la API de Anthropic para generar texto basado en prompts relacionados con SEO.
- El nodo `agent` procesa y refina los resultados, aplicando lógica para crear cabeceras coherentes y optimizadas para SEO.
  
Número de nodos: 3  
Categoría: marketing/seo  
Etiquetas: Sistema SEO

## Ejemplos de uso
- Generar títulos atractivos y optimizados para publicaciones de blog enfocadas en keywords específicas.
- Crear estructuras de cabeceras para mejorar la organización y SEO on-page de contenidos web.
- Automatizar la investigación y generación de ideas para artículos en campañas de marketing digital.
```