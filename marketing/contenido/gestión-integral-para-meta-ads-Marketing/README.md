```markdown
# Gestión integral para Meta Ads

## Descripción
Workflow para automatizar y optimizar la gestión de campañas de publicidad en Meta Ads, integrando procesamiento de lenguaje natural, toma de decisiones, manejo de datos y automatización de tareas de marketing y contenido.

## Requisitos
- Credenciales API para Meta Ads (Facebook Graph API)
- Claves de acceso para OpenAI y Google Gemini (modelos LangChain)
- Acceso a Airtable (base de datos para almacenamiento y seguimiento)
- n8n configurado con nodos necesarios instalados:
  - `@n8n/n8n-nodes-langchain` (OpenAI, Google Gemini, outputParserStructured, chainLlm)
  - Nodos base de n8n (`switch`, `if`, `code`, `scheduleTrigger`, `stickyNote`, `set`, `airtable`, `splitOut`, `httpRequest`, `facebookGraphApi`, `wait`, `webhook`)

## Instrucciones de configuración
1. Importar el workflow en n8n.
2. Configurar las credenciales:
   - Añadir API keys para OpenAI y Google Gemini en nodos LangChain.
   - Configurar Facebook Graph API con token válido para Meta Ads.
   - Vincular Airtable con API Key y base/datos requeridos.
3. Revisar y modificar parámetros específicos como IDs de campañas, tablas Airtable, URLs y tiempos en nodos `scheduleTrigger` y `wait`.
4. Activar el webhook para recibir eventos externos o iniciar el workflow manualmente.

## Detalles de funcionamiento
- El workflow inicia con un disparador programado (`scheduleTrigger`) o webhook.
- Utiliza modelos de lenguaje LangChain para generación y análisis de contenido publicitario.
- Evalúa condiciones y bifurca el flujo usando nodos `switch` e `if` para tomar decisiones dinámicas.
- Integra llamadas a Facebook Graph API para gestionar campañas, anuncios y métricas.
- Envía y recupera datos desde Airtable para seguimiento y almacenamiento estructurado.
- Maneja el procesamiento paralelo y secuencial de tareas con nodos `splitOut`, `wait` y `code`.
- Genera reportes y ajustes automáticos en base al análisis realizado por modelos de lenguaje y datos recogidos.

## Ejemplos de uso
- Automatizar la creación y ajuste de anuncios según análisis de desempeño y recomendaciones generadas por IA.
- Sincronizar datos de campañas entre Meta Ads y bases Airtable para reporting actualizado.
- Generar contenido creativo para anuncios y variaciones de texto con modelos OpenAI y Google Gemini.
- Controlar flujos de trabajo condicionales para activar pausas o reorientar campañas en tiempo real.

---

**Número de nodos:** 54  
**Categoría:** marketing/contenido  
**Etiquetas:** Marketing
```