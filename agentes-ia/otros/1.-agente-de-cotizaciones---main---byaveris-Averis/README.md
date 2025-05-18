```markdown
# 1. Agente de Cotizaciones - Main - byAveris

## Descripción  
Workflow diseñado para gestionar y automatizar cotizaciones mediante inteligencia artificial, integrando diversas fuentes y herramientas para optimizar la generación, procesamiento y envío de cotizaciones.

## Requisitos  
- Credenciales de OpenAI para el nodo `lmChatOpenAi`  
- Acceso y configuración de WhatsApp en n8n para el nodo `whatsApp`  
- Cuenta Gmail configurada para el nodo `gmail`  
- Permisos de lectura y escritura para manejar archivos locales (`readWriteFile`, `extractFromFile`)  
- n8n versión compatible con nodos de @n8n/n8n-nodes-langchain  

## Instrucciones de configuración  
1. Configure y autentique las credenciales de OpenAI en n8n.  
2. Configure la integración de WhatsApp con la cuenta deseada.  
3. Vincule su cuenta Gmail para poder enviar y recibir correos.  
4. Ajuste rutas y permisos de archivos para la carga y extracción de datos.  
5. Importe el workflow en n8n y verifique que todos los nodos estén correctamente vinculados.  

## Detalles de funcionamiento  
El workflow utiliza un conjunto de 20 nodos que incluyen: agregaciones, limitadores, disparadores manuales y múltiples nodos de inteligencia artificial para manejo de texto, cálculos y análisis.  
- Recopila y procesa documentos y datos de cotizaciones.  
- Utiliza modelos de lenguaje para generar respuestas y resúmenes.  
- Integra herramientas calculadoras y workflows anidados para optimización.  
- Envía notificaciones y cotizaciones a través de WhatsApp y email.  

## Ejemplos de uso  
- Solicitar una cotización personalizada a través de WhatsApp, que el agente procesa y envía por correo.  
- Resumir y analizar múltiples cotizaciones recibidas para comparación rápida.  
- Automatizar el cálculo de costos y parámetros de cotización usando herramientas integradas.  

---

**Categoría:** agentes-ia/otros  
**Etiquetas:** Averis, Agente, *****, Cotizaciones  
**Número de nodos:** 20
```