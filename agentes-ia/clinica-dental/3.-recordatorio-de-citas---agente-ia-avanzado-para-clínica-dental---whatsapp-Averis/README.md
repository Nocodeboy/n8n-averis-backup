```markdown
# 3. Recordatorio de citas - Agente IA Avanzado para Clínica Dental - WhatsApp

## Descripción
Workflow diseñado para enviar recordatorios automatizados de citas a pacientes de una clínica dental a través de WhatsApp, utilizando un agente IA avanzado que integra procesamiento de lenguaje natural y APIs externas para gestionar comunicaciones efectivas y personalizadas.

## Requisitos
- Credenciales válidas para OpenAI API (modelo ChatGPT)
- Acceso y configuración de Evolution API para interacción con WhatsApp
- Credenciales para el cliente MCP Tool de LangChain
- n8n instalado y configurado con acceso a los nodos mencionados

## Instrucciones de configuración
1. Configure las credenciales en n8n para:
   - OpenAI (`lmChatOpenAi`)
   - MCP Client Tool (`mcpClientTool`)
   - Evolution API (`evolutionApi`)
2. Ajuste la programación en el nodo `scheduleTrigger` para definir la frecuencia de recordatorios.
3. Personalice el agente IA en el nodo `agent` según las necesidades específicas de la clínica.
4. Asegure que la integración de WhatsApp esté activa y correctamente enlazada con Evolution API.

## Detalles de funcionamiento
- El workflow se activa según la programación definida en `scheduleTrigger`.
- El agente IA, mediante LangChain, procesa las citas próximas y genera mensajes personalizados.
- Se utilizan las APIs para enviar mensajes vía WhatsApp de forma automatizada.
- La interacción es monitoreada y adaptada con base en respuestas y flujo definido en el agente IA.

## Ejemplos de uso
- Recordar a los pacientes su cita dental un día antes por WhatsApp.
- Confirmar o reagendar citas mediante respuestas automatizadas del agente IA.
- Envío de instrucciones pre y post-cita personalizada a cada paciente.

---

### Detalles técnicos
- Categoría: `agentes-ia/clinica-dental`
- Tipos de nodos utilizados:  
  `@n8n/n8n-nodes-langchain.mcpClientTool`,  
  `@n8n/n8n-nodes-langchain.lmChatOpenAi`,  
  `n8n-nodes-base.scheduleTrigger`,  
  `@n8n/n8n-nodes-langchain.agent`,  
  `n8n-nodes-evolution-api.evolutionApi`
- Número de nodos: 6
- Etiquetas: `Averis`, `Whatsapp`, `Clínicas`, `Booking`
```