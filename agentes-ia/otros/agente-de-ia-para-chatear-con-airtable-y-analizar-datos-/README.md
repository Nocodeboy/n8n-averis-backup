```markdown
# Agente de IA para chatear con Airtable y analizar datos

## Descripción

Workflow diseñado para crear un agente de inteligencia artificial que interactúa mediante chat, accede y analiza datos almacenados en Airtable. Utiliza diversos nodos para orquestar consultas, procesamiento y respuestas inteligentes basadas en datos en tiempo real.

## Requisitos

- Cuenta y API Key de Airtable con permisos para acceder a las bases y tablas necesarias.
- API Key de OpenAI para el nodo `lmChatOpenAi` (modelo de lenguaje).
- Acceso a n8n con los nodos necesarios instalados, incluyendo los relacionados con Langchain.
- Credenciales configuradas dentro de n8n para Airtable y OpenAI.

## Instrucciones de configuración

1. **Configurar credenciales en n8n**  
   - Añadir credencial de Airtable con API Key y base ID correspondientes.  
   - Añadir credencial de OpenAI con la API Key válida.

2. **Importar el workflow en n8n**  
   - Subir el archivo JSON del workflow o crear uno nuevo con los nodos indicados.

3. **Ajustar parámetros**  
   - En el nodo Airtable, definir tabla y vistas según la base de datos utilizada.  
   - Configurar los prompts y parámetros de los nodos Langchain para adecuarse al análisis esperado.

4. **Activar el trigger de chat**  
   - Configurar el nodo `chatTrigger` para iniciar las conversaciones según corresponda.

## Detalles de funcionamiento

El workflow consta de 41 nodos y utiliza las siguientes funciones:

- **Entrada de conversación** por el nodo `chatTrigger` y `executeWorkflowTrigger`.  
- **Gestión de memoria y contexto** con `memoryBufferWindow` para mantener el hilo del diálogo.  
- **Consulta y análisis de datos** en Airtable a través del nodo `airtable`.  
- **Procesamiento y decisión** con nodos `switch`, `if` y `merge` para control de flujo.  
- **Interacción con modelo de lenguaje** usando `lmChatOpenAi` para generar respuestas inteligentes.  
- **Análisis avanzado y herramientas auxiliares** mediante nodos como `toolWorkflow` y `toolCode`.  
- **Organización visual** con `stickyNote` para documentación interna del workflow.  
- **Agente IA** implementado con el nodo `agent` que coordina la lógica del chat y acciones.

El conjunto permite que el agente interprete consultas en lenguaje natural, extraiga y analice datos desde Airtable y responda con información precisa o acciones automáticas.

## Ejemplos de uso

- **Consulta de inventario:**  
  Usuario pregunta:  
  > "¿Cuántos productos quedan en stock en la tabla de inventario?"  
  Respuesta generada con datos actualizados desde Airtable.

- **Análisis personalizado:**  
  Usuario consulta:  
  > "Muéstrame el resumen de ventas del último mes."  
  El agente accede, agrega datos con `aggregate`, y responde con un resumen.

- **Soporte interactivo:**  
  Integrado en un chat donde un operador puede solicitar insights al agente sobre bases de datos específicas en Airtable.

---

Este workflow permite integrar capacidades conversacionales con bases de datos de Airtable, facilitando análisis y consulta dinámica con soporte IA.  
```