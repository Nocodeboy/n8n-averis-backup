```markdown
# T - Recordatorios automáticos para seguimientos con IA y humanos en Gmail

## Descripción

Workflow diseñado para automatizar recordatorios de seguimiento combinando inteligencia artificial y gestión humana, integrando Gmail y Google Calendar para maximizar la productividad en tareas de seguimiento.

## Requisitos

- Credenciales configuradas para:
  - Gmail
  - Google Calendar
- API Key de OpenAI para el nodo `@n8n/n8n-nodes-langchain.lmChatOpenAi`
- Acceso habilitado a las APIs necesarias en Google Cloud Console
- n8n instalado con soporte para nodos Langchain y nodos base utilizados

## Instrucciones de configuración

1. Configure sus credenciales de Gmail y Google Calendar dentro de n8n.
2. Añada su clave API de OpenAI en las credenciales correspondientes.
3. Importe el workflow en n8n.
4. Ajuste los parámetros del nodo `scheduleTrigger` para definir la frecuencia deseada de ejecución.
5. Personalice filtros y plantillas en los nodos según sus necesidades de seguimiento.
6. Verifique las configuraciones de nodos Langchain para adaptar la lógica IA a su contexto.

## Detalles de funcionamiento

- **Disparador:** `scheduleTrigger` inicia el flujo en intervalos definidos.
- **Procesamiento IA:** Utiliza `lmChatOpenAi` y `agent` para interpretar y generar recordatorios contextuales.
- **Filtrado:** `filter` y `removeDuplicates` aseguran que solo se gestionen tareas relevantes y únicas.
- **Gestión de tareas:** Gmail para envío y seguimiento de correos, Google Calendar para agendado de eventos.
- **Soporte visual y batch:** `stickyNote` para anotaciones, `splitInBatches` para manejar grandes volúmenes de datos.
- **Parseo estructurado:** `outputParserStructured` organiza la salida de la IA para facilitar acciones posteriores.

## Ejemplos de uso

- Enviar recordatorios personalizados a clientes tras reuniones.
- Agendar automáticamente eventos de seguimiento en Google Calendar.
- Filtrar y evitar duplicados en listas de tareas pendientes.
- Crear notas internas con puntos clave detectados por IA para mejorar la comunicación del equipo.
```
