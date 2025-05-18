```markdown
# 4. Agente para Abogados - Agente de Calendario

## Descripción
Workflow diseñado para abogados que automatiza la gestión de agendas mediante un agente inteligente. Utiliza modelos de lenguaje y herramientas integradas para interactuar con calendarios de Microsoft Outlook y ejecutar tareas recomendadas.

## Requisitos
- Credenciales válidas de Microsoft Outlook (para acceso y gestión de calendario).
- API Key para OpenAI (utilizada por el nodo `@n8n/n8n-nodes-langchain.lmChatOpenAi`).
- Permisos adecuados para ejecutar workflows en n8n.

## Instrucciones de Configuración
1. Configurar la conexión de Microsoft Outlook en n8n con las credenciales correspondientes.
2. Añadir la API Key de OpenAI en las credenciales de `lmChatOpenAi`.
3. Importar el workflow en n8n.
4. Verificar que todos los nodos estén conectados y configurados correctamente.

## Detalles de Funcionamiento
- El workflow consta de 9 nodos, incluyendo nodos de tipo:
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi` para procesamiento de lenguaje natural.
  - `@n8n/n8n-nodes-langchain.agent` como agente inteligente que determina acciones.
  - `n8n-nodes-base.set` para manipulación de datos.
  - `n8n-nodes-base.executeWorkflowTrigger` para activación del flujo.
  - `n8n-nodes-base.microsoftOutlookTool` para gestión directa del calendario.
- Un agente IA interpreta solicitudes relacionadas con la agenda y ejecuta las acciones correspondientes en el calendario Outlook.

## Ejemplos de Uso
- Programar, modificar o consultar citas en el calendario de un abogado mediante comandos de lenguaje natural.
- Automatizar recordatorios y organización de eventos legales.
- Integrar solicitudes de clientes para agendar reuniones sin intervención manual.

---
Categoría: agentes-ia/otros  
Número de nodos: 9  
```