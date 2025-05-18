```markdown
# 2. Agente de Presupuestos - Subworkflow - byAveris

## Descripción
Workflow orientado a la gestión y automatización de presupuestos dentro del proceso de ventas y cotizaciones. Este subworkflow utiliza inteligencia artificial y herramientas de cálculo para generar y validar presupuestos de forma eficiente.

## Requisitos
- Credenciales de OpenAI configuradas para el nodo `@n8n/n8n-nodes-langchain.lmChatOpenAi`.
- Acceso a la base de datos PostgreSQL para el nodo `n8n-nodes-base.postgresTool`.
- Permisos para ejecutar workflows en n8n (`n8n-nodes-base.executeWorkflowTrigger`).
- APIs y configuraciones necesarias para los nodos `@n8n/n8n-nodes-langchain.agent` y `@n8n/n8n-nodes-langchain.toolCalculator`.

## Instrucciones de configuración
1. Configure las credenciales de OpenAI en n8n.
2. Establezca la conexión a la base de datos PostgreSQL con las credenciales adecuadas.
3. Importe o integre este subworkflow en su flujo principal de ventas/cotizaciones.
4. Configure los permisos y triggers necesarios para la ejecución automática.
5. Revise y adapte las herramientas y agentes según la lógica de negocio específica.

## Detalles de funcionamiento
- El nodo `lmChatOpenAi` procesa consultas y genera respuestas inteligentes para la interacción.
- `toolCalculator` realiza cálculos precisos de los presupuestos basados en entradas dinámicas.
- `postgresTool` permite la consulta y actualización de datos relacionados con presupuestos en la base de datos.
- El agente (`agent`) coordina la lógica, resolviendo tareas y tomando decisiones automáticas.
- El nodo `executeWorkflowTrigger` maneja la ejecución del subworkflow dentro del contexto del flujo principal.

## Ejemplos de uso
- Generación automática de cotizaciones detalladas a partir de solicitudes de clientes.
- Actualización y validación de presupuestos con cálculos precisos e integración directa a la base de datos.
- Uso como subworkflow para dar soporte a workflows mayores del área de ventas y cotizaciones en n8n.

---

**Categoría:** ventas/cotizaciones  
**Etiquetas:** Averis, *****, Cotizaciones  
**Número de nodos:** 5  
**Nodos utilizados:**  
- `@n8n/n8n-nodes-langchain.lmChatOpenAi`  
- `@n8n/n8n-nodes-langchain.toolCalculator`  
- `n8n-nodes-base.postgresTool`  
- `@n8n/n8n-nodes-langchain.agent`  
- `n8n-nodes-base.executeWorkflowTrigger`  
```