```markdown
# Confirmar solicitudes de citas y crear eventos en Google Calendar

## Descripción
Workflow diseñado para gestionar la confirmación automática de solicitudes de citas y la creación de eventos en Google Calendar, optimizando la productividad y la organización de la agenda.

## Requisitos
- Cuenta y credenciales configuradas para:
  - Google Calendar API
  - Gmail API
- Acceso configurado a n8n con nodos:
  - `@n8n/n8n-nodes-langchain` (lmChatOpenAi, chainLlm, textClassifier)
  - `n8n-nodes-base` (form, if, formTrigger, executeWorkflow, gmail, stickyNote, set, executeWorkflowTrigger, googleCalendar)
- API Key para OpenAI (u otro proveedor compatible con Langchain)

## Instrucciones de configuración
1. Importar el workflow en n8n.
2. Configurar las credenciales de Google Calendar y Gmail en n8n.
3. Añadir y validar la API Key para OpenAI en los nodos de Langchain.
4. Personalizar el formulario para la recepción de solicitudes según necesidades.
5. Ajustar condiciones en nodos `if` para adaptarlas a las reglas de confirmación.
6. Activar el workflow.

## Detalles de funcionamiento
- El workflow inicia con un formulario que recibe solicitudes de citas.
- Un modelo de lenguaje natural (OpenAI via Langchain) clasifica y procesa la información recibida.
- Mediante nodos condicionales se determina la viabilidad y tipo de confirmación.
- Se envían correos electrónicos automáticos de confirmación usando Gmail.
- Los eventos confirmados se crean directamente en Google Calendar.
- Se utilizan notas adhesivas (`stickyNote`) y ajustes (`set`) para gestión interna y customizaciones.
- El workflow está compuesto por 25 nodos interconectados cuidadosamente para asegurar flujo eficiente y robusto.

## Ejemplos de uso
- Recepción y confirmación automática de citas médicas, generando eventos de paciente en calendario.
- Organización de entrevistas laborales con confirmación via correo y agenda centralizada.
- Gestión de reservas y confirmaciones en centros educativos o consultorios.

---

*Categoría: productividad/agenda*  
*Número de nodos: 25*  
*Etiquetas: -*
```