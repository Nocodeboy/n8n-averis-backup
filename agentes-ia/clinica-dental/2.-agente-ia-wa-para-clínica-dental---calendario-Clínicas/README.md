```markdown
# 2. Agente IA WA para Clínica Dental - Calendario

## Descripción
Workflow diseñado para gestionar la interacción con pacientes mediante un agente IA en WhatsApp, integrando la gestión de citas en Google Calendar para clínicas dentales. Automatiza la consulta, creación y modificación de eventos en el calendario, optimizando la coordinación de citas.

## Requisitos
- Cuenta en n8n con acceso a los nodos de Langchain y Google Calendar.
- Credenciales configuradas para:
  - OpenAI (para el nodo `lmChatOpenAi`).
  - Google Calendar API (para el nodo `googleCalendarTool`).
- Acceso configurado al workflow para su ejecución desde WhatsApp (p.ej., mediante un trigger externo que active `executeWorkflowTrigger`).

## Instrucciones de configuración
1. Configure las credenciales de OpenAI en n8n.
2. Configure las credenciales de acceso a Google Calendar con permisos para lectura y escritura de eventos.
3. Importe este workflow en n8n y revise que los nodos tengan asociadas las credenciales correctas.
4. Adapte los parámetros del agente IA (`agent`) según el lenguaje y tono deseado para la clínica.
5. Conecte la entrada del workflow con el canal de WhatsApp o sistema de mensajería correspondiente para activar el agente.

## Detalles de funcionamiento
- **lmChatOpenAi**: Genera respuestas inteligentes basadas en la conversación con el paciente.
- **toolWorkflow**: Permite ejecutar sub-workflows complementarios para tareas específicas.
- **agent**: Gestiona la lógica del agente IA para interpretar y responder consultas.
- **executeWorkflowTrigger**: Dispara el workflow ante mensajes entrantes o eventos externos.
- **googleCalendarTool**: Consulta, crea y modifica eventos en el calendario de la clínica.

El flujo combina procesamiento de lenguaje natural con integración directa al calendario para ofrecer una experiencia fluida y automatizada.

## Ejemplos de uso
- Paciente solicita la disponibilidad para una limpieza dental y el agente responde con los horarios libres.
- Paciente envía una solicitud para cambiar la cita, el agente gestiona la modificación en Google Calendar.
- Consulta general sobre horarios de atención y servicios disponibles.

---

**Categoría:** agentes-ia/clinica-dental  
**Etiquetas:** Clínicas  
**Número de nodos:** 8
```