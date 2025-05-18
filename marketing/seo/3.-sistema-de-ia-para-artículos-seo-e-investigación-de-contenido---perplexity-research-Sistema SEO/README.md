```markdown
# 3. Sistema de IA para artículos SEO e Investigación de Contenido - Perplexity Research

## Descripción
Workflow diseñado para optimizar la creación de artículos SEO mediante un sistema inteligente que investiga contenido relevante usando Perplexity Research. Automatiza la recolección y procesamiento de información para mejorar estrategias de marketing digital.

## Requisitos
- Cuenta activa en n8n.
- Acceso a la API de Perplexity Research (si aplica).
- Credenciales configuradas para realizar solicitudes HTTP externas.
- Permisos para ejecutar workflows en n8n.

## Instrucciones de configuración
1. Importa el workflow en tu instancia de n8n.
2. Configura las credenciales necesarias para el nodo `HTTP Request` con la API de Perplexity Research.
3. Ajusta los parámetros del nodo `Set` para definir las variables de entrada según tus necesidades específicas.
4. Verifica que el nodo `Execute Workflow Trigger` esté habilitado para iniciar el flujo automáticamente.

## Funcionamiento
- El nodo `Execute Workflow Trigger` inicia el proceso.
- El nodo `Set` prepara los datos de entrada para la consulta.
- El nodo `HTTP Request` realiza llamadas a Perplexity Research para obtener información relevante para la creación de artículos SEO.
- Los resultados pueden ser procesados o almacenados según configuración adicional.

## Ejemplos de uso
- Generar resúmenes de contenido competitivo para un nicho específico.
- Investigar palabras clave y temas relacionados mediante consultas automatizadas.
- Apoyar la redacción de artículos optimizados para motores de búsqueda con datos actualizados.

---

**Categoría:** marketing/seo  
**Etiquetas:** Sistema SEO  
**Nodos utilizados:** 3 (Execute Workflow Trigger, Set, HTTP Request)
```