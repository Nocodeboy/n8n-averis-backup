```markdown
# Agente logístico

## Descripción
Workflow diseñado para automatizar y optimizar tareas logísticas mediante IA, integrando Google Sheets, Gmail y agentes conversacionales de LangChain para gestionar información y decisiones en tiempo real.

## Requisitos
- Cuenta de Google con acceso a Google Sheets y Gmail.
- Credenciales configuradas en n8n para:
  - Google Sheets API
  - Gmail API
- API Key de OpenAI para el nodo `lmChatOpenAi`.
- n8n con los siguientes paquetes instalados y activados:
  - `@n8n/n8n-nodes-langchain`
  - nodos base estándar de n8n.

## Instrucciones de configuración
1. Configure las credenciales de Google Sheets y Gmail en n8n.
2. Ingrese su API Key de OpenAI en el nodo `lmChatOpenAi`.
3. Importe el workflow en n8n.
4. Ajuste las referencias a las hojas de Google Sheets según su caso.
5. Verifique y personalice los parámetros internos de los nodos según su flujo logístico.

## Detalles de funcionamiento
- El workflow inicia con un disparador de Gmail (`gmailTrigger`) que detecta nuevos correos relacionados con logística.
- Un nodo condicional (`if`) evalúa el contenido para decidir próximos pasos.
- Los datos se leen y escriben en Google Sheets usando `googleSheets`.
- El agente de LangChain (`agent`) junto con el modelo de lenguaje (`lmChatOpenAi`) procesan información, generan respuestas y toman decisiones.
- Código personalizado (`code`) y notas adhesivas (`stickyNote`) facilitan manipulación de datos y seguimiento.
- La salida estructurada se formatea con el nodo `outputParserStructured` para integraciones posteriores o reportes.

## Ejemplos de uso
- Recepción automática y clasificación de solicitudes logísticas vía email.
- Consulta dinámica y actualización de inventarios en Google Sheets mediante lenguaje natural.
- Generación de respuestas automáticas personalizadas para clientes o colaboradores.
- Automatización de decisiones basadas en reglas y aprendizaje del agente conversacional.

---

**Categoría:** agentes-ia/otros  
**Etiquetas:** n8nCommunity  
**Número de nodos:** 12  
**Tipos de nodos utilizados:**  
- n8n-nodes-base.googleSheets  
- @n8n/n8n-nodes-langchain.lmChatOpenAi  
- n8n-nodes-base.gmailTrigger  
- n8n-nodes-base.if  
- n8n-nodes-base.code  
- @n8n/n8n-nodes-langchain.agent  
- n8n-nodes-base.stickyNote  
- @n8n/n8n-nodes-langchain.outputParserStructured  
```