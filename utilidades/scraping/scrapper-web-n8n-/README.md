```markdown
# Scrapper web n8n

## Descripción
Workflow de n8n para realizar scraping web y procesamiento avanzado de contenido utilizando nodos de LangChain, HTML y diversas utilidades para manipulación y control de datos.

## Requisitos
- Cuenta y credenciales de OpenAI (o servicio compatible) para nodos `lmChatOpenAi` y cadenas LangChain.
- Acceso a URLs públicas o privadas para scraping mediante HTTP Request.
- n8n instalado con los siguientes paquetes:
  - `@n8n/n8n-nodes-langchain`
  - `n8n-nodes-base`

## Instrucciones de configuración
1. Configure las credenciales de OpenAI en n8n.
2. Asigne las URLs objetivo en los nodos `httpRequest`.
3. Ajuste parámetros de límites, división de texto y resumen según necesidad.
4. Active el workflow manualmente o mediante trigger configurado en el nodo `manualTrigger`.

## Detalles de funcionamiento
- El workflow inicia con un disparo manual (`manualTrigger`).
- Realiza solicitudes HTTP para obtener contenido HTML.
- Utiliza nodos `html` para extraer datos específicos.
- Divide los textos largos con `textSplitterRecursiveCharacterTextSplitter`.
- Aplica modelos de lenguaje (`lmChatOpenAi`) para resumir y analizar el contenido.
- Controla el flujo con nodos `limit`, `merge`, `splitOut` y `set`.
- Documenta o muestra información con `stickyNote`.
- Usa cargas y cadenas LangChain para manejo avanzado de documentos y resúmenes.

## Ejemplos de uso
- Extracción y resumen automático de artículos web.
- Generación de insights a partir de páginas HTML extensas.
- Automatización de informes basados en contenido online actualizado.

---

**Nodos utilizados (16):**  
`@n8n/n8n-nodes-langchain.lmChatOpenAi`,  
`n8n-nodes-base.limit`,  
`n8n-nodes-base.merge`,  
`n8n-nodes-base.html`,  
`n8n-nodes-base.manualTrigger`,  
`@n8n/n8n-nodes-langchain.textSplitterRecursiveCharacterTextSplitter`,  
`n8n-nodes-base.stickyNote`,  
`n8n-nodes-base.set`,  
`n8n-nodes-base.splitOut`,  
`n8n-nodes-base.httpRequest`,  
`@n8n/n8n-nodes-langchain.chainSummarization`,  
`@n8n/n8n-nodes-langchain.documentDefaultDataLoader`
```