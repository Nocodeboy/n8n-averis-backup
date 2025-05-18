```markdown
# T - Scrappeador y analizador de ofertas de trabajo en Hacker News

## Descripción
Workflow diseñado para extraer y analizar automáticamente las ofertas de trabajo publicadas en Hacker News. Utiliza técnicas de scraping combinadas con procesamiento de lenguaje natural para categorizar y priorizar las oportunidades laborales.

## Requisitos
- Cuenta y credenciales de [OpenAI](https://platform.openai.com/) para utilizar el nodo `@n8n/n8n-nodes-langchain.lmChatOpenAi`.
- Acceso a Airtable con una base y tabla configuradas para almacenar las ofertas (`n8n-nodes-base.airtable`).
- n8n versión compatible con los nodos utilizados, incluyendo nodos de Langchain y los integrados estándar de n8n.

## Instrucciones de configuración
1. Configura tus credenciales de OpenAI en n8n.
2. Añade las credenciales de Airtable en n8n con acceso a la base donde se guardarán las ofertas.
3. Importa o crea el workflow en n8n.
4. Ajusta los parámetros del nodo HTTP Request para apuntar a la URL de Hacker News (por defecto configurado para scraping de ofertas de trabajo).
5. Revisa y adapta los filtros y cadenas de análisis según tus necesidades específicas.

## Detalles de funcionamiento
- El workflow inicia con un trigger manual (`manualTrigger`).
- Se realiza un scraping a la sección de trabajos de Hacker News usando `httpRequest`.
- Se procesa y divide la información (`splitOut`) para analizar cada oferta individualmente.
- Se utilizan nodos de Langchain (`lmChatOpenAi`, `chainLlm`, `outputParserStructured`) para analizar el texto y estructurar la información relevante.
- Los nodos de código y filtros refinan y descartan resultados irrelevantes.
- Finalmente, las ofertas analizadas se almacenan en Airtable para su posterior consulta y seguimiento.
- Se usan nodos auxiliares como `stickyNote`, `set` y `limit` para manejo interno y control del flujo.

## Ejemplos de uso
- Ejecutar manualmente para obtener un listado actualizado de ofertas de trabajo en Hacker News.
- Automatizar ejecuciones periódicas para mantener una base de datos actualizada de oportunidades laborales.
- Aplicar análisis personalizados para categorizar y priorizar ofertas según criterios definidos en Langchain.
```
