```markdown
# Entrega de Leadmagnets

## Descripción
Workflow automatizado para la entrega efectiva de leadmagnets a potenciales clientes, integrando múltiples canales de comunicación y validaciones para optimizar la generación y seguimiento de leads.

## Requisitos
- Credenciales de Google Sheets para acceso y manipulación de hojas de cálculo.
- Configuración de servicios de email (SMTP o Gmail API).
- Token y configuraciones para Slack y Telegram.
- Credenciales de Gmail configuradas en n8n.
- API key de OpenAI para procesamiento de contenido.
- Configuración de Webhooks pública para recepción de datos externos.

## Instrucciones de configuración
1. Importar el workflow en tu instancia de n8n.
2. Configurar las credenciales en n8n:
   - Google Sheets
   - Email (Gmail o SMTP)
   - Slack y Telegram
   - OpenAI API
3. Establecer URLs públicas para los nodos Webhook y RespondToWebhook.
4. Personalizar las hojas de Google Sheets utilizadas para almacenar y buscar leads.
5. Ajustar los mensajes y contenido en nodos de email, Slack y Telegram según tu leadmagnet y marca.

## Detalles de funcionamiento
- El workflow recibe datos de leads mediante Webhooks.
- Valida y filtra información con nodos IF y Función.
- Registra y consulta datos en Google Sheets.
- Envía el material del leadmagnet vía email, Slack o Telegram según configuración.
- Integra OpenAI para generar contenido dinámico o respuestas personalizadas.
- Utiliza nodos Wait para controlar tiempos de entrega y seguimiento.
- Registra actividad mediante nodos Sticky Note y Set para trazabilidad.

## Ejemplos de uso
- Captura un lead desde un formulario web conectado a un Webhook.
- Envío automático del recurso digital (PDF, eBook, etc.) al email del lead.
- Notificación en Slack y Telegram para el equipo de ventas cuando se entrega el leadmagnet.
- Generación dinámica de mensajes personalizados usando OpenAI antes del envío.

---

**Número de nodos:** 30  
**Categoría:** ventas/lead-generation  
**Tipos de nodos usados:** googleSheets, emailSend, if, function, slack, telegram, gmail, stickyNote, set, openAi, respondToWebhook, wait, webhook
```