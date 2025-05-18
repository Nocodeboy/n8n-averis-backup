```markdown
# 4. Tool Seguimientos - Agente IA WhatsApp Denipharma v2

## Descripción

Workflow diseñado para gestionar seguimientos automáticos a través de un agente IA en WhatsApp, integrando capacidades de lenguaje natural, manejo de bases de datos en Airtable y ejecución coordinada de tareas.

## Requisitos

- Credenciales para OpenAI (para el nodo `lmChatOpenAi`)
- Acceso y API key de Airtable (para el nodo `airtableTool`)
- n8n configurado con permisos para ejecutar workflows internos
- Configuración del agente IA en nodos `agent` de Langchain

## Instrucciones de Configuración

1. **OpenAI**
   - Añadir la API key en las credenciales de n8n bajo `OpenAI`.
2. **Airtable**
   - Configurar la conexión con Airtable proporcionando Base ID, Tabla y API key.
3. **Workflow**
   - Revisar los nodos `set` y `executeWorkflowTrigger` para ajustar parámetros específicos según su entorno.
4. **Agente IA**
   - Verificar la configuración del nodo `agent` para asegurar la correcta integración del modelo y flujo conversacional.

## Detalles de Funcionamiento

- El workflow inicia mediante un trigger ejecutado internamente.
- Utiliza el modelo OpenAI para generar respuestas automatizadas en WhatsApp.
- Consulta y actualiza datos relevantes en Airtable para seguimiento personalizado.
- El nodo `set` se encarga de gestionar variables y datos temporales dentro del flujo.
- El agente IA coordina el diálogo y la lógica del seguimiento mediante Langchain.

## Ejemplos de Uso

- Seguimiento automático de casos pendientes con clientes a través de WhatsApp.
- Actualización y consulta dinámica de información almacenada en Airtable.
- Respuestas inteligentes y contextuales generadas por IA para consultas frecuentes.
- Ejecución programada o manual de seguimientos mediante triggers internos en n8n.

---

**Categoría:** agentes-ia/whatsapp  
**Etiquetas:** Agente, Worker  
**Número de nodos:** 6  
**Nodos utilizados:** `@n8n/n8n-nodes-langchain.lmChatOpenAi`, `n8n-nodes-base.airtableTool`, `n8n-nodes-base.set`, `n8n-nodes-base.executeWorkflowTrigger`, `@n8n/n8n-nodes-langchain.agent`
```