```markdown
# Multiagentes de creación de contenido

## Descripción
Workflow orientado a la generación y gestión automática de contenido mediante múltiples agentes de IA. Integra modelos de lenguaje y Google Sheets para coordinar, crear y almacenar contenido de manera eficiente.

## Requisitos
- Credenciales de Google Sheets con permisos de lectura/escritura
- API Key de OpenAI para acceso al modelo `lmChatOpenAi`
- n8n con los nodos necesarios instalados:
  - `n8n-nodes-base.aggregate`
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`
  - `n8n-nodes-base.googleSheets`
  - `n8n-nodes-base.googleSheetsTrigger`
  - `@n8n/n8n-nodes-langchain.agent`
  - `n8n-nodes-base.set`
  - `n8n-nodes-base.splitOut`
  - `n8n-nodes-base.httpRequest`

## Instrucciones de configuración
1. Configure las credenciales de Google Sheets en n8n.
2. Añada la API Key de OpenAI en las credenciales de LangChain.
3. Importe este workflow en su instancia de n8n.
4. Ajuste las hojas de Google Sheets de entrada y salida según su necesidad.
5. Personalice parámetros en los nodos `lmChatOpenAi` y agentes para adaptar el contenido.

## Detalles de funcionamiento
- El workflow inicia con un trigger conectado a Google Sheets que detecta cambios o nuevas entradas.
- Utiliza agentes IA para analizar y expandir contenido mediante llamadas a `lmChatOpenAi`.
- Los datos se procesan y agregan con nodos `aggregate` y se dividen con `splitOut` para manejo individual.
- Resultados finales se almacenan y actualizan en Google Sheets para seguimiento.
- También incluye nodos HTTP Request para integración con APIs externas según necesidad.

## Ejemplos de uso
- Generación automática de artículos o posts a partir de temas listados en Google Sheets.
- Coordinación de múltiples agentes IA para creación colaborativa de contenido.
- Automatización de actualización y seguimiento de estado de contenido en hojas compartidas.

---
**Categoría:** agentes-ia/otros  
**Número de nodos:** 12  
**Etiquetas:** _(sin etiquetas asignadas)_
```