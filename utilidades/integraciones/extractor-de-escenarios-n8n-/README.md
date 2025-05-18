```markdown
# Extractor de Escenarios n8n

## Descripción
Workflow diseñado para extraer, procesar y gestionar escenarios a partir de diversas fuentes, integrando Google Drive y herramientas de lenguaje natural mediante LangChain. Optimiza la automatización y análisis de datos en tu flujo de trabajo.

## Requisitos
- Cuenta y credenciales de Google Drive con acceso a los recursos necesarios.
- API Key válida para LangChain (OpenRouter) para los nodos de lenguaje.
- n8n instalado con soporte para nodos base y nodos LangChain (`@n8n/n8n-nodes-langchain`).
- Permisos adecuados para funcionamiento de nodos como manualTrigger y scheduleTrigger.

## Instrucciones de configuración
1. Importa el workflow en tu instancia de n8n.
2. Configura las credenciales de Google Drive en “Credenciales” dentro de n8n.
3. Añade tu API Key de OpenRouter en las credenciales para nodos LangChain.
4. Ajusta los nodos de configuración (`set`, `code`, `filter`) según tus escenarios específicos.
5. Define los disparadores (`manualTrigger`, `scheduleTrigger`) según la frecuencia deseada.
6. Verifica los permisos de acceso para cada nodo que interactúa con recursos externos.

## Detalles de funcionamiento
- El workflow contiene 33 nodos combinando utilidades para formularios, manejo de datos, filtros y procesamiento de lenguaje natural.
- Utiliza nodos de LangChain para interpretar y generar respuestas avanzadas mediante OpenRouter.
- Integra Google Drive para lectura y almacenamiento de archivos y datos de escenarios.
- Utiliza nodos como `merge`, `splitInBatches` y `itemLists` para manejar flujo y transformación de datos.
- Contiene lógica condicional y de programación (`if`, `code`) para direccionar el flujo según criterios definidos.
- Soporta disparadores manuales y programados para mayor flexibilidad.

## Ejemplos de uso
- Extracción automática de escenarios y generación de resúmenes a partir de documentos almacenados en Google Drive.
- Procesamiento de formularios recibidos y análisis mediante modelos de lenguaje.
- Automatización de tareas periódicas para actualización y clasificación de escenarios.
- Uso de agentes LangChain para responder consultas específicas sobre escenarios extraídos.

---

*Categoría:* utilidades/integraciones  
*Número de nodos:* 33  
*Tipos de nodos:*  
`n8n-nodes-base.form`, `n8n-nodes-base.n8n`, `n8n-nodes-base.googleDrive`, `n8n-nodes-base.merge`, `@n8n/n8n-nodes-langchain.lmChatOpenRouter`, `n8n-nodes-base.if`, `n8n-nodes-base.manualTrigger`, `n8n-nodes-base.filter`, `n8n-nodes-base.code`, `n8n-nodes-base.scheduleTrigger`, `n8n-nodes-base.stickyNote`, `n8n-nodes-base.set`, `@n8n/n8n-nodes-langchain.agent`, `n8n-nodes-base.splitInBatches`, `n8n-nodes-base.moveBinaryData`, `n8n-nodes-base.itemLists`
```