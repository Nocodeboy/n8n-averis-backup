```markdown
# Creación de Mockups a partir de foto

## Descripción
Workflow de n8n que permite generar mockups a partir de una foto enviada por el usuario. Utiliza integración con Google Sheets para manejar datos, toma decisiones con nodos condicionales, procesa la información mediante código y responde vía Telegram, facilitando la automatización en la creación de mockups personalizados.

## Requisitos
- Cuenta y credenciales de Google Sheets con acceso a la hoja configurada.
- Token de bot de Telegram.
- URL o API para generación de mockups (usada en nodo HTTP Request).
- Acceso y permisos para ejecutar workflows en n8n.

## Instrucciones de configuración
1. Importar el workflow en n8n.
2. Configurar credenciales de Google Sheets (asegurar acceso a la hoja utilizada).
3. Configurar el nodo `Telegram` con el token del bot y chat ID correspondiente.
4. Ajustar el nodo `HTTP Request` con la URL y parámetros adecuados para la generación de mockups.
5. Revisar y adaptar el código del nodo `Code` si es necesario para el procesamiento de datos.
6. Publicar o habilitar el workflow para su ejecución mediante formulario (formTrigger).

## Detalles de funcionamiento
- El flujo inicia con un formulario que recibe la foto.
- Se registran y consultan datos en Google Sheets.
- Mediante nodos de condición se controla el flujo según la información recibida.
- En lotes, se procesan las solicitudes para optimizar rendimiento.
- Se realiza una petición HTTP para generar el mockup a partir de la foto.
- Finalmente, el resultado o notificación se envía al usuario vía Telegram.

## Ejemplos de uso
- Un diseñador recibe una foto de un producto y obtiene automáticamente un mockup para presentación.
- Equipo de marketing envía imágenes y recibe mockups listos para campañas.
- Automatización de generación de muestras visuales sin intervención manual.

---

**Categoría:** agentes-ia/otros  
**Nodos utilizados:** Google Sheets, IF, Form Trigger, Code, Telegram, Split In Batches, HTTP Request  
**Número de nodos:** 9
```