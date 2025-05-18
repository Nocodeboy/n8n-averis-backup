```markdown
# Averis - Fase Reunion Inicial - Preparación de llamadas

## Descripción
Workflow diseñado para optimizar la preparación de llamadas en la fase inicial de reuniones de Averis, automatizando la recopilación, análisis y gestión de información para una comunicación efectiva y organizada.

## Requisitos
- Credenciales de n8n para acceso y ejecución de workflows.
- API Key de OpenAI para nodos `lmChatOpenAi` y `chainLlm`.
- Cuenta y autorización de WhatsApp para envío y recepción de mensajes.
- Acceso a Gmail mediante credenciales OAuth para gestión de correos.
- Acceso a Google Calendar para sincronización de eventos.
- Permisos para realizar solicitudes HTTP externas (nodo `httpRequest`).

## Instrucciones de configuración
1. Configure las credenciales de OpenAI en n8n.
2. Establezca credenciales válidas para Gmail y Google Calendar.
3. Vincule la cuenta de WhatsApp en el nodo correspondiente.
4. Ajuste las variables y parámetros en nodos `set` para personalizar el flujo según necesidades.
5. Importe el workflow en su instancia de n8n y active los triggers de ejecución.

## Detalles de funcionamiento
- El workflow inicia con un trigger programado o manual para preparar las llamadas.
- Se utilizan nodos de agregación (`aggregate`) y extracción de información (`informationExtractor`) para procesar datos relevantes.
- Modelos de lenguaje OpenAI (`lmChatOpenAi`, `chainLlm`) generan resúmenes y respuestas inteligentes.
- Múltiples nodos condicionales (`switch`, `if`) dirigen el flujo según escenarios específicos.
- Comunicación por WhatsApp y Gmail garantiza la diseminación y seguimiento adecuados.
- La integración con Google Calendar ayuda a sincronizar las reuniones planificadas.
- Nodos auxiliares como `merge`, `splitOut`, y `stickyNote` organizan la información y los procesos.
- Estructura modular con nodos `executeWorkflow` para facilitar mantenimiento y escalabilidad.

## Ejemplos de uso
- Preparar automáticamente una lista de temas y objetivos antes de una reunión inicial.
- Enviar recordatorios personalizados por WhatsApp y correo electrónico a los participantes.
- Generar resúmenes automáticos de documentos y datos relevantes para la llamada.
- Actualizar agendas y notas en Google Calendar en función de los resultados de la reunión.

---

**Número total de nodos:** 61  
**Categoría:** productividad/reuniones
```