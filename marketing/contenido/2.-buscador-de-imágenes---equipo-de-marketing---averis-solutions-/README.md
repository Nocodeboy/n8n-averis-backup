```markdown
# 2. Buscador de Imágenes - Equipo de Marketing - Averis Solutions

## Descripción
Workflow diseñado para facilitar la búsqueda, organización y distribución de imágenes relevantes para el Equipo de Marketing de Averis Solutions, automatizando la interacción con Google Drive, Google Sheets y Telegram mediante inteligencia artificial.

## Requisitos
- Credenciales de Google Drive con permisos para acceso y búsqueda de archivos.
- Credenciales de Google Sheets para lectura y escritura de datos.
- Token API para el modelo de lenguaje OpenRouter (usado en nodos Langchain).
- Bot de Telegram con token para enviar notificaciones y resultados.
- n8n instalado con los siguientes nodos disponibles:
  - `n8n-nodes-base.googleDrive`
  - `@n8n/n8n-nodes-langchain.lmChatOpenRouter`
  - `n8n-nodes-base.googleSheetsTool`
  - `n8n-nodes-base.if`
  - `n8n-nodes-base.telegram`
  - `@n8n/n8n-nodes-langchain.agent`
  - `n8n-nodes-base.executeWorkflowTrigger`
  - `n8n-nodes-base.set`
  - `n8n-nodes-base.stickyNote`
  - `@n8n/n8n-nodes-langchain.outputParserStructured`

## Instrucciones de configuración
1. **Google Drive**: Configure las credenciales en n8n para permitir operaciones de búsqueda y acceso a las carpetas necesarias.
2. **Google Sheets**: Configure credenciales y establezca las hojas de cálculo asociadas para registrar datos o resultados.
3. **OpenRouter (Langchain)**: Añada el token de API para habilitar llamadas al modelo de lenguaje.
4. **Telegram**: Configure el bot con su token y establezca el chat ID al que se enviarán los mensajes.
5. Importe el workflow en n8n y ajuste parámetros específicos (carpetas, hojas, condiciones) según necesidades del equipo.

## Detalles de funcionamiento
- El workflow se activa mediante un disparador personalizado (`executeWorkflowTrigger`).
- Utiliza nodos de Google Drive para buscar imágenes basadas en criterios definidos.
- Integra Langchain para procesar entradas y optimizar la búsqueda con inteligencia artificial.
- Registra resultados y estados en Google Sheets.
- Condicionalmente ejecuta acciones mediante nodos `if`.
- Envía resultados y notificaciones a través de Telegram para mantener al equipo actualizado.
- Incluye nodos para estructurar salidas y facilitar la comprensión de resultados.

## Ejemplos de uso
- Búsqueda de imágenes recientes para campañas específicas, con entrega automática de links en Telegram.
- Monitoreo y registro de nuevas imágenes agregadas en carpetas de marketing en Google Drive.
- Automatización del flujo de trabajo para alimentar bases de datos visuales con contenido validado y clasificado.

---

**Número de nodos:** 21  
**Categoría:** marketing/contenido  
**Etiquetas:** *(no definidas)*
```