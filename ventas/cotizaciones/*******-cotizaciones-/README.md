```markdown
# ******* Cotizaciones

## Descripción
Workflow diseñado para automatizar el proceso de cotizaciones en el área de ventas, integrando generación de contenido con IA, manejo de hojas de cálculo y envío de correos electrónicos.

## Requisitos
- Credenciales de OpenAI para el nodo `@n8n/n8n-nodes-langchain.lmChatOpenAi`
- Acceso a Google Sheets con permisos para el nodo `n8n-nodes-base.googleSheetsTool`
- Configuración del nodo `n8n-nodes-base.gmailTool` con cuenta Gmail válida
- Acceso y permisos para ejecutar workflows con `n8n-nodes-base.executeWorkflowTrigger`
- Configuración adecuada para `@n8n/n8n-nodes-langchain.toolWorkflow` y `@n8n/n8n-nodes-langchain.agent`

## Instrucciones de configuración
1. Configure las credenciales de OpenAI dentro de n8n.
2. Proporcione acceso a la hoja de cálculo de Google Sheets utilizada para almacenar o recuperar datos de cotizaciones.
3. Configure la cuenta Gmail en el nodo `gmailTool` para enviar correos.
4. Revise y ajuste los parámetros de cada nodo según el flujo y los datos específicos de su negocio.
5. Habilite el workflow para que se active mediante el nodo `executeWorkflowTrigger`.

## Detalles de funcionamiento
- El workflow inicia mediante un trigger que puede ser manual o automático.
- El nodo de IA (`lmChatOpenAi`) genera mensajes o respuestas personalizadas para las cotizaciones.
- Los datos se consultan o actualizan en Google Sheets para mantener registros actualizados.
- Se utilizan herramientas y agentes de LangChain para gestionar la lógica y operaciones complejas.
- Finalmente, las cotizaciones son enviadas por Gmail a los destinatarios correspondientes.

## Ejemplos de uso
- Envío automatizado de cotizaciones personalizadas a clientes tras solicitud.
- Actualización dinámica de registros y seguimiento en Google Sheets.
- Generación de respuestas inteligentes utilizando IA para consultas relacionadas con ventas.

---
**Categoría:** ventas/cotizaciones  
**Número de nodos:** 7  
**Etiquetas:** (ninguna)
```