```markdown
# 5. Agente para Abogados - Agente de Emails

## Descripción  
Workflow diseñado para gestionar y automatizar la administración de correos electrónicos para abogados, utilizando agentes de IA y herramientas integradas para optimizar respuestas y seguimiento.

## Requisitos  
- Credenciales de Microsoft Outlook para acceso y gestión del correo electrónico.  
- API Key de OpenAI para el nodo `lmChatOpenAi`.  
- Configuración del nodo `agent` de LangChain para la gestión del flujo conversacional.  

## Instrucciones de configuración  
1. Configure sus credenciales de Microsoft Outlook en n8n.  
2. Añada su clave API de OpenAI en el nodo `lmChatOpenAi`.  
3. Ajuste los parámetros del agente LangChain según sus necesidades específicas.  
4. Asegúrese de que el workflow `executeWorkflowTrigger` esté correctamente habilitado para iniciar el proceso.  

## Detalles de funcionamiento  
El workflow consta de 12 nodos que combinan capacidades de procesamiento de lenguaje natural y automatización de correo:  
- `executeWorkflowTrigger` activa el flujo.  
- Nodos `set` preparan y organizan datos.  
- `lmChatOpenAi` genera respuestas inteligentes basadas en el contenido del correo.  
- El nodo `agent` coordina la conversión y toma decisiones automatizadas.  
- `microsoftOutlookTool` envía y recibe correos electrónicos directamente desde la cuenta configurada.  

## Ejemplos de uso  
- Responder automáticamente correos de clientes con información legal relevante.  
- Filtrar y clasificar correos entrantes para asignación interna.  
- Gestionar recordatorios y seguimientos automáticos para casos legales.  
```