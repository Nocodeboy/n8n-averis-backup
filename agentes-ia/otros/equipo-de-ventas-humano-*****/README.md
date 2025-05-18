```markdown
# Equipo de ventas humano

## Descripción
Workflow diseñado para optimizar el proceso de ventas combinando inteligencia artificial avanzada con la supervisión y gestión humana ("Human in the Loop"). Integra modelos de lenguaje, herramientas de correo electrónico y manejo de bases de datos para asistir en la gestión de clientes y campañas.

## Requisitos
- Credenciales de Google Gmail para envío y recepción de correos.
- API keys para los siguientes nodos LangChain:
  - Google Gemini (`@n8n/n8n-nodes-langchain.lmChatGoogleGemini`)
  - Anthropic (`@n8n/n8n-nodes-langchain.lmChatAnthropic`)
- Acceso y configuración de tablas en Airtable (lectura y escritura).
- Credenciales para n8n Airtable Trigger y Airtable Tool.
- Permisos para crear y gestionar notas adhesivas en n8n.
- Acceso a nodos de clasificación y análisis de texto de LangChain.
  
## Instrucciones de configuración
1. Configure las credenciales de Gmail en n8n.
2. Añada las API keys correspondientes para Google Gemini y Anthropic en las credenciales de LangChain.
3. Configure las credenciales y URLs de las bases de datos Airtable que se usarán.
4. Ajuste los parámetros de los nodos de clasificación y análisis según sus necesidades específicas.
5. Verifique que el nodo Airtable Trigger esté correctamente vinculado a la tabla que activará el workflow.
6. Compruebe la conexión y permisos para la creación de notas adhesivas en el workflow.
7. Importe el workflow en n8n y realice pruebas iniciales para validar el flujo.

## Detalles de funcionamiento
- El flujo inicia con un desencadenante en Airtable cuando un nuevo registro o cambio relevante ocurre.
- Se emplean modelos de lenguaje de Google Gemini y Anthropic para procesar y generar respuestas inteligentes.
- El nodo agente LangChain coordina tareas avanzadas de análisis y toma de decisiones.
- Correos electrónicos personalizados se envían y reciben mediante el nodo Gmail para gestionar la comunicación con clientes.
- La información procesada se almacena y actualiza en Airtable para un control centralizado.
- El nodo de clasificación de texto y el parser estructurado analizan las respuestas para mejorar la interacción.
- Notas adhesivas permiten a los usuarios humanos intervenir y agregar contexto, manteniendo un enfoque "Human in the Loop".
- En total se usan 12 nodos para ejecutar todas las tareas coordinadamente.

## Ejemplos de uso
- Automatización de seguimiento de leads con intervención humana para validar oportunidades.
- Clasificación inteligente de correos entrantes y generación automática de respuestas preliminares.
- Actualización y mantenimiento de bases de datos de clientes sincronizadas con interacciones de ventas.
- Supervisión y anotación manual de procesos mediante notas para mejorar el rendimiento comercial.

---

**Categoría:** agentes-ia/otros  
**Etiquetas:** *****, Human in the Loop  
**Número de nodos:** 12  
```