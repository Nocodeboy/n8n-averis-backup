```markdown
# Scrapping de páginas web

## Descripción
Workflow diseñado para extraer y procesar información de páginas web mediante técnicas de scraping automatizado, integrando capacidades de procesamiento con OpenAI y almacenamiento en Google Sheets.

## Requisitos
- Credenciales para API de OpenAI (`@n8n/n8n-nodes-langchain.openAi`)
- Cuenta y credenciales de Google Sheets (`n8n-nodes-base.googleSheets`)
- Acceso a internet para realizar solicitudes HTTP
- n8n versión compatible con los nodos utilizados

## Instrucciones de configuración
1. Configure las credenciales de OpenAI en n8n.
2. Configure las credenciales de Google Sheets con acceso a la hoja donde se almacenarán los datos.
3. Ajuste las URLs o fuentes web en el nodo HTTP Request según las páginas objetivo.
4. Adapte las reglas y condiciones en los nodos If, Code y Merge de acuerdo a la lógica específica del scraping.
5. Revise los parámetros del nodo ChatTrigger para controlar la interacción con modelos de lenguaje.

## Detalles de funcionamiento
Este workflow consta de 29 nodos que combinan procesos para:
- Realizar solicitudes HTTP a páginas web específicas.
- Parsear contenido XML/HTML utilizando nodos XML.
- Aplicar lógica condicional para filtrar o dirigir datos mediante nodos If.
- Procesar y transformar datos mediante nodos Code.
- Enriquecer información y generar resúmenes con OpenAI.
- Almacenar resultados ordenados en hojas de Google Sheets.
- Generar notas y documentación en markdown para seguimiento interno.
- Utilizar nodos de integración con Langchain para chat y comandos específicos.

## Ejemplos de uso
- Extracción automática de productos con descripción y precio desde tiendas online.
- Monitoreo de noticias o blogs ingresando URLs para análisis y resumen.
- Generación de reportes diarios con información extraída y consolidada en Google Sheets.
- Automatización de respuestas o análisis mediante OpenAI a partir del contenido scraping.

---

**Categoría:** utilidades/scraping  
**Etiquetas:** _(pendiente)_  
**Nodos usados:** 29  
**Tipos de nodos:** `@n8n/n8n-nodes-langchain.openAi`, `n8n-nodes-base.googleSheets`, `n8n-nodes-base.merge`, `n8n-nodes-base.if`, `n8n-nodes-base.code`, `n8n-nodes-base.stickyNote`, `n8n-nodes-base.xml`, `n8n-nodes-base.httpRequest`, `@n8n/n8n-nodes-langchain.chatTrigger`, `n8n-nodes-base.markdown`
```