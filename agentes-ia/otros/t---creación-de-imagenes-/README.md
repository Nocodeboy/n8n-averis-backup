```markdown
# T - Creación de imagenes

## Descripción
Workflow de n8n para la generación automatizada de imágenes utilizando agentes IA y diversas integraciones, facilitando la creación, gestión y envío de imágenes mediante triggers manuales y formularios.

## Requisitos
- Credenciales de LinkedIn para el nodo `linkedIn`
- Clave API y acceso configurado para OpenRouter (usada por `lmChatOpenRouter`)
- Cuenta Gmail configurada para envío de correos (`gmail`)
- Acceso a APIs HTTP externas si aplica (`httpRequest`, `toolHttpRequest`)
- Permisos adecuados para ejecución manual o vía formulario (`manualTrigger`, `formTrigger`)

## Instrucciones de configuración
1. Importar el workflow en n8n.
2. Configurar las credenciales:
   - Añadir credenciales de LinkedIn en n8n.
   - Configurar la conexión con OpenRouter para el nodo de lenguaje.
   - Vincular cuenta Gmail para el envío de correos.
3. Ajustar parámetros de triggers según necesidades (manual o formulario).
4. Revisar y actualizar endpoints HTTP o herramientas externas si es necesario.
5. Guardar los cambios y activar el workflow.

## Detalles de funcionamiento
- El workflow inicia con triggers manuales o formulario para recibir solicitudes.
- Usa agentes de lenguaje IA (`lmChatOpenRouter`, `agent`) para procesar prompts y generar descripciones o parámetros para la creación de imágenes.
- Realiza llamadas HTTP a APIs externas para generar o manipular imágenes (`httpRequest`, `toolHttpRequest`).
- Convierte resultados a archivos (`convertToFile`) para su posterior uso o envío.
- Envía las imágenes generadas y/o información relacionada vía Gmail.
- Incluye nodos de notas adhesivas para documentación interna y seguimiento.
- Integra LinkedIn para posibles publicaciones o interacciones automáticas.

## Ejemplos de uso
- Generar imágenes a partir de texto proporcionado en un formulario, enviándolas automáticamente por correo.
- Automatizar publicaciones visuales en LinkedIn con imágenes creadas dinámicamente.
- Realizar pruebas manuales de creación de imágenes desde el panel de n8n para evaluación rápida.
- Utilizar el agente IA para describir imágenes y adjuntar notas de contexto internas.

---

_Número de nodos utilizados: 22  
Categoría: agentes-ia/otros_
```