```markdown
# 3. Recordatorio de citas - Agente IA Avanzado para Clínica Dental - WhatsApp

## Descripción
Workflow diseñado para gestionar y enviar recordatorios automáticos de citas a pacientes de clínicas dentales mediante WhatsApp, utilizando un agente IA avanzado que integra varias APIs y herramientas para una comunicación efectiva y personalizada.

## Requisitos
- Credenciales de API para:
  - OpenAI (modelo ChatGPT)
  - Evolution API (para integración con sistemas de gestión clínica)
- Configuración del módulo WhatsApp (según la integración disponible en tu cuenta n8n)
- Acceso a `@n8n/n8n-nodes-langchain` y `n8n-nodes-evolution-api`
- Permisos para configuración de triggers programados en n8n

## Instrucciones de configuración
1. Importa el workflow en n8n.
2. Configura las credenciales de OpenAI en el nodo `lmChatOpenAi`.
3. Configura las credenciales de Evolution API en el nodo `evolutionApi`.
4. Ajusta el nodo `scheduleTrigger` para definir la frecuencia de consultas y envíos de recordatorios.
5. Personaliza los mensajes y respuestas del agente IA en el nodo `agent` para adaptarlos al tono y necesidades de la clínica dental.
6. Verifica la conexión con WhatsApp para asegurar la correcta entrega de mensajes.

## Detalles de funcionamiento
- El workflow se activa según la programación establecida en `scheduleTrigger`.
- Obtiene datos relevantes de citas a través de Evolution API.
- El agente IA, mediante nodos de LangChain (`mcpClientTool` y `lmChatOpenAi`), elabora mensajes personalizados.
- Finalmente, se envían los recordatorios a los pacientes vía WhatsApp, gestionando respuestas automatizadas si es necesario.

## Ejemplos de uso
- Envío diario de recordatorios de citas para pacientes con cita programada al día siguiente.
- Gestión de respuestas de pacientes via WhatsApp para confirmar, reagendar o cancelar citas.
- Seguimiento proactivo para reducir ausencias en clínicas dentales utilizando IA.

---

**Categoría:** agentes-ia/clinica-dental  
**Etiquetas:** Booking, Clínicas, Averis, Whatsapp  
**Número de nodos:** 6  
**Nodos utilizados:**  
- `@n8n/n8n-nodes-langchain.mcpClientTool`  
- `@n8n/n8n-nodes-langchain.lmChatOpenAi`  
- `n8n-nodes-base.scheduleTrigger`  
- `@n8n/n8n-nodes-langchain.agent`  
- `n8n-nodes-evolution-api.evolutionApi`  
```