```markdown
# AI LinkedIn Lead Gen System with n8n, Apify, and DeepSeek V3.1 to Replace Clay

## Descripción

Workflow de automatización diseñado para generación de leads en LinkedIn, integrando n8n con Apify y DeepSeek V3.1. Este sistema reemplaza la funcionalidad de Clay para extraer y gestionar información de prospectos, optimizando procesos de ventas y lead generation.

## Requisitos

- Cuenta activa en n8n con permisos para configurar workflows.
- Credenciales de Google Sheets para almacenar y acceder a datos.
- API Key de Apify para extracción de datos.
- Credenciales para DeepSeek V3.1 API.
- Cuenta Gmail para envío de correos automáticos.
- Configuración de acceso a OpenRouter Chat (OpenAI o similar) para procesamiento de lenguaje natural.

## Instrucciones de configuración

1. Importar el workflow en tu instancia de n8n.
2. Configurar las credenciales para:
   - Google Sheets (lectura/escritura).
   - Apify (API key).
   - DeepSeek V3.1.
   - Gmail.
   - OpenRouter Chat (LM Chat de LangChain).
3. Ajustar las hojas de Google Sheets utilizadas, definiendo columnas y rango según tu base de datos.
4. Personalizar los triggers de programación para definir la frecuencia de ejecución.
5. Verificar las condiciones en nodos IF y límites de ejecución según necesidad.

## Detalles de funcionamiento

- El workflow inicia con un trigger programado que activa la extracción de datos desde Apify y DeepSeek.
- Los datos son procesados y filtrados mediante nodos IF y limitadores para manejar volúmenes y calidad.
- La información extraída se envía a Google Sheets para su almacenamiento y seguimiento.
- Usa modelos de lenguaje en OpenRouter Chat para analizar y enriquecer los datos de prospectos.
- Automatiza el envío de correos personalizados vía Gmail para contactar leads generados.
- Incluye nodos para notas y seteo dinámico de variables internas que controlan el flujo.
- En total, emplea 25 nodos, combinando nodos base de n8n y nodos especializados de LangChain.

## Ejemplos de uso

- Generar listas de leads actualizadas semanalmente desde LinkedIn usando Apify.
- Enriquecer perfiles de contacto con información adicional procesada por DeepSeek y LangChain.
- Automatizar campañas de email marketing personalizadas para leads recién capturados.
- Sustituir procesos manuales de prospección con una solución integrada y escalable.

---

*Categoría: ventas / lead-generation*  
*Nodos utilizados: n8n-nodes-base.googleSheets, n8n-nodes-base.limit, @n8n/n8n-nodes-langchain.lmChatOpenRouter, n8n-nodes-base.if, @n8n/n8n-nodes-langchain.chainLlm, n8n-nodes-base.scheduleTrigger, n8n-nodes-base.stickyNote, n8n-nodes-base.set, @n8n/n8n-nodes-langchain.informationExtractor, n8n-nodes-base.gmail, n8n-nodes-base.httpRequest*  
*Número total de nodos: 25*
```