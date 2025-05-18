```markdown
# 7. Creador de Video Faceless - Equipo de Marketing - Averis Solutions

## Descripción
Workflow automatizado diseñado para el equipo de marketing que facilita la creación de videos sin rostro ("faceless"). Integra generación de contenido con IA, gestión de datos en Google Sheets y Google Drive, y comunicación vía Telegram para optimizar el proceso creativo y editorial.

## Requisitos
- Cuenta y credenciales de OpenAI (API key) para nodos @n8n/n8n-nodes-langchain.openAi y relacionados.
- Credenciales de Google (Sheets y Drive) con acceso adecuado.
- Token API para la integración de Telegram.
- n8n instalado con los nodos requeridos:
  - @n8n/n8n-nodes-langchain.openAi
  - n8n-nodes-base.googleSheets
  - n8n-nodes-base.googleDrive
  - n8n-nodes-base.merge
  - @n8n/n8n-nodes-langchain.lmChatOpenRouter
  - n8n-nodes-base.code
  - n8n-nodes-base.telegram
  - @n8n/n8n-nodes-langchain.agent
  - n8n-nodes-base.stickyNote
  - n8n-nodes-base.executeWorkflowTrigger
  - @n8n/n8n-nodes-langchain.outputParserStructured
  - n8n-nodes-base.splitOut
  - n8n-nodes-base.httpRequest
  - n8n-nodes-base.wait

## Instrucciones de configuración
1. Configurar credenciales de OpenAI en n8n.
2. Autorizar y conectar Google Sheets y Google Drive con las cuentas del equipo.
3. Configurar el nodo Telegram con el token del bot.
4. Ajustar cualquier parámetro personalizado en los nodos de código y agentes según necesidades específicas.
5. Importar el workflow en n8n y validar la conexión entre nodos.

## Detalles de funcionamiento
- El workflow comienza con la captura y procesamiento de datos desde Google Sheets.
- Utiliza modelos de lenguaje OpenAI para generar guiones y contenido de video.
- Gestiona archivos y recursos multimedia mediante Google Drive.
- Emplea nodos de código y agentes LangChain para lógica avanzada y manejo de estructuras.
- Integra comunicación y notificaciones vía Telegram para seguimiento y control.
- Incorpora mecanismos de espera y división para control de flujo y paralelismo.
- Total nodos: 29, combinando procesamiento, integración y comunicación para un flujo robusto.

## Ejemplos de uso
- Generación automática de guiones para videos de productos sin necesidad de grabar rostro.
- Envío de notificaciones a equipos cuando un video está listo para revisión.
- Actualización automática de fichas de contenido en Google Sheets según avances en el workflow.
- Descarga y organización de recursos multimedia en Google Drive para su posterior publicación.

---
*Categoría: marketing/contenido*  
*Nodos utilizados: listados en requisitos*  
*Número de nodos: 29*
```