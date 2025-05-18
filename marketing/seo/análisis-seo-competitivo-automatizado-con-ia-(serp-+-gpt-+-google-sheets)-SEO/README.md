```markdown
# Análisis SEO Competitivo Automatizado con IA (SERP + GPT + Google Sheets)

## Descripción

Workflow automatizado para realizar un análisis SEO competitivo combinando resultados de búsqueda (SERP), inteligencia artificial (OpenAI GPT) y gestión de datos en Google Sheets. Ideal para marketing y SEO, permite obtener insights rápidos sobre la competencia y optimizar estrategias.

## Requisitos

- Cuenta y credenciales de OpenAI para acceder a la API de GPT.
- Cuenta de Google con acceso a Google Sheets y proyecto habilitado para Google Sheets API.
- Credenciales configuradas en n8n para OpenAI y Google Sheets.
- n8n versión compatible con los nodos mencionados.

## Instrucciones de configuración

1. Importa el workflow en tu instancia de n8n.
2. Configura las credenciales de OpenAI (`@n8n/n8n-nodes-langchain.openAi`) con tu API key.
3. Configura las credenciales de Google Sheets (`n8n-nodes-base.googleSheets`) con acceso a la hoja donde se almacenarán los datos.
4. Ajusta los parámetros iniciales en el nodo `formTrigger` según tus necesidades (como palabras clave o URLs a analizar).
5. Verifica que todas las conexiones y límites en nodos `limit`, `splitInBatches`, y demás estén correctamente configurados para tu volumen de datos.

## Detalles de funcionamiento

- Recopila datos SEO competitivos desde SERP mediante consultas HTTP.
- Procesa y analiza la información con OpenAI GPT para obtener resúmenes e insights.
- Almacena y actualiza resultados en Google Sheets para fácil seguimiento y colaboración.
- Utiliza control de flujo avanzado con nodos como `if`, `merge`, `wait`, `removeDuplicates` para asegurar datos limpios y procesos eficientes.
- Integra nodos de batch y límite para manejar grandes volúmenes manteniendo rendimiento estable.

## Ejemplos de uso

- Evaluar la posición y estrategia SEO de competidores en un nicho específico.
- Generar reportes automáticos con recomendaciones SEO basadas en datos actuales.
- Monitorear cambios en posicionamiento y ajustar campañas en tiempo real.

---

**Categoría:** marketing/seo  
**Etiquetas:** SEO  
**Número de nodos:** 36  
**Nodos principales:**  
`@n8n/n8n-nodes-langchain.openAi`, `n8n-nodes-base.googleSheets`, `n8n-nodes-base.limit`, `n8n-nodes-base.merge`, `n8n-nodes-base.if`, `n8n-nodes-base.formTrigger`, `n8n-nodes-base.wait`, `n8n-nodes-base.stickyNote`, `n8n-nodes-base.set`, `n8n-nodes-base.splitInBatches`, `n8n-nodes-base.httpRequest`, `n8n-nodes-base.splitOut`, `n8n-nodes-base.removeDuplicates`, `n8n-nodes-base.markdown`
```