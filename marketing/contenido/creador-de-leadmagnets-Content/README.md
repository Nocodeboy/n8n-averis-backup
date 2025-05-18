```markdown
# Creador de leadmagnets

## Descripción
Workflow de n8n orientado a la generación automática de leadmagnets para estrategias de marketing de contenido. Utiliza nodos avanzados de LangChain y herramientas de automatización para crear, estructurar y almacenar contenido valioso que atrae y convierte leads.

## Requisitos
- Credenciales de n8n para acceso y ejecución del workflow.
- API Key para servicios de LLM (ej. Anthropic) configurada en los nodos `lmChatAnthropic` y `chainLlm`.
- Acceso a Airtable con API Key y la base y tabla configuradas para almacenar los leadmagnets generados.
- Configuración adecuada del webhook para disparar el workflow externamente (opcional).
- Permisos para realizar solicitudes HTTP (nodo `httpRequest`).

## Instrucciones de configuración
1. Importa el workflow en tu instancia de n8n.
2. Configura las credenciales de lenguaje natural en los nodos `chainLlm` y `lmChatAnthropic`.
3. Ajusta las variables y parámetros del nodo `set` según tus necesidades específicas de leadmagnets.
4. Define la tabla y base de Airtable en el nodo `airtable` para almacenamiento.
5. Configura el webhook (si se utiliza) para permitir ejecuciones remotas.
6. Revisa y adapta los nodos de parsing (`outputParserStructured`, `outputParserAutofixing`) para la correcta interpretación del output según el prompt.

## Detalles de funcionamiento
- El workflow se inicia mediante un disparador manual, webhook o trigger configurado.
- Se utilizan modelos de lenguaje de Anthropic para generar ideas y contenido de leadmagnets.
- El contenido generado pasa por nodos de parsing para asegurar estructura y corrección automática.
- Se emplean agentes y herramientas internas con LangChain para mejorar la coherencia y precisión del contenido.
- El contenido final se formatea en HTML para visualización o envío.
- Se almacena la información en Airtable para seguimiento y gestión.
- Optativamente, el workflow puede esperar o hacer solicitudes http adicionales según el proceso definido.

## Ejemplos de uso
- Crear un ebook descargable para captar emails en campañas de marketing.
- Generar checklist o plantillas personalizadas para atraer suscriptores.
- Producir resúmenes de contenido o guías rápidas automatizadas para distribución en redes sociales.
- Automatizar la producción y almacenamiento de recursos valiosos para leads en Airtable.

---
> **Número de nodos:** 18  
> **Categoría:** marketing/contenido  
> **Etiquetas:** Content  
> **Tipos de nodos utilizados:**  
> `@n8n/n8n-nodes-langchain.chainLlm`, `n8n-nodes-base.manualTrigger`, `n8n-nodes-base.html`, `@n8n/n8n-nodes-langchain.lmChatAnthropic`,  
> `@n8n/n8n-nodes-langchain.toolWorkflow`, `@n8n/n8n-nodes-langchain.agent`, `n8n-nodes-base.set`, `n8n-nodes-base.airtable`,  
> `@n8n/n8n-nodes-langchain.outputParserStructured`, `@n8n/n8n-nodes-langchain.outputParserAutofixing`, `n8n-nodes-base.httpRequest`, `n8n-nodes-base.wait`, `n8n-nodes-base.webhook`
```