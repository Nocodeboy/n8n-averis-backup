```markdown
# 1. Sistema de IA para artículos SEO e Investigación de Contenido - Main

## Descripción
Este workflow de n8n automatiza la generación y optimización de artículos SEO mediante técnicas avanzadas de inteligencia artificial e investigación de contenido. Utiliza modelos de lenguaje OpenAI y herramientas Langchain para crear textos optimizados, estructurados y con análisis profundo de palabras clave.

## Requisitos
- Cuenta y credenciales API de OpenAI (para nodos `@n8n/n8n-nodes-langchain.openAi` y `lmChatOpenRouter`)
- Credenciales de Google para acceder a Google Docs (nodo `n8n-nodes-base.googleDocs`)
- n8n versión compatible con nodos de Langchain y versiones específicas de nodos base
- Acceso a internet para realizar solicitudes HTTP

## Instrucciones de configuración
1. Configura las credenciales de OpenAI en n8n:
   - Añade tu API key en el panel de credenciales para los nodos Langchain.
2. Configura las credenciales de Google Docs:
   - Añade la cuenta o credenciales OAuth para permitir la creación y edición de documentos.
3. Revisa los parámetros de los nodos `formTrigger` y código para adaptarlos a tus necesidades específicas de SEO.
4. Asegúrate que todas las dependencias y nodos están instalados y actualizados en tu entorno n8n.

## Detalles de funcionamiento
- El workflow inicia mediante un formulario (`formTrigger`) para capturar inputs de contenido o keywords.
- Los nodos Langchain integran modelos OpenAI para generar textos, realizar análisis semántico y estructurar la información.
- Se utiliza agregación de datos (`aggregate`), procesamiento por lotes (`splitInBatches`) y herramientas estructuradoras (`outputParserStructured`, `outputParserAutofixing`) para optimizar la calidad del contenido.
- Los resultados finales se almacenan y actualizan en documentos de Google Docs.
- Nodos adicionales como `set`, `code`, `stickyNote` y `httpRequest` facilitan gestión interna, anotaciones y peticiones externas para enriquecer la información.
- El agente Langchain (`agent`) orquesta la ejecución inteligente de cadenas y tareas automatizadas.

## Ejemplos de uso
- Generar un artículo optimizado para la palabra clave "marketing digital" a partir de un formulario.
- Realizar una investigación de contenido para un nicho específico y exportar resultados en Google Docs.
- Automatizar la corrección y mejora continua de textos SEO generados por IA.

---

**Categoría:** marketing/seo  
**Etiquetas:** Sistema SEO  
**Número de nodos:** 30
```