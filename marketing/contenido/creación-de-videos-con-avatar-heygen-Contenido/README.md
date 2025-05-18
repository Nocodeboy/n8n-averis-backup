```markdown
# Creación de videos con Avatar Heygen

## Descripción
Workflow automatizado para la creación de videos utilizando Avatares de Heygen, enfocado en la generación de contenido de marketing. Combina procesamiento de lenguaje natural, APIs y herramientas de automatización para producir videos atractivos y personalizados.

## Requisitos
- Cuenta y credenciales API de Heygen para generación de avatares y videos.
- API Key de OpenAI para los nodos `@n8n/n8n-nodes-langchain.openAi` y `@n8n/n8n-nodes-langchain.lmChatOpenAi`.
- Acceso a Internet para nodos HTTP Request y APIs externas.
- n8n instalado y configurado con acceso para ejecutar workflows con al menos 29 nodos.

## Instrucciones de configuración
1. Configure las credenciales de OpenAI en n8n (`OpenAI API Key`).
2. Añada las credenciales necesarias para la API de Heygen en el nodo HTTP Request o credenciales personalizadas.
3. Ajuste los parámetros en nodos de lenguaje y agentes para definir el tono y contenido del video.
4. Establezca el trigger según su necesidad (horarios, eventos externos, etc.) utilizando el nodo `scheduleTrigger`.
5. Revise y personalice cualquier texto o meta información dentro de los nodos tipo `set` y `stickyNote`.

## Detalles de funcionamiento
- El workflow inicia mediante un trigger programado.
- Utiliza nodos de OpenAI para generación y refinamiento de guiones.
- El agente Langchain procesa instrucciones y coordina tareas complejas.
- Solicitudes a Heygen para crear y obtener videos con avatares personalizados vía nodos HTTP Request.
- Incluye nodos de espera y control para sincronizar procesos.
- Herramientas adicionales como hackerNewsTool se usan para inspiración y contenido contextual.

## Ejemplos de uso
- Generar un video de marketing diario con un avatar presentando nuevas promociones.
- Automatizar contenido semanal para redes sociales utilizando guiones creados por IA.
- Crear mensajes personalizados para campañas con avatares reales y textos adaptados en tiempo real.

---

**Categoría:** marketing/contenido  
**Etiquetas:** Contenido, Avatar  
**Número de nodos:** 29  
**Nodos principales:**  
`@n8n/n8n-nodes-langchain.openAi`, `@n8n/n8n-nodes-langchain.lmChatOpenAi`, `n8n-nodes-base.hackerNewsTool`, `n8n-nodes-base.scheduleTrigger`, `@n8n/n8n-nodes-langchain.agent`, `n8n-nodes-base.set`, `n8n-nodes-base.stickyNote`, `n8n-nodes-base.httpRequest`, `n8n-nodes-base.wait`
```