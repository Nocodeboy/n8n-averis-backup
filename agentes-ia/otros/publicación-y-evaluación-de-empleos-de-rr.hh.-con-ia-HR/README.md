```markdown
# Publicación y evaluación de empleos de RR.HH. con IA

## Descripción

Workflow diseñado para automatizar la publicación y la evaluación de ofertas de empleo en el área de Recursos Humanos, utilizando agentes de IA para mejorar la selección y análisis de candidatos de forma eficiente y precisa.

## Requisitos

- Credenciales de OpenAI para los nodos `@n8n/n8n-nodes-langchain` (openAi, lmChatOpenAi, agent, outputParserStructured).
- Cuenta y acceso a Google Drive y Google Calendar con las APIs correspondientes habilitadas.
- Cuenta y acceso a Airtable con las credenciales adecuadas para gestión y almacenamiento de datos.
- Servidor o instancia donde correr n8n con permisos para enviar emails.
  
## Instrucciones de configuración

1. Configure las credenciales de OpenAI con su API key en n8n.
2. Añada las credenciales de Google Drive y Google Calendar.
3. Configure el acceso a Airtable con la API key y base para la gestión de datos.
4. Ajuste el nodo `formTrigger` para recibir datos de solicitudes de empleo.
5. Verifique que el nodo de envío de email esté correctamente configurado para notificaciones.

## Detalles de funcionamiento

- El workflow inicia con un formulario que captura las postulaciones de empleo.
- Utiliza agentes de IA de Langchain para analizar, evaluar y clasificar las aplicaciones recibidas.
- Archivos adjuntos son almacenados y procesados en Google Drive.
- La información relevante se sincroniza y actualiza en Airtable para su seguimiento.
- Dependiendo de las evaluaciones, se envían correos electrónicos automáticos de respuesta.
- Se crean eventos en Google Calendar para entrevistas o seguimiento.
- El uso de nodos condicionales (`if`) permite ramificar el flujo según los resultados del análisis.

## Ejemplos de uso

- Publicar automáticamente una nueva oferta de empleo y evaluar las respuestas recibidas.
- Analizar currículums y generar reportes de candidatos con insights generados por IA.
- Automatizar notificaciones por correo a candidatos preseleccionados o descartados.
- Sincronizar eventos de entrevistas directamente en el calendario del equipo de RR.HH.

---

**Categoría:** agentes-ia/otros  
**Etiquetas:** HR  
**Número de nodos:** 36
```