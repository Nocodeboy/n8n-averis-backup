```markdown
# 7. Sistema de IA para artículos SEO e Investigación de Contenido - Keyword Research

## Descripción
Workflow diseñado para automatizar la investigación de palabras clave mediante Inteligencia Artificial, optimizando la creación de artículos SEO y estrategias de contenido. Facilita la recopilación, análisis y agregación de datos clave para mejorar el posicionamiento web.

## Requisitos
- Cuenta activa en n8n.
- Credenciales para APIs utilizadas en la investigación (configuradas en el nodo HTTP Request).
- Permisos para ejecutar workflows anidados (Execute Workflow Trigger).

## Instrucciones de configuración
1. Configura las credenciales necesarias en n8n para las APIs de investigación de palabras clave.
2. Ajusta el nodo `Execute Workflow Trigger` para invocar el workflow deseado según la lógica de integración.
3. Personaliza parámetros en el nodo `Set` para definir las palabras clave o temas a investigar.
4. Verifica los endpoints y autenticación en el nodo `HTTP Request`.
5. Configura el nodo `Aggregate` según los criterios de consolidación de datos.

## Detalles de funcionamiento
- El flujo inicia con un disparador que activa el workflow (Execute Workflow Trigger).
- El nodo `Set` define las variables o términos para la búsqueda de keywords.
- `HTTP Request` realiza consultas a servicios externos de análisis de palabras clave.
- Finalmente, `Aggregate` procesa y consolida los resultados para obtener insights precisos.

## Ejemplos de uso
- Generar listas actualizadas de keywords relevantes para nuevos artículos.
- Analizar la competencia y volumen de búsqueda de términos específicos.
- Optimizar contenido existente basándose en datos agregados y tendencias actuales.
```