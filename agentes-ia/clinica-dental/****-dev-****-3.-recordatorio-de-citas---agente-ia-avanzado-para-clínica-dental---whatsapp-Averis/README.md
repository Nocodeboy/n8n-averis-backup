```markdown
# **** DEV **** 3. Recordatorio de citas - Agente IA Avanzado para Clínica Dental - WhatsApp

## Descripción

Workflow diseñado para enviar recordatorios automáticos de citas a pacientes de una clínica dental mediante WhatsApp, utilizando un agente de IA avanzado para gestionar la comunicación y optimizar la experiencia de booking.

## Requisitos

- Credenciales de API para OpenAI (lmChatOpenAi)
- Acceso a la API de Evolution para envíos WhatsApp (n8n-nodes-evolution-api.evolutionApi)
- Configuración del cliente MCP para herramientas personalizadas (@n8n/n8n-nodes-langchain.mcpClientTool)
- Permisos para triggers programados (scheduleTrigger)
- n8n instalado y configurado con soporte para nodos LangChain y Evolution API

## Instrucciones de configuración

1. Configure las credenciales de OpenAI en n8n.
2. Configure las credenciales de Evolution API para WhatsApp.
3. Ajuste el `scheduleTrigger` según la frecuencia deseada de envío de recordatorios.
4. Personalice el agente IA (@n8n/n8n-nodes-langchain.agent) para adecuar el tono y mensajes a la clínica dental.
5. Verifique que el cliente MCP esté correctamente configurado para llamadas adicionales si aplica.
6. Habilite y active el workflow en su entorno n8n.

## Detalles de funcionamiento

- El nodo `scheduleTrigger` inicia el flujo según el horario programado.
- El agente IA usa `lmChatOpenAi` para generar mensajes personalizados y gestionar interacciones.
- `mcpClientTool` integra funcionalidades auxiliares que apoyan la gestión de datos.
- El nodo `evolutionApi` envía los recordatorios por WhatsApp directamente a los pacientes.
- El workflow consta de 6 nodos en total, coordinados para garantizar el correcto envío y seguimiento de los mensajes.

## Ejemplos de uso

- Envío automático de recordatorios 24 horas antes de la cita.
- Respuestas conversacionales vía WhatsApp para confirmar, reprogramar o cancelar citas.
- Seguimiento personalizado según historial del paciente y servicios solicitados.

---

**Categoría:** agentes-ia/clinica-dental  
**Etiquetas:** Averis, Whatsapp, Clínicas, Booking  
**Número de nodos:** 6  
**Nodos utilizados:** @n8n/n8n-nodes-langchain.mcpClientTool, @n8n/n8n-nodes-langchain.lmChatOpenAi, n8n-nodes-base.scheduleTrigger, @n8n/n8n-nodes-langchain.agent, n8n-nodes-evolution-api.evolutionApi
```