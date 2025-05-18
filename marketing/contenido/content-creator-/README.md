```markdown
# Content creator

## Descripción
Workflow orientado a la creación automatizada de contenido para marketing, utilizando capacidades de lenguaje natural y agentes inteligentes para generar textos optimizados y relevantes.

## Requisitos
- Credenciales de OpenAI o proveedor compatible para `@n8n/n8n-nodes-langchain.lmChatOpenRouter`.
- Configuración del agente en `@n8n/n8n-nodes-langchain.agent`.
- Acceso a APIs externas si se usan herramientas HTTP (`@n8n/n8n-nodes-langchain.toolHttpRequest`).

## Instrucciones de configuración
1. Añadir las credenciales de OpenAI o el servicio LM en n8n.
2. Configurar el nodo `lmChatOpenRouter` con el modelo y parámetros adecuados.
3. Definir las herramientas y agentes en el nodo `agent`.
4. Ajustar la configuración del nodo `toolHttpRequest` para llamadas HTTP externas si aplica.
5. Validar los nodos `set` y `executeWorkflowTrigger` según el flujo deseado.

## Detalles de funcionamiento
El workflow consta de 6 nodos que integran generación de texto, ejecución de agentes inteligentes y llamadas HTTP para ampliar datos o contenido. Los nodos:
- `lmChatOpenRouter`: maneja la comunicación con el modelo de lenguaje.
- `agent`: coordina la lógica de generación y toma de decisiones.
- `toolHttpRequest`: realiza peticiones para obtener o enviar información adicional.
- `set`: configura variables y datos necesarios.
- `executeWorkflowTrigger`: inicia o conecta otros flujos complementarios.

## Ejemplos de uso
- Generar descripciones de productos automáticamente.
- Crear borradores de posts para redes sociales.
- Automatizar respuestas creativas para campañas de marketing.
- Integrar contenido generado con fuentes externas mediante HTTP requests.
```