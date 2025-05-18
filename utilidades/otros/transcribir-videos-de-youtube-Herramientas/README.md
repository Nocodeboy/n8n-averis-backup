```markdown
# Transcribir videos de Youtube

## Descripción
Workflow para transcribir automáticamente videos de Youtube mediante la extracción de audio y la generación de texto. Ideal para obtener transcripciones rápidas y precisas sin salir de n8n.

## Requisitos
- Credenciales de Google Docs para crear y editar documentos.
- Acceso a la API de Youtube (opcional, según el método de obtención del video).
- n8n con nodos: formTrigger, function, code, set, googleDocs, httpRequest.

## Instrucciones de configuración
1. Configure la credencial de Google Docs en n8n para permitir la creación y edición de documentos.
2. Si utilizas la API de Youtube, añade y configura las credenciales correspondientes en n8n.
3. Ajusta el nodo `formTrigger` para capturar la URL o ID del video que deseas transcribir.
4. Verifica que todos los nodos estén correctamente vinculados y configurados para procesar el flujo.

## Detalles de funcionamiento
- El workflow inicia con un formulario que recibe el enlace del video de Youtube.
- A través de nodos de función y código, se procesa el enlace para extraer el audio o datos necesarios.
- Se realiza una solicitud HTTP para obtener o enviar el audio a un servicio de transcripción.
- La transcripción recibida se formatea y guarda en un documento de Google Docs.
- Se utiliza el nodo `set` para manejar los datos y preparar la salida final.

## Ejemplos de uso
- Obtener la transcripción de una conferencia o charla disponible en Youtube.
- Generar subtítulos automáticos para videos propios.
- Crear resúmenes escritos de contenido audiovisual para consultas rápidas.

---

**Categoría:** utilidades/otros  
**Nodos utilizados:** formTrigger, function, code, set, googleDocs, httpRequest  
**Etiquetas:** Herramientas, Youtube  
**Número de nodos:** 7
```