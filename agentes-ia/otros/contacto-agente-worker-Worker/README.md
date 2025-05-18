```markdown
# Contacto Agente Worker

## Descripción
Workflow diseñado para gestionar interacciones automáticas mediante agentes IA, facilitando el contacto y seguimiento eficiente a través de integración con Airtable y modelos de lenguaje OpenAI.

## Requisitos
- Credenciales de OpenAI configuradas para el nodo `@n8n/n8n-nodes-langchain.lmChatOpenAi`
- API Key de Airtable para acceso de lectura/escritura en bases de datos (`n8n-nodes-base.airtableTool`)
- n8n instalado con los nodos:
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`
  - `@n8n/n8n-nodes-langchain.agent`
  - `n8n-nodes-base.set`
  - `n8n-nodes-base.executeWorkflowTrigger`
  - `n8n-nodes-base.airtableTool`

## Configuración
1. Importar el workflow en n8n.
2. Configurar las credenciales OpenAI en el nodo `lmChatOpenAi`.
3. Añadir las credenciales de Airtable en el nodo `airtableTool` con acceso a la base de datos correspondiente.
4. Ajustar parámetros específicos en los nodos según la lógica del agente y sus triggers.
5. Verificar que el nodo `executeWorkflowTrigger` esté habilitado para activar el flujo adecuadamente.

## Funcionamiento
El workflow consta de 7 nodos que trabajan en conjunto para:
- Recibir y procesar solicitudes mediante un agente IA.
- Ejecutar lógica personalizada con el nodo agent de LangChain.
- Almacenar y actualizar información de contacto en Airtable.
- Controlar el flujo mediante nodos de set y triggers internos para asegurar respuestas y acciones coordinadas.

## Ejemplos de uso
- Automatizar respuestas de contacto para soporte o consultas internas.
- Seguimiento y gestión de tareas asignadas a agentes en un entorno de trabajo colaborativo.
- Integración de modelos de lenguaje para enriquecer la interacción con datos almacenados en Airtable.

---

**Categoría:** agentes-ia/otros  
**Etiquetas:** Worker, Agente  
**Número de nodos:** 7
```