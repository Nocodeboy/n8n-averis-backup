```markdown
# 2. Seguimientos - Agente IA Ecommerce RAG Avanzado en WhatsApp byAveris

## Descripción
Workflow diseñado para gestionar seguimientos automáticos mediante un agente de IA avanzado en WhatsApp, orientado a ecommerce. Utiliza técnicas RAG (Retrieval-Augmented Generation) para proporcionar respuestas personalizadas y eficientes a través de integraciones con Airtable y OpenAI.

## Requisitos
- Cuenta y credenciales de OpenAI con acceso a modelos compatibles (para `lmChatOpenAi`).
- Cuenta y API key de Airtable con permiso para acceder a las bases de datos necesarias.
- n8n configurado y acceso para importar y ejecutar workflows.
- Configuración de WhatsApp Business API o integración compatible para mensajería.
- Acceso y permisos para ejecutar workflows complementarios en n8n.

## Instrucciones de configuración
1. Importar el workflow en su instancia n8n.
2. Configurar credenciales en n8n:
    - OpenAI (para el nodo `lmChatOpenAi`)
    - Airtable (para `airtableTool`)
    - WhatsApp (según la integración implementada).
3. Ajustar los IDs o campos específicos en el nodo `airtableTool` para apuntar a la base y tablas correctas.
4. Configurar cualquier variable o dato en el nodo `set` necesario para personalizar el flujo.
5. Vincular o habilitar el trigger `executeWorkflowTrigger` para iniciar el flujo automáticamente.
6. Revisar y ajustar parámetros del agente IA en el nodo `agent` para optimizar respuestas.

## Detalles de funcionamiento
- El workflow se activa mediante un trigger, recibiendo mensajes o solicitudes desde WhatsApp.
- Realiza consultas dinámicas a Airtable para obtener información relevante del cliente o el seguimiento.
- Utiliza el modelo `lmChatOpenAi` para generar respuestas basadas en datos recuperados y el contexto.
- El agente IA ejecuta acciones avanzadas para personalizar la interacción y sugerir pasos siguientes.
- Los resultados se formatean y envían de vuelta al usuario a través de WhatsApp, asegurando continuidad en la conversación.

## Ejemplos de uso
- Seguimiento automático a clientes tras una compra para ofrecer soporte o promociones.
- Respuesta personalizada a consultas frecuentes sobre productos o estados de pedidos.
- Creación de tickets o registros en Airtable desde interacciones de WhatsApp para equipos de ventas o atención al cliente.
- Agente conversacional proactivo que sugiere upselling o cross-selling basado en historial almacenado.

---

**Categoría:** agentes-ia/whatsapp  
**Etiquetas:** Averis, Customer / Sales, Whatsapp, *****, Agente  
**Número de nodos:** 6
```