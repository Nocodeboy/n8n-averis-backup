```markdown
# Main agent

## Descripción
Workflow de n8n que implementa un agente inteligente combinando herramientas de cálculo, manejo de flujos, memoria contextual y comunicación con APIs externas, para automatizar tareas complejas usando nodos LangChain y nodos base de n8n.

## Requisitos
- Credenciales para OpenAI (configurar en el nodo `lmChatOpenAi`).
- Acceso habilitado para llamadas HTTP externas (para el nodo `toolHttpRequest`).
- Permisos para ejecutar workflows y manejar webhooks en n8n.
  
## Instrucciones de configuración
1. Importa el workflow `Main agent` en tu instancia de n8n.
2. Configura las credenciales de OpenAI en el nodo `lmChatOpenAi`.
3. Ajusta la URL y parámetros en el nodo `toolHttpRequest` según tus necesidades.
4. Verifica que los webhooks (`webhook` y `respondToWebhook`) estén habilitados y accesibles.
5. Revisa los ajustes de la memoria en `memoryBufferWindow` para definir el tamaño del contexto.
6. Guarda y activa el workflow.

## Detalles de funcionamiento
El workflow utiliza 11 nodos combinados para crear un agente IA con las siguientes funcionalidades:

- **Agente LangChain (`agent`)**: Coordina la lógica principal del agente usando las herramientas disponibles.
- **Cálculo (`toolCalculator`)**: Ejecuta operaciones matemáticas cuando se requieren.
- **Memoria contextual (`memoryBufferWindow`)**: Mantiene el contexto reciente para mejorar la continuidad en las interacciones.
- **Gestión de flujo (`toolWorkflow`)**: Orquesta la llamada a sub-workflows o tareas específicas.
- **Comunicación OpenAI (`lmChatOpenAi`)**: Provee capacidades de lenguaje natural a través de modelos de OpenAI.
- **Peticiones HTTP (`toolHttpRequest`)**: Permite consultas a APIs externas.
- **Webhooks (`webhook`, `respondToWebhook`)**: Facilitan la interacción con sistemas externos vía HTTP.

## Ejemplos de uso
- Automatización de consultas complejas que requieren cálculos y acceso a APIs.
- Asistentes virtuales que mantienen contexto en conversaciones prolongadas.
- Integración de diversas herramientas en un flujo único y coordinado.
- Despliegue rápido de agentes personalizados para tareas específicas mediante sub-workflows.

---
Categoría: agentes-ia/otros  
Nodos utilizados: @n8n/n8n-nodes-langchain.toolCalculator, @n8n/n8n-nodes-langchain.lmChatOpenAi, @n8n/n8n-nodes-langchain.memoryBufferWindow, @n8n/n8n-nodes-langchain.toolWorkflow, @n8n/n8n-nodes-langchain.agent, @n8n/n8n-nodes-langchain.toolHttpRequest, n8n-nodes-base.respondToWebhook, n8n-nodes-base.webhook  
Número de nodos: 11
```