```markdown
# Enviar propuesta Contrato

## Descripción
Workflow diseñado para automatizar el envío de propuestas de contrato dentro del área de ventas y cotizaciones, integrando generación de contenido con IA, manejo de documentos en Google Drive y Google Docs, y captura de información mediante formularios.

## Requisitos
- Credenciales de Google Drive con acceso a los documentos y carpetas necesarias.
- Credenciales de Google Docs para edición y creación de documentos.
- API key de OpenAI para los nodos de LangChain (openAi).
- Acceso a la API de Evolution a través del nodo `n8n-nodes-evolution-api.evolutionApi`.
- n8n instalado y configurado.

## Instrucciones de configuración
1. Configure las credenciales de Google Drive y Google Docs en n8n.
2. Agregue la API key de OpenAI en el nodo `@n8n/n8n-nodes-langchain.openAi`.
3. Configure el nodo `n8n-nodes-evolution-api.evolutionApi` con los datos de acceso a la API correspondiente.
4. Defina el formulario en el nodo `formTrigger` para capturar los datos necesarios para la propuesta.
5. Ajuste carpetas y permisos en Google Drive para almacenamiento y extracción de archivos.

## Detalles de funcionamiento
- El workflow inicia con la captura de datos mediante un formulario (`formTrigger`).
- Utiliza OpenAI para generar contenido personalizado para la propuesta contractual.
- Extrae información de archivos almacenados en Google Drive para enriquecer la propuesta.
- Combina y genera documentos formateados en Google Docs.
- Usa notas adhesivas (`stickyNote`) para anotaciones rápidas o seguimiento interno.
- Interactúa con la API Evolution para obtener o validar información complementaria.
- Finalmente, envía o almacena la propuesta de contrato generada para su revisión y envío.

El flujo está compuesto por 13 nodos que trabajan coordinadamente para asegurar un proceso eficiente y automatizado.

## Ejemplos de uso
- Envío automático de propuestas a clientes tras completar un formulario web.
- Creación dinámica de contratos personalizados según los datos ingresados.
- Integración con otras herramientas de ventas para seguimiento y gestión.
```