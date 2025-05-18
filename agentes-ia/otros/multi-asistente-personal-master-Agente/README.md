```markdown
# Multi Asistente Personal Master

## Descripción
Workflow avanzado que permite la gestión y coordinación de múltiples asistentes personales basados en inteligencia artificial. Utiliza agentes IA para ejecutar tareas variadas mediante cálculo, consultas HTTP, manejo de memoria y ejecución de sub-workflows.

## Requisitos
- Credenciales válidas para OpenAI (API key) para el nodo `lmChatOpenAi`.
- Acceso a n8n con los nodos de LangChain instalados:
  - `@n8n/n8n-nodes-langchain.lmChatOpenAi`
  - `@n8n/n8n-nodes-langchain.toolCalculator`
  - `@n8n/n8n-nodes-langchain.memoryBufferWindow`
  - `@n8n/n8n-nodes-langchain.toolWorkflow`
  - `@n8n/n8n-nodes-langchain.agent`
  - `@n8n/n8n-nodes-langchain.toolHttpRequest`
  - `n8n-nodes-base.executeWorkflowTrigger`

## Instrucciones de configuración
1. Importar el workflow en n8n.
2. Configurar la credencial de OpenAI en el nodo `lmChatOpenAi`.
3. Ajustar URLs y parámetros en el nodo `toolHttpRequest` según sea necesario.
4. En nodos de ejecución de workflow (`toolWorkflow`, `executeWorkflowTrigger`), asignar los workflows target existentes.
5. Revisar y adaptar el buffer de memoria en `memoryBufferWindow` para el contexto deseado.

## Detalles de funcionamiento
- El workflow inicia con un disparador `executeWorkflowTrigger`.
- Utiliza el modelo OpenAI para interpretar y generar respuestas.
- Ejecuta cálculos personalizados mediante `toolCalculator`.
- Realiza llamadas HTTP para obtener datos externos con `toolHttpRequest`.
- Mantiene contexto y memoria de la conversación usando `memoryBufferWindow`.
- Coordina sub-workflows y agentes especializados para tareas específicas.
- La lógica de agente orquesta el flujo y la toma de decisiones.

## Ejemplos de uso
- Asistencia personalizada en múltiples dominios (finanzas, agenda, consultas web).
- Automatización de tareas complejas combinando IA y operaciones externas.
- Soporte interactivo con memoria contextual activa durante la sesión.

---

**Categoría**: agentes-ia/otros  
**Etiquetas**: Agente, Master  
**Número de nodos**: 10
```