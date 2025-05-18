```markdown
# 2. Tool Seguimientos - Agente IA WhatsApp Denipharma v2

## Descripción
Workflow diseñado para gestionar seguimientos mediante un agente de inteligencia artificial integrado con WhatsApp, optimizando la comunicación y el soporte a clientes de Denipharma.

## Requisitos
- Credenciales de OpenAI (para el nodo `lmChatOpenAi`)
- Acceso a Airtable con API Key y base configurada (para el nodo `airtableTool`)
- Cuenta y configuración de n8n con permisos para ejecutar workflows y agentes LangChain
- Integración habilitada con WhatsApp (externa al workflow, vía API o plataforma que utilice el agente)

## Instrucciones de configuración
1. Configure las credenciales de OpenAI en n8n para el nodo `lmChatOpenAi`.
2. Añada las credenciales de Airtable con acceso a la base y tabla necesarias para almacenar y consultar los seguimientos.
3. Personalice los nodos `set` y `executeWorkflowTrigger` según los disparadores específicos de su entorno.
4. Revise y ajuste los parámetros del agente LangChain (`agent`), asegurando que las configuraciones de contexto y conversación sean adecuadas a los requerimientos de Denipharma.
5. Enlace el workflow al canal WhatsApp a través del mecanismo de integración seleccionado.

## Detalles de funcionamiento
Este workflow consta de 6 nodos que combinan capacidades de IA conversacional y gestión de datos en Airtable para automatizar seguimientos:
- `lmChatOpenAi`: genera respuestas inteligentes basadas en solicitudes recibidas.
- `airtableTool`: consulta y actualiza registros de seguimientos.
- `set`: estructura y prepara datos para los siguientes pasos.
- `executeWorkflowTrigger`: activa flujos secundarios o adicionales según condiciones.
- `agent` (LangChain): orquesta la conversación y lógica del agente IA.
El flujo garantiza un manejo eficiente y contextualizado de las interacciones WhatsApp con clientes.

## Ejemplos de uso
- Automatizar respuestas y actualización de estado sobre pedidos o consultas en WhatsApp.
- Seguimiento proactivo de clientes que requieren soporte o información complementaria.
- Registro automático de interacciones en Airtable para análisis y reporte.
```