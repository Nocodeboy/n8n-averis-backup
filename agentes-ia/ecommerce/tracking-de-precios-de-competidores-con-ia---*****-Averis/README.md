```markdown
# Tracking de Precios de Competidores con IA - *****

## Descripción
Workflow diseñado para monitorear y analizar precios de competidores en ecommerce utilizando inteligencia artificial. Integra Google Sheets para el almacenamiento de datos, modelos de lenguaje para análisis y comunicación automatizada a través de Slack.

## Requisitos
- Credenciales de Google Sheets con acceso a la hoja de seguimiento.
- API Key para Google Gemini (modelo de lenguaje de Google).
- Configuración de Slack Webhook o credenciales para enviar notificaciones.
- Acceso a Internet para realizar solicitudes HTTP.

## Instrucciones de configuración
1. Configure las credenciales de Google Sheets en n8n.
2. Añada la API Key de Google Gemini en las credenciales específicas del modelo de lenguaje.
3. Configure las credenciales de Slack para notificaciones.
4. Ajuste la hoja de Google Sheets con las columnas necesarias para el tracking de precios.
5. Personalice los parámetros del workflow según sus criterios de investigación y frecuencia de monitoreo.

## Detalles de funcionamiento
- El workflow se activa según un trigger programado (`scheduleTrigger`).
- Extrae datos desde Google Sheets (`googleSheets`) en lotes (`splitInBatches`).
- Utiliza modelos de lenguaje (`lmChatGoogleGemini`, `chainLlm`) para analizar y generar insights sobre precios.
- Emplea nodos condicionales (`if`) para filtrar alertas relevantes.
- Envía notificaciones automáticamente a Slack.
- Gestiona tiempos de espera (`wait`) para controlar el flujo y la frecuencia de requests.
- Procesa y formatea resultados usando nodos Markdown y parsers estructurados.
- Realiza solicitudes HTTP para interacciones adicionales o consultas externas.

Total de nodos utilizados: 42

## Ejemplos de uso
- Monitoreo diario automatizado de cambios en precios de productos clave.
- Generación automática de reportes con análisis de tendencias para el equipo de ecommerce.
- Alertas inmediatas vía Slack ante variaciones significativas en precios de competidores.

---

**Etiquetas:** Averis, Ecommerce, Investigación  
**Categoría:** agentes-ia/ecommerce
```