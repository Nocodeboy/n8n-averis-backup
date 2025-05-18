```markdown
# My workflow 4

## Descripción
Workflow diseñado para integrar agentes inteligentes utilizando nodos de LangChain y herramientas variadas, incluyendo Gmail y HTTP requests, permitiendo automatizar tareas complejas con lógica condicional y ejecución de sub-workflows.

## Requisitos
- Credenciales de OpenAI para uso de nodos `openAi` y `lmChatOpenAi`.
- Credenciales de Gmail configuradas para nodos `gmail` y `gmailTool`.
- Acceso a n8n con permisos para ejecutar workflows y triggers.
- APIs externas utilizadas deben estar disponibles y sus endpoints correctamente configurados.

## Instrucciones de configuración
1. Configura tus credenciales de OpenAI en n8n.
2. Configura tus credenciales de Gmail en n8n.
3. Ajusta los parámetros de los nodos `httpRequest` conforme a tus APIs destino.
4. Revisa y personaliza el nodo `formTrigger` para iniciar el workflow con los datos requeridos.
5. Importa el workflow en tu instancia de n8n y activa los triggers necesarios.

## Detalles de funcionamiento
- El workflow inicia con un trigger de formulario (`formTrigger`).
- Se usan nodos de LangChain para ejecutar consultas y gestionar agentes de IA.
- Nodos de decisión (`if`) permiten lógica condicional basada en resultados.
- Se integran herramientas externas como Gmail para enviar y procesar correos.
- Sub-workflows se ejecutan mediante `toolWorkflow` y `executeWorkflowTrigger`.
- El nodo `httpRequest` permite conexión con APIs externas para ampliar funcionalidades.

## Ejemplos de uso
- Automatizar respuestas inteligentes a correos electrónicos.
- Procesar solicitudes recibidas vía formulario con soporte de IA.
- Ejecutar flujos condicionales para tareas automatizadas integrando múltiples servicios.
- Orquestar agentes IA en distintos escenarios mediante nodos LangChain y herramientas nativas.

---
**Número de nodos:** 11  
**Categoría:** agentes-ia/otros  
**Etiquetas:** (ninguna asignada)
```