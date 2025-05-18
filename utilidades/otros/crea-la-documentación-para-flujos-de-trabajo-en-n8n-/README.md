```markdown
# Crea la documentación para flujos de trabajo en n8n

## Descripción

Workflow diseñado para automatizar la creación y mantenimiento de documentación para flujos de trabajo en n8n, facilitando la generación estructurada y actualizada de información relevante sobre cada flujo.

## Requisitos

- n8n instalado y configurado.
- Credenciales para OpenAI (usadas por nodos `@n8n/n8n-nodes-langchain.lmChatOpenAi`).
- Permisos para crear y gestionar archivos en el sistema (para los nodos `n8n-nodes-base.readWriteFile`, `convertToFile` y `extractFromFile`).
- Acceso a webhook público o configuración local según entorno (para `n8n-nodes-base.webhook` y `respondToWebhook`).

## Instrucciones de configuración

1. Configure las credenciales de OpenAI en n8n.
2. Ajuste las URLs o endpoints de webhook según su entorno.
3. Revise y adapte las rutas de archivo para lectura/escritura según su sistema.
4. Verifique que los nodos `switch`, `if` y `merge` estén configurados conforme a sus condiciones específicas.
5. Asegúrese de tener acceso a ejecutar comandos del sistema (nodo `executeCommand`) si aplica.

## Detalles de funcionamiento

- El flujo utiliza 60 nodos, integrando desde procesamiento de lenguaje natural hasta manipulación avanzada de archivos.
- Nodos clave incluyen:
  - `lmChatOpenAi` para generación de texto automatizado.
  - `outputParserStructured` y `outputParserAutofixing` para validar y corregir la salida.
  - Múltiples nodos base para control de flujo (`switch`, `if`, `merge`), manipulación de archivos, y ejecución de comandos.
- Webhooks gestionan la entrada y respuesta externa, facilitando integración con otras aplicaciones o servicios.
- El flujo produce documentación estructurada, que puede ser exportada, almacenada o utilizada para actualizar flujos en tiempo real.

## Ejemplos de uso

- Generar documentación automática luego de modificar o crear un flujo en n8n.
- Actualizar documentación existente al detectar cambios en elementos del flujo.
- Integrar con un sistema externo para mostrar documentación actualizada a usuarios sin acceso directo a n8n.
- Automatizar revisiones y correcciones en la documentación con soporte de IA.

---

Este workflow ofrece una solución completa para mantener la documentación de flujos n8n organizada, precisa y actualizada con mínima intervención manual.
```