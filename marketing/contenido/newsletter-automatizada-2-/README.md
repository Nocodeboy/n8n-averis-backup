```markdown
# Newsletter Automatizada 2

## Descripción
Workflow automatizado para generar y enviar newsletters personalizadas utilizando diversas herramientas de IA y servicios de correo electrónico. Ideal para marketing de contenido, facilita la creación, agregación y distribución eficiente de boletines informativos.

## Requisitos
- Credenciales de OpenAI (para nodos `@n8n/n8n-nodes-langchain.openAi` y `lmChatOpenAi`)
- Credenciales de Anthropic (para nodo `lmChatAnthropic`)
- Cuenta de Gmail con acceso OAuth o credenciales SMTP (para nodo `gmail`)
- Acceso y permisos para ejecutar workflows en n8n
- Configuración de webhooks para el nodo `formTrigger`

## Instrucciones de configuración
1. Configure las credenciales de OpenAI y Anthropic en n8n.
2. Autentique y conecte su cuenta de Gmail en n8n.
3. Ajuste el nodo `formTrigger` para recibir entradas externas que activarán el workflow.
4. Revise los nodos `httpRequest`, `executeWorkflowTrigger` y `toolWorkflow` para ajustar llamadas a APIs y sub-workflows según sus necesidades.
5. Personalice el contenido y el diseño de la newsletter mediante los nodos de Chat y agregación.

## Detalles de funcionamiento
- El workflow inicia con un formulario o disparador externo (`formTrigger`).
- Utiliza modelos de lenguaje de OpenAI y Anthropic para generar contenido relevante y personalizado.
- Agrega y fusiona distintos fragmentos de contenido (`aggregate`, `merge`).
- Emplea nodos especializados (`agent`, `toolWorkflow`) para tareas específicas o sub-workflows.
- Realiza llamadas HTTP externas para obtener datos adicionales o integrarse con otras plataformas.
- Finalmente, envía la newsletter por correo electrónico a través del nodo `gmail`.

## Ejemplos de uso
- Enviar boletines semanales con resúmenes personalizados a suscriptores.
- Automatizar campañas de marketing de contenido con actualizaciones generadas por IA.
- Integrar feedback y datos externos para newsletters dinámicas y segmentadas.

---

**Número de nodos:** 20  
**Categoría:** marketing/contenido  
**Etiquetas:** _(ninguna)_  
**Nodos principales:**  
`@n8n/n8n-nodes-langchain.openAi`, `@n8n/n8n-nodes-langchain.lmChatOpenAi`, `n8n-nodes-base.aggregate`, `n8n-nodes-base.merge`, `n8n-nodes-base.formTrigger`, `@n8n/n8n-nodes-langchain.lmChatAnthropic`, `@n8n/n8n-nodes-langchain.toolWorkflow`, `n8n-nodes-base.gmail`, `@n8n/n8n-nodes-langchain.agent`, `n8n-nodes-base.executeWorkflowTrigger`, `n8n-nodes-base.set`, `n8n-nodes-base.stickyNote`, `n8n-nodes-base.splitOut`, `n8n-nodes-base.httpRequest`
```