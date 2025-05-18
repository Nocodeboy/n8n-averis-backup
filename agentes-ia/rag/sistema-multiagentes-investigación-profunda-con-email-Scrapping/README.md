```markdown
# Sistema Multiagentes Investigación profunda con email

## Descripción
Workflow avanzado para realizar investigaciones profundas utilizando un sistema multiagentes basado en inteligencia artificial. Integra extracción de datos vía scrapping, análisis mediante modelos OpenAI y rutas dinámicas, gestión y envío de email con Gmail, y almacenamiento de resultados en Google Sheets para un proceso automatizado y robusto.

## Requisitos
- Cuenta n8n con los siguientes nodos instalados:
  - @n8n/n8n-nodes-langchain.lmChatOpenRouter
  - n8n-nodes-base.gmail
  - @n8n/n8n-nodes-langchain.outputParserStructured
  - n8n-nodes-base.httpRequest
  - @n8n/n8n-nodes-langchain.lmChatOpenAi
  - n8n-nodes-base.switch
  - n8n-nodes-base.limit
  - n8n-nodes-base.stickyNote
  - n8n-nodes-base.splitInBatches
  - n8n-nodes-base.merge
  - @n8n/n8n-nodes-langchain.agent
  - n8n-nodes-base.googleSheets
  - n8n-nodes-base.aggregate
  - n8n-nodes-base.form
  - n8n-nodes-base.html
  - @n8n/n8n-nodes-langchain.chainLlm
  - n8n-nodes-base.formTrigger
  - n8n-nodes-base.code
  - n8n-nodes-base.set
  - n8n-nodes-base.splitOut

- Credenciales:
  - API Key de OpenAI o proveedor compatible para nodos LangChain.
  - Cuenta Gmail con acceso SMTP configurado en n8n.
  - Acceso a Google Sheets habilitado para n8n.

## Instrucciones de configuración
1. **Configurar credenciales:**
   - Añadir y validar las credenciales de OpenAI en n8n.
   - Configurar credenciales Gmail con permisos para envío de emails.
   - Conectar Google Sheets con la cuenta correspondiente y permisos de edición.

2. **Personalizar parámetros:**
   - Ajustar las URLs o endpoints en nodos de solicitud HTTP para el scrapping.
   - Modificar prompts y parámetros del LM Chat según objetivo de la investigación.
   - Configurar destinatarios y plantilla de email en el nodo Gmail.

3. **Activar el workflow:**
   - Importar el workflow a n8n.
   - Realizar pruebas con datos de ejemplo.
   - Activar para ejecución automática según flujo configurado (form triggers o disparadores definidos).

## Detalles de funcionamiento
- El workflow inicia con un trigger desde formulario o entrada manual.
- Realiza consultas HTTP para obtener datos relevantes de diversas fuentes.
- Procesa la información con modelos LangChain usando OpenRouter y OpenAI para análisis profundo.
- Utiliza agentes multiagentes para distribuir tareas específicas y optimizar la investigación.
- Resultados estructurados se almacenan en Google Sheets para consulta y seguimiento.
- Envía reportes o alertas por email vía Gmail con resúmenes o insights relevantes.
- Control de flujo, batches y límites garantizan ejecución escalable y ordenada.
- Nodo Switch y lógica permite rutas condicionales según resultados parciales.

## Ejemplos de uso
- Realizar investigación de mercado con scraping web y resumen automatizado.
- Monitorear menciones o datos específicos en tiempo real con alertas por email.
- Integrar inteligencia artificial para análisis complejos en procesos de auditoría o compliance.
- Generar reportes íntegros y actualizados con centralización en Google Sheets.

---

**Categoría:** agentes-ia/rag  
**Etiquetas:** Scrapping, Investigación, Averis, Multiagentes  
**Número de nodos:** 98
```