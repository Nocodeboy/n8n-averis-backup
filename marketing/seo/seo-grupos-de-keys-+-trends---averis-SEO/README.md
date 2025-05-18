```markdown
# SEO Grupos de Keys + Trends - Averis

## Descripción  
Workflow orientado a marketing y SEO que automatiza la recopilación, análisis y organización de grupos de keywords junto con tendencias actuales, integrando Google Sheets, OpenAI y WordPress para optimizar la estrategia SEO de Averis.

## Requisitos  
- Credenciales de Google Sheets con acceso a las hojas correspondientes.  
- API Key de OpenAI para el nodo LangChain (openAi).  
- Acceso API a WordPress para publicación o actualización de contenido.  
- Configuración de endpoints HTTP si se requiere integración externa.  
- n8n con los nodos necesarios instalados y autorizados.

## Instrucciones de configuración  
1. Configurar las credenciales de Google Sheets en n8n con acceso a los documentos deseados.  
2. Ingresar la API Key de OpenAI en el nodo correspondiente (`@n8n/n8n-nodes-langchain.openAi`).  
3. Configurar el nodo de WordPress con los datos de autenticación (usuario, contraseña/token, URL).  
4. Ajustar parámetros en nodos HTTP y ScheduleTrigger según la frecuencia y endpoints requeridos.  
5. Revisar y personalizar las hojas de Google Sheets y los contenidos para SEO conforme a los objetivos.

## Detalles de funcionamiento  
- El workflow se activa por un trigger programado (`scheduleTrigger`).  
- Solicita y procesa datos de keywords y tendencias mediante llamadas a APIs externas y OpenAI.  
- Agrega, filtra y organiza la información utilizando nodos agregadores y de seteo.  
- Registra y almacena los resultados en Google Sheets para seguimiento y análisis.  
- Publica o actualiza contenidos en WordPress automáticamente basados en los insights generados.  
- Utiliza notas adhesivas (`stickyNote`) para anotaciones internas y seguimiento en el flujo.  
- En total, contiene 33 nodos que colaboran en un flujo integral para gestión SEO.

## Ejemplos de uso  
- Actualización semanal automática de grupos de keywords con datos de tendencias actuales.  
- Generación de briefs de contenido SEO para redactores mediante OpenAI.  
- Publicación directa en blogs WordPress basados en los datos procesados.  
- Seguimiento y monitoreo de keywords en hojas de cálculo compartidas.

---

**Etiquetas:** SEO, Marketing, Averis  
**Categoría:** marketing/seo  
**Nodos utilizados:**  
- n8n-nodes-base.googleSheets  
- @n8n/n8n-nodes-langchain.openAi  
- n8n-nodes-base.aggregate  
- n8n-nodes-base.scheduleTrigger  
- n8n-nodes-base.stickyNote  
- n8n-nodes-base.set  
- n8n-nodes-base.httpRequest  
- n8n-nodes-base.wordpress  
```