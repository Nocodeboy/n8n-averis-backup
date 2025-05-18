```markdown
# Análisis de sentimiento

## Descripción
Workflow diseñado para realizar análisis de sentimiento de textos utilizando modelos de lenguaje, integrando múltiples fuentes de datos y canales de comunicación.

## Requisitos
- Credenciales de OpenAI para el nodo `@n8n/n8n-nodes-langchain.lmChatOpenAi`.
- Acceso y credenciales a Airtable para consultas y actualizaciones (`n8n-nodes-base.airtable` y `airtableTrigger`).
- Token y configuración para integración con Slack (`n8n-nodes-base.slack`).
- Endpoint GraphQL accesible para consultas relacionadas (`n8n-nodes-base.graphql`).

## Instrucciones de configuración
1. Configure las credenciales de OpenAI en n8n.
2. Vincule su cuenta de Airtable y configure las bases y tablas correspondientes.
3. Establezca las credenciales y canales de Slack para recibir notificaciones o enviar mensajes.
4. Configure el endpoint GraphQL con las credenciales necesarias.
5. Revise y ajuste el nodo `scheduleTrigger` según la frecuencia deseada.
6. Personalice las reglas en el nodo `switch` para manejar distintos flujos según resultados.

## Detalles de funcionamiento
- El workflow se inicia con el `scheduleTrigger`.
- Extrae información relevante mediante `informationExtractor`.
- Utiliza el modelo OpenAI para analizar el sentimiento del texto.
- Procesa los resultados con nodos lógicos (`switch`, `splitInBatches`, `removeDuplicates`) para gestionar múltiples entradas.
- Actualiza registros en Airtable y envía alertas o resúmenes a Slack.
- Incluye notas y estados mediante `stickyNote` y `set` para seguimiento interno.
- Soporta activación por cambios en Airtable con `airtableTrigger`.
- Complementa consultas y gestión con GraphQL.

## Ejemplos de uso
- Análisis periódico de comentarios de clientes almacenados en Airtable.
- Notificación automática vía Slack cuando se detecta sentimiento negativo.
- Extracción y procesamiento batch de textos para reportes semanales.
```
