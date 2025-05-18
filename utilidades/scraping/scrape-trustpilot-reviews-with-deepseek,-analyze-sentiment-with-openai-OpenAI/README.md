```markdown
# Scrape Trustpilot Reviews with DeepSeek, Analyze Sentiment with OpenAI

## Descripción
Este workflow de n8n permite extraer reseñas de Trustpilot utilizando DeepSeek y analizar el sentimiento de los textos con OpenAI. Ideal para automatizar la recolección y análisis de opiniones de clientes para obtener insights rápidos y accionables.

## Requisitos
- Credenciales de OpenAI API (para análisis de sentimiento y procesamiento de texto)
- Credenciales de Google Drive/Google Sheets (para almacenar y administrar datos)
- API o acceso a DeepSeek para scraping de reseñas Trustpilot (o acceso HTTP configurado)
- n8n instalado y configurado con los nodos necesarios

## Instrucciones de configuración
1. Configure las credenciales de OpenAI en n8n (`lmChatOpenAi` y `sentimentAnalysis`).
2. Configure las credenciales de Google Drive/Google Sheets para gestionar la hoja donde se guardarán las reseñas.
3. Ajuste el nodo HTTP Request o el nodo correspondiente para conectar con la API de DeepSeek y extraer las reseñas de Trustpilot.
4. Revise y adapte los parámetros del workflow como filtros, límites y condiciones en caso de ser necesarios.
5. Importe el workflow y active el trigger manual para iniciar el proceso.

## Detalles de funcionamiento
- El workflow se dispara manualmente o mediante trigger personalizado.
- Hace scraping de reseñas de Trustpilot mediante DeepSeek (nodos HTTP Request y configuración personalizada).
- Procesa y divide el contenido HTML para extraer la información relevante.
- Utiliza nodos de LangChain con OpenAI para análisis y extracción semántica (sobre el contenido textual y sentimiento).
- Filtra y limita resultados según criterios definidos (por ejemplo, número máximo de reseñas).
- Guarda los datos procesados en Google Sheets para su consulta y análisis posterior.
- Incluye nodos de control y lógica para manejar flujos condicionales y procesamiento por lotes.

## Ejemplos de uso
- Monitorizar la reputación de una empresa recogiendo opiniones actualizadas automáticamente.
- Realizar análisis cualitativo y cuantitativo del sentimiento en reseñas para mejorar productos o servicios.
- Generar reportes periódicos con insights extraídos directamente en Google Sheets.

---

**Categoría:** utilidades/scraping  
**Etiquetas:** OpenAI, Google Drive  
**Número de nodos:** 20  
**Nodos principales utilizados:**  
`googleSheets`, `lmChatOpenAi`, `limit`, `if`, `manualTrigger`, `html`, `stickyNote`, `set`, `informationExtractor`, `splitOut`, `httpRequest`, `sentimentAnalysis`
```