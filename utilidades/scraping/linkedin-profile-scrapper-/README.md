```markdown
# Linkedin profile Scrapper

## Descripción
Workflow de n8n para extraer y estructurar información de perfiles de LinkedIn mediante técnicas de scraping y procesamiento avanzado, facilitando la organización y análisis de los datos obtenidos.

## Requisitos
- Credenciales válidas para acceso a Google Sheets (API y OAuth).
- Acceso a la API de LinkedIn o métodos alternativos para obtener datos de perfiles.
- Configuración de nodos de LangChain para procesamiento de lenguaje natural.
- n8n actualizado con los nodos utilizados instalados.

## Instrucciones de configuración
1. Configure las credenciales de Google Sheets en n8n, asegurándose de tener permisos adecuados para lectura y escritura en las hojas deseadas.
2. Configure las credenciales para acceso a LinkedIn o los métodos HTTP necesarios en el nodo `httpRequest`.
3. Ajuste las claves y modelos en los nodos de LangChain (`chainLlm`, `lmChatDeepSeek`, `outputParserStructured`) según las APIs de IA que utilice.
4. Personalice los filtros y parámetros en los nodos `filter`, `set` y `code` según sus necesidades específicas.
5. Revise y configure los lotes en `splitInBatches` para optimizar el rendimiento y evitar bloqueos.

## Detalles de funcionamiento
- El workflow inicia con un disparador manual para controlar el inicio del proceso.
- Utiliza scraping y llamadas HTTP para obtener datos crudos de perfiles de LinkedIn.
- Aplica nodos de procesamiento de lenguaje natural con LangChain para estructurar y analizar la información.
- Usa Google Sheets para almacenar y organizar los resultados de forma dinámica.
- Incorpora lógica condicional y procesamiento por lotes para manejo eficiente y filtrado de datos.
- Complementado con nodos de notas adhesivas (`stickyNote`) y markdown para documentación interna y presentación.

## Ejemplos de uso
- Extraer detalles de experiencia laboral y formación de un conjunto de perfiles LinkedIn.
- Analizar habilidades y palabras clave recurrentes en perfiles específicos.
- Generar reportes actualizados en Google Sheets para campañas de reclutamiento o inteligencia de mercado.

---

**Categoría:** utilidades/scraping  
**Nodos utilizados:** n8n-nodes-base.googleSheets, n8n-nodes-base.aggregate, @n8n/n8n-nodes-langchain.chainLlm, n8n-nodes-base.manualTrigger, n8n-nodes-base.filter, n8n-nodes-base.code, n8n-nodes-base.stickyNote, n8n-nodes-base.set, @n8n/n8n-nodes-langchain.outputParserStructured, n8n-nodes-base.splitInBatches, n8n-nodes-base.httpRequest, n8n-nodes-base.markdown, @n8n/n8n-nodes-langchain.lmChatDeepSeek  
**Número de nodos:** 20
```