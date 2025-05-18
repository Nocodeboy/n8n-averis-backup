```markdown
# Linkedin Posts

## Descripción
Workflow de n8n para automatizar la creación y publicación de contenido en LinkedIn, combinando datos de Google Sheets con la generación de texto mediante OpenAI, para optimizar estrategias de marketing de contenido.

## Requisitos
- Credenciales de Google Sheets configuradas en n8n.
- API Key de OpenAI para el nodo `lmChatOpenAi`.
- Acceso y credenciales para la API de Ghost (opcional, según configuración).
- n8n instalado con los nodos:
  - `n8n-nodes-base.googleSheets`
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`
  - `n8n-nodes-base.merge`
  - `n8n-nodes-base.manualTrigger`
  - `n8n-nodes-base.code`
  - `@n8n/n8n-nodes-langchain.agent`
  - `n8n-nodes-base.ghost`
  - `n8n-nodes-base.set`
  - `n8n-nodes-base.stickyNote`
  - `n8n-nodes-base.splitInBatches`

## Instrucciones de configuración
1. Configura las credenciales de Google Sheets en n8n con acceso a la hoja donde están los datos.
2. Añade la API Key de OpenAI en el nodo `lmChatOpenAi`.
3. Si usas Ghost para publicar, configura las credenciales de acceso en el nodo correspondiente.
4. Personaliza la hoja de Google Sheets con el contenido o ideas base para los posts.
5. Ajusta los parámetros de los nodos `lmChatOpenAi` y `agent` según el tipo de contenido que quieres generar.
6. Activa el workflow con el nodo `manualTrigger` o programa su ejecución.

## Detalles de funcionamiento
- El workflow inicia con un disparador manual o programado.
- Lee las ideas o datos base desde Google Sheets.
- Utiliza la inteligencia de OpenAI para generar textos optimizados para LinkedIn.
- Procesa y fusiona resultados para crear posts completos.
- Opcionalmente, publica los posts directamente en Ghost o prepara el contenido para otras plataformas.
- Incluye nodos de control y procesamiento como `splitInBatches` para manejo eficiente de grandes volúmenes.
- Utiliza nodos de código y notas adhesivas para ajustes y documentación interna del flujo.

## Ejemplos de uso
- Automatizar la generación semanal de posts en LinkedIn para aumentar la presencia digital.
- Extraer temas relevantes desde una hoja de cálculo y desarrollar contenido creativo con IA.
- Publicar automáticamente artículos o resúmenes en plataformas vinculadas como Ghost.
- Adaptar fácilmente a otros canales de marketing cambiando solo los nodos finales de publicación.

---

**Categoría:** marketing/contenido  
**Etiquetas:** n8nCommunity  
**Número de nodos:** 14
```